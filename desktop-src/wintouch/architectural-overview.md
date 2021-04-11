---
title: Übersicht über die Architektur
description: Diese Architektur Übersicht stellt den Kontext für die Windows-Fingereingabe-API für Tablet-und Touchscreen-Technologien bereit und erläutert, wie Sie in die größere Windows 7-Architektur passt.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows-Touchscreen, Übersicht über die Architektur
- Windows-Fingereingabe, Manipulationen
- Windows-Fingereingabe, Meldungen
- Windows-Fingereingabe, Trägheit
- Windows-Toucheingabe, Gesten
- Gesten, Informationen
- Manipulationen, Informationen zu
- Trägheit, Info
- Manipulations Prozessor, Übersicht über die Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807113211d77f0aad0ed01fc24570d033063474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948757"
---
# <a name="architectural-overview"></a>Übersicht über die Architektur

Diese Architektur Übersicht stellt den Kontext für die Windows-Fingereingabe-API für Tablet-und Touchscreen-Technologien bereit und erläutert, wie Sie in die größere Windows 7-Architektur passt.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Nachrichten für Windows-toucheingaben und Gesten

Messaging Features für Windows-Finger Eingaben werden aktiviert, indem Nachrichten während der Ausführung überwacht und interpretiert werden. In der folgenden Abbildung wird gezeigt, wie Nachrichten von der Hardware generiert und von Windows 7 an Anwendungen gesendet werden.

![Abbildung, die zeigt, wie Windows 7 Nachrichten von multifingerhardware an eine Anwendung sendet](images/wm-multitouch-messaging.png)

In der Spalte ganz links in der Abbildung empfängt die berührungsempfindliche Hardware Eingaben von einem Benutzer. Ein Treiber kommuniziert dann zwischen der Hardware und dem Betriebssystem. Als nächstes generiert das Betriebssystem eine [**WM- \_ touchnachricht**](wm-touchdown.md) oder eine [**WM- \_ Gesten**](wm-gesture.md) Nachricht, die dann an das HWND einer Anwendung gesendet wird. Die Anwendung aktualisiert dann die Benutzeroberfläche anhand der Informationen, die in der Nachricht gekapselt sind.

Anwendungen erhalten standardmäßig Gesten. Wenn eine Anwendung nicht für Windows Touch-Eingabe Nachrichten mit der [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) -Funktion registriert wird, werden Benachrichtigungen für Gesten ([**WM- \_ Gesten**](wm-gesture.md) Meldungen) von Windows erstellt und an dieses Anwendungsfenster gesendet. Wenn ein Anwendungsfenster zum Empfangen von Berührungs Nachrichten registriert wird, werden Benachrichtigungen für Windows-Fingereingabe Eingaben (WM-Fingereingabe Meldungen) an dieses Anwendungsfenster gesendet.[**\_**](wm-touchdown.md) Windows-toucheingaben und Gesten Meldungen sind insofern gierig, als dass nach einer Toucheingabe oder einer Geste in einem Anwendungsfenster alle Nachrichten an diese Anwendung gesendet werden, bis die Geste abgeschlossen ist oder der primäre touchvorgang abgeschlossen ist.

Zur Unterstützung älterer Geräte interpretiert Windows die [**WM- \_ Gesten**](wm-gesture.md) Nachrichten, wenn diese zusammengefügt werden, und sendet oder sendet entsprechende Nachrichten, die der Geste zugeordnet sind. Um eine Unterbrechung der Legacy Unterstützung zu vermeiden, stellen Sie sicher, dass Sie WM- \_ Gesten Nachrichten mithilfe von [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)weiterleiten Weitere Informationen zum Legacy-Support finden Sie im Abschnitt [Übersicht über Windows-Touchgesten](windows-touch-gestures-overview.md).

## <a name="manipulations-and-inertia"></a>Manipulationen und Trägheit

Windows-touchprogrammierer müssen in der Lage sein, Gesten aus mehreren Quellen auf eine Weise zu interpretieren, die für die Bewegung von Bedeutung ist. Microsoft stellt die Bearbeitungs-API zum Durchführen dieser Berechnungen bereit. Manipulationen sind im wesentlichen Gesten mit Werten, die Ihnen zugeordnet sind und die gesamte Geste beschreiben. Nachdem Sie die Eingabedaten mit dem Manipulations Prozessor verbunden haben, können Sie Informationen zu Aktionen abrufen, die der Benutzer für das Objekt vornimmt. Die folgende Abbildung zeigt eine Möglichkeit, Manipulationen zu verwenden.

![Abbildung, die anzeigt, wie Windows-Finger Eingabenachrichten an den Manipulations Prozessor eines Objekts, der Ereignisse mit der \- imanipulationevents-Schnittstelle verarbeitet](images/manipulation-arch.png)

In der oberen linken Ecke der Abbildung hat der Benutzer den Bildschirm berührt, der touchnachrichten erstellt. Diese Nachrichten enthalten eine x-Koordinate und eine y-Koordinate, die verwendet werden, um das Objekt zu bestimmen, das den Fokus besitzt. Das Objekt, das den Fokus besitzt, enthält einen Bearbeitungs Prozessor. Anschließend wird in der [**WM- \_ Touch**](wm-touchdown.md) -Nachricht mit dem **toucheventf- \_ up** -Flag das Objekt im Fokus des Benutzers ausgewählt, auf den Manipulations Prozessor verwiesen, und die Nachricht wird an den Manipulations Prozessor gesendet. Nachfolgende **WM \_ Touch** -Nachrichten, die diesem Kontakt zugeordnet sind, werden an den Manipulations Prozessor gesendet, bis die **WM- \_ Touch** -Nachricht mit dem **toucheventf- \_ up** -Flag empfangen und das ausgewählte Objekt dereferenziert wird. Im unteren rechten Abschnitt der Abbildung wird eine Manipulations Ereignis Senke, die die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle implementiert, verwendet, um die Manipulations Ereignisse zu behandeln, die während der Erstellung der Fingereingabe Meldungen ausgelöst werden. Die Ereignis Senke kann Aktualisierungen an der-Schnittstelle basierend auf den Manipulations Ereignissen durchführen, während Sie auftreten.

In Windows-Finger eingabeanwendungen ist es üblich, einfache Physik zu integrieren, sodass Objekte reibungslos zu einem Ende kommen, anstatt abrupt anzuhalten, wenn Sie nicht mehr berührt werden. Microsoft stellt die Trägheit-API bereit, um die Berechnungen für diese einfache Physik auszuführen, sodass sich Ihre Anwendung ähnlich verhält wie andere Anwendungen. Dies spart Ihnen außerdem den Aufwand, der zum Erstellen robuster Physik-Funktionen erforderlich ist. In der folgenden Abbildung wird gezeigt, wie Sie Trägheit verwenden können.

![Darstellung der an die IInertiaProcessor-Schnittstelle eines Objekts weiter gegebenen Windows-Fingereingabe Meldungen, die Ereignisse mit der \- imanipulationevents-Schnittstelle auslöst](images/inertia-arch.png)

Beachten Sie die Ähnlichkeiten zwischen Trägheit und Bearbeitung. Der einzige Unterschied zwischen den beiden besteht darin, dass interpretiertes Nachrichten im Fall von Trägheit an einen Trägheits Prozessor und nicht an einen Manipulations Prozessor übergeben werden und dass der Trägheits Prozessor die Ereignisse auslöst. In der oberen linken Ecke der Abbildung wird in der [**WM \_ Touch**](wm-touchdown.md) -Nachricht mit dem **toucheventf- \_ up** -Flag Touch-Nachrichten verwendet, um ein Objekt zu identifizieren, das einen Trägheits Prozessor und einen Bearbeitungs Prozessor enthält. Nachfolg **Ende \_ WM** -Finger Eingaben werden an den Manipulations Prozessor gesendet, und der Manipulations Prozessor führt Aktualisierungen der Benutzeroberfläche der Anwendung aus. Nachdem die Bearbeitung abgeschlossen ist, werden Geschwindigkeitswerte aus der Bearbeitung verwendet, um einen Trägheits Prozessor einzurichten. Wie in der mittleren Spalte dargestellt, wird die [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) -oder [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) -Methode für die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle aufgerufen, indem ein Timer oder eine andere Schleife in einem separaten Thread verwendet wird, bis die Aufrufe angeben, dass die Verarbeitung des Prozessors abgeschlossen ist. Während diese Aufrufe durchgeführt werden, werden Manipulations Ereignisse ausgelöst, die von einer Manipulations Ereignis Senke auf der Grundlage der [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle behandelt werden. Im unteren rechten Abschnitt der Abbildung führt diese Ereignis Senke dann Aktualisierungen der Anwendungs Benutzeroberfläche basierend auf Manipulations Ereignissen aus, wenn Sie durch Ereignishandler in der Ereignis Senke auftreten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 