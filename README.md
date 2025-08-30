# hse.github.io

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Avaliação de Desempenho - Técnico de Segurança Offshore</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f5f5f5;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(135deg, #2c3e50, #3498db);
            color: white;
            padding: 30px;
            text-align: center;
        }
        
        .header h1 {
            font-size: 2.2em;
            margin-bottom: 10px;
        }
        
        .header p {
            font-size: 1.1em;
            opacity: 0.9;
        }
        
        .form-section {
            padding: 30px;
        }
        
        .employee-info {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 30px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            font-weight: 600;
            margin-bottom: 8px;
            color: #2c3e50;
        }
        
        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 2px solid #e1e8ed;
            border-radius: 5px;
            font-size: 16px;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
            outline: none;
            border-color: #3498db;
        }
        
        .evaluation-section {
            margin: 30px 0;
        }
        
        .section-title {
            background: #34495e;
            color: white;
            padding: 15px 20px;
            margin: 0 -30px 20px -30px;
            font-size: 1.3em;
            font-weight: 600;
        }
        
        .competency-group {
            border: 1px solid #e1e8ed;
            border-radius: 8px;
            margin-bottom: 20px;
            overflow: hidden;
        }
        
        .competency-header {
            background: #ecf0f1;
            padding: 15px 20px;
            font-weight: 600;
            color: #2c3e50;
            border-bottom: 1px solid #e1e8ed;
        }
        
        .competency-items {
            padding: 20px;
        }
        
        .competency-item {
            display: grid;
            grid-template-columns: 2fr 100px 1fr;
            gap: 15px;
            align-items: center;
            padding: 15px 0;
            border-bottom: 1px solid #f0f0f0;
        }
        
        .competency-item:last-child {
            border-bottom: none;
        }
        
        .competency-desc {
            font-weight: 500;
        }
        
        .rating-scale {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .rating-scale input[type="radio"] {
            width: auto;
            margin: 0 2px;
        }
        
        .scale-labels {
            display: flex;
            justify-content: space-between;
            font-size: 0.8em;
            color: #666;
            margin-top: 5px;
        }
        
        .comments-area {
            width: 100%;
            min-height: 60px;
            resize: vertical;
        }
        
        .score-summary {
            background: #f8f9fa;
            border: 2px solid #3498db;
            border-radius: 10px;
            padding: 25px;
            margin: 30px 0;
            text-align: center;
        }
        
        .score-display {
            font-size: 3em;
            font-weight: bold;
            color: #3498db;
            margin: 10px 0;
        }
        
        .score-category {
            font-size: 1.2em;
            font-weight: 600;
            margin-top: 10px;
        }
        
        .action-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin: 30px 0;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 12px 30px;
            border: none;
            border-radius: 6px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .btn-primary {
            background: #3498db;
            color: white;
        }
        
        .btn-primary:hover {
            background: #2980b9;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background: #95a5a6;
            color: white;
        }
        
        .btn-secondary:hover {
            background: #7f8c8d;
        }
        
        .development-plan {
            background: #fff3cd;
            border: 1px solid #ffeaa7;
            border-radius: 8px;
            padding: 20px;
            margin: 20px 0;
            display: none;
        }
        
        .legend {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 5px;
            margin: 20px 0;
        }
        
        .legend h4 {
            margin-bottom: 10px;
            color: #2c3e50;
        }
        
        .legend-item {
            display: flex;
            justify-content: space-between;
            margin: 5px 0;
            font-size: 0.9em;
        }
        
        @media (max-width: 768px) {
            .container {
                margin: 10px;
            }
            
            .competency-item {
                grid-template-columns: 1fr;
                gap: 10px;
            }
            
            .action-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Avaliação de Desempenho</h1>
            <p>Técnico de Segurança do Trabalho - Operações Offshore</p>
        </div>
        
        <div class="form-section">
            <!-- Informações do Colaborador -->
            <div class="employee-info">
                <div class="form-group">
                    <label for="employeeName">Nome do Colaborador:</label>
                    <input type="text" id="employeeName" placeholder="Nome completo">
                </div>
                <div class="form-group">
                    <label for="evaluationDate">Data da Avaliação:</label>
                    <input type="date" id="evaluationDate">
                </div>
                <div class="form-group">
                    <label for="evaluatorName">Avaliador:</label>
                    <input type="text" id="evaluatorName" placeholder="Nome do gestor">
                </div>
                <div class="form-group">
                    <label for="workPeriod">Tempo na Posição:</label>
                    <select id="workPeriod">
                        <option value="">Selecione</option>
                        <option value="0-3">0-3 meses</option>
                        <option value="3-6">3-6 meses</option>
                        <option value="6-12">6-12 meses</option>
                        <option value="12+">Mais de 12 meses</option>
                    </select>
                </div>
            </div>

            <!-- Legenda da Escala -->
            <div class="legend">
                <h4>Escala de Avaliação (1-5):</h4>
                <div class="legend-item">
                    <span><strong>1 - Insatisfatório:</strong></span>
                    <span>Não atende aos requisitos mínimos</span>
                </div>
                <div class="legend-item">
                    <span><strong>2 - Abaixo do Esperado:</strong></span>
                    <span>Atende parcialmente, precisa de melhorias</span>
                </div>
                <div class="legend-item">
                    <span><strong>3 - Atende Expectativas:</strong></span>
                    <span>Desempenho adequado e satisfatório</span>
                </div>
                <div class="legend-item">
                    <span><strong>4 - Acima do Esperado:</strong></span>
                    <span>Bom desempenho, supera expectativas</span>
                </div>
                <div class="legend-item">
                    <span><strong>5 - Excepcional:</strong></span>
                    <span>Excelente desempenho, referência para equipe</span>
                </div>
            </div>

            <!-- Seção 1: Competências Técnicas -->
            <div class="evaluation-section">
                <div class="section-title">1. COMPETÊNCIAS TÉCNICAS DE SEGURANÇA</div>
                
                <div class="competency-group">
                    <div class="competency-header">Conhecimento Técnico</div>
                    <div class="competency-items">
                        <div class="competency-item">
                            <div class="competency-desc">Domínio das NRs aplicáveis (NR-10, NR-12, NR-33, NR-34, NR-35)</div>
                            <div class="rating-scale">
                                <input type="radio" name="nr_knowledge" value="1">
                                <input type="radio" name="nr_knowledge" value="2">
                                <input type="radio" name="nr_knowledge" value="3">
                                <input type="radio" name="nr_knowledge" value="4">
                                <input type="radio" name="nr_knowledge" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Identificação e análise de riscos offshore</div>
                            <div class="rating-scale">
                                <input type="radio" name="risk_analysis" value="1">
                                <input type="radio" name="risk_analysis" value="2">
                                <input type="radio" name="risk_analysis" value="3">
                                <input type="radio" name="risk_analysis" value="4">
                                <input type="radio" name="risk_analysis" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Elaboração de PT (Permissão de Trabalho) e APR</div>
                            <div class="rating-scale">
                                <input type="radio" name="permit_work" value="1">
                                <input type="radio" name="permit_work" value="2">
                                <input type="radio" name="permit_work" value="3">
                                <input type="radio" name="permit_work" value="4">
                                <input type="radio" name="permit_work" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Conhecimento de equipamentos de segurança offshore</div>
                            <div class="rating-scale">
                                <input type="radio" name="safety_equipment" value="1">
                                <input type="radio" name="safety_equipment" value="2">
                                <input type="radio" name="safety_equipment" value="3">
                                <input type="radio" name="safety_equipment" value="4">
                                <input type="radio" name="safety_equipment" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Seção 2: Competências Comportamentais -->
            <div class="evaluation-section">
                <div class="section-title">2. COMPETÊNCIAS COMPORTAMENTAIS</div>
                
                <div class="competency-group">
                    <div class="competency-header">Motivação e Engajamento</div>
                    <div class="competency-items">
                        <div class="competency-item">
                            <div class="competency-desc">Proatividade na execução das atividades</div>
                            <div class="rating-scale">
                                <input type="radio" name="proactivity" value="1">
                                <input type="radio" name="proactivity" value="2">
                                <input type="radio" name="proactivity" value="3">
                                <input type="radio" name="proactivity" value="4">
                                <input type="radio" name="proactivity" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Adesão às demandas obrigatórias offshore</div>
                            <div class="rating-scale">
                                <input type="radio" name="compliance" value="1">
                                <input type="radio" name="compliance" value="2">
                                <input type="radio" name="compliance" value="3">
                                <input type="radio" name="compliance" value="4">
                                <input type="radio" name="compliance" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Demonstração de interesse no crescimento profissional</div>
                            <div class="rating-scale">
                                <input type="radio" name="growth_interest" value="1">
                                <input type="radio" name="growth_interest" value="2">
                                <input type="radio" name="growth_interest" value="3">
                                <input type="radio" name="growth_interest" value="4">
                                <input type="radio" name="growth_interest" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                    </div>
                </div>
                
                <div class="competency-group">
                    <div class="competency-header">Relacionamento Interpessoal</div>
                    <div class="competency-items">
                        <div class="competency-item">
                            <div class="competency-desc">Comunicação efetiva com a equipe</div>
                            <div class="rating-scale">
                                <input type="radio" name="communication" value="1">
                                <input type="radio" name="communication" value="2">
                                <input type="radio" name="communication" value="3">
                                <input type="radio" name="communication" value="4">
                                <input type="radio" name="communication" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Colaboração e trabalho em equipe</div>
                            <div class="rating-scale">
                                <input type="radio" name="teamwork" value="1">
                                <input type="radio" name="teamwork" value="2">
                                <input type="radio" name="teamwork" value="3">
                                <input type="radio" name="teamwork" value="4">
                                <input type="radio" name="teamwork" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Relacionamento com outras equipes/contratante</div>
                            <div class="rating-scale">
                                <input type="radio" name="external_relations" value="1">
                                <input type="radio" name="external_relations" value="2">
                                <input type="radio" name="external_relations" value="3">
                                <input type="radio" name="external_relations" value="4">
                                <input type="radio" name="external_relations" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Gestão de conflitos e assertividade</div>
                            <div class="rating-scale">
                                <input type="radio" name="conflict_management" value="1">
                                <input type="radio" name="conflict_management" value="2">
                                <input type="radio" name="conflict_management" value="3">
                                <input type="radio" name="conflict_management" value="4">
                                <input type="radio" name="conflict_management" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Seção 3: Adaptação ao Ambiente Offshore -->
            <div class="evaluation-section">
                <div class="section-title">3. ADAPTAÇÃO AO AMBIENTE OFFSHORE</div>
                
                <div class="competency-group">
                    <div class="competency-header">Características Específicas Offshore</div>
                    <div class="competency-items">
                        <div class="competency-item">
                            <div class="competency-desc">Resistência física e mental para embarcações</div>
                            <div class="rating-scale">
                                <input type="radio" name="physical_resistance" value="1">
                                <input type="radio" name="physical_resistance" value="2">
                                <input type="radio" name="physical_resistance" value="3">
                                <input type="radio" name="physical_resistance" value="4">
                                <input type="radio" name="physical_resistance" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Adaptação aos horários e rotinas offshore</div>
                            <div class="rating-scale">
                                <input type="radio" name="schedule_adaptation" value="1">
                                <input type="radio" name="schedule_adaptation" value="2">
                                <input type="radio" name="schedule_adaptation" value="3">
                                <input type="radio" name="schedule_adaptation" value="4">
                                <input type="radio" name="schedule_adaptation" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Convivência em espaço confinado</div>
                            <div class="rating-scale">
                                <input type="radio" name="confined_space" value="1">
                                <input type="radio" name="confined_space" value="2">
                                <input type="radio" name="confined_space" value="3">
                                <input type="radio" name="confined_space" value="4">
                                <input type="radio" name="confined_space" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Gestão do stress e pressão do ambiente</div>
                            <div class="rating-scale">
                                <input type="radio" name="stress_management" value="1">
                                <input type="radio" name="stress_management" value="2">
                                <input type="radio" name="stress_management" value="3">
                                <input type="radio" name="stress_management" value="4">
                                <input type="radio" name="stress_management" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Seção 4: Satisfação e Engajamento -->
            <div class="evaluation-section">
                <div class="section-title">4. SATISFAÇÃO E ENGAJAMENTO</div>
                
                <div class="competency-group">
                    <div class="competency-header">Aspectos Motivacionais</div>
                    <div class="competency-items">
                        <div class="competency-item">
                            <div class="competency-desc">Nível de satisfação com a posição atual</div>
                            <div class="rating-scale">
                                <input type="radio" name="job_satisfaction" value="1">
                                <input type="radio" name="job_satisfaction" value="2">
                                <input type="radio" name="job_satisfaction" value="3">
                                <input type="radio" name="job_satisfaction" value="4">
                                <input type="radio" name="job_satisfaction" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Identificação com a empresa contratada</div>
                            <div class="rating-scale">
                                <input type="radio" name="company_identification" value="1">
                                <input type="radio" name="company_identification" value="2">
                                <input type="radio" name="company_identification" value="3">
                                <input type="radio" name="company_identification" value="4">
                                <input type="radio" name="company_identification" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Perspectiva de permanência na função</div>
                            <div class="rating-scale">
                                <input type="radio" name="retention_perspective" value="1">
                                <input type="radio" name="retention_perspective" value="2">
                                <input type="radio" name="retention_perspective" value="3">
                                <input type="radio" name="retention_perspective" value="4">
                                <input type="radio" name="retention_perspective" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Comprometimento com metas e resultados</div>
                            <div class="rating-scale">
                                <input type="radio" name="commitment" value="1">
                                <input type="radio" name="commitment" value="2">
                                <input type="radio" name="commitment" value="3">
                                <input type="radio" name="commitment" value="4">
                                <input type="radio" name="commitment" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Seção 5: Performance Operacional -->
            <div class="evaluation-section">
                <div class="section-title">5. PERFORMANCE OPERACIONAL</div>
                
                <div class="competency-group">
                    <div class="competency-header">Execução e Resultados</div>
                    <div class="competency-items">
                        <div class="competency-item">
                            <div class="competency-desc">Cumprimento de prazos e cronogramas</div>
                            <div class="rating-scale">
                                <input type="radio" name="deadlines" value="1">
                                <input type="radio" name="deadlines" value="2">
                                <input type="radio" name="deadlines" value="3">
                                <input type="radio" name="deadlines" value="4">
                                <input type="radio" name="deadlines" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Qualidade dos relatórios e documentações</div>
                            <div class="rating-scale">
                                <input type="radio" name="documentation_quality" value="1">
                                <input type="radio" name="documentation_quality" value="2">
                                <input type="radio" name="documentation_quality" value="3">
                                <input type="radio" name="documentation_quality" value="4">
                                <input type="radio" name="documentation_quality" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Autonomia na resolução de problemas</div>
                            <div class="rating-scale">
                                <input type="radio" name="problem_solving" value="1">
                                <input type="radio" name="problem_solving" value="2">
                                <input type="radio" name="problem_solving" value="3">
                                <input type="radio" name="problem_solving" value="4">
                                <input type="radio" name="problem_solving" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                        
                        <div class="competency-item">
                            <div class="competency-desc">Capacidade de tomada de decisão em situações críticas</div>
                            <div class="rating-scale">
                                <input type="radio" name="critical_decisions" value="1">
                                <input type="radio" name="critical_decisions" value="2">
                                <input type="radio" name="critical_decisions" value="3">
                                <input type="radio" name="critical_decisions" value="4">
                                <input type="radio" name="critical_decisions" value="5">
                            </div>
                            <textarea class="comments-area" placeholder="Comentários específicos..."></textarea>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Resumo da Avaliação -->
            <div class="score-summary">
                <h3>Resultado da Avaliação</h3>
                <div class="score-display" id="totalScore">0.0</div>
                <div class="score-category" id="scoreCategory">Aguardando avaliação</div>
                <p>Pontuação Total: <span id="detailedScore">0/100</span></p>
            </div>

            <!-- Seção de Desenvolvimento -->
            <div class="development-plan" id="developmentPlan">
                <h3>🎯 Plano de Desenvolvimento Sugerido</h3>
                <div id="developmentActions"></div>
            </div>

            <!-- Observações Gerais -->
            <div class="form-group">
                <label for="generalComments">Observações Gerais e Plano de Ação:</label>
                <textarea id="generalComments" rows="6" placeholder="Descreva observações gerais, pontos de melhoria, ações de desenvolvimento e próximos passos..."></textarea>
            </div>

            <!-- Botões de Ação -->
            <div class="action-buttons">
                <button class="btn btn-primary" onclick="calculateScore()">Calcular Pontuação</button>
                <button class="btn btn-secondary" onclick="generateReport()">Gerar Relatório</button>
                <button class="btn btn-secondary" onclick="clearForm()">Limpar Formulário</button>
            </div>
        </div>
    </div>

    <script>
        // Definir data atual
        document.getElementById('evaluationDate').value = new Date().toISOString().split('T')[0];
        
        function calculateScore() {
            const radioGroups = [
                'nr_knowledge', 'risk_analysis', 'permit_work', 'safety_equipment',
                'proactivity', 'compliance', 'growth_interest',
                'communication', 'teamwork', 'external_relations', 'conflict_management',
                'physical_resistance', 'schedule_adaptation', 'confined_space', 'stress_management',
                'job_satisfaction', 'company_identification', 'retention_perspective', 'commitment',
                'deadlines', 'documentation_quality', 'problem_solving', 'critical_decisions'
            ];
            
            let totalScore = 0;
            let answeredQuestions = 0;
            
            radioGroups.forEach(group => {
                const selectedRadio = document.querySelector(`input[name="${group}"]:checked`);
                if (selectedRadio) {
                    totalScore += parseInt(selectedRadio.value);
                    answeredQuestions++;
                }
            });
            
            if (answeredQuestions === 0) {
                alert('Por favor, responda pelo menos uma questão para calcular a pontuação.');
                return;
            }
            
            const averageScore = totalScore / answeredQuestions;
            const percentageScore = (averageScore / 5) * 100;
            
            // Atualizar display da pontuação
            document.getElementById('totalScore').textContent = averageScore.toFixed(1);
            document.getElementById('detailedScore').textContent = `${totalScore}/${answeredQuestions * 5} (${percentageScore.toFixed(1)}%)`;
            
            // Determinar categoria e cor
            let category = '';
            let color = '';
            
            if (averageScore >= 4.5) {
                category = 'EXCEPCIONAL';
                color = '#27ae60';
            } else if (averageScore >= 3.5) {
                category = 'ACIMA DO ESPERADO';
                color = '#3498db';
            } else if (averageScore >= 2.5) {
                category = 'ATENDE EXPECTATIVAS';
                color = '#f39c12';
            } else if (averageScore >= 1.5) {
                category = 'ABAIXO DO ESPERADO';
                color = '#e67e22';
            } else {
                category = 'INSATISFATÓRIO';
                color = '#e74c3c';
            }
            
            document.getElementById('scoreCategory').textContent = category;
            document.getElementById('totalScore').style.color = color;
            
            // Gerar plano de desenvolvimento
            generateDevelopmentPlan(radioGroups, averageScore);
        }
        
        function generateDevelopmentPlan(radioGroups, averageScore) {
            const developmentPlan = document.getElementById('developmentPlan');
            const developmentActions = document.getElementById('developmentActions');
            
            let lowScoreAreas = [];
            
            // Identificar áreas com pontuação baixa (≤ 2)
            radioGroups.forEach(group => {
                const selectedRadio = document.querySelector(`input[name="${group}"]:checked`);
                if (selectedRadio && parseInt(selectedRadio.value) <= 2) {
                    lowScoreAreas.push(group);
                }
            });
            
            let actionPlan = '';
            
            if (averageScore < 2.5) {
                actionPlan += '<div style="background: #ffebee; padding: 15px; border-radius: 5px; margin: 10px 0;"><strong>🚨 AÇÃO URGENTE NECESSÁRIA</strong><br>';
                actionPlan += 'O colaborador apresenta performance crítica que requer intervenção imediata.</div>';
            }
            
            // Ações específicas baseadas nas áreas problemáticas
            const developmentActions_map = {
                'nr_knowledge': '📚 Treinamento intensivo em Normas Regulamentadoras aplicáveis',
                'risk_analysis': '🔍 Capacitação em análise de riscos e metodologias HAZOP',
                'permit_work': '📋 Workshop prático de elaboração de PT e APR',
                'safety_equipment': '🛡️ Treinamento em equipamentos de segurança offshore',
                'proactivity': '💡 Coaching para desenvolvimento de proatividade',
                'compliance': '⚖️ Alinhamento sobre importância das demandas obrigatórias',
                'growth_interest': '🎯 Sessão de orientação de carreira e definição de metas',
                'communication': '🗣️ Treinamento em comunicação assertiva',
                'teamwork': '🤝 Dinâmicas de integração e trabalho em equipe',
                'external_relations': '🌐 Orientação sobre relacionamento com contratante',
                'conflict_management': '⚡ Capacitação em gestão de conflitos',
                'physical_resistance': '💪 Avaliação médica e orientação sobre condicionamento',
                'schedule_adaptation': '⏰ Acompanhamento próximo na adaptação aos horários',
                'confined_space': '🏗️ Orientação psicológica para ambientes confinados',
                'stress_management': '🧘 Técnicas de gestão de stress e bem-estar',
                'job_satisfaction': '😊 Conversa individual sobre expectativas e motivações',
                'company_identification': '🏢 Programa de integração e valores da empresa',
                'retention_perspective': '📈 Discussão sobre plano de carreira e crescimento',
                'commitment': '🎪 Alinhamento de metas e responsabilidades',
                'deadlines': '📅 Treinamento em gestão de tempo e prioridades',
                'documentation_quality': '📝 Mentoria em elaboração de documentos técnicos',
                'problem_solving': '🧩 Desenvolvimento de habilidades analíticas',
                'critical_decisions': '⚡ Simulações e estudos de caso críticos'
            };
            
            if (lowScoreAreas.length > 0) {
                actionPlan += '<h4>Ações de Desenvolvimento Prioritárias:</h4><ul>';
                lowScoreAreas.forEach(area => {
                    if (developmentActions_map[area]) {
                        actionPlan += `<li style="margin: 8px 0;">${developmentActions_map[area]}</li>`;
                    }
                });
                actionPlan += '</ul>';
            }
            
            // Recomendações gerais baseadas na pontuação
            if (averageScore < 2.0) {
                actionPlan += '<div style="background: #ffcdd2; padding: 15px; border-radius: 5px; margin: 15px 0;"><strong>Recomendação:</strong> Considerar remanejamento ou programa intensivo de capacitação antes da próxima avaliação.</div>';
            } else if (averageScore < 3.0) {
                actionPlan += '<div style="background: #fff3e0; padding: 15px; border-radius: 5px; margin: 15px 0;"><strong>Recomendação:</strong> Implementar plano de desenvolvimento estruturado com acompanhamento semanal.</div>';
            } else if (averageScore >= 4.0) {
                actionPlan += '<div style="background: #e8f5e8; padding: 15px; border-radius: 5px; margin: 15px 0;"><strong>Recomendação:</strong> Colaborador com bom potencial. Considerar para projetos especiais ou mentoria de novos membros.</div>';
            }
            
            developmentActions.innerHTML = actionPlan;
            developmentPlan.style.display = 'block';
        }
        
        function generateReport() {
            const employeeName = document.getElementById('employeeName').value;
            const evaluationDate = document.getElementById('evaluationDate').value;
            const evaluatorName = document.getElementById('evaluatorName').value;
            
            if (!employeeName || !evaluationDate || !evaluatorName) {
                alert('Por favor, preencha as informações básicas do colaborador.');
                return;
            }
            
            calculateScore();
            
            // Gerar relatório em nova janela
            const reportWindow = window.open('', '_blank');
            const reportContent = generateReportHTML();
            reportWindow.document.write(reportContent);
            reportWindow.document.close();
        }
        
        function generateReportHTML() {
            const employeeName = document.getElementById('employeeName').value;
            const evaluationDate = document.getElementById('evaluationDate').value;
            const evaluatorName = document.getElementById('evaluatorName').value;
            const totalScore = document.getElementById('totalScore').textContent;
            const scoreCategory = document.getElementById('scoreCategory').textContent;
            const generalComments = document.getElementById('generalComments').value;
            
            return `
                <!DOCTYPE html>
                <html>
                <head>
                    <title>Relatório de Avaliação - ${employeeName}</title>
                    <style>
                        body { font-family: Arial, sans-serif; margin: 40px; }
                        .header { text-align: center; border-bottom: 2px solid #3498db; padding-bottom: 20px; }
                        .info-table { width: 100%; margin: 20px 0; }
                        .info-table td { padding: 8px; border-bottom: 1px solid #eee; }
                        .score-highlight { background: #f0f8ff; padding: 20px; text-align: center; margin: 20px 0; border-radius: 8px; }
                        .comments { background: #f9f9f9; padding: 15px; margin: 20px 0; border-radius: 5px; }
                    </style>
                </head>
                <body>
                    <div class="header">
                        <h1>RELATÓRIO DE AVALIAÇÃO DE DESEMPENHO</h1>
                        <h2>Técnico de Segurança do Trabalho - Operações Offshore</h2>
                    </div>
                    
                    <table class="info-table">
                        <tr><td><strong>Colaborador:</strong></td><td>${employeeName}</td></tr>
                        <tr><td><strong>Data da Avaliação:</strong></td><td>${new Date(evaluationDate).toLocaleDateString('pt-BR')}</td></tr>
                        <tr><td><strong>Avaliador:</strong></td><td>${evaluatorName}</td></tr>
                    </table>
                    
                    <div class="score-highlight">
                        <h3>RESULTADO GERAL</h3>
                        <h2 style="color: #3498db;">Pontuação: ${totalScore}/5.0</h2>
                        <h3>${scoreCategory}</h3>
                    </div>
                    
                    <div class="comments">
                        <h3>Observações e Plano de Ação:</h3>
                        <p>${generalComments || 'Nenhuma observação adicional registrada.'}</p>
                    </div>
                    
                    <div style="margin-top: 40px; text-align: center; color: #666;">
                        <p>Relatório gerado em: ${new Date().toLocaleString('pt-BR')}</p>
                    </div>
                </body>
                </html>
            `;
        }
        
        function clearForm() {
            if (confirm('Tem certeza que deseja limpar todos os dados do formulário?')) {
                document.querySelectorAll('input[type="radio"]').forEach(radio => radio.checked = false);
                document.querySelectorAll('textarea').forEach(textarea => textarea.value = '');
                document.querySelectorAll('input[type="text"]').forEach(input => {
                    if (input.id !== 'evaluationDate') input.value = '';
                });
                document.querySelectorAll('select').forEach(select => select.value = '');
                
                document.getElementById('totalScore').textContent = '0.0';
                document.getElementById('scoreCategory').textContent = 'Aguardando avaliação';
                document.getElementById('detailedScore').textContent = '0/100';
                document.getElementById('developmentPlan').style.display = 'none';
            }
        }
        
        // Auto-calcular quando houver mudanças
        document.addEventListener('change', function(e) {
            if (e.target.type === 'radio') {
                setTimeout(calculateScore, 100);
            }
        });
    </script>
</body>
</html>
