# resumo-do-lab-Configurando-Recursos-e-Dimensionamentos-em-Maquinas-Virtuais-na-Azure
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

# Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

Este repositório fornece uma visão geral e explicação sobre como configurar recursos e dimensionar **Máquinas Virtuais (VMs)** na **Microsoft Azure**. A criação e dimensionamento adequado de VMs são fundamentais para garantir que as cargas de trabalho rodem de forma eficiente, segura e com o melhor custo-benefício. Configurar recursos e dimensionar VMs na Azure é essencial para garantir desempenho eficiente e otimização de custos para seus aplicativos.

## 1. **Escolhendo a Imagem da Máquina Virtual**
Antes de criar uma **VM**, é necessário escolher a imagem do sistema operacional (SO) que será executado na máquina virtual. A Azure oferece imagens para os seguintes sistemas operacionais:
- **Windows Server** (variações como 2016, 2019)
- **Ubuntu**
- **RedHat**
- **CentOS**
- **Debian**

A escolha da imagem depende da aplicação que será executada na VM.


## 2. **Selecionando o Tipo de Série da VM**
A Azure oferece várias **séries de VMs**, cada uma projetada para cenários específicos de uso:
- **B-series**: Máquinas de baixo custo, recomendadas para cargas de trabalho de baixo desempenho.
- **D-series**: Máquinas equilibradas, adequadas para cargas de trabalho de médio porte.
- **F-series**: Focadas em alto desempenho de processamento, com maior capacidade de CPU.


## 3. **Definindo o Tamanho da VM**
O **tamanho** da VM envolve a definição de:
- **Número de núcleos de CPU**
- **Memória RAM** (tamanho em GB)
- **Armazenamento** (tamanho do disco de sistema e dados)
  - Escolha a série apropriada de VM baseada no tipo de carga de trabalho.
  - Determine o tamanho da VM que especifica CPU, memória e outras características.

A Azure oferece uma variedade de tamanhos de VM para atender diferentes necessidades. O dimensionamento correto depende das necessidades da aplicação e da carga de trabalho.


## 4. **Escolhendo o Armazenamento**
O armazenamento das VMs no Azure pode ser dividido em:
- **Discos do Sistema Operacional**: O disco principal onde o SO está instalado.
- **Discos de Dados**: Usados para armazenar dados da aplicação ou banco de dados.

O Azure oferece dois tipos principais de armazenamento:
- **Standard**: Armazenamento baseado em HDD (mais econômico).
- **Premium**: Armazenamento baseado em SSD (mais rápido e adequado para workloads intensivas).
  - Selecione entre diferentes tipos de discos (HDD, SSD padrão, SSD premium) conforme suas necessidades.
  - Configure discos adicionais para dados temporários, cache ou armazenamento persistente.


## 5. **Configuração de Rede**
Cada VM no Azure necessita de uma configuração de rede:
- **Endereço IP**: Endereço público ou privado para comunicação com outros recursos.
- **Sub-rede**: A sub-rede dentro de uma **Rede Virtual (VNet)** onde a VM será criada.
- **Interfaces de Rede**: Configurações que permitem à VM se comunicar com outras VMs ou com a internet.

Além disso, é possível configurar **Grupos de Segurança de Rede (NSG)** para controlar o tráfego de entrada e saída. Configure interfaces de rede, incluindo IPs públicos e privados e utilize **VNet** para isolar VMs para configurar **sub-redes** e **peering**.


## 6. **Escalabilidade e Autoescalamento**
O Azure permite a configuração de **VMs escaláveis** usando o **Virtual Machine Scale Sets (VMSS)**. Isso permite adicionar ou remover instâncias de VMs automaticamente com base na demanda. A funcionalidade de **autoescalamento** é útil para manter a performance e otimizar os custos, especialmente durante picos de uso.

### Vertical Scaling (Escalonamento Vertical)
- Adicione mais recursos (CPU, memória) à VM existente.
- Use SKUs maiores da mesma série para aumentar os recursos disponíveis.

### Horizontal Scaling (Escalonamento Horizontal)
- Adicione mais instâncias de VMs para distribuir a carga.
- Utilize VM Scale Sets para gerenciar um grupo de VMs idênticas.


## 7. **Monitoramento e Otimização**
O **Azure Monitor** oferece uma maneira de acompanhar o desempenho das VMs. Ele coleta métricas como uso de CPU, memória, I/O de disco e tráfego de rede. Usando esses dados, você pode:
- Ajustar os recursos (por exemplo, aumentar a RAM ou CPU)
- Alterar o tipo de série da VM para otimizar o desempenho
- Definir alertas para monitorar a saúde da VM e detectar problemas precocemente.

  ### Boas Práticas
   1. **Monitoramento e Ajustes**
      - Use Azure Monitor e Application Insights para monitorar o desempenho e ajustar os recursos conforme necessário.
   2. **Automação**
      - Utilize scripts e templates ARM para automatizar a criação e configuração das VMs.
   3. **Custo-benefício**
      - Analise a relação custo-benefício ao escolher tipos de VMs e armazenamento, equilibrando desempenho e custo.

## Conclusão
A configuração adequada de recursos e dimensionamento das **Máquinas Virtuais no Azure** é fundamental para garantir que sua aplicação rode com alta performance, escalabilidade e baixo custo. Lembre-se de escolher o tipo de série e o tamanho adequado, configurar a rede corretamente e monitorar o desempenho para otimizar os recursos.

## Recursos Adicionais
- [Documentação oficial do Azure - Máquinas Virtuais](https://learn.microsoft.com/en-us/azure/virtual-machines/)
- [Guia de Dimensionamento de VMs no Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/sizes)
- [DIO - Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure](https://web.dio.me/project/computacao-e-rede-laboratorio/learning/85b45fef-7863-4c43-a211-a1c4342f9cda?back=/track/microsoft-azure-essentials&tab=undefined&moduleId=undefined)

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para fazer um fork deste repositório e enviar pull requests.

## Licença

Este repositório está licenciado sob a [MIT License](LICENSE).

## Contato

Se você tiver dúvidas ou sugestões, entre em contato através do meu e-mail: [anderson.coelho.2477@gmail.com]
