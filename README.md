#  Active Directory Lab — Infraestrutura de Redes

Projeto de laboratório simulando um ambiente corporativo com Active Directory e serviços de infraestrutura de rede no Windows Server.

Este projeto é uma **continuação de um ambiente de Active Directory previamente criado**, onde foi implementado um domínio base e usuários no diretório (`lab.local`), expandindo agora com serviços de rede e suporte técnico.

---

#  Objetivo

Simular um ambiente real de TI com foco em Active Directory, DHCP, File Server, GPO e suporte técnico (N1/N2).

---

#  Tecnologias Utilizadas

- Windows Server  
- Active Directory Domain Services (AD DS)  
- DHCP Server  
- File Server (SMB)  
- Group Policy Management (GPMC)  
- VMware Workstation  
- Windows Client  

---

## COMANDOS UTILIZADOS:

##  DHCP

- ipconfig
- ipconfig /release
- ipconfig /renew
- ipconfig /all
- ping google.com

---

## FILE SERVER

- ping <ip-do-servidor>
- Acesso ao compartilhamento de rede via Explorer (Win + R)
  \\servidor\compartilhamento
  
---

## GPO

- gpupdate /force
- gpresult /r
- control

---

#  CHAMADO 01 — DHCP (Cliente sem IP)

## ⚙️ Pré-configuração do servidor

Instalação do serviço DHCP no Windows Server.

![Instalação DHCP](img/dhcp/instalacao-DHCP.png)

---

Configuração inicial do serviço DHCP no servidor.

![Configuração DHCP](img/dhcp/configuracao-dhcp.png)

---

##  Criação do escopo

Criação do escopo DHCP responsável pela distribuição de IPs na rede.

![Escopo DHCP](img/dhcp/dhcp-02-escopo.png)

---

##  Problema
Cliente sem endereço IP válido na rede.

![IP inválido](img/dhcp/dhcp-01-ip-invalido.png)

---

##  Diagnóstico
Verificação do funcionamento do DHCP após criação do escopo.

---

##  Solução
Correção da configuração do escopo DHCP e liberação de IP automático ao cliente.

![IP correto](img/dhcp/dhcp-04-ip-correto.png)

---

##  Resultado
Conectividade com a internet restabelecida com sucesso.

![Internet OK](img/dhcp/dhcp-05-internet-ok.png)

---

#  CHAMADO 02 — FILE SERVER (Acesso negado)

##  Problema
Usuário não conseguia acessar a pasta compartilhada.

![Problema](img/file-server/fs-02-erro-acesso.png)

---

##  Diagnóstico
Permissões incorretas identificadas no compartilhamento.

![Diagnóstico](img/file-server/fs-01-acesso-negado.png)

---

##  Solução
Correção das permissões da pasta compartilhada.

![Solução](img/file-server/permissoes-ok.png)

---

##  Complemento
Validação do acesso pelo cliente.

![Cliente acesso](img/file-server/fs-03-acesso-cliente.png)

---

## 📸Resultado final
Acesso liberado com sucesso.

![Resultado](img/file-server/fs-05-acesso-ok.png)

---

#  CHAMADO 03 — GPO (Bloqueio do Painel de Controle)

##  Situação inicial
Usuário com restrição de acesso ao Painel de Controle.

![Situação inicial](img/gpo/gpo-04-bloqueio.png)

---

##  Problema
Política de grupo aplicada bloqueando o acesso ao Painel de Controle.

![Problema](img/gpo/gpo-05-gpresult.png)

---

##  Diagnóstico
Verificação da GPO aplicada no domínio.

![Diagnóstico](img/gpo/gpo-03-gpupdate.png)

---

##  Solução
Correção da GPO e atualização das políticas no cliente.

![Solução](img/gpo/gpo-06-correcao.png)

---

##  Resultado
Acesso ao sistema restaurado após ajuste da política.

![Resultado](img/gpo/gpo-07-funcionando.png)

---

#  Conclusão

Projeto desenvolvido em ambiente de laboratório com fins de estudo, simulando uma infraestrutura corporativa de TI. Foram aplicados conceitos de Active Directory, DHCP, File Server e GPO, além de práticas de troubleshooting de rede.

---


