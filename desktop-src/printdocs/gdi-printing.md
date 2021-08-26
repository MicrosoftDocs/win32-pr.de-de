---
description: Die GDI-Druck-API stellt Anwendungen eine geräteunabhängige Druckschnittstelle bereit.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: GDI-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc2a872b3a310ea44ddfc84103ddbd11cff61998d4884dca5f490e88c3d73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949195"
---
# <a name="gdi-print-api"></a>GDI-Druck-API

Die GDI-Druck-API stellt Anwendungen eine geräteunabhängige Druckschnittstelle bereit. Verwenden Sie diese Schnittstelle, wenn die Anwendung GDI zum Rendern von Text und Grafiken verwendet.

Wenn Sie Anwendungen für Windows Vista oder höhere Versionen von Windows schreiben, sollten Sie die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) und die [XPS-Druck-API](xps-printing.md) verwenden, um die grafikschnittstellen mit höherer Leistung zu verwenden, die von XPSDrv-Druckertreibern unterstützt werden.

Dieser Abschnitt enthält Informationen zu den folgenden Themen.



| Thema                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zur GDI-Druck-API](about-the-gdi-print-api.md)<br/>                                 | Eine Übersicht über die GDI-Druckfunktionen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Verwenden der GDI-Druck-API](using-the-printing-functions.md)<br/>                            | Informationen zur Verwendung der GDI-Druck-API in einer Anwendung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [GDI-Druck-API-Referenz](gdi-print-api-reference.md)<br/>                                 | Ausführliche Beschreibungen der Funktionen, Strukturen und anderen Elemente der GDI-Druck-API.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md)<br/> | Der [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) ist eine Komponente, mit der Anwendungen die GDI-Druck-API mit Druckern verwenden können, die über einen XPSDrv-Druckertreiber verfügen.<br/>                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md)<br/>              | Der [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) stellt Anwendungen die Funktionen "Als XPS speichern" oder "Nach XPS exportieren" zur Verfügung. Anwendungen, die xps-Dokumentinhalte nicht nativ erstellen, können den MXDW verwenden, um XPS-Dokumentdateien zu erstellen, ohne die [XPS-Dokument-API zu verwenden.](/previous-versions/windows/desktop/dd316976(v=vs.85)) Die XPS-Dokument-API bietet einer Anwendung jedoch die Möglichkeit, die grafikschnittstellen mit höherer Leistung zu verwenden, die von XPSDrv-Druckertreibern unterstützt werden.<br/> |



 

Das folgende Diagramm zeigt die Beziehung zwischen der GDI-Druck-API und den anderen Druck-APIs, die eine Anwendung verwenden kann.

![Diagramm, das die Beziehung zwischen der gdi-Druck-API und den anderen Druck-APIs zeigt, die eine win32-Anwendung verwenden kann](images/print-apis-gdi.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[XPS-Druck-API](xps-printing.md)
</dt> <dt>

[Druckspooler-API](print-spooler-api.md)
</dt> <dt>

[Druckticket-API](print-ticket-api.md)
</dt> </dl>

 

