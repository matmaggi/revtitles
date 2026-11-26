# RevTitles

**Revisor de legendas em português do Brasil e espanhol da América Latina, com regras da Netflix e IA opcional.**

O RevTitles revisa um arquivo de legenda inteiro e aponta erros de ortografia, gramática, pontuação, formatação e tempo, seguindo o guia de estilo da Netflix. Também compara a tradução com o original usando IA. Funciona no navegador, sem instalação.

## Formatos aceitos
SRT, DFXP, PXTT, TTML e TTAL.

## Idiomas
- 🇧🇷 Português (Brasil)
- 🌎 Español (Latinoamérica)

A interface e as regras mudam conforme o idioma escolhido.

## Funcionalidades

### Revisão automática (sem IA)
- **Perfis de legenda:** legenda comum adulto (17 car./s), legenda comum infantil (13 car./s), SDH adulto (20 car./s) e SDH infantil (17 car./s).
- **Frame rate:** 24 (23,976), 25 e 30 (29,97).
- **Tempo e leitura:** velocidade de leitura acima do limite, duração mínima (5/6 s) e máxima, intervalo mínimo de 2 quadros entre legendas, sobreposição e fim anterior ao início.
- **Tamanho:** linhas com mais de 42 caracteres, mais de duas linhas, legendas que cabem em uma linha só.
- **Quebra de linha:** sugere quebras melhores, sem separar artigos e preposições da palavra seguinte.
- **Pontuação e espaços:** espaços duplos ou sobrando, espaço antes de pontuação, sinais duplicados ou combinados, ponto depois de ! ou ?, `--` no lugar de reticências, falta de pontuação final.
- **Reticências entre legendas:** uso correto quando a frase continua na legenda seguinte.
- **Diálogos:** hífen e espaço nas duas linhas, hífen indevido em legenda de uma linha, dois falantes na mesma linha.
- **Aspas, parênteses e colchetes** não fechados; estilos de aspas misturados no arquivo.
- **Itálico:** tag aberta e não fechada; letras de música em itálico; identificações e efeitos sonoros fora do itálico.
- **Música:** ♪ no início e no fim, com espaço.
- **Maiúsculas:** início de frase, legenda toda em maiúsculas (reservada para narrativa forçada), narrativa forçada misturada com diálogo.
- **Números:** de 1 a 10 por extenso, número no início de frase, "mil" em vez de "1 mil", moedas por extenso.
- **Abreviações e siglas:** Sr., Dra., Prof. com ponto; unidades de medida sem ponto; siglas sem pontos (EUA).
- **Palavras repetidas** ("eu eu").
- **SDH:** avisa colchetes de efeitos sonoros e identificação de falantes fora do perfil SDH; minúsculas dentro dos colchetes.
- **Consistência no arquivo** (versão em espanhol): nomes escritos de duas formas, tratamento misturado (tu/você, tú/usted/vos), grafias diferentes e concordância sujeito-verbo.
- **Espanhol:** detecta vocabulário, expressões e interjeições da Espanha, leísmo, *vosotros* e pretérito perfeito composto.
- **Ortografia e gramática online** (opcional), pelo serviço gratuito LanguageTool.

### Comparador com IA
Compara a tradução com o template original, inclusive o itálico, e aponta:
sentido incorreto, omissão, acréscimo, números e datas, nomes e termos, ortografia, gramática e concordância, pontuação, itálico, registro e tom, regionalismo, tradução literal, naturalidade e fluidez, concisão, humor e referências, e consistência.

- **Níveis de detecção:** Leve (só erros claros), Médio (erros e dúvidas prováveis) e Pesado (inclui nuances e pequenas melhorias).
- **Serviços de IA:** Groq (plano gratuito, padrão), Gemini (plano gratuito), OpenRouter (modelos gratuitos), Claude (Anthropic), ChatGPT (OpenAI) ou qualquer serviço compatível com a API da OpenAI (Ollama, LM Studio, Mistral, DeepSeek…). A página lembra o último serviço escolhido.
- **Configurações avançadas:** modelo, buscar modelos disponíveis na sua conta, endereço do servidor, preços por token e CPS máximo.
- **Contexto entre lotes:** cada lote enviado à IA leva também as legendas vizinhas, para que frases divididas entre lotes sejam entendidas.
- **Custo:** estimativa durante a análise e custo total ao final, com preços de referência editáveis.
- Espera sozinho quando o limite de uso do serviço é atingido e avisa quando a resposta da IA foi cortada.
- Sugestões que passariam de 42 caracteres por linha são descartadas.

### Trabalhando com os apontamentos
- Aplicar a sugestão, editar o texto à mão, desfazer ou dispensar.
- Aplicar a mesma correção em todas as legendas do arquivo.
- Ignorar uma palavra, um termo ou um tipo de erro (com opção de restaurar depois).
- Ignorar palavras desconhecidas com inicial maiúscula (nomes próprios).
- Filtrar por tipo de erro.

### Exportação
- Baixar a legenda com as suas alterações, no formato original ou em .srt.
- Baixar o relatório com todos os apontamentos em TXT, HTML ou XLSX (Excel), tanto da revisão quanto do Comparador com IA.

## Privacidade
A revisão automática roda no seu navegador. O texto só sai do computador se você usar o LanguageTool ou o Comparador com IA, e nesse caso vai apenas para o serviço escolhido. A chave de API fica salva só no seu navegador.
