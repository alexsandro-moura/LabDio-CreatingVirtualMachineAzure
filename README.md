# LabDio-CreatingVirtualMachineAzure
Resumo do processo de criação e configuração de uma máquina virtual na Microsoft Azure

1. Acessar o Portal Azure
Vá para https://portal.azure.com

Faça login com sua conta.

2. Criar um novo recurso
Clique em "Criar um recurso".

Pesquise por “Máquina Virtual” e selecione "Virtual Machine".

3. Configurar as Informações Básicas
Preencha os dados iniciais:

Assinatura e Grupo de Recursos

Nome da VM

Região (escolha a mais próxima para melhor desempenho)

Imagem (Windows, Ubuntu, CentOS, etc.)

Tamanho da VM (escolha com base no uso: B1s para testes, D2s para produção leve)

Usuário e senha/SSH: método de acesso

📝 Dica:
Para ambientes de teste ou estudo, use imagens gratuitas e tamanhos menores (economiza 💰).

4. Disco do Sistema Operacional
Escolha o tipo de disco:

Standard HDD (mais barato, desempenho básico)

Standard SSD (boa opção equilibrada)

Premium SSD (alto desempenho, mas mais caro)

📝 Dica:
Para ambientes críticos, vá de Premium SSD. Para testes, HDD ou Standard SSD bastam.

5. Rede
Crie ou selecione uma rede virtual (VNet)

Configure o grupo de segurança de rede (NSG):

Libere a porta 3389 (Windows) ou 22 (Linux) para acesso remoto.

📝 Dica de segurança:
Não exponha portas diretamente à internet! Use IPs restritos ou o Azure Bastion.

6. Configurações Adicionais
Ative Auto-shutdown (útil para máquinas de teste).

Ative Monitoramento (logs, métricas, diagnósticos).

Use tags para organização, especialmente em ambientes corporativos.

7. Revisar e Criar
Verifique todas as opções.

Clique em "Criar". O Azure provisionará a VM em alguns minutos.

8. Acessar a Máquina Virtual
Após criada, vá até o recurso.

Use o IP público e a senha/SSH para se conectar:

Windows: via RDP (Área de Trabalho Remota)

Linux: via terminal SSH
