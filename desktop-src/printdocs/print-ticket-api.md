---
description: Die-Druck Ticket-API ermöglicht es Anwendungen, Druck Tickets zu verwalten und zu konvertieren.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: Print Ticket-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050726"
---
# <a name="print-ticket-api"></a>Print Ticket-API

Die-Druck Ticket-API ermöglicht es Anwendungen, Druck Tickets zu verwalten und zu konvertieren.

Ein Druck Ticket ist eine XPS-Dokument Komponente, die die bevorzugten Druckereinstellungen für eine Seite in einem Dokument, ein gesamtes Dokument oder einen Druckauftrag enthält, der ein oder mehrere Dokumente enthält. Beachten Sie, dass Druck Tickets nur in XPS-Dokumenten gefunden werden.

Bevor der Drucker das Druck Ticket verwenden kann, muss das Druck Ticket anhand der Merkmale des Druckers überprüft werden, die in den Druckfunktionen des Druckers definiert sind. Die Anwendung führt diese Überprüfung durch Aufrufen der Druck Ticket-API durch.

Die Funktionen PrintTicket und printwerden mithilfe von Elementen des Druck Schemas beschrieben, das durch die [Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)definiert wird.

Dieses Thema enthält Informationen über die folgenden API-Elemente:

-   [Druckticket-API-Funktionen](print-ticket-api-functions.md)
-   [API-Enumerationen der Druck Ticket](print-ticket-api-enumerations.md)

Das folgende Diagramm zeigt die Beziehung zwischen der Druck Ticket-API und den anderen Druck-APIs, die von einer systemeigenen Windows-Anwendung verwendet werden können.

![ein Diagramm, das die Beziehung zwischen der Druck Ticket-API und den anderen Druck-APIs anzeigt, die eine systemeigene Windows-Anwendung verwenden kann](images/print-apis-pt.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XPS-Druck-API](xps-printing.md)
</dt> <dt>

[Druckspoolerapi](print-spooler-api.md)
</dt> <dt>

[GDI-Druck-API](gdi-printing.md)
</dt> <dt>

[Druck Schema Spezifikation](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XML Paper Specification](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



