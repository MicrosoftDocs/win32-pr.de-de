---
description: Protokollierungs Fehler
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Protokollierungs Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745969"
---
# <a name="logging-errors"></a>Protokollierungs Fehler

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

[DirectShow-Bearbeitungs Dienste (DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) ) bieten einen integrierten Mechanismus zum Protokollieren von Fehlern, die beim Laden, erstellen oder Rendern eines des-Projekts auftreten. Dieser Artikel enthält eine Beispiel Konsolenanwendung, die eine XML-Projektdatei lädt und versucht, Sie zu Rendering. Wenn ein Fehler auftritt, gibt die Anwendung im Konsolenfenster eine Fehlermeldung aus. Der Beispielcode in diesem Artikel baut auf dem Beispiel auf, das beim [Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md)angegeben ist.

> [!Note]  
> Es ist nicht erforderlich, dass Ihre Anwendung die Fehler Protokollierung implementiert. DES protokolliert keine Fehler, es sei denn, Sie fordern Sie explizit an.

 

In diesem Artikel wird davon ausgegangen, dass Sie die com-Client Programmierung und das des-Zeitachsen Modells verstehen Außerdem müssen Sie die Grundlagen der COM-Objekt Programmierung verstehen. Informationen zu Zeitachsen in des finden Sie [unter Zeitachsen Modell](the-timeline-model.md).

Dieser Artikel enthält folgende Abschnitte.

-   [Übersicht über die Fehler Protokollierung](overview-of-error-logging.md)
-   [Erstellen einer Fehler Protokollierungs Klasse](creating-an-error-logging-class.md)
-   [Implementieren von iamerrorlog](implementing-iamerrorlog.md)
-   [Festlegen des Fehler Protokolls](setting-the-error-log.md)
-   [DES-Fehler Protokollierung: Beispiel Code](des-error-logging--example-code.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungs Diensten](using-directshow-editing-services.md)
</dt> </dl>

 

 



