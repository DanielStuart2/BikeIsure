# BikeIsure - Sistema de Validação Online de Seguros de Bicletas 🚴‍♂️🤖

## 📝 Explicação do Projeto

### 1.1 Justificativa
Um sistema de validação online de seguros de bicicletas automatizado e robotizado é essencial para melhorar a eficiência e precisão do processo de validação, reduzindo o tempo de processamento de reclamações. Atualmente, a dependência de intervenção humana resulta em atrasos e erros. Com a automação, as seguradoras podem validar reclamações de forma rápida e precisa, comparando fotos de bicicletas registradas com as fotos da bicicleta roubada ou furtada. Isso aumenta a conveniência para o consumidor e reduz o risco de fraudes.

### 1.2 Objetivo
O objetivo do projeto **BikeIsure** é criar um sistema de vistoria online para a Porto Seguro, eliminando a necessidade de intervenção humana. Utilizamos tecnologias avançadas como **TensorFlow** e **React** para desenvolver uma solução moderna e segura. O sistema é treinado com o **Dataset COCO**, que utiliza imagens reais de bicicletas para aprimorar a inteligência artificial (IA), evitando fraudes como imagens modificadas, espelhadas ou baixadas da internet.

Além disso, o sistema é autossustentável: os próprios clientes alimentam o banco de dados com fotos de suas bicicletas durante a vistoria, permitindo que a IA aprenda com seus erros e melhore continuamente. A interface é intuitiva e acessível, com mensagens claras para guiar o cliente durante o processo.

O **BikeIsure** é versátil e pode ser adaptado para outros tipos de vistorias, como veículos, casas ou celulares, tornando-o uma solução escalável para a Porto Seguro.

### 1.3 Conclusão
O sistema está em fase final de desenvolvimento, com funcionalidades como reconhecimento de números de série e detecção de imagens fraudulentas já implementadas. A simplicidade e agilidade do sistema atendem às expectativas dos consumidores, oferecendo uma experiência rápida e segura. A capacidade de autocorreção da IA e a versatilidade do sistema são diferenciais que posicionam a Porto Seguro à frente da concorrência.

---

## 🎥 Vídeo Explicativo
Para uma visão detalhada do projeto, assista ao [vídeo explicativo](https://www.youtube.com/watch?v=UXw2VwCRTx4).

---

## 🛠️ Tecnologias Utilizadas
- **TensorFlow**: Para aprendizado de máquina e reconhecimento de imagens.
- **React**: Para a interface do usuário.
- **Dataset COCO**: Para treinamento da IA com imagens reais de bicicletas.
- **API VIACEP**: Para integração de endereços com base no CEP (uso demonstrativo).

---

## 📋 Instruções para Execução
1. **Banco de Dados**:
   - Crie as tabelas necessárias com os comandos SQL fornecidos:
     ```sql
     create table bicicleta (
       cd_bicicleta NUMERIC (4) constraint pk_bicicleta primary key,
       id_cliente NUMERIC (5),
       cd_marca NUMERIC(4),
       cd_foto NUMERIC (4),
       ds_cor VARCHAR2(20),
       ds_numero_serie NUMERIC(9) NOT NULL UNIQUE,
       ds_preco_nota_fiscal NUMBER (10,2),
       an_ano_compra date
     );

     CREATE TABLE cliente(
       id_cliente NUMERIC (5) constraint pk_cliente primary key,
       nm_nome VARCHAR2 (60),
       numero_cpf CHAR (11),
       numero_rg CHAR (9),
       contato_cliente VARCHAR2(15),
       dt_nascimento DATE,
       el_email VARCHAR2(100)
     );
     ```

2. **Configuração do Código**:
   - No arquivo `functions.py`, atualize os caminhos nas linhas 8 e 15 para os locais onde estão o `login.json` e a pasta `instaclient_21_11`.

3. **Execução**:
   - Execute o código Python para testar a funcionalidade do sistema.

---

## 📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---
