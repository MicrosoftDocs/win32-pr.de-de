---
description: Wenn eine bestimmte Aktion ausgeführt wird, werden die Systemereignisse (mit dem Präfix ISG \_ ) nahezu sofort von der Anwendung gesendet und empfangen.
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: Zeitachse von Mausmeldungen und Systemereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635147b3f30b8746c75901de78336102ac8d1b41a685919c27f990496f5f225d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819604"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>Zeitachse von Mausmeldungen und Systemereignissen

Wenn eine bestimmte Aktion ausgeführt wird, werden die Systemereignisse (mit dem Präfix ISG \_ ) nahezu sofort von der Anwendung gesendet und empfangen. Die Mausnachrichten (mit dem Präfix WM \_ ) werden gesendet, wenn die Aktion ausgeführt wird, und werden von der Anwendung empfangen, nachdem die Verarbeitung des Ereignisses durch den Microsoft Windows Messagingdienst dauert. Darüber hinaus sind **CursorDown** und **CursorUp** Stiftereignisse, die von der Stifthardware empfangen werden. Sie werden gesendet, wenn der Tablettstift den Bildschirm berührt bzw. wenn er vom Bildschirm entfernt wird.

Stiftereignisse und Mausnachrichten werden nicht synchronisiert. Es gibt keine Garantie dafür, dass entsprechende Mausnachrichten und Stiftereignisse in einer bestimmten Reihenfolge auftreten. Das folgende Diagramm zeigt die erwartete, aber nicht immer vorhersagbare Abfolge der gesendeten System- und Mausereignisse. Beachten Sie im Diagramm, dass die Mausereignisse verzögert werden, wenn Systemgestenereignisse erkannt werden.

![Erwartete Sequenz von System- und Mausereignissen für Stifteingaben](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>Wichtige Überlegungen zur Implementierung

Berücksichtigen Sie bei der Entwicklung für Mausnachrichten und Systemereignisse Folgendes:

-   Stiftereignisse und Mausnachrichten werden unabhängig davon, ob der Stift oder die Maus verwendet wird, an eine Anwendung gesendet.
-   Wenn Ihre Anwendung sowohl auf Stift- als auch auf Mausnachrichten lauscht, ist es schwierig, die Beziehung der Nachrichten und damit das letztliche Verhalten vorherzusagen. Stiftereignisse und Mausnachrichten werden nicht synchronisiert. Es gibt keine Garantie dafür, dass entsprechende Mausmeldungen und Stiftereignisse (z. B. WM \_ LBUTTONDOWN und **ISG \_ TAP** oder WM \_ LBUTTONDBLCLK und **ISG \_ DBLTAP)** in einer bestimmten Reihenfolge auftreten. Die Beziehung zwischen diesen Nachrichten ist komplex.
-   Es wird davon abraten, Maus- und Stiftereignisse in derselben Anwendungsfunktion zu mischen und abzugleichen. Beispielsweise verhält sich ein Anwendungsfeature, das auf **CursorDown** und **MouseUp** reagiert, möglicherweise nicht wie erwartet oder mit zukünftigen Versionen des Tablet PC SDK.
-   Wenn der Benutzer den Tablettstift vor Abschluss der Sequenz zieht, entsprechen die gesendeten Ereignisse für die Hold-Through-Ereignissequenz dem linken Ziehpunkt. Wenn der Ziehpunkt beispielsweise gestartet wird, werden **ISG \_ DRAG** und WM \_ LBUTTONDOWN gesendet. Wenn der Stift schließlich per Lifting übertragen wird, werden **CursorUp** und WM \_ LBUTTONUP gesendet. Das Gestenereignis des Systems wird möglicherweise nicht sofort ausgelöst, da es bestimmen muss, welche Art von Ereignis auftritt.
-   Ein Doppeltippen mit einem Tablettstift ist häufig weniger genau als ein Doppelklick mit der Maus. Dies ergibt sich aus der inhärenten Natur der Ausführung eines doppelten Tippens mit einem Tablettstift. Da der Benutzer den Tablettstift zum Ausführen eines Doppeltippens per Lift liften muss, ist die Zeit zwischen Tippen häufig größer als die entsprechende Zeit zwischen Klicks eines Doppelklicks. Darüber hinaus ist es wahrscheinlich, dass die beiden Tippbewegungen des Tablettstifts an Bildschirmkoordinaten auftreten, die weiter voneinander entfernt sind als die für die beiden Mausklicks. Um dies zu berücksichtigen, verfügt Windows XP Tablet PC Edition über Einstellungen für den zeitlichen und räumlichen Abstand zwischen den beiden Tippen eines Doppeltipps, die von den Mauseinstellungen für einen Doppelklick getrennt sind. Diese Einstellungen können in Tablet und Stift Einstellungen in Systemsteuerung angepasst werden.

Aufgrund dieser Überlegungen sollten Anwendungen nur auf eine Gruppe von Nachrichten anstatt auf beide lauschen. Wenn Sie eine Stift-fähige Anwendung erstellen, lauschen Sie nur auf die System- und Stiftmeldungen. Diese Nachrichten sind vorhersagbar und funktionieren gut mit dem Tablettstift. Wenn Sie eine Anwendung erstellen, die nicht stiftfähig ist, lauschen Sie nur auf die Mausnachrichten.

 

 



