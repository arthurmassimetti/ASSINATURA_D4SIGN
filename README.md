# Automação de Assinatura e Gerenciamento de Documentos para PCMSO

![Python Version](https://img.shields.io/badge/Python-3.8%2B-brightgreen)
![Selenium Version](https://img.shields.io/badge/Selenium-3.141%2B-brightgreen)
![PyAutoGUI Version](https://img.shields.io/badge/PyAutoGUI-0.9%2B-brightgreen)

Este projeto oferece uma solução automatizada para o processo de assinatura e gerenciamento de documentos relacionados ao PCMSO (Programa de Controle Médico de Saúde Ocupacional) usando Python, Selenium e PyAutoGUI.

## Funcionalidades

- **Assinatura Automatizada**: Utilizando o Selenium, nosso script automatiza o processo de login na plataforma D4sign, localiza o documento PCMSO, insere a assinatura médica e finaliza o processo de assinatura.

- **Autorização Médica**: Após a assinatura, o documento requer autorização e liberação do médico responsável. Este processo é acompanhado manualmente, garantindo o controle adequado.

- **Download e Arquivamento**: Após a autorização médica, nosso próximo passo é automatizar o download dos documentos PCMSO em formato PDF. Esses arquivos são então organizados e armazenados em um local específico.

- **Integração com Banco de Dados**: Os documentos em PDF são enviados automaticamente para um banco de dados, garantindo um registro seguro e acessível.

## Como Usar

1. **Configuração do Ambiente**:
   - Certifique-se de ter Python 3.8+ instalado.
   - Instale as bibliotecas necessárias com `pip install -r requirements.txt`.
   
2. **Execução do Script**:
   - Execute o script principal: `python assinatura_pcmso.py`.
   - Siga as instruções interativas para realizar a assinatura e gerenciamento de documentos.

3. **Autorização Médica**:
   - Após a assinatura, acompanhe manualmente a autorização e liberação médica na plataforma D4sign.

4. **Download Automático**:
   - Após a autorização, execute `python download_pcmso.py` para baixar automaticamente os PDFs.

5. **Integração com Banco de Dados**:
   - Configure a integração com o seu banco de dados no arquivo `database.py`.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues, propor melhorias ou enviar pull requests.

## Autor

- Arthur Massimetti Sartori
