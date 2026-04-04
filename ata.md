KELLY RODRIGUES BATISTA

Na minha parte do projeto, desenvolvi os servidores, focando na configuração do Web Server e File Server. Fiz a configuração da VLAN de servidores na matriz, incluindo o Servidor Web Corporativo com portal interno e o Servidor Web Externo na DMZ para acesso público. Configurei também o Servidor de Arquivos/FTP com usuário de teste e autenticação básica, e o Servidor DNS com registros internos e externos. Todos os servidores foram conectados ao switch da matriz com endereços IP organizados e gateways configurados para roteamento inter-VLAN. Além disso, organizei a topologia da matriz isolada, documentando todos os IPs, VLANs e serviços, garantindo que a integração com as demais partes do projeto possa ser feita de forma clara e eficiente.

LUINI DE FREITAS SALLES

   Ajudei com o desenvolvimento inicial do projeto, quais os serviços essenciais seriam usados, e como deveriam ser implementados no escopo do projeto. Fizemos a distribuição dos serviços entre os colegas, onde eu fiquei com os serviços de AD, Banco de Dados e rede WAN.
Elaborei a parte explicativa sobre todos esses serviços e montei no Packet Tracer o modelo esquemático da rede WAN, com as configurações de IPs internos de cada rede, e comunicação entre os roteadores interligando as redes através de conexão via porta serial, usando o protocolo RIP.

#### SARAH CESAR MARTINS DOS SANTOS
##### Wi-Fi e CRM Server

Na parte que desenvolvi no projeto, fiquei responsável pela implementação do **Wi-Fi**, pela análise da representação do **CRM Server** e também pelo apoio na **organização da documentação** do projeto. Em relação ao CRM Server, é importante destacar que **não é possível configurá-lo de forma funcional dentro do Packet Tracer**, já que essa ferramenta é voltada principalmente para simulação de infraestrutura de rede, e não para sistemas corporativos completos. Assim, o CRM Server não foi representado na topologia.

Já a implementação do **Wi-Fi** foi realizada considerando a **topologia em árvore** adotada no projeto. Para isso, foi adicionado um **Access Point (AP-PT)** em cada switch de cada unidade da rede. Nesse contexto:

- a **Port 0** do AP corresponde à interface **cabeada**, responsável pela ligação com o switch e pelo recebimento das informações que trafegam na rede local;
- a **Port 1** corresponde à parte **wireless**, onde são definidas as configurações da rede sem fio.

Em cada **Access Point** foram configurados os seguintes parâmetros:

- **SSID** da rede sem fio;
- **tipo de autenticação**;
- **PSK Pass Phrase**;
- **senha de acesso**.

Para validar a conectividade Wi-Fi, foram adicionados **laptops e PCs para testes**. Para que esses dispositivos pudessem se conectar à rede sem fio, foi necessário:

1. desligar os dispositivos;
2. remover o módulo de rede original;
3. instalar as interfaces adequadas:
   - **WPC300N** nos laptops;
   - **WMP300N** nos PCs.

Após essa etapa, os dispositivos puderam localizar a rede configurada e se conectar por meio da opção **PC Wireless**, utilizando a senha definida no Access Point.

> **Observação importante:** não é possível configurar, apenas com o **AP-PT**, dois tipos de acesso separados, como rede de **convidados** e rede **corporativa**. Para isso, seria necessário realizar uma segmentação lógica da rede por meio de **VLANs**, permitindo separar adequadamente os acessos de colaboradores e visitantes.

Dessa forma, a solução implementada no Packet Tracer atende ao funcionamento básico da rede sem fio, mas possui limitações em relação a uma estrutura corporativa mais completa. Além disso, houve contribuição na **organização da documentação do projeto**, auxiliando na estruturação e apresentação das informações desenvolvidas ao longo da atividade.

André Mateus Fonseca Neves

Nesta etapa do projeto, realizei as configurações de DHCP e DNS, definindo as rotas padrão para as estações de trabalho e utilizando os equipamentos previamente selecionados pelos demais integrantes. Uma funcionalidade testada, mas descartada para a versão final, foi a configuração de VLANs. Durante os testes, validamos que a versão utilizada do Cisco Packet Tracer não suportava adequadamente a segregação de rede via ACL (Listas de Controle de Acesso) para esse cenário; portanto, o uso de VLANs teria apenas fins organizacionais, já que a comunicação entre elas permaneceria aberta. Além disso, os nomes dos servidores das demais unidades foram configurados no DNS, permitindo a resolução de nomes e a conectividade entre a filial e a matriz.<br>
Obs.: Foi feita uma tentativa para a segregação das Vlan, onde foi feita 2 DHCP para as 2 faixas, onde mostrou que seria inviável pois estariam usando 2 porta do switch e do router.
