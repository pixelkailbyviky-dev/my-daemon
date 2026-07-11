# my-daemon
   .github/workflows/daemon.yml
   name: My Daemon

on:
  schedule:
    - cron: '0 */6 * * *'  # Запуск каждые 6 часов
  workflow_dispatch:  # Возможность ручного запуска

jobs:
  run-daemon:
    runs-on: ubuntu-latest
    
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3
      
      - name: Run daemon task
        run: |
          echo " Daemon is running..."
          echo "📅 Date: $(date)"
          echo "✅ Task completed!"
