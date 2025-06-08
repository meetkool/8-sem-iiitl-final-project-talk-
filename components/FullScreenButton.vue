<template>
  <div class="fullscreen-container">
    <button 
      @click="openFullScreen" 
      class="fullscreen-button"
      title="Open in Full Screen"
    >
      🔍 Full Screen
    </button>
  </div>
</template>

<script setup>
const props = defineProps({
  diagramCode: {
    type: String,
    required: true
  },
  title: {
    type: String,
    default: 'Diagram - Full Screen View'
  }
})

const openFullScreen = () => {
  const newWindow = window.open('', '_blank', 'width=1200,height=800,scrollbars=yes,resizable=yes')
  newWindow.document.write(`
    <!DOCTYPE html>
    <html>
    <head>
      <title>${props.title}</title>
      <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
      <style>
        body { 
          margin: 0; 
          padding: 20px; 
          background: #1a1a1a; 
          color: white; 
          font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
          display: flex;
          flex-direction: column;
          align-items: center;
        }
        .container {
          width: 100%;
          max-width: 1400px;
          display: flex;
          flex-direction: column;
          align-items: center;
        }
        h1 { 
          text-align: center; 
          margin-bottom: 30px; 
          font-size: 24px;
          font-weight: 600;
        }
        .mermaid-container { 
          display: flex; 
          justify-content: center; 
          align-items: center; 
          min-height: 70vh;
          width: 100%;
          background: rgba(255, 255, 255, 0.05);
          border-radius: 15px;
          padding: 20px;
          box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        .mermaid {
          max-width: 100%;
          overflow: visible;
        }
        .close-btn {
          position: fixed;
          top: 20px;
          right: 20px;
          background: rgba(255, 255, 255, 0.9);
          color: #333;
          border: none;
          border-radius: 8px;
          padding: 10px 15px;
          cursor: pointer;
          font-size: 14px;
          box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
          transition: all 0.3s ease;
        }
        .close-btn:hover {
          background: rgba(255, 255, 255, 1);
          transform: translateY(-2px);
        }
      </style>
    </head>
    <body>
      <button class="close-btn" onclick="window.close()">✕ Close</button>
      <div class="container">
        <h1>${props.title}</h1>
        <div class="mermaid-container">
          <div class="mermaid">
            ${props.diagramCode}
          </div>
        </div>
      </div>
      <script>
        mermaid.initialize({ 
          startOnLoad: true,
          theme: 'dark',
          sequence: {
            actorMargin: 60,
            boxMargin: 15,
            boxTextMargin: 8,
            noteMargin: 15,
            messageMargin: 40,
            mirrorActors: true,
            wrap: true
          },
          flowchart: {
            nodeSpacing: 50,
            rankSpacing: 50
          }
        });
      </script>
    </body>
    </html>
  `)
  newWindow.document.close()
}
</script>

<style scoped>
.fullscreen-container {
  position: absolute;
  top: 15px;
  right: 15px;
  z-index: 10;
}

.fullscreen-button {
  background: rgba(255, 255, 255, 0.9);
  border: none;
  border-radius: 10px;
  padding: 10px 16px;
  cursor: pointer;
  font-size: 13px;
  font-weight: 600;
  color: #333;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15);
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.fullscreen-button:hover {
  background: rgba(255, 255, 255, 1);
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
}

.fullscreen-button:active {
  transform: translateY(0);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}
</style> 