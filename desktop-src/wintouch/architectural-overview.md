---
title: Übersicht über die Architektur
description: Diese Architekturübersicht bietet Kontext für die Windows Touch-API für Tablet- und Touchtechnologien und erläutert, wie sie in die größere Windows 7-Architektur passt.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Touch,Architekturübersicht
- Windows Touch,Manipulationen
- Windows Touch,Nachrichten
- Windows Touch,Trägheit
- Windows Touch,Gesten
- Gesten,About
- Manipulationen,About
- Trägheit, Informationen
- Manipulationsprozessor,Architekturübersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b5ce003c88a66e96072fa9f96bc6ae73bd91cb39f53e03ab3748dd14a194d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448655"
---
# <a name="architectural-overview"></a>Übersicht über die Architektur

Diese Architekturübersicht bietet Kontext für die Windows Touch-API für Tablet- und Touchtechnologien und erläutert, wie sie in die größere Windows 7-Architektur passt.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Nachrichten für Windows Toucheingabe und Gesten

Messagingfunktionen für Windows Touch werden durch Lauschen und Interpretieren von Nachrichten während der Ausführung aktiviert. Die folgende Abbildung zeigt, wie Nachrichten von Hardware generiert und von Windows 7 an Anwendungen gesendet werden.

![Abbildung, die zeigt, wie Windows 7 Nachrichten von Multitouchhardware an eine Anwendung sendet](images/wm-multitouch-messaging.png)

In der spalte ganz links in der Abbildung empfängt die berührungsempfindliche Hardware Eingaben von einem Benutzer. Ein Treiber kommuniziert dann zwischen der Hardware und dem Betriebssystem. Als Nächstes generiert das Betriebssystem eine [**WM \_ TOUCH-**](wm-touchdown.md) oder [**WM \_ GESTURE-Nachricht,**](wm-gesture.md) die dann an das HWND einer Anwendung gesendet wird. Die Anwendung aktualisiert dann die Benutzeroberfläche, wenn die informationen in der Nachricht gekapselt sind.

Anwendungen empfangen standardmäßig Gesten. Sofern sich eine Anwendung nicht für Windows Touch-Eingabemeldungen mit der [**RegisterTouchWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) registriert, werden Benachrichtigungen für Gesten [**(WM \_ GESTURE-Meldungen)**](wm-gesture.md) von Windows erstellt und an dieses Anwendungsfenster gesendet. Wenn sich ein Anwendungsfenster für den Empfang von Touchnachrichten registriert, werden Benachrichtigungen für Windows Toucheingabe [**(WM \_ TOUCH-Nachrichten)**](wm-touchdown.md) an dieses Anwendungsfenster gesendet. Windows Touch- und Gestennachrichten sind gierig in dem Sinne, dass nach dem Starten einer Fingerbewegung oder einer Geste in einem Anwendungsfenster alle Nachrichten an diese Anwendung gesendet werden, bis die Geste abgeschlossen ist oder die primäre Fingerbewegung abgeschlossen ist.

Für legacy-Unterstützung interpretiert Windows [**WM \_ GESTURE-Nachrichten,**](wm-gesture.md) wenn sie hochgeblasen werden, und sendet dann entsprechende SEND- oder POST-Nachrichten, die der Geste zuordnen. Stellen Sie sicher, dass Sie WM GESTURE-Nachrichten mit DefWindowProc weiterverenden, um zu vermeiden, dass die \_ [Legacyunterstützung nicht unterbricht.](/windows/win32/api/winuser/nf-winuser-defwindowproca) Weitere Informationen zur Legacyunterstützung finden Sie im Abschnitt Windows Übersicht über [Touchgesten.](windows-touch-gestures-overview.md)

## <a name="manipulations-and-inertia"></a>Manipulationen und Trägheit

Windows Touch-Programmierer müssen Gesten aus mehreren Quellen in einer Weise interpretieren können, die für die durchgeführte Geste sinnvoll ist. Microsoft stellt die Bearbeitungs-API bereit, um diese Berechnungen durchzuführen. Manipulationen sind im Wesentlichen Gesten mit zugeordneten Werten, die die gesamte Geste beschreiben. Nachdem Sie die Eingabedaten mit dem Bearbeitungsprozessor verbinden, können Sie Informationen abrufen, die für aktionen relevant sind, die der Benutzer für das Objekt vorsteuert. Die folgende Abbildung zeigt eine Möglichkeit, Manipulationen zu verwenden.

![Abbildung: Fenster berühren Nachrichten, die an den Bearbeitungsprozessor eines Objekts übergeben werden, der Ereignisse mit der \- Imanipulationevents-Schnittstelle behandelt](images/manipulation-arch.png)

Oben links in der Abbildung hat der Benutzer den Bildschirm berührt, wodurch Touchnachrichten erstellt werden. Diese Nachrichten enthalten eine x-Koordinate und eine y-Koordinate, die verwendet werden, um das Objekt zu bestimmen, das sich im Fokus befindet. Das Objekt im Fokus enthält einen Bearbeitungsprozessor. Als Nächstes wird in der [**WM \_ TOUCH-Nachricht**](wm-touchdown.md) mit dem **TOUCHEVENTF \_ UP-Flag** das Objekt im Fokus des Benutzers ausgewählt, auf den Bearbeitungsprozessor verwiesen, und die Nachricht wird an den Bearbeitungsprozessor gesendet. Nachfolgende **WM \_ TOUCH-Nachrichten,** die diesem Kontakt zugeordnet sind, werden an den Manipulationsprozessor gesendet, bis die **WM \_ TOUCH-Nachricht** mit dem **TOUCHEVENTF \_ UP-Flag** empfangen und das ausgewählte Objekt dereferenziert wird. Im unteren rechten Abschnitt der Abbildung wird eine Manipulationsereignissenke verwendet, die die [**\_ IManipulationEvents-Schnittstelle**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) implementiert, um die Manipulationsereignisse zu behandeln, die ausgelöst werden, während die Touchnachrichten erstellt werden. Die Ereignissenke kann Aktualisierungen der Schnittstelle basierend auf den Manipulationsereignissen ausführen, während sie auftreten.

In Windows Touch-Anwendungen ist es üblich, einfache Physik zu integrieren, damit Objekte reibungslos beendet werden, anstatt plötzlich anzuhalten, wenn sie nicht mehr berührt werden. Microsoft stellt die Trägheits-API bereit, um die Berechnungen für diese einfache Physik durchzuführen, damit sich Ihre Anwendung ähnlich wie andere Anwendungen verhalten kann. Dies spart Ihnen auch den Aufwand, der zum Erstellen robuster physikalischer Funktionen erforderlich ist. Die folgende Abbildung zeigt, wie Sie Trägheit verwenden können.

![Abbildung: Fenster touch nachrichten, die an die iinertiaprocessor-Schnittstelle eines Objekts übergeben werden, wodurch Ereignisse mit \- imanipulationevents-Schnittstelle ausgelöst werden](images/inertia-arch.png)

Beachten Sie die Ähnlichkeiten zwischen Trägheit und Manipulation. Der einzige Unterschied zwischen den beiden besteht in der Übergabe interpretierter Nachrichten bei Trägheit an einen Trägheitsprozessor statt an einen Manipulationsprozessor, und der Trägheitsprozessor löst die Ereignisse aus. Links oben in der Abbildung werden in der [**WM \_ TOUCH-Nachricht**](wm-touchdown.md) mit dem **TOUCHEVENTF \_ UP-Flag** Touchnachrichten verwendet, um ein Objekt im Fokus zu identifizieren, das einen Trägheitsprozessor und einen Manipulationsprozessor enthält. Nachfolgende **WM \_ TOUCH-Nachrichten** werden an den Manipulationsprozessor gesendet, und der Bearbeitungsprozessor führt Aktualisierungen der Anwendungsbenutzeroberfläche durch. Nach Abschluss der Bearbeitung werden Geschwindigkeitswerte aus der Manipulation verwendet, um einen Trägheitsprozessor zu einrichten. Wie in der mittleren Spalte dargestellt, wird die [**Process-**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) oder [**ProcessTime-Methode**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) auf der [**IInertiaProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) mithilfe eines Timers oder einer anderen Schleife in einem separaten Thread aufgerufen, bis die Aufrufe angeben, dass die Verarbeitung des Prozessors abgeschlossen ist. Während diese Aufrufe vorgenommen werden, werden Manipulationsereignisse ausgelöst, die von einer Manipulationsereignissenke verarbeitet werden, die auf der [**\_ IManipulationEvents-Schnittstelle**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) basiert. Im unteren rechten Abschnitt der Abbildung führt diese Ereignissenke dann Aktualisierungen der Anwendungsbenutzeroberfläche basierend auf Manipulationsereignissen aus, wenn sie über Ereignishandler in der Ereignissenke auftreten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 