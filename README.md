## Pedro Ramos

Construo **ferramentas de desktop para Windows** e **coisas em tempo real na web**.
Português, a trabalhar sozinho, do primeiro commit ao instalador publicado.

*I build Windows desktop tools and real-time web software — from first commit to shipped installer.*

---

### O que está aqui

**[FC 26 Optimizer](https://github.com/pdramos/fifa)** · Electron · ~4.400 linhas · **3 versões publicadas**

Otimizador para o EA SPORTS FC 26. Aplica ajustes oficiais do Windows e do próprio jogo —
nenhuma alteração em memória, nenhum risco de banimento. Motor de otimizações separado do
catálogo, com execução reversível: cada ajuste guarda o estado anterior e sabe voltar atrás.

O problema interessante não foi otimizar — foi **desfazer**. Uma ferramenta que mexe no
registo do Windows e não sabe reverter é uma ferramenta que estraga o PC de alguém.

**[Menos Ping](https://github.com/pdramos/menos-ping)** · Electron + React + TypeScript · ~8.100 linhas

Otimizador de latência para jogos online. Deteta o jogo em execução, traça a rota até ao
servidor, mede perda e variação de atraso, e compara o antes e o depois. Módulos nativos
próprios para *traceroute*, DNS, conexões e processos — sem depender de binários externos.

Doze serviços isolados por responsabilidade, nove ecrãs, e um gestor de cópias de segurança
pela mesma razão do projeto acima: mexer na rede de alguém sem caminho de volta é irresponsável.

**GESTICULA!** · JavaScript sem dependências · ~9.600 linhas · 264 commits · 40 ficheiros de teste

Jogo de mímica pelo navegador: a pessoa aparece recortada do fundo, em tempo real, e a sala
adivinha. Servidor Node **sem uma única dependência** — o WebSocket foi escrito à mão a partir
da RFC 6455. Segmentação de imagem por WebGL, retransmissão de vídeo por sala, migração
automática de anfitrião quando quem criou a sala desaparece.

*Privado por agora — os diários de desenvolvimento estão no mesmo repositório. Peça e eu mostro.*

---

### Como eu trabalho

Escrevo testes para **encontrar** defeitos, não para confirmar que o código funciona.

No GESTICULA! isso deu 40 ficheiros de teste com jogadores sintéticos que abrem navegadores
a sério, jogam partidas inteiras, desligam-se a meio, recarregam a página e voltam. Um deles
sorteia o caos a partir de uma semente reproduzível e verifica sete invariantes no fim.

Foi assim que apanhei um erro que nenhum teste roteirizado apanharia: quando o anfitrião saía,
o rodízio continuava a chamar a vez de quem já não estava lá, e a sala inteira olhava para um
palco vazio até o tempo acabar.

Quando encontro um defeito, a primeira pergunta não é como corrigir — é **por que é que não o
tinha encontrado antes**. Normalmente a resposta muda o teste, não só o código.

---

📍 Portugal
