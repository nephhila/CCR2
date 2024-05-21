# REATOR BATELADA - CINÉTICA E CÁLCULO DE REATORES 🧪

🔹CÓDIGO #2 - REAÇÃO ELEMENTAR DE SEGUNDA ORDEM

📌 INTRODUÇÃO 📌

Este código realiza a simulação de uma reação de segunda ordem do tipo aA + bB → cC + dD. Ele calcula e plota as concentrações do reagente (A) e do produto (B) ao longo do tempo, além de fornecer uma opção para verificar a conversão do reagente em um ponto específico do tempo. O objetivo é que ele seja versátil e simples justamente para que possa ser alterado conforme as necessidades da empresa e/ou do usuário.

#️⃣ O MÉTODO NUMÉRICO #️⃣

Baseado em fórmulas analíticas derivadas para reações de segunda ordem, as fórmulas permitem calcular diretamente a concentração dos reagentes e produtos em função do tempo.Em uma reação deste tipo a taxa de reação é proporcional ao produto das concentrações dos dois reagentes, então a velocidade desta reação pode ser expressa como:

* r = k_B [A][B]

Onde:

* [A] é a concentração do reagente A
* [B] é a concentração do reagente B
* k_B é a constante de velocidade da reação

O método analítico é muito útil para reações de segunda ordem e não requer a utilização de métodos mais complexos.

▶️ FUNCIONALIDADE DO CÓDIGO ▶️

 1. Funções de cálculo das concentrações dos reagentes:

	> concentracao_reagente_A(cA0, kB, t): Calcula a concentração do reagente A em um determinado tempo t. A fórmula utilizada é [A] (t) = [A0] / 1 + k * [A]0 * t
	> concentracao_reagente_B(cB0, kB, t):: Calcula a concentração do reagente B em um determinado tempo t. A fórmula utilizada é [B] (t) = [B0] / 1 + k * [B]0 * t

 2. Funções de cálculo das concentrações dos produtos:

* Obtidas considerando que a formação de produtos é diretamente proporcional ao consumo dos reagentes

	> concentracao_produto_C(cA0, cB0, kB, t): A fórmula utilizada é C (t) = [A]0 * [B]0 * k * t / 1 + k * [A]0 * t
 
	> concentracao_produto_D(cA0, cB0, kB, t): A fórmula utilizada é D (t) = [A]0 * [B]0 * k * t / 1 + k * [B]0 * t

 3. Conversão dos reagentes:

* É a medida da fração do reagente que foi consumida durante a reação

	> conversao_reagente_A(cA0, cA): A fórmula utilizada é Xa (t) = [A]0 - [A] (t) / [A]0
 
	> conversao_reagente_B(cB0, cB): A fórmula utilizada é Xb (t) = [B]0 - [B] (t) / [B]0


 4. Interação com o usuário:

	> O usuário fornece as condições iniciais (concentrações iniciais dos reagentes, constante de velocidade e tempo final da simulação).
 
	> Uma seção opcional permite ao usuário verificar a conversão do reagente em um ponto específico no tempo. A conversão é calculada como Conversão = (1 - A/[A]_0) * 100.

 5. Simulação e Plotagem:

	> O código utiliza a função np.linspace para criar uma série de pontos no tempo de 0 até o tempo final especificado.
 
	> As concentrações dos reagentes e produtos são calculadas para cada ponto no tempo utilizando as funções definidas.
 
	> Duas figuras são geradas usando matplotlib:
 
	* A primeira figura mostra as concentrações de A, B, C e D ao longo do tempo.
	* A segunda figura mostra a conversão dos reagentes A e B ao longo do tempo.

💻 TECNOLOGIAS UTILIZADAS 💻 

 * Python (3.10.12)
 * Google Collab

🧑‍🔬 AUTORES 🧑‍🔬

 * DIMI FOGAÇA CANTELLI
 * GLEICI EVELLIN DE OLIVEIRA
 * PATRÍCIA LOUISE DA SILVA FERREIRA
 * TAINARA ADRIELE SCHUENKE

🔗 ACESSO AO PROJETO 🔗

https://github.com/nephhila/CCR2
