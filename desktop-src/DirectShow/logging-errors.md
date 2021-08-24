---
description: Protokollierungsfehler
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Protokollierungsfehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7402ade284f0d9a71b032f233276277dfdcd8c5e2844c85f03782caed101d095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685150"
---
# <a name="logging-errors"></a>Protokollierungsfehler

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

[DirectShow Editing Services](directshow-editing-services.md) (DES) bietet einen integrierten Mechanismus zum Protokollieren von Fehlern, die beim Laden, Erstellen oder Rendern eines DES-Projekts auftreten. Dieser Artikel enthält eine Beispielkonsolenanwendung, die eine XML-Projektdatei lädt und versucht, sie zu rendern. Wenn ein Fehler auftritt, gibt die Anwendung eine Fehlermeldung im Konsolenfenster aus. Der in diesem Artikel vorgestellte Beispielcode baut auf dem Beispiel unter Laden und Anzeigen einer Vorschau [einer](loading-and-previewing-a-project.md)Project.

> [!Note]  
> Ihre Anwendung ist nicht erforderlich, um die Fehlerprotokollierung zu implementieren. DES protokolliert keine Fehler, es sei denn, Sie fordern sie explizit an.

 

In diesem Artikel wird davon ausgegangen, dass Sie die COM-Clientprogrammierung und das DES-Zeitachsenmodell verstehen. Darüber hinaus müssen Sie die Grundlagen der COM-Objektprogrammierung verstehen. Informationen zu Zeitachsen in DES finden Sie unter [Das Zeitachsenmodell](the-timeline-model.md).

Dieser Artikel enthält folgende Abschnitte.

-   [Übersicht über die Fehlerprotokollierung](overview-of-error-logging.md)
-   [Erstellen einer Fehlerprotokollierungsklasse](creating-an-error-logging-class.md)
-   [Implementieren von IAMErrorLog](implementing-iamerrorlog.md)
-   [Festlegen des Fehlerprotokolls](setting-the-error-log.md)
-   [DES-Fehlerprotokollierung: Beispielcode](des-error-logging--example-code.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungsdiensten](using-directshow-editing-services.md)
</dt> </dl>

 

 



