# 🎤 NoTom

Treino de afinação vocal no navegador, em um único arquivo HTML — sem dependências, sem build.

Visual estilo Melodyne: teclado vertical, trilha da voz rolando com cores de afinação, precisão em % e desvio em cents em tempo real.

## Funcionalidades

- **Detecção de pitch (YIN)** monofônica pela Web Audio API, com seletor de microfone
- **Precisão da nota**: 100% no centro, 0% a 50 cents; instrução direta ("suba 18¢")
- **Tom da música**: manual ou detecção automática (Krumhansl-Schmuckler) com trava de estabilidade
- **Vibrato**: julgado pelo centro da oscilação (vibrar ≠ desafinar); mede velocidade, amplitude e regularidade, e aponta defeitos
- **Letra sincronizada** (beta): cole a letra, avanço por sílabas + Web Speech; teleprompter clicável
- **Tomadas por música**: grava a linha de pitch, compara com tomadas anteriores (fantasmas na trilha) e mostra a evolução
- **Revisão**: com o microfone desligado, arraste/role para rever tudo o que cantou
- **🎮 Modo jogo**: 20 fases de segurar a nota sorteada na sua região vocal; tolerância aperta de ±35¢ até ±12¢; 3 ★ (média ≥ 90%) liberam a próxima fase

## Rodar

Qualquer servidor estático serve. Ex.:

```bash
python -m http.server 5599
```

Abra `http://localhost:5599` no Chrome e permita o microfone. Use fone de ouvido.

> O microfone só é liberado em `localhost` ou HTTPS.

Dados (tomadas, letras, progresso do jogo) ficam no `localStorage` do navegador.
