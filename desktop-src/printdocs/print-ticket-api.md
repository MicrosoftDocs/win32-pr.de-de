---
description: Mit der Druckticket-API können Anwendungen Drucktickets verwalten und konvertieren.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: Druckticket-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac91cc976addba630bae3f250d244442ba1dd3b61f741575fe21cb250bab4a2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947794"
---
# <a name="print-ticket-api"></a>Druckticket-API

Mit der Druckticket-API können Anwendungen Drucktickets verwalten und konvertieren.

Ein Druckticket ist eine XPS-Dokumentkomponente, die die bevorzugten Druckereinstellungen für eine Seite in einem Dokument, für ein gesamtes Dokument oder für einen Druckauftrag enthält, der ein oder mehrere Dokumente enthält. Beachten Sie, dass Drucktickets nur in XPS-Dokumenten gefunden werden.

Bevor der Drucker das Druckticket verwenden kann, muss das Druckticket anhand der Eigenschaften des Druckers überprüft werden, die in den Druckfunktionen des Druckers definiert sind. Die Anwendung führt diese Überprüfung durch Aufrufen der Druckticket-API aus.

PrintTicket und PrintCapabilities werden mithilfe von Elementen des Druckschemas beschrieben, das durch die [Druckschemaspezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)definiert wird.

Dieses Thema enthält Informationen zu den folgenden API-Elementen:

-   [Druckticket-API-Funktionen](print-ticket-api-functions.md)
-   [Druckticket-API-Enumerationen](print-ticket-api-enumerations.md)

Das folgende Diagramm zeigt die Beziehung zwischen der Druckticket-API und den anderen Druck-APIs, die von einer nativen Windows Anwendung verwendet werden können.

![Diagramm, das die Beziehung zwischen der Druckticket-API und den anderen Druck-APIs zeigt, die von einer nativen Windows-Anwendung verwendet werden können](images/print-apis-pt.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XPS-Druck-API](xps-printing.md)
</dt> <dt>

[Druckspooler-API](print-spooler-api.md)
</dt> <dt>

[GDI-Druck-API](gdi-printing.md)
</dt> <dt>

[Spezifikation des Druckschemas](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XML Paper Specification](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



