# Sistema de Gerenciamento de Discos Linux

![Banner do Projeto](https://api.placeholder.com/800/200?text=Gerenciamento+de+Discos+Linux)

## Sobre o Projeto

O Sistema de Gerenciamento de Discos Linux é uma aplicação web educativa e informativa que serve como guia completo sobre particionamento, formatação e gerenciamento de discos no Linux. Esta aplicação foi projetada para ser uma referência abrangente tanto para iniciantes quanto para administradores de sistemas experientes.

## Características Principais

- **Conteúdo Abrangente**: Inclui informações detalhadas sobre partições, sistemas de arquivos, montagem, RAID e solução de problemas
- **Interface Responsiva**: Design adaptável para desktop e dispositivos móveis
- **Temas Claro/Escuro**: Alternância de tema para melhor experiência de leitura
- **Comandos Copiáveis**: Botões para copiar comandos diretamente para a área de transferência
- **Busca Integrada**: Funcionalidade de busca para encontrar conteúdo rapidamente
- **Visualizações Interativas**: Visualização gráfica de conceitos como particionamento de disco

## Estrutura do Projeto

```
gerenciamento-discos-linux/
├── index.html            # Página principal - início até formatos de sistema de arquivos
└── README.md             # Esta documentação
```

## Conteúdo do Guia

O sistema cobre os seguintes tópicos principais:

1. **Introdução ao Gerenciamento de Discos no Linux**
   - Conceitos básicos
   - Anatomia de um disco no Linux
   - Representação de dispositivos de armazenamento

2. **Partições de Disco**
   - Tipos de partições (primária, estendida, lógica, swap)
   - Tabelas de partições (MBR vs GPT)
   - Criação e redimensionamento de partições

3. **Formatos de Sistema de Arquivos**
   - Sistemas nativos do Linux (Ext4, Btrfs, XFS, ZFS)
   - Sistemas para compatibilidade (exFAT, NTFS, FAT32)
   - Comparação detalhada de características

4. **Formatação de Discos**
   - Comandos de formatação para diferentes sistemas de arquivos
   - Formatação segura e sobrescrita de dados
   - Opções avançadas de formatação

5. **Montagem de Volumes**
   - Montagem manual
   - Configuração do fstab
   - Montagem automática com udisks2 e autofs

6. **Ferramentas de Gerenciamento**
   - fdisk, parted, GParted
   - LVM (Logical Volume Manager)
   - Monitoramento de saúde dos discos com smartctl

7. **Configuração de RAID**
   - Tipos de RAID (0, 1, 5, 6, 10)
   - RAID por software com mdadm
   - RAID por hardware e suas ferramentas

8. **Solução de Problemas**
   - Recuperação de dados
   - Identificação de bad blocks
   - Erros comuns e suas soluções

## Funcionalidades Técnicas

### Interface de Usuário

- **Navegação por Abas**: Sistema de abas para alternar entre diferentes conteúdos relacionados
- **Barra Lateral**: Menu de navegação com links para todas as seções
- **Cards Informativos**: Apresentação de informações em cards visualmente agradáveis
- **Tabelas Comparativas**: Comparação de características entre diferentes sistemas e tecnologias
- **Caixas de Informação**: Destaque para dicas, avisos e informações importantes

### Interatividade

- **Botões de Cópia**: Todos os comandos podem ser copiados com um clique
- **Barra de Progresso**: Indicador visual do progresso de leitura
- **Botão "Voltar ao Topo"**: Navegação facilitada em páginas longas
- **Menu Mobile**: Menu responsivo para dispositivos móveis
- **Modo Escuro**: Alternância entre temas claro e escuro, com persistência via localStorage

### Canvas e Visualizações

- **Visualizador de Disco**: Representação gráfica de um disco com partições usando Canvas
- **Legenda Interativa**: Explicação visual dos componentes do disco
- **Redimensionamento Automático**: Adaptação da visualização ao tamanho da tela

## Requisitos Técnicos

- Navegador web moderno com suporte a:
  - HTML5
  - CSS3 (Flexbox, Grid, Variáveis CSS)
  - JavaScript ES6+
  - Canvas API
  - localStorage

## Instalação e Uso

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/gerenciamento-discos-linux.git
   ```

2. Navegue até o diretório do projeto:
   ```bash
   cd gerenciamento-discos-linux
   ```

3. Abra o arquivo `index.html` em um navegador moderno:
   ```bash
   firefox index.html
   # ou
   google-chrome index.html
   # ou
   open index.html  # no macOS
   ```

4. Alternativamente, use um servidor local como o módulo `http-server` do Node.js:
   ```bash
   npm install -g http-server
   http-server
   ```

## Personalização

### Adicionando Novos Temas

O sistema usa variáveis CSS para definir cores. Para adicionar um novo tema:

1. Adicione novas variáveis de cores no estilo CSS:
   ```css
   :root {
       /* Tema atual */
       --primary-color: #2b2d42;
       /* Novo tema */
       --primary-color-alt: #1a237e;
   }
   ```

2. Adicione lógica de alternância no JavaScript:
   ```javascript
   document.querySelector('.theme-switch').addEventListener('click', function() {
       document.body.classList.toggle('alt-theme');
   });
   ```

### Expandindo o Conteúdo

Para adicionar novas seções:

1. Adicione a nova seção ao HTML seguindo o padrão existente:
   ```html
   <section id="nova-secao" class="section">
       <h2>Título da Nova Seção</h2>
       <p>Conteúdo da seção...</p>
   </section>
   ```

2. Adicione a referência à seção no menu lateral:
   ```html
   <li><a href="#nova-secao">Título da Nova Seção</a></li>
   ```

## Contribuição

Contribuições são bem-vindas! Siga estes passos:

1. Faça um fork do repositório
2. Crie um branch para sua feature (`git checkout -b feature/nova-feature`)
3. Faça commit de suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Faça push para o branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.

## Créditos

- **Ícones**: Material Design Icons
- **Fontes**: Segoe UI, Arial, sans-serif
- **Cores**: Esquema de cores baseado em Material Design

## Contato

Para dúvidas, sugestões ou problemas, abra uma issue no repositório ou entre em contato pelo email: exemplo@dominio.com

---

Desenvolvido com ❤️ para a comunidade Linux
