---
description: Stellt eine Schnittstelle zum Druck Spooler bereit. Anwendungen können diese API verwenden, um XPS-Dokumente an einen Drucker zu senden.
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: XPS-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359996"
---
# <a name="xps-print-api"></a>XPS-Druck-API

\[Die XPS-Druck-API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Client Anwendungen sollten stattdessen die [API zum Drucken von Dokument Paketen](./tailored-app-printing-api.md) verwenden.\]

Stellt eine Schnittstelle zum Druck Spooler bereit. Anwendungen können diese API verwenden, um XPS-Dokumente an einen Drucker zu senden.

Dieser Abschnitt enthält Informationen zu den folgenden Themen.

<dl>

[Informationen zur XPS-Druck-API](about-xps-print-api.md)  
[Verwenden der XPS-Druck-API](using-the-xps-print-api.md)  
[XPS-Druck-API-Referenz](xpsprint-interfaces.md)  
</dl>

Native Windows-Anwendungen, die XPS-Dokumente erstellen, z. b. mithilfe der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)), können die XPS-Druck-API verwenden, um XPS-Dokumentinhalte an einen Drucker zu senden.

Das folgende Diagramm zeigt die Beziehung der XPS-Druck-API zu den anderen Druck-APIs, die von einer systemeigenen Windows-Anwendung verwendet werden können.

![ein Diagramm, das die Beziehung zwischen der XPS-Druck-API und den anderen Druck-APIs anzeigt, die eine systemeigene Windows-Anwendung verwenden kann](images/print-apis-xps.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[Druckspoolerapi](print-spooler-api.md)
</dt> <dt>

[Print Ticket-API](print-ticket-api.md)
</dt> <dt>

[GDI-Druck-API](gdi-printing.md)
</dt> </dl>

 

 
