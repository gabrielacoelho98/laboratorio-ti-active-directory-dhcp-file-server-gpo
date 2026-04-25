# 🖥️ Active Directory Lab — Infraestrutura de Rede

Projeto de laboratório simulando um ambiente corporativo com Active Directory e serviços de infraestrutura de rede no Windows Server.

---

# 🎯 Objetivo

Simular um ambiente real de TI com foco em:

- Active Directory (AD DS)
- DHCP Server
- File Server (SMB)
- Group Policy (GPO)
- Suporte técnico (N1/N2)

---

# 🧩 Tecnologias Utilizadas

- Windows Server  
- Active Directory Domain Services (AD DS)  
- DHCP Server  
- File Server (SMB)  
- Group Policy Management (GPMC)  
- VMware Workstation  
- Windows Client  

---

# 📡 CHAMADO 01 — DHCP (Cliente sem IP)

## ⚙️ Pré-configuração do servidor

Instalação do serviço DHCP no Windows Server.

![Instalação DHCP](img/dhcp/instalacao-DHCP.png)

---

Configuração inicial do serviço DHCP no servidor.

![Configuração DHCP](img/dhcp/configuracao-dhcp.png)

---

## 🟨 Criação do escopo

Criação do escopo DHCP responsável pela distribuição de IPs na rede.

![Escopo DHCP](img/dhcp/dhcp-02-escopo.png)

---

## 🟥 Problema
Cliente sem endereço IP válido na rede.

![IP inválido](img/dhcp/dhcp-01-ip-invalido.png)

---

## 🔍 Diagnóstico
Verificação do funcionamento do DHCP após criação do escopo.

---

## 🟩 Solução
Correção da configuração do escopo DHCP e liberação de IP automático ao cliente.

![IP correto](img/dhcp/dhcp-04-ip-correto.png)

---

## 🌐 Resultado
Conectividade com a internet restabelecida com sucesso.

![Internet OK](img/dhcp/dhcp-05-internet-ok.png)

---

# 📁 CHAMADO 02 — FILE SERVER (Acesso negado)

## 🟦 Situação inicial
Usuário tentando acessar pasta compartilhada na rede.

![Situação inicial](img/file-server/fs-02-erro-acesso.png)

---

## 🟥 Problema
Acesso negado devido a permissões incorretas no compartilhamento.

![Problema](img/file-server/fs-01-acesso-negado.png)

---

## 🔍 Diagnóstico
Verificação de permissões NTFS e compartilhamento da pasta.

![Diagnóstico](img/file-server/pasta-compartilhamento.png)

---

## 🟩 Solução
Correção de permissões NTFS e liberação de acesso ao usuário.

![Solução](img/file-server/fs-04-permissao-corrigida.png)

---

## 📸 Resultado
Usuário conseguiu acessar a pasta compartilhada.

![Resultado](img/file-server/fs-03-acesso-cliente.png)  
![Resultado](img/file-server/fs-05-acesso-ok.png)

---

# 🔐 CHAMADO 03 — GPO (Bloqueio do Painel de Controle)

## 🟦 Situação inicial
Usuário com restrição de acesso ao Painel de Controle.

![Situação inicial](img/gpo/gpo-04-bloqueio.png)

---

## 🟥 Problema
Política de grupo aplicada bloqueando o acesso ao Painel de Controle.

![Problema](img/gpo/gpo-05-gpresult.png)

---

## 🔍 Diagnóstico
Verificação da GPO aplicada no domínio.

![Diagnóstico](img/gpo/gpo-03-gpupdate.png)

---

## 🟩 Solução
Correção da GPO e atualização das políticas no cliente.

![Solução](img/gpo/gpo-06-correcao.png)

---

## 📸 Resultado
Acesso ao sistema restaurado após ajuste da política.

![Resultado](img/gpo/gpo-07-funcionando.png)

---

# 🧠 Competências Desenvolvidas

- Active Directory Administration  
- DHCP Server Configuration  
- File Server Management  
- Group Policy (GPO)  
- Troubleshooting de rede  
- Suporte técnico em Windows Server  

---

# 🏁 Conclusão

Projeto simula ambiente corporativo real de infraestrutura de TI com administração de servidores e resolução de incidentes.

---

# 🚀 Resultado Final

✔ Active Directory funcional  
✔ DHCP configurado corretamente  
✔ File Server operacional  
✔ GPO aplicada com sucesso  
✔ Projeto pronto para portfólio de estágio em TI  
