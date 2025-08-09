
# Formulário Termo de Opção de Vale-Transporte

Este projeto é um formulário HTML responsivo para coleta de informações relacionadas
ao Termo de Opção de Vale-Transporte. Inclui integração com geração de PDF via jsPDF
e envio de dados pré-formatados via WhatsApp.

## Funcionalidades Principais

- Campos organizados em seções: Identificação, Endereço, Meios de Transporte e Linhas.
- Limite de até 8 linhas de transporte com cálculo automático do valor mensal.
- Validação de campos obrigatórios com destaque visual e mensagens de erro.
- Geração de PDF formatado de acordo com layout definido.
- Envio de dados via WhatsApp com texto padronizado.
- Layout adaptável para dispositivos móveis.

## Função de Capitalização Automática (Title Case)

Para melhorar a padronização dos dados, o formulário implementa um script JavaScript
que converte automaticamente as entradas de texto para o formato "Title Case"
(Primeira letra maiúscula de cada palavra).

### Regras de Aplicação

- **Aplica Title Case** em: Nome, Endereço, Cidade, Unidade, Local de Admissão, Observações,
  Denominação das linhas de transporte.
- **Não aplica Title Case** em: CPF, CEP, CTPS nº, Série, Matrícula, Competência, Data de Admissão,
  campos numéricos (valores, quantidades).
- **UF (Estado)**: sempre convertido para 2 letras maiúsculas (ex.: "sp" -> "SP").
- Palavras comuns como "de", "da", "dos", "e", "para" permanecem em minúsculas no meio das frases,
  exceto quando são a primeira palavra.

### Exemplo de Conversão

Entrada: `SÃO PAULO` -> Saída: `São Paulo`  
Entrada: `rua morro grande` -> Saída: `Rua Morro Grande`  
Entrada: `sp` (UF) -> Saída: `SP`

## Tecnologias Utilizadas

- HTML5 e CSS3
- JavaScript (Vanilla)
- jsPDF + jsPDF-Autotable

## Como Usar

1. Abra o arquivo HTML no navegador.
2. Preencha os campos obrigatórios.
3. Clique em "Gerar PDF" para salvar o documento gerado.
4. Clique em "Enviar dados via WhatsApp" para abrir a conversa com os dados preenchidos.

## Observações

- O campo LGPD é preenchido automaticamente e é somente leitura.
- O formulário é totalmente offline, sem envio de dados para servidores.
- O script é modular e permite fácil adaptação para outros layouts e regras.

---
