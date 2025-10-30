# Gender Distribution Chart for Power BI# Gender Distribution Visualization for Power BI



Custom Power BI visual that delivers a polished, highly configurable view of gender-based metrics. This repository intentionally ships only the packaged visual (`.pbiviz`). The source code remains private.Um visual personalizado para Power BI que exibe distribuição por gênero de forma elegante e interativa, construído com React, TypeScript e D3.



## Highlights![Gender Distribution Visual](assets/screenshot.png)



- Responsive icon-based layout that scales from small cards to large dashboards## 🎯 Características

- Up to five gender icon styles (auto, suit, dress, neutral, stick) with per-category overrides

- Dynamic color palette integration with Power BI theme colors- **Altamente Personalizável**: Configure cores, tamanhos, fontes e muito mais

- Percentage and value labels with configurable font families, sizes, and colors- **Responsivo**: Adapta-se automaticamente ao tamanho do container

- Cross-filtering support, selection state handling, and highlight awareness- **Animações Suaves**: Transições e animações elegantes para melhor UX

- Portuguese localization of the format pane- **Múltiplas Categorias**: Suporte para 2 ou mais categorias de gênero

- **Performático**: Otimizado para grandes conjuntos de dados

## Download- **Acessível**: Suporte completo a teclado e leitores de tela



The packaged visual is available in this repository root:## 🚀 Tecnologias



- `genderDistributionVizE8F4A1B2C3D4E5F6.1.0.0.0.pbiviz`- **React 18**: Framework UI moderno e performático

- **TypeScript**: Type-safety e melhor experiência de desenvolvimento

You can download it directly from GitHub (Code → Download ZIP) or via the *Releases* tab if you publish a release.- **D3.js**: Manipulação de dados e animações

- **Power BI Visual Tools**: Integração nativa com Power BI

## Installation in Power BI Desktop- **LESS**: Pré-processador CSS



1. Download the `.pbiviz` file.## 📦 Instalação

2. Open Power BI Desktop and go to **Home → Get more visuals → Import a visual from a file**.

3. Select the downloaded package and confirm.### Pré-requisitos

4. The visual will appear in the Visualizations pane ready for use.

- Node.js (v14 ou superior)

## Using the Visual- Power BI Desktop

- Power BI Visual Tools (pbiviz)

1. Drag the visual onto the report canvas.

2. Provide at least one categorical field (e.g., "Gênero") and one numerical measure.### Instalar Power BI Visual Tools

3. Use the format pane (Portuguese labels) to adjust:

   - Orientation, icon size, spacing, and style per category```bash

   - Percentage and value label fonts, colors, and decimal precisionnpm install -g powerbi-visuals-tools

   - Category label typography and colors```

   - Palette overrides for specific categories

4. Interact with the visual as you would with native Power BI visuals (selection, cross-filtering, etc.).### Criar certificado (primeira vez)



## Support & Feedback```bash

pbiviz --install-cert

Requests, issues, or feature ideas are welcome via GitHub Issues or by emailing Alexandre Lourenço at [alexandre.2.lourenco@outlook.com](mailto:alexandre.2.lourenco@outlook.com).```



## License### Instalar dependências do projeto



All rights reserved. The packaged visual is provided for deployment within Power BI reports. Redistribution of the source code is not permitted.```bash

cd genderDistributionViz
npm install
```

## 🛠️ Desenvolvimento

### Iniciar servidor de desenvolvimento

```bash
npm start
```

O visual estará disponível em modo de desenvolvimento no Power BI Desktop. Ative o modo de desenvolvedor em Power BI Desktop:
1. Arquivo > Opções e Configurações > Opções
2. Visualizações > Visuais de Desenvolvedor > Habilitar

### Build para produção

```bash
npm run build
```

### Criar pacote .pbiviz

```bash
npm run package
```

O arquivo `.pbiviz` será criado na pasta `dist/`.

## 📊 Como Usar

### 1. Adicionar Dados

Arraste campos para as áreas de dados:

- **Category**: Campo de categoria (ex: Gender, Gênero, etc.)
- **Values**: Valores numéricos a serem exibidos

### 2. Personalização

Use o painel de formatação para personalizar:

#### General
- **Show Percentage**: Exibir/ocultar percentuais
- **Show Values**: Exibir/ocultar valores
- **Orientation**: Vertical ou Horizontal

#### Icon Settings
- **Icon Size**: Tamanho dos ícones de pessoa (40-200px)
- **Icon Spacing**: Espaçamento entre ícones (5-100px)
- **Show Category Labels**: Exibir/ocultar rótulos

#### Percentage Settings
- **Font Size**: Tamanho da fonte para percentuais
- **Font Family**: Família de fonte
- **Font Color**: Cor da fonte
- **Font Weight**: Peso da fonte (Normal, Bold, Bolder)
- **Decimal Places**: Casas decimais (0-2)

#### Value Settings
- **Font Size**: Tamanho da fonte para valores
- **Font Family**: Família de fonte
- **Font Color**: Cor da fonte
- **Display Units**: Auto, None, Thousands, Millions, Billions

#### Color Settings
- **Use Custom Colors**: Usar cores personalizadas
- **Color 1-5**: Defina até 5 cores personalizadas

#### Animation Settings
- **Enable Animations**: Ativar/desativar animações
- **Animation Duration**: Duração das animações (ms)

## 🎨 Estrutura do Projeto

```
genderDistributionViz/
├── src/
│   ├── components/
│   │   ├── GenderDistributionChart.tsx  # Componente principal
│   │   ├── PersonIcon.tsx               # Ícones de pessoa
│   │   └── DataLabel.tsx                # Labels de dados
│   ├── models/
│   │   └── index.ts                     # Interfaces e tipos
│   ├── settings/
│   │   └── visualSettings.ts            # Classes de configuração
│   ├── utils/
│   │   ├── formatters.ts                # Funções de formatação
│   │   ├── colorUtils.ts                # Utilitários de cor
│   │   └── dataTransform.ts             # Transformação de dados
│   ├── constants.ts                     # Constantes globais
│   ├── visual.ts                        # Classe principal do visual
│   └── index.ts                         # Ponto de entrada
├── style/
│   └── visual.less                      # Estilos CSS
├── capabilities.json                     # Definição de capacidades
├── pbiviz.json                          # Configuração do visual
├── tsconfig.json                        # Configuração TypeScript
└── package.json                         # Dependências npm
```

## 🏗️ Arquitetura

### Princípios SOLID

- **Single Responsibility**: Cada componente tem uma responsabilidade única
- **Open/Closed**: Extensível sem modificar código existente
- **Liskov Substitution**: Componentes são substituíveis
- **Interface Segregation**: Interfaces específicas e focadas
- **Dependency Inversion**: Dependências de abstrações, não implementações

### Padrões Utilizados

- **Component Pattern**: Componentes React reutilizáveis
- **Container/Presenter**: Separação de lógica e apresentação
- **Factory Pattern**: Criação de objetos de configuração
- **Observer Pattern**: Gerenciamento de estado e eventos

## 🔧 Boas Práticas Implementadas

1. **Type Safety**: TypeScript estrito para prevenir erros
2. **Code Splitting**: Componentes modulares e reutilizáveis
3. **Performance**: Memoização e otimizações React
4. **Accessibility**: ARIA labels e suporte a teclado
5. **Error Handling**: Tratamento robusto de erros
6. **Testing Ready**: Estrutura preparada para testes
7. **Clean Code**: Código limpo e bem documentado

## 📝 Exemplos de Uso

### Exemplo 1: Distribuição Binária
```
Categoria | Valor
Male      | 680
Female    | 320
```

### Exemplo 2: Múltiplas Categorias
```
Categoria     | Valor
Masculino     | 450
Feminino      | 380
Não-binário   | 120
Outro         | 50
```

## 🐛 Troubleshooting

### Visual não aparece no Power BI
- Verifique se o modo de desenvolvedor está ativado
- Certifique-se de que `npm start` está rodando
- Reinicie o Power BI Desktop

### Erro de certificado
```bash
pbiviz --install-cert
```

### Erro de dependências
```bash
rm -rf node_modules package-lock.json
npm install
```

## 🤝 Contribuindo

Contribuições são bem-vindas! Por favor:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## ✨ Funcionalidades Futuras

- [ ] Exportar como imagem
- [ ] Mais estilos de ícones
- [ ] Temas predefinidos
- [ ] Suporte a tooltips customizados
- [ ] Drill-through support
- [ ] Bookmarks support
- [ ] Mobile optimizations

## 📧 Contato

Para dúvidas e sugestões, abra uma issue no GitHub.

---

**Desenvolvido com ❤️ usando React, TypeScript e D3**
