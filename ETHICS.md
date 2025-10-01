# 🛡️ ETHICS.md
Este documento descreve os princípios éticos, limitações e boas práticas associadas ao uso do **Community Policy Classifier**, um projeto educacional de NLP para classificação de frases **Adequadas vs. Potencialmente Violadoras de Políticas de Comunidade**.

---

## 📌 Finalidade do Projeto
- Projeto criado **exclusivamente para fins acadêmicos e de portfólio**.  
- Não deve ser usado em **produção** ou em ambientes reais de moderação sem supervisão humana.  
- O dataset utilizado é **fictício e seguro**, evitando exposição de exemplos reais de discurso de ódio.

---

## ⚠️ Riscos Identificados
1. **Falsos positivos**  
   - Frases adequadas podem ser incorretamente classificadas como violadoras.  
   - Risco: censura indevida, impacto na liberdade de expressão.

2. **Falsos negativos**  
   - Frases ofensivas podem não ser detectadas.  
   - Risco: exposição de usuários a conteúdo prejudicial.

3. **Viés algorítmico**  
   - Modelos de linguagem podem reproduzir ou amplificar vieses presentes no dataset.  
   - Risco: discriminação injusta contra grupos específicos.

4. **Generalização limitada**  
   - O dataset é pequeno e sintético, não reflete toda a diversidade linguística real.  
   - Risco: má performance em contextos reais.

---

## ✅ Medidas de Mitigação
- **Uso restrito**: deixar claro no README e no próprio repositório que o modelo é didático.  
- **Explicabilidade**: aplicação de **LIME e SHAP** para entender as decisões do modelo.  
- **Dataset fictício**: não contém frases reais sensíveis, reduzindo risco de vazamento ou exposição indevida.  
- **Supervisão humana**: reforçar que modelos desse tipo devem ser usados apenas como suporte, nunca como decisão final.

---

## 🔎 Boas Práticas Recomendadas
- **Treinamento com dados reais** → apenas em contextos controlados, anonimizados e com consentimento.  
- **Validação por especialistas** → linguistas, juristas e equipes de Trust & Safety devem revisar modelos de moderação em produção.  
- **Atualização contínua** → linguagem ofensiva muda ao longo do tempo, exigindo re-treinamento frequente.  
- **Monitoramento de métricas éticas** → como *false positive rate* e *false negative rate* em diferentes grupos de usuários.

---

## 🚫 Limitações do Projeto
- Não é uma ferramenta oficial de moderação.  
- Não substitui revisão humana.  
- Não cobre múltiplos idiomas ou contextos culturais.  
- Resultados apresentados servem apenas para **fins ilustrativos e educacionais**.

---

## 📖 Referências
- Davidson et al. (2017) – *Automated Hate Speech Detection and the Problem of Offensive Language*  
- Jigsaw (Google) – *Toxic Comment Classification Challenge*  
- IEEE Ethically Aligned Design Guidelines  

---

✍️ **Autor:** Josiele Ferreira  
🔗 [LinkedIn](https://www.linkedin.com/in/josieleferreira/)  
