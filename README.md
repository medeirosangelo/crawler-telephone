O arquivo `README.md` é crucial para fornecer informações sobre o seu projeto, como ele funciona, como usá-lo e outros detalhes importantes para desenvolvedores ou usuários. Aqui está um modelo básico que você pode usar para o seu crawler de telefone, adaptado ao seu código:

---

# Crawler de Telefone

Este projeto é um crawler para coletar números de telefone de anúncios de automóveis no site [django-anuncios.solyd.com.br](https://django-anuncios.solyd.com.br/). O crawler busca os links dos anúncios e extrai os números de telefone presentes nas descrições dos carros.

## Funcionalidades

- **Busca de Anúncios**: Coleta links de páginas de anúncios de automóveis.
- **Extração de Telefones**: Utiliza expressões regulares para identificar e extrair números de telefone das descrições dos anúncios.
- **Multithreading**: Utiliza múltiplas threads para acelerar o processo de coleta de dados.
- **Armazenamento em CSV**: Os números de telefone extraídos são salvos em um arquivo CSV para fácil acesso e análise.

## Requisitos

- Python 3.x
- Bibliotecas Python:
  - `requests` (para requisições HTTP)
  - `beautifulsoup4` (para parsing de HTML)
  - `re` (para expressões regulares)
  - `threading` (para execução simultânea de tarefas)

Para instalar as dependências, basta usar o seguinte comando:

```bash
pip install requests beautifulsoup4
```

## Como Usar

### Passo 1: Clonar o Repositório

Clone este repositório para sua máquina local usando o seguinte comando:

```bash
git clone https://github.com/medeirosangelo/crawler-telefone.git
```

### Passo 2: Executar o Crawler

1. Navegue até o diretório do projeto:

    ```bash
    cd crawler-telefone
    ```

2. Execute o script Python:

    ```bash
    python crawler.py
    ```

O script irá buscar os anúncios de automóveis, extrair os números de telefone e salvá-los em um arquivo CSV chamado `telefones.csv`.

### Passo 3: Verificar os Telefones

Após a execução, você encontrará os números de telefone extraídos no arquivo `telefones.csv`. Cada linha do arquivo conterá um número de telefone no formato:

```
(XX) 9XXXX-XXXX
```

## Estrutura do Projeto

- `crawler.py`: Script principal do crawler.
- `telefones.csv`: Arquivo onde os números de telefone extraídos são salvos.
- `README.md`: Este arquivo de documentação.

## Contribuições

Se você deseja contribuir para este projeto, por favor, siga os seguintes passos:

1. Faça um fork deste repositório.
2. Crie uma nova branch para suas alterações:
   
   ```bash
   git checkout -b minha-nova-funcionalidade
   ```

3. Realize suas alterações.
4. Faça o commit das suas mudanças:

   ```bash
   git commit -m "Descrição do que foi feito"
   ```

5. Envie suas alterações para o repositório remoto:

   ```bash
   git push origin minha-nova-funcionalidade
   ```

6. Abra um Pull Request no GitHub.

## Avisos

- **Uso Responsável**: Ao executar crawlers em sites, é importante garantir que você está respeitando os Termos de Serviço do site em questão. O uso excessivo ou inadequado de crawlers pode resultar em bloqueio de IP ou outros problemas.
- **Taxa de Requisições**: Este script utiliza múltiplas threads para acelerar o processo, mas é importante usar com moderação para não sobrecarregar o servidor.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
