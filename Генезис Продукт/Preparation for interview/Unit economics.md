Тримай повний концентрований чіт-шит (шпаргалку) з продуктової Unit-економіки. Тут зібрано формули, логіку розрахунків, типові пастки та готові шаблони для відповідей на інтерв'ю.

  

# Cheat Sheet: Unit Economics for Product Interviews

## 1. Фундаментальні метрики та формули

  ![[Pasted image 20260925133627.png]]
Search Assist

CPA in product refers to the cost per acquisition metric used to measure how much is spent to acquire a new user or customer for a product, calculated by dividing total campaign costs by the number of acquisitions.
![[Pasted image 20260925133104.png]]
### Залучення та конверсії

- **CAC (Customer Acquisition Cost):**
    
      
    
    $$\text{CAC} = \frac{\text{Total Acquisition Spend}}{\text{New Paying Customers}}$$
    
    - _Пастка:_ не плутай вартість інсталу/ліда (CPI/CPL) з CAC клієнта. Якщо $CPI = \$2$, а конверсія в оплату $CR = 4\%$, то:
        
          
        
        $$\text{CAC} = \frac{CPI}{CR} = \frac{2}{0.04} = \$50$$
        
- **Conversion Rate (CR):**
    
      
    
    $$CR_{A \to B} = \frac{\text{Users reaching step B}}{\text{Users reaching step A}} \times 100\%$$
    
- **ARPU vs ARPPU:**
    
      
    - **ARPU (Average Revenue Per User):** Виручка на _всіх_ зареєстрованих юзерів / інстали.
        
          
        
        $$ARPU = \frac{\text{Total Revenue}}{\text{Total Users}} = ARPPU \times CR_{\text{paying}}$$
        
    - **ARPPU (Average Revenue Per Paying User):** Виручка тільки з тих, хто реально заплатив.
        
          
        
        $$ARPPU = \frac{\text{Total Revenue}}{\text{Paying Users}}$$
        

### Дохідність, маржинальність та LTV

- **LTV (Lifetime Value) — спрощена базова формула:**
    
      
    
    $$LTV = ARPU \times \text{Lifetime} \quad \text{або} \quad LTV = \frac{ARPU}{\text{Churn Rate}}$$
    
    - Для платників: $LTV_{\text{paying}} = \frac{ARPPU}{\text{Customer Churn}}$.
        
            
Search Assist

Customer churn refers to the rate at which customers stop doing business with a company over a specific period
        
- **Net LTV (Реальний чистий LTV — те, що вимагають на інтерв'ю):**
    
    Виручка «брутто» не належить компанії повністю. Потрібно вираховувати змінні витрати:
    
      
    
    $$\text{Net Revenue} = \text{Gross Revenue} - \text{Store Fee (15-30\%)} - \text{Refunds/Chargebacks} - \text{COGS per user}$$
    
    $$\text{Net LTV} = \text{Net Revenue per Period} \times \text{Lifetime}$$
    
- **Churn Rate (Відтік):**
    
      
    
    $$\text{Churn Rate} = \frac{\text{Lost Customers during period}}{\text{Total Customers at start of period}}$$
    
    $$\text{Lifetime} = \frac{1}{\text{Churn Rate}}$$
    
    _(Наприклад: якщо щомісяця йде 10% клієнтів, середній Lifetime = $1 / 0.10 = 10\text{ місяців}$)._
    
      
    

### Збіжність економіки (Unit Viability)

- **LTV / CAC Ratio:**
    
      
    - $< 1.0\times$ — бізнес спалює гроші на кожному клієнті.
        
          
        
    - $1.0\times - 2.5\times$ — ризиковано, не покриває фіксовані витрати (зарплати, оренду, R&D).
        
          
        
    - **$3.0\times+$** — **золотий стандарт** венчурних та продуктових бізнесів.
        
          
        
    - $> 5.0\times$ — неефективний маркетинг, компанія недоінвестовує в ріст і втрачає частку ринку.
        
    
        
- **Payback Period (Період окупності CAC):**
    
    Час (у місяцях або днях), за який маржинальний прибуток від клієнта повертає витрачений на нього CAC.
    
      
    
    $$\text{Payback Period} = \frac{\text{CAC}}{\text{Net Margin per User per Month}}$$
    
    - Для B2C підписок здоровий показник: **1–3 місяці** (ідеально — Day 0 / Day 30).
        
          Маржа, или маржинальный доход — это разница между суммарными объемами продаж компании (выручкой) и переменными затратами (расходами).  
        
    - Для B2B SaaS: **6–12 місяців**.
        
          
        
- **ROAS / ROMI (Return on Ad Spend / Marketing Investment):**
    
      
    
    $$ROAS = \frac{\text{Revenue from Ads}}{\text{Ad Spend}} \times 100\%$$
    
    $$ROMI = \frac{\text{Gross Profit from Ads} - \text{Ad Spend}}{\text{Ad Spend}} \times 100\%$$
    
    _(Якщо $ROAS = 150\%$, ти заробив $\$1.50$ виручки на кожен $\$1.00$ спенду)._
    
      
    

## 2. Специфіка за бізнес-моделями

|**Модель**|**Головний юніт**|**Ключові змінні витрати (COGS / Deductions)**|**Формула доходу юніта**|
|---|---|---|---|
|**B2C Subscriptions (Apps)**|Платний підписник|Store Commission (15–30%), рефанди, чарджбеки ($15 fee), еквайринг|$\text{Price} \times (1 - \text{Fee}) \times (1 - \text{Refund\%}) \times \text{Renewals}$|
|**Marketplace (двосторонній)**|Транзакція (Замовлення)|Еквайринг (2–3%), виплати саппорту, страхування, B2B онбординг постачальника|$\text{GMV} \times \text{Take Rate\%} - \text{Ops Cost}$|
|**E-commerce**|Замовлення|Собівартість товару, логістика, упакування, повернення|$(\text{AOV} - \text{COGS}) \times \text{Margin\%}$|
|**B2B SaaS**|Акаунт (Логотип)|Сервери на клієнта, Customer Success, інтеграції|$\text{MRR} \times \text{Gross Margin\%} / \text{Logo Churn}$|

## 3. Топ-6 підступних питань на інтерв'ю та як відповідати

### 1. «Як порахувати необхідний спенд на A/B тест?»

> **Відповідь:**
> 
>   
> 
> 1. Визначаємо базову конверсію ($CR_0$) та бажаний ефект ($MDE$, наприклад $+10\%$).
>     
>       
>     
> 2. За формулою вибірки (при $\alpha=5\%, \beta=20\%$) отримуємо потрібний **Sample Size на групу** ($N$).
>     
>       
>     
> 3. Загальна кількість юзерів для тесту $N_{\text{total}} = 2 \times N$.
>     
>       
>     
> 4. Рахуємо конверсію від платного кліку/інсталу до кроку тесту: $\text{Required Traffic} = N_{\text{total}} / CR_{\text{funnel}}$.
>     
>       
>     
> 5. Множимо на вартість залучення: $\text{Budget} = \text{Required Traffic} \times \text{CPC (або CPI)}$.
>     
>       
>     

### 2. «Що краще: підняти ціну на 20% чи конверсію на 20%?»

> **Відповідь:**
> 
>   
> 
> **Підняти ціну на 20% майже завжди вигідніше**, тому що зростання ціни на $100\%$ падає в чистий маржинальний прибуток (COGS не росте). Зростання конверсії масштабує виручку, але пропорційно масштабує і всі змінні витрати (саппорт, сервери, комісії).
> 
>   

### 3. «Чому формулу $LTV = ARPU / Churn$ небезпечно використовувати для молодих продуктів?»

> **Відповідь:**
> 
>   
> 
> 1. Вона передбачає постійний (лінійний) Churn, тоді як у реальності відтік має гіперболічну форму (когортний спад): найбільший відтік у 1–2 місяці, а далі крива виходить на плато.
>     
>       
>     
> 2. Якщо когорта ще не прожила достатньо циклів, реальний відтік невідомий, і екстраполяція дає завищений у кілька разів LTV.
>     
>       
>     

### 4. «LTV рахувати на когорту інсталів чи на когорту платників?»

> **Відповідь:**
> 
>   
> 
> Можна і так, і так, головне узгодити CAC:
> 
>   
> 
> - Якщо рахуємо **LTV на платника** $\implies$ ділимо маркетинг на кількість _платників_ ($\text{CAC}_{\text{buyer}}$).
>     
>       
>     
> - Якщо рахуємо **Cumulative ARPU на інстал** $\implies$ порівнюємо з вартістю _інсталу_ ($CPI$).
>     
>       
>     
>     _Помилка — брати дохід з платника і порівнювати його з CPI._
>     
>       
>     

### 5. «Як враховувати чарджбеки (Chargebacks) у підписках?»

> **Відповідь:**
> 
>   
> 
> Чарджбек — це не просто повернення грошей ($-\text{Price}$). Це подвійний збиток:
> 
>   
> 
> 1. Втрата повної суми покупки (мінус виручка).
>     
>       
>     
> 2. Фіксований штраф від банку/Stripe (зазвичай **$15 за інцидент**).
>     
>       
>     
> 3. Якщо Chargeback Rate перевищує **1%**, платіжні системи ставлять аккаунт на штрафний моніторинг або блокують еквайринг.
>     
>       
>     

### 6. «Що таке Blended CAC vs Paid CAC?»

> **Відповідь:**
> 
>   
> 
> - **Paid CAC:** $\frac{\text{Ad Spend}}{\text{Paid Users from Ads}}$ (чесна ціна платної реклами).
>     
>       
>     
> - **Blended CAC:** $\frac{\text{Ad Spend}}{\text{All Users (Paid + Organic)}}$.
>     
>       
>     
>     _Пастка:_ не можна масштабувати маркетинг, орієнтуючись на Blended CAC, тому що органічний хвіст не масштабується лінійно зі спендом.
>     
>       
>     

## 4. Швидкий чек-лист розрахунку «на серветці»

Перед тим як озвучити фінальну цифру на співбесіді, перевір:

  

- [ ] Чи відняв комісію Apple/Google ($15\%$ або $30\%$)?
    
      
    
- [ ] Чи врахував рефанди ($3\text{--}7\%$ за замовчуванням)?
    
      
    
- [ ] Чи порівнюєш однаковий знаменник (інстал з інсталом, платника з платником)?
    
      
    
- [ ] Чи не переплутав відсотки: $+20\%$ від $5\%$ — це $6\%$ (відносний ріст), а не $25\%$ (абсолютний).

Download amplitude