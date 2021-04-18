---
description: Wenn eine bestimmte Aktion durchgeführt wird, werden die Systemereignisse (mit dem Präfix ISG \_ ) fast sofort von der Anwendung gesendet und empfangen.
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: Zeitachse von Maus Meldungen und System Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee3e6cb7882e1628fee0d2bc40f79ed1e29f55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358547"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>Zeitachse von Maus Meldungen und System Ereignissen

Wenn eine bestimmte Aktion durchgeführt wird, werden die Systemereignisse (mit dem Präfix ISG \_ ) fast sofort von der Anwendung gesendet und empfangen. Die Maus Meldungen (mit dem Präfix WM \_ ) werden gesendet, wenn die Aktion ausgeführt wird. Sie werden von der Anwendung nach dem Zeitpunkt empfangen, zu dem das Ereignis vom Microsoft Windows-Messaging Dienst verarbeitet werden muss. Außerdem handelt es sich bei " **Cursor** " und " **Cursor" um** Pen-Ereignisse, die von der Stift Hardware empfangen werden. Sie werden gesendet, wenn der Tablettstift den Bildschirm berührt, bzw. wenn er vom Bildschirm entfernt wird.

Pen-Ereignisse und Maus Meldungen werden nicht synchronisiert. Es gibt keine Garantie dafür, dass entsprechende Maus Meldungen und Stift Ereignisse in einer bestimmten Reihenfolge auftreten. Das folgende Diagramm zeigt die erwartete, aber nicht immer vorhersagbare Sequenz von System-und Mausereignissen, die gesendet werden. Beachten Sie im Diagramm, dass die Mausereignisse verzögert werden, wenn systemgesten Ereignisse erkannt werden.

![erwartete Sequenz von System-und Mausereignissen für Stift Eingaben](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>Wichtige Überlegungen zur Implementierung

Beachten Sie Folgendes, wenn Sie für Maus Meldungen und Systemereignisse entwickeln:

-   Beide Pen-Ereignisse und Maus Meldungen werden an eine Anwendung gesendet, unabhängig davon, ob der Stift oder die Maus verwendet wird.
-   Wenn Ihre Anwendung sowohl nach Pen-als auch Nachrichten überwacht, ist es schwierig, die Beziehung der Nachrichten und somit das letztendliche Verhalten vorherzusagen. Pen-Ereignisse und Maus Meldungen werden nicht synchronisiert. Es gibt keine Garantie dafür, dass entsprechende Maus Meldungen und Stift Ereignisse (z. b. WM \_ lbuttondown und **ISG \_ Tap** oder WM \_ lbuttondblclk und **ISG \_ dbltap**) in einer bestimmten Reihenfolge auftreten. Die Beziehung zwischen diesen Nachrichten ist komplex.
-   Es wird empfohlen, Maus-und Stift Ereignisse nicht in derselben Anwendungsfunktion zu kombinieren und abzugleichen. Ein Anwendungs Feature, das auf " **currsordown** " und " **MouseUp** " antwortet, verhält sich z. b. möglicherweise nicht erwartungsgemäß oder mit zukünftigen Versionen des Tablet PC SDK.
-   Wenn der Benutzer den Tablettstift zieht, bevor die Sequenz fertiggestellt wird, entsprechen die gesendeten Ereignisse dem Ziehpunkt, wenn der Benutzer den Tablettstift zieht, bevor die Sequenz fertiggestellt wird. Wenn der Zieh Vorgang z. b. gestartet wird, werden **ISG \_ Drag** und WM \_ lbuttondown gesendet. Wenn der Stift schließlich angehoben wird, werden " **Cursor** " und "WM \_ lbuttonup" gesendet. Das System Gesten Ereignis wird möglicherweise nicht sofort ausgelöst, da es bestimmen muss, welche Art von Ereignis auftritt.
-   Eine Doppel Abzweigung mit einem Tablettstift ist oft weniger genau als ein Doppelklick mit der Maus. Dies ergibt sich aus der inhärenten Natur der Durchführung einer Doppel Abzweigung mit einem Tablettstift. Da der Benutzer den Tablettstift zum Durchführen eines Doppel anhebers abhaken muss, ist die Zeit zwischen den Tap oft größer als die entsprechende Zeit zwischen den Klicks eines Doppelklicks. Außerdem ist es wahrscheinlich, dass die beiden Abzweigungen des Tablettstifts bei Bildschirm Koordinaten auftreten, die sich weiter voneinander unterscheiden als die beiden Mausklicks. Um dies zu ermöglichen, verfügt Windows XP Tablet PC Edition über Einstellungen für die zeitliche und räumliche Entfernung zwischen den zwei Abzweigungen einer Doppel Abzweigung, die von den Mauseinstellungen für einen Doppelklick getrennt sind. Diese Einstellungen können in den Einstellungen "Tablet" und "Pen" in der Systemsteuerung angepasst werden.

Aufgrund dieser Überlegungen sollten Anwendungen nur auf eine Reihe von Nachrichten lauschen und nicht auf beides. Wenn Sie eine Stift aktivierte Anwendung entwickeln, lauschen Sie nur auf die System-und Stift Nachrichten. Diese Nachrichten sind vorhersagbar und funktionieren gut für den Tablettstift. Wenn Sie eine Anwendung entwickeln, die nicht für Stift aktiviert ist, lauschen Sie nur auf die Maus Meldungen.

 

 



