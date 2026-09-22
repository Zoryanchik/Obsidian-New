**CustDev-інтерв'ю (Customer Development Interview)** — це глибинне якісне інтерв'ю з потенційними або поточними користувачами, мета якого — перевірити гіпотези щодо проблем, потреб, контексту та реальної поведінки людей перед тим, як писати код чи запускати фічу.

This project addresses fragmented information across multiple transport operators (Archway Travel, Stagecoach, Blackpool Transport, etc.) by building a scalable, resilient multi-platform application that integrates:

- **Live Bus Data:** REST API feeds with route information and GPS tracking
- **Rail Data:** Network Rail TRUST and TD messages via STOMP protocol
- **Static Infrastructure:** NaPTAN/NPTG database and BPLAN rail planning data
- **Advanced Features:** Multi-leg route planning, historical delay prediction, and real-time tracking