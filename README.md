# Computer-Networks

1. Estrutura Geral

A topologia representa uma rede empresarial segmentada por VLANs, dividida por departamentos e interligada a servidores centrais e serviços externos.
O desenho segue uma arquitetura hierárquica em três camadas:

Acesso – ligação de dispositivos de utilizadores (PCs, impressoras, etc.);

Distribuição – switches intermédios que agregam o tráfego;

Núcleo (Core) – equipamentos responsáveis pelo roteamento inter-VLAN e ligação à Internet.

Esta estrutura garante melhor desempenho, segurança e escalabilidade da rede.

2. Segmentação e VLANs
🟧 Zona Laranja – Rede Interna / Departamentos

Contém as VLANs de cada departamento (RH, Contabilidade, TI, Marketing, etc.);

Cada VLAN tem endereço IP próprio e é ligada a um switch local;

O roteamento entre VLANs é feito pelo roteador central;

Proporciona isolamento de tráfego, melhor desempenho e segurança interna.

🟦 Zona Azul – Núcleo de Rede / Core Network

Inclui o Switch Core e o Roteador Principal;

Responsável pela interligação de todas as VLANs;

Faz a ligação com a Internet e com a DMZ;

Integra dispositivos de segurança como firewall e IDS.

🩷 Zona Rosa – DMZ (Zona Desmilitarizada)

Contém servidores públicos: Web Server, DNS, E-mail;

Isolada logicamente da rede interna;

Garante acesso externo controlado e proteção adicional aos recursos internos.

🟩 Zona Verde – Rede Remota / Filial

Representa uma filial conectada por VPN Site-to-Site;

Ligação segura e criptografada entre matriz e filial;

Permite acesso remoto controlado aos recursos corporativos.

🟪 Zona Roxa – Serviços Externos / Internet e Cloud

Liga a infraestrutura interna a provedores externos e serviços na nuvem;

Inclui servidores de autenticação, DNS externo e data center remoto.

3. Equipamentos Principais

Switches de Acesso: Ligam PCs e impressoras das VLANs locais;

Switch Core: Faz agregação e encaminhamento inter-VLAN;

Roteador Central: Executa o roteamento dinâmico e as políticas de QoS;

Firewall / IDS: Controla e monitora o tráfego entre LAN, DMZ e WAN;

Servidores Internos: DHCP, DNS, File Server, Mail Server, Web Server;

Gateway VPN: Estabelece conexão segura entre matriz e filiais.

4. Comunicação e Segurança

O tráfego entre VLANs é controlado por ACLs (Access Control Lists);

Firewall implementa regras de filtragem e NAT;

Autenticação centralizada via servidor LDAP/AD;

Backups automáticos e registo de logs em servidores dedicados;

VPNs cifradas garantem a integridade e confidencialidade das comunicações remotas.

5. Boas Práticas e Considerações Finais

A topologia segue as melhores práticas de design de redes corporativas:

Segmentação lógica por VLANs;

Redundância e escalabilidade;

Separação por camadas (Core, Distribuição, Acesso);

Políticas de segurança multicamada;

Integração com serviços externos e cloud computing.

O resultado é uma rede segura, eficiente e preparada para crescimento futuro.
