# llm-planet-sim

A geopolitical simulation where LLM agents govern regions of a planet.

Four agents — Politics, Economy, Military, Science — each control a region 
with resources, population, army, and tech level. Every turn each agent 
receives the world state as JSON and returns a single action as JSON.

This repository documents a manual proof of concept: 12 ticks simulated 
by hand with llama3.1-uncensored via Ollama and Open WebUI. The agent 
reached a unified planetary government in one year of simulated time.

Key findings: the agent traded short-term stability for long-term tech 
investment, chose the only free action available when resources hit zero, 
and picked diplomacy over war after winning. 100% valid JSON on every turn.

Unexpected: with web search enabled, the model could not find the fictional 
regions and switched to real-world geopolitical analogies — Pentagon strategy 
documents, Soviet-Afghan conflict doctrine, US Civil War lessons. It adapted 
them to the simulation.

The full simulation log is in `log.txt`. Next step is automating the Game 
Master: a Node.js server with four agent loops, WebSocket broadcast, and a 
live browser dashboard.
