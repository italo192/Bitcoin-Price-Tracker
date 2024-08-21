Bitcoin Price Tracker
Este é um script Python que monitora o preço do Bitcoin em tempo real e envia alertas por e-mail quando o valor cai abaixo de um limite definido pelo usuário. O projeto utiliza a API da CoinGecko para obter os preços e a biblioteca smtplib para o envio de e-mails.

Funcionalidades
Rastreamento do preço do Bitcoin: Obtém o preço do Bitcoin em BRL usando a API da CoinGecko.
Envio de alertas por e-mail: Envia um e-mail de alerta para um ou mais destinatários quando o preço cai abaixo de um limite especificado.
Automatização: Executa o rastreamento a cada 10 minutos automaticamente.
Requisitos
Python 3.7+
Bibliotecas Python:
requests
smtplib (parte da biblioteca padrão do Python)
email (parte da biblioteca padrão do Python)
decouple
schedule
Conta de e-mail no Gmail para o envio dos alertas
Instalação
Clone este repositório para o seu ambiente local.

bash
Copiar código
git clone https://github.com/seu-usuario/bitcoin-price-tracker.git
cd bitcoin-price-tracker
Crie e ative um ambiente virtual (opcional, mas recomendado).

bash
Copiar código
python3 -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
Instale as dependências necessárias.

bash
Copiar código
pip install -r requirements.txt
Crie um arquivo .env na raiz do projeto e adicione suas credenciais de e-mail:

graphql
Copiar código
EMAIL_USER=seu_email@gmail.com
EMAIL_PASS=sua_senha_de_app
RECIPIENT_EMAIL=email_destinatario1@gmail.com,email_destinatario2@gmail.com
Nota: Por questões de segurança, utilize uma senha de aplicativo gerada no Gmail em vez da sua senha principal.

Uso
Execute o script principal:

bash
Copiar código
python tracker.py
Insira o valor limite para o alerta do Bitcoin quando solicitado.

O script começará a rastrear o preço do Bitcoin e enviará e-mails de alerta conforme necessário.

Personalização
Intervalo de tempo: O script está configurado para verificar o preço a cada 10 minutos. Esse intervalo pode ser ajustado na linha onde o agendamento é definido:

python
Copiar código
schedule.every(10).minutes.do(check_price, threshold)
Destinatários do e-mail: Você pode adicionar ou remover destinatários editando a variável RECIPIENT_EMAIL no arquivo .env.

Contribuição
Sinta-se à vontade para fazer um fork do projeto, abrir issues ou enviar pull requests.

Licença
Este projeto está licenciado sob a MIT License.

