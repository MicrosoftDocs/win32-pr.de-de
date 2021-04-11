---
description: Die GDI-Druck-API stellt Anwendungen eine geräteunabhängige Druck Schnittstelle bereit.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: GDI-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215974"
---
# <a name="gdi-print-api"></a>GDI-Druck-API

Die GDI-Druck-API stellt Anwendungen eine geräteunabhängige Druck Schnittstelle bereit. Verwenden Sie diese Schnittstelle, wenn die Anwendung GDI zum Renderen von Text und Grafiken verwendet.

Wenn Sie Anwendungen für Windows Vista oder spätere Versionen von Windows schreiben, sollten Sie die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) und die [XPS-Druck-API](xps-printing.md) verwenden, um die leistungsstarken Grafik Schnittstellen zu verwenden, die von XPSDrv-Druckertreibern unterstützt werden.

Dieser Abschnitt enthält Informationen zu den folgenden Themen.



| Thema                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zur GDI-Druck-API](about-the-gdi-print-api.md)<br/>                                 | Eine Übersicht über die GDI-Druck Funktionalität.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Verwenden der GDI-Druck-API](using-the-printing-functions.md)<br/>                            | Informationen zur Verwendung der GDI-Druck-API in einer Anwendung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Referenz zur GDI-Druck-API](gdi-print-api-reference.md)<br/>                                 | Ausführliche Beschreibungen der Funktionen, Strukturen und anderen Elemente der GDI-Druck-API.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Converter (mxdc)](microsoft-xps-document-converter--mxdc-.md)<br/> | Der [Microsoft XPS Document Converter (mxdc)](microsoft-xps-document-converter--mxdc-.md) ist eine Komponente, die es Anwendungen ermöglicht, die GDI-Druck-API mit Druckern zu verwenden, die über einen XPSDrv-Druckertreiber verfügen.<br/>                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md)<br/>              | Der [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) bietet Anwendungen die Funktion "als XPS speichern" oder "in XPS exportieren". Anwendungen, die keinen nativ XPS-Dokumentinhalt erstellen, können MXDW zum Erstellen von XPS-Dokument Dateien verwenden, ohne die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))zu verwenden. Die XPS-Dokument-API bietet jedoch eine Anwendung mit der Möglichkeit, die von XPSDrv-Druckertreibern unterstützten Grafik Schnittstellen mit höherer Leistung zu verwenden.<br/> |



 

Das folgende Diagramm zeigt die Beziehung zwischen der GDI-Druck-API und den anderen Druck-APIs, die von einer Anwendung verwendet werden können.

![ein Diagramm, das die Beziehung zwischen der GDI-Druck-API und den anderen Druck-APIs anzeigt, die eine Win32-Anwendung verwenden kann](images/print-apis-gdi.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[XPS-Druck-API](xps-printing.md)
</dt> <dt>

[Druckspoolerapi](print-spooler-api.md)
</dt> <dt>

[Print Ticket-API](print-ticket-api.md)
</dt> </dl>

 

