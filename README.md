# Benefícios da Nuvem - Máquinas Virtuais na Azure

## Visão Geral

Este repositório documenta os aprendizados sobre os benefícios da computação em nuvem e a criação de máquinas virtuais no Microsoft Azure, part da formação **AZ-900 (Azure Fundamentals)**.

---

## Principais Benefícios da Nuvem

### 1. **Escalabilidade**
- Aumentar ou diminuir recursos conforme a demanda
- Pãga-se apenas pelo que se usa
- Não é necessário provisionar hardware antecipadamente
- Crescimento fácil sem interrupção de serviços

### 2. **Confiabilidade e Disponibilidade**
- SLA (Service Level Agreement) de até 99,99%
- Redundância geográfica automática
- Recuper ação de desastres integrada
- Backup automático e replicafra de dados

### 3. **Segurança**
- Criptografia de dados em trânsito e em repouso
- Controle de acesso baseado em função (RBAC)
- Monitoramento e conformidade contínuos
- Proteção contra ameaças avanadas
- Firewall e grupos de segurança integrados

### 4. **Reduz Custos**
- Não há custo inicial (CAPEX)
- Modelo de preço por consumo (OPEX)
- Reduzem custos operacionais
- Sem custo de manutenção de hardware
- Sem custo de espaço físico (data center)

### 5. **Desempenho**
- Rede de fibra ótica global
- Baixa latência em conexões
- CDN (Content Delivery Network) integrado
- Data centers próximos aos usuários

### 6. **Flexibilidade**
- Múltiplas opções de configuração
- Compatibilidade com tecnologias existentes
- Integração fácil com on-premises
- Modelo híbrido de nuvem

---

## 🖱 Máquinas Virtuais na Azure

### O que é uma VM?

Uma máquina virtual (VM) é uma emulação de um computador físico executando um sistema operacional e aplicações em um servidor remoto na nuvem.

### Vantagens das VMs na Azure:

#### **Flexibilidade de SO**
- Windows Server (2019, 2022, etc.)
- Linux (Ubuntu, CentOS, RHEL, etc.)
- Suporte a imagens personalizadas

#### **Tipos de VM**
- **General Purpose**: Uso geral, balãnceadas
- **Compute Optimized**: Alto desempenho computacional
- **Memory Optimized**: Alto consumo de memória
- **Storage Optimized**: Alto throughput de I/O
- **GPU**: Para processamento gráfico e IA/ML

#### **Configuração**
- CPU: 1 a 416 vCPUs
- RAM: 0,5 GB a 11.4 TB
- Armazenamento: SSD ou HD tradicional
- Rede: Banda lárga dedicada

### Componentes de uma VM na Azure

```
VM Azure
├─ Sistema Operacional
├─ Discos (OS + Dados)
├─ Rede Virtual (VNet)
├─ Interface de Rede (NIC)
├─ Grupo de Segurança (NSG)
├─ Endereço IP Público (opcional)
└─ Tags de Recurso
```

### Etapas para Criar uma VM no Azure

1. **Acessar o Portal do Azure** (portal.azure.com)
2. **Navegar para "Máquinas Virtuais"**
3. **Clicar em "Criar" > "Máquina Virtual"**
4. **Preencher Detalhes Básicos:**
   - Subscription
   - Resource Group
   - Nome da VM
   - Região
   - Imagem do SO
   - Tamanho da VM
5. **Configurar Rede:**
   - Virtual Network (VNet)
   - Sub-rede
   - IP Público
   - Grupo de Segurança
6. **Configurar Discos:**
   - Tipo de disco (Premium SSD, Standard HDD)
   - Tamanho do disco
7. **Revisar e Criar**
8. **Gerar ou Usar Par de Chaves SSH/RDP**

### Gestão da VM

- **Iniciar/Parar**: Economiza custos
- **Redimensionar**: Alterar número de vCPUs e RAM
- **Backup**: Proteger dados
- **Monitoramento**: Performance e saúde
- **Atualizações**: Patches de segurança

---

## Casos de Uso

### VMs são Ideais Para:

- Hospedagem de aplicações web
- Servidores de banco de dados
- Processamento de dados em lote
- Ambientes de desenvolvimento e teste
- Migração de carga de trabalho on-premises
- Aplicativos de desktop virtual (RDS)

---

## Modelo de Preço

O preço das VMs na Azure depende de:

- **Tamanho da VM** (CPU e memória)
- **Sistema Operacional** (Windows mais caro)
- **Tipo de Armazenamento**
- **Transferência de Dados**
- **Licenças de Software**

### Opções de Custo:

1. **Pay-as-You-Go**: Preço por hora
2. **Reserved Instances**: Economia de até 70%
3. **Spot Instances**: Até 90% de desconto (carga variável)
4. **Hybrid Benefit**: Desconto para licenças existentes

---

## Melhores Práticas

### Segurança
- Sempre usar NSGs restritivos
- Ativar Azure Disk Encryption
- Usar Azure Bastion para acesso remoto
- Implementar Windows Defender ou antivírus
- Atualizar regularmente o SO

### Performance
- Monitorar CPU, memória e disco
- Usar Application Insights para logs
- Configurar auto-scaling
- Otimizar tamanho da VM conforme necessidade

### Gerenciamento de Custos
- Usar Azure Cost Management
- Desligar VMs quando não usadas
- Considerar Reserved Instances
- Usar Spot Instances para cargas não críticas
- Implementar governança com Azure Policies

---

## 🔗 Links Üteis

- [Criar uma Máquina Virtual do Windows - Microsoft Learn](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
- [Criar uma Máquina Virtual do Linux - Microsoft Learn](https://learn.microsoft.com/pt-br/azure/virtual-machines/linux/quick-create-portal)
- [Documentação do Azure VMs](https://learn.microsoft.com/pt-br/azure/virtual-machines/)
- [Preços Azure](https://azure.microsoft.com/pt-br/pricing/details/virtual-machines/)

---

## 🎆 Conclusão

A Azure Virtual Machines oferece uma solução robusta, escalável e cost-effective para computação em nuvem. Com os benefícios da nuvem - como escalabilidade, confiabilidade e segurança - as VMs são ideais para empresas que buscam modernizar sua infraestrutura.
