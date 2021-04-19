---
description: Die Anwendung bietet optimalen Entwurf und Verwendung des Tablettstifts, indem sowohl Microsoft Windows-Maus Nachrichten als auch Systemereignisse gesendet werden.
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: System Ereignisse und Maus Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45c068e30db6ca1a85429667e2a8f1f93c505299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359586"
---
# <a name="system-events-and-mouse-messages"></a>System Ereignisse und Maus Meldungen

Die Anwendung bietet optimalen Entwurf und Verwendung des Tablettstifts, indem sowohl Microsoft Windows-Maus Nachrichten als auch Systemereignisse gesendet werden. Anwendungen empfangen beide Sätze von Ereignissen für jede Stift Bewegung oder Aktion. Die Anwendung wählt dann das geeignete Ereignis aus, das basierend auf dem Kontext der Aktion verwendet werden soll. Windows-Maus Meldungen funktionieren gut für das zeigen und Auswählen von Aktivitäten, und Sie sollten Sie für Aktivitäten verwenden, die eine Interaktion mit Benutzeroberflächen Elementen beinhalten. Pen-Ereignisse funktionieren gut für echt Zeit Freihand-Anwendungen, Stift Aktionen und Handschrift.

> [!Note]  
> Beide Pen-Ereignisse und Maus Meldungen werden an eine Anwendung gesendet, unabhängig davon, ob der Stift oder die Maus verwendet wird.

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>Unterscheiden von Stift Eingaben von Maus und Berührung

Wenn Ihre Anwendung eine Maus Nachricht empfängt (z. b. WM \_ lbuttondown), kann Sie die [**getMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) -Funktion aufrufen, um auszuwerten, ob die Nachricht von einem Stift oder einem Mausgerät stammt.

Der von [**getMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) zurückgegebene Wert muss mit 0xffffff00 maskiert und dann mit 0xff515700 verglichen werden. Die folgenden Definitionen können dies deutlicher machen:


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



Wenn der Vergleich true ist, wurde diese Maus Meldung von einem Tablet PC-Stift oder Touchscreen generiert. In allen anderen Fällen können Sie davon ausgehen, dass diese Meldung von einem Mausgerät generiert wurde.

Die unteren 8 Bits, die von [**getMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) zurückgegeben werden, sind Variable. Von diesen Bits werden 7 (die unteren 7, maskiert durch 0x7F) verwendet, um die Cursor-ID, 0 (null) für die Maus oder einen variablen Wert für die Stift-ID darzustellen. Darüber hinaus wird in Windows Vista das achte Bit, das von 0x80 maskiert wird, zur Unterscheidung von Berührungs Eingaben von Stift Eingaben (0 = Stift, 1 = berühren) verwendet.

## <a name="supported-system-gestures"></a>Unterstützte System Gesten

In der folgenden Tabelle sind die System Gesten aufgelistet, die derzeit in der Windows XP Tablet PC Edition enthalten sind. Außerdem werden die entsprechenden Stift Aktionen und Systemereignisse erläutert und gezeigt, wie Sie sich auf herkömmliche Mausaktionen beziehen.



| Stift Bewegung                                  | Mausaktion                                                    | Stift Gesten Beschreibung                                                                                                                                                                                                             | Ereignismeldungen                                                                                                                       | Maus Meldungen                                                                                                                        | Verhalten in Windows-basierten Anwendungen                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tippen<br/>                               | Linksklick<br/>                                           | Tippen Sie einmal mit dem Stift auf den Bildschirm.<br/>                                                                                                                                                                                        | Der ISG- \_ TAP wird gesendet, wenn der Stift angehoben wird.<br/>                                                                                         | WM \_ lbuttondown und WM \_ lbuttonup gesendet, wenn der Stift angehoben wurde.<br/>                                                                    | Wählen Sie im Menü oder in der Symbolleiste Befehl aus, wählen Sie Aktionen aus, wenn der Befehl ausgewählt ist, legen Sie die Einfügemarke (IP)<br/>                                                |
| Doppeltippen<br/>                        | Doppelklicken<br/>                                         | Tippen Sie in schneller Folge zweimal auf den Bildschirm.<br/>                                                                                                                                                                                    | ISG- \_ Double TAP wird bei Second Tap (unten) gesendet. Das ISG- \_ Tap-Ereignis wird beim ersten tippen gesendet.<br/>                                           | WM \_ lbuttondblclk wird bei zweiter Tap (unten) gesendet. WM \_ lbuttondown und WM \_ lbuttonup werden bei der ersten Abzweigung (nach oben) als für eine einzelne Tap gesendet.<br/> | Wählen Sie Word, Datei oder Ordner öffnen aus.<br/>                                                                                                                                     |
| Drücken und Halten<br/>                    | Klicken Sie mit der rechten Maustaste auf<br/>                                          | Tippen Sie auf den Bildschirm, bis ein Maus Symbol angezeigt wird, und heben Sie dann den Stift auf, um ein Kontextmenü anzuzeigen. Eine Anwendung könnte eine Aktion durchführen, die sich von der Anzeige eines Rechtsklick Menüs unterscheidet, wenn der Stift angehoben wird.<br/> | ISG- \_ holdenter, wenn der Stift lang genug ist. ISG \_ -RightTap wird gesendet, wenn der Stift angehoben wird und mit der rechten Maustaste angezeigt wird.<br/> | Die WM \_ -rbuttondown-und die WM- \_ rbuttonup werden gesendet, wenn mit der rechten Maustaste ein Klick erfolgt<br/>                                       | Kontextmenü anzeigen.<br/>                                                                                                                                                   |
| Durchhalten<br/>                      | Linksklick<br/>                                           | Tippen Sie auf den Bildschirm, und halten Sie gedrückt, bis das Maus Symbol angezeigt wird. Der Benutzer ist wahrscheinlich, dass dies bei einem unmöglichen drücken und halten von Benutzern der Fall ist.<br/>                                                 | Der ISG- \_ TAP wird gesendet, wenn der Stift angehoben wird.<br/>                                                                                         | WM \_ lbuttondown und WM \_ lbuttonup werden gesendet, wenn der Stift angehoben wird.<br/>                                                                 | Klicken Sie mit der linken Maustaste auf einen langen Zeitraum. Es ist keine Maus Äquivalent vorhanden. Dies ist ein Fall Back für den Fall, dass ein Benutzer eine lange Zeit gedrückt hält. Das Ereignis wird als Tap wieder hergestellt.<br/> |
| Ziehen<br/>                              | Left-Drag-Vorgang<br/>                                            | Tippen Sie auf den Bildschirm, um das Objekt auszuwählen, das verschoben werden soll, und ziehen Sie es dann nach Auswahl des Objekts.<br/>                                                                                                                     | Beim Starten des Zieh Vorgangs wird der ISG- \_ Drag<br/>                                                                                          | WM \_ lbuttondown wird gesendet, wenn der Zieh Vorgang beginnt, gefolgt von einer Reihe von Maus Verschiebungs Meldungen und gefolgt von einem WM- \_ lbuttonup-Ereignis.<br/> | Ziehen Sie die Select-Option wie in Microsoft Word, wenn Sie mit einer IP-Adresse beginnen. mehrere Wörter auswählen; Ziehen Sie, als wenn Sie ein Objekt in Windows ziehen. Scroll.<br/>                            |
| Halten Sie gedrückt, gefolgt von Drag<br/> | Rechter Ziehpunkt<br/>                                           | Tippen Sie auf den Bildschirm, um das Objekt auszuwählen, das verschoben werden soll. Halten Sie das Symbol gedrückt, bis das Maus Symbol angezeigt wird, und verschieben Sie das Objekt. Heben Sie den Stift auf, um ein Kontextmenü anzuzeigen.<br/>                                                   | ISG- \_ holdenter wurde gesendet, wenn der Stift seit einiger Zeit nicht mehr angezeigt wird. ISG- \_ RightDrag wird gesendet, wenn der Zieh Vorgang beginnt.<br/>                           | WM- \_ rbuttondown wird gesendet, wenn der Zieh Vorgang beginnt, gefolgt von einer Reihe von Maus Verschiebungs Meldungen, gefolgt von einem WM- \_ rbuttonup-Ereignis.<br/>     | Ziehen Sie, als wenn Sie ein Objekt oder eine Auswahl ziehen, gefolgt von einem Kontextmenü.<br/>                                                                                             |
| Stift Hover<br/>                         | Mauszeiger<br/>                                          | Halten Sie den Stift in einer kleinen Entfernung vom Bildschirm konstant.<br/>                                                                                                                                                                 | ISG \_ HoverEnter-Ereignis, das Anfangs gesendet wurde. Wenn das Hover-Intervall abgeschlossen ist, wird ISG \_ hoverleaveis gesendet.<br/>                           | Keine entsprechende Maus Meldung.<br/>                                                                                               | Anzeigen von QuickInfo, Rollover-Effekten und anderen Mauszeiger Verhalten.<br/>                                                                                                     |
| In-Air-Shake<br/>                      | **Tablet PC-Eingabe** Bereich anzeigen. Keine Maus Äquivalent.<br/> | Bewegen Sie den Stift schnell von Seite zu Seite, und halten Sie den obigen Tipp, aber innerhalb des Bereichs von, dem Bildschirm.<br/>                                                                                                                          | Das Ereignis wird nicht an die Anwendung übermittelt.<br/>                                                                                   | Keine entsprechende Maus Meldung.<br/>                                                                                               | Neu, speziell für Tablet PC.<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>Angeben von Stift-und Berührungs Interaktionen

Standardmäßig empfängt das Fenster alle systemgesten-Ereignisse und verwendet das Standard Interaktionsmodell. Einige Teile dieses Modells können Ihre Anwendung beeinträchtigen, sodass Sie Sie selektiv deaktivieren können, indem Sie in der WndProc-Meldung auf die " [**WM \_ Tablet \_ querysystemgesturestatus**](wm-tablet-querysystemgesturestatus-message.md) "-Meldung Antworten.

 

 
