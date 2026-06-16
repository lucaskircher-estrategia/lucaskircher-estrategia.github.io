# lucaskircher-estrategia.github.io
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora do Novo Social v2 | DZ Studio</title>
    <style>
        :root {
            --bg-color: #0f0f11;
            --card-bg: #18181c;
            --accent-color: #ff5e00;
            --text-color: #f1f1f5;
            --text-muted: #9e9eac;
            --border-color: #2c2c35;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            max-width: 650px;
            width: 100%;
            background: var(--card-bg);
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
            border: 1px solid var(--border-color);
        }

        h1 {
            font-size: 24px;
            margin-bottom: 8px;
            color: #fff;
        }

        .subtitle {
            font-size: 14px;
            color: var(--text-muted);
            margin-bottom: 30px;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 15px;
        }

        .question {
            margin-bottom: 25px;
        }

        .question-title {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 4px;
            color: #fff;
        }

        .question-hint {
            font-size: 12px;
            color: var(--text-muted);
            margin-bottom: 12px;
        }

        .options-group {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .option-label {
            display: flex;
            align-items: flex-start;
            gap: 12px;
            padding: 14px;
            background: #202024;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: 14px;
            line-height: 1.4;
        }

        .option-label:hover {
            border-color: var(--accent-color);
            background: #242429;
        }

        input[type="checkbox"], input[type="radio"] {
            margin-top: 3px;
            accent-color: var(--accent-color);
        }

        button {
            width: 100%;
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 16px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.2s;
            margin-top: 15px;
        }

        button:hover {
            background-color: #e05300;
        }

        #result-screen {
            display: none;
        }

        .result-box {
            background: #202024;
            border: 1px solid var(--accent-color);
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 25px;
            text-align: center;
        }

        .price-tag {
            font-size: 36px;
            font-weight: 800;
            color: var(--accent-color);
            margin: 15px 0;
        }

        .pitch-box {
            background: #131316;
            border-left: 4px solid var(--text-muted);
            padding: 15px;
            font-style: italic;
            font-size: 14px;
            color: #d1d1d6;
            line-height: 1.6;
            white-space: pre-line;
        }

        .reset-btn {
            background-color: transparent;
            border: 1px solid var(--border-color);
            color: var(--text-muted);
            margin-top: 20px;
        }
        .reset-btn:hover {
            background-color: #202024;
            color: #fff;
        }
    </style>
</head>
<body>

<div class="container">
    <form id="quiz-form">
        <h1>Diagnóstico do Novo Social</h1>
        <div class="subtitle">Descubra a postura de marca e o escopo ideal para o seu e-commerce.</div>

        <!-- Q1 (Checkbox) -->
        <div class="question">
            <div class="question-title">1. Quando um cliente decide NÃO comprar de você, quais costumam ser os motivos?</div>
            <div class="question-hint">Selecione todas as opções que se aplicam.</div>
            <div class="options-group">
                <label class="option-label"><input type="checkbox" name="pilar-points" value="cultura"> Ele simplesmente não lembra que a nossa marca existe ou nos acha muito frios/corporativos.</label>
                <label class="option-label"><input type="checkbox" name="pilar-points" value="resposta"> Ele fica inseguro, tem muitas dúvidas técnicas ou acha o nosso produto complexo.</label>
                <label class="option-label"><input type="checkbox" name="pilar-points" value="vitrine"> Ele até quer o produto, mas desiste no meio do caminho porque o processo de compra ou o site é chato.</label>
            </div>
        </div>

        <!-- Q2 (Checkbox) -->
        <div class="question">
            <div class="question-title">2. Como é a dinâmica de desejo do seu produto no mercado?</div>
            <div class="question-hint">Selecione todas as opções que se aplicam.</div>
            <div class="options-group">
                <label class="option-label"><input type="checkbox" name="pilar-points" value="resposta"> É um produto de escolha lógica. O cliente pesquisa muito, compara preços e busca especificações.</label>
                <label class="option-label"><input type="checkbox" name="pilar-points" value="cultura"> É pura identificação ou impulso. O cliente compra porque se conectou com a nossa identidade ou estética.</label>
                <label class="option-label"><input type="checkbox" name="pilar-points" value="vitrine"> Nós dependemos de campanhas agressivas de conversão, promoções e estoque girando rápido.</label>
            </div>
        </div>

        <!-- Q3 (Checkbox) -->
        <div class="question">
            <div class="question-title">3. Se fôssemos criar conteúdos em vídeo hoje, quais cenários seriam úteis para o seu comercial?</div>
            <div class="question-hint">Selecione todas as opções que se aplicam.</div>
            <div class="options-group">
                <label class="option-label"><input type="checkbox" name="pilar-points" value="cultura"> Vídeos que inserem a marca em trends do momento, gerando compartilhamentos por DM.</label>
                <label class="option-label"><input type="checkbox" name="pilar-points" value="resposta"> Vídeos tutoriais ou explicativos que respondem exatamente ao que o cliente digita na busca.</label>
                <label class="option-label"><input type="checkbox" name="pilar-points" value="vitrine"> Vídeos nativos de produto (tipo TikTok Shop) com atalho direto de compra.</label>
            </div>
        </div>

        <!-- Q4 (Radio - Obrigatório) -->
        <div class="question">
            <div class="question-title">4. Como funciona a rotina de marketing e captação de conteúdo na sua empresa hoje?</div>
            <div class="question-hint">Escolha apenas uma opção.</div>
            <div class="options-group">
                <label class="option-label"><input type="radio" name="q4" value="1" required> Não temos ninguém interno para coletar imagens ou gravar vídeos. Dependemos 100% de terceiros.</label>
                <label class="option-label"><input type="radio" name="q4" value="2"> Temos pessoas em campo ou equipe interna que consegue enviar trechos brutos de vídeo toda semana.</label>
                <label class="option-label"><input type="radio" name="q4" value="3"> Temos uma infraestrutura robusta de e-commerce e catálogo integrado, além de braço para mídia.</label>
            </div>
        </div>

        <!-- Q5 (Radio - Obrigatório) -->
        <div class="question">
            <div class="question-title">5. Quanto tempo a sua liderança ou o compliance leva para aprovar uma ideia de conteúdo oportuna?</div>
            <div class="question-hint">Escolha apenas uma opção.</div>
            <div class="options-group">
                <label class="option-label"><input type="radio" name="q5" value="1" required> Aprovamos em até 2 horas via WhatsApp. Temos autonomia total.</label>
                <label class="option-label"><input type="radio" name="q5" value="2"> Leva de 2 a 5 dias úteis. Precisa passar por gerências ou jurídico.</label>
            </div>
        </div>

        <button type="submit">Calcular Escopo Ideal</button>
    </form>

    <!-- Tela de Resultados -->
    <div id="result-screen">
        <h1>Resultado do Diagnóstico</h1>
        <div class="subtitle">Este é o escopo técnico e financeiro sugerido para o projeto.</div>

        <div class="result-box">
            <div style="font-size: 14px; color: var(--text-muted);">Modelo Recomendado</div>
            <div id="recommended-model" style="font-size: 20px; font-weight: bold; margin: 5px 0; color: #fff;">-</div>
            <div style="font-size: 14px; color: var(--text-muted); margin-top: 10px;">Tamanho de Escopo</div>
            <div id="recommended-size" style="font-size: 18px; font-weight: bold; color: #fff;">-</div>
            <div class="price-tag" id="calculated-price">R$ 0,00</div>
        </div>

        <div class="question-title">Script de Apresentação Comercial:</div>
        <div class="pitch-box" id="commercial-pitch"></div>

        <button class="reset-btn" onclick="resetQuiz()">Refazer Diagnóstico</button>
    </div>
</div>

<script>
    const pricingMatrix = {
        "O Ímã Cultural": { "P": "R$ 4.500", "M": "R$ 9.500", "G": "R$ 22.000" },
        "O Varejista Persuasivo": { "P": "R$ 5.000", "M": "R$ 11.000", "G": "R$ 26.000" },
        "O Conversor de Atenção": { "P": "R$ 6.000", "M": "R$ 13.000", "G": "R$ 30.000+" }
    };

    document.getElementById('quiz-form').addEventListener('submit', function(e) {
        e.preventDefault();

        // 1. Contagem dos Checkboxes (Bloco 1)
        let cultura = 0, resposta = 0, vitrine = 0;
        const checkboxes = document.querySelectorAll('input[name="pilar-points"]:checked');
        
        // Validação caso o cliente não marque nada nas três primeiras
        if (checkboxes.length === 0) {
            alert("Por favor, selecione ao menos uma opção de desafio ou objetivo nas perguntas iniciais.");
            return;
        }

        checkboxes.forEach(cb => {
            if (cb.value === "cultura") cultura += 2;
            if (cb.value === "resposta") resposta += 2;
            if (cb.value === "vitrine") vitrine += 2;
        });

        // 2. Lógica de Pareamento dos dois maiores pilares
        const pillars = [
            { name: "cultura", score: cultura },
            { name: "resposta", score: resposta },
            { name: "vitrine", score: vitrine }
        ];

        // Ordena do maior score para o menor
        pillars.sort((a, b) => b.score - a.score);

        let model = "";
        // Se houver empate triplo total ou Cultura e Resposta dominarem
        if (pillars[0].score === pillars[2].score || (pillars[0].name === "cultura" && pillars[1].name === "resposta") || (pillars[0].name === "resposta" && pillars[1].name === "cultura")) {
            model = "O Ímã Cultural";
        } else if ((pillars[0].name === "resposta" && pillars[1].name === "vitrine") || (pillars[0].name === "vitrine" && pillars[1].name === "resposta")) {
            model = "O Varejista Persuasivo";
        } else {
            model = "O Conversor de Atenção";
        }

        // 3. Cálculo da Complexidade (Tamanho - Bloco 2)
        const q4 = parseInt(document.querySelector('input[name="q4"]:checked').value);
        const q5 = parseInt(document.querySelector('input[name="q5"]:checked').value);
        
        // Adiciona um bônus de complexidade se o cliente tiver marcado muitos objetivos juntos
        let multiObjectiveBonus = checkboxes.length >= 5 ? 1 : 0;
        
        const sizeScore = q4 + q5 + multiObjectiveBonus;
        let size = "P";
        if (sizeScore <= 3) size = "P";
        else if (sizeScore === 4) size = "M";
        else size = "G";

        // 4. Cruzamento de Preço
        const finalPrice = pricingMatrix[model][size];

        // 5. Renderização
        document.getElementById('recommended-model').innerText = model;
        document.getElementById('recommended-size').innerText = `Tamanho ${size}`;
        document.getElementById('calculated-price').innerText = `${finalPrice} / mês`;

        const pitch = `"Entendendo que os seus desafios envolvem múltiplas frentes do Novo Social, o sistema da DZ cruzou os seus objetivos com a sua capacidade operacional de aprovação e infraestrutura.\n\nA recomendação ideal para o seu cenário é a implementação do modelo **${model}** estruturado no **Tamanho ${size}**.\n\nPara este escopo combinado, o seu investimento mensal estimado fica em **${finalPrice}**. Esse valor reflete a alocação de horas do nosso time de especialistas focado em dar tração real ao seu negócio, contornando os gargalos apontados no diagnóstico.\n\n*Nota: Este valor compreende o fee de estratégia e execução da agência. Verbas de mídia e contratos de creators terceiros serão orçados na proposta definitiva.*"`;
        
        document.getElementById('commercial-pitch').innerText = pitch;

        document.getElementById('quiz-form').style.display = 'none';
        document.getElementById('result-screen').style.display = 'block';
    });

    function resetQuiz() {
        document.getElementById('quiz-form').reset();
        document.getElementById('quiz-form').style.display = 'block';
        document.getElementById('result-screen').style.display = 'none';
    }
</script>

</body>
</html>
