---
description: Ihre Anwendung integriert den optimalen Entwurf und die optimale Verwendung des Tablettstifts, indem sowohl Microsoft Windows Mausnachrichten als auch Systemereignisse gesendet werden.
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: Systemereignisse und Mausmeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d118b4cc0de115ddcf57fcebbbcea9923656fdad5bb11f31173fb03f4edfb1d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335110"
---
# <a name="system-events-and-mouse-messages"></a>Systemereignisse und Mausmeldungen

Ihre Anwendung integriert den optimalen Entwurf und die optimale Verwendung des Tablettstifts, indem sowohl Microsoft Windows Mausnachrichten als auch Systemereignisse gesendet werden. Anwendungen empfangen beide Sätze von Ereignissen für jede Stiftbewegung oder Aktion. Die Anwendung wählt dann das entsprechende Ereignis aus, das basierend auf dem Kontext der Aktion verwendet werden soll. Windows Mausnachrichten funktionieren gut zum Zeigen und Auswählen von Aktivitäten, und Sie sollten sie für Aktivitäten verwenden, die die Interaktion mit Elementen der Benutzeroberfläche (UI) beinhalten. Stiftereignisse funktionieren gut für Diekanwendung in Echtzeit, Stiftaktionen und Handschrift.

> [!Note]  
> Stiftereignisse und Mausmeldungen werden an eine Anwendung gesendet, unabhängig davon, ob der Stift oder die Maus verwendet wird.

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>Unterscheiden der Stifteingabe von Maus und Touch

Wenn Ihre Anwendung eine Mausnachricht empfängt (z. B. WM LBUTTONDOWN), kann sie die \_ [**GetMessageExtraInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) aufrufen, um zu bewerten, ob die Nachricht von einem Stift oder einem Mausgerät stammt.

Der wert, der von [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) zurückgegeben wird, muss maskiert 0xFFFFFF00 und dann mit dem 0xFF515700. Die folgenden Definitionen können dies deutlich machen:


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



Wenn der Vergleich true ist, wurde diese Mausmeldung von einem Tablet PC-Stift oder Touchscreen generiert. In allen anderen Fällen können Sie davon ausgehen, dass diese Nachricht von einem Mausgerät generiert wurde.

Die unteren 8 Bits, die von [**GetMessageExtraInfo zurückgegeben werden,**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) sind variabel. Von diesen Bits werden 7 (die untere 7, durch 0x7F maskiert) verwendet, um die Cursor-ID, null für die Maus oder einen Variablenwert für die Stift-ID zu darstellen. Darüber hinaus wird in Windows Vista das achte Bit, maskiert von 0x80, verwendet, um Toucheingaben von Stifteingaben (0 = Stift, 1 = Touch) zu unterscheiden.

## <a name="supported-system-gestures"></a>Unterstützte Systemgesten

In der folgenden Tabelle sind die derzeit in der Windows XP Tablet PC Edition enthaltenen Systemgesten aufgeführt. Außerdem werden die entsprechenden Stiftaktionen und Systemereignisse sowie deren Beziehung zu herkömmlichen Mausaktionen aufgeführt.



| Stiftgeste                                  | Mausaktion                                                    | Stiftgestenbeschreibung                                                                                                                                                                                                             | Ereignismeldungen                                                                                                                       | Mausmeldungen                                                                                                                        | Verhalten in Windows-basierten Anwendungen                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tippen<br/>                               | Linksklick<br/>                                           | Tippen Sie einmal mit dem Stift auf den Bildschirm.<br/>                                                                                                                                                                                        | ISG \_ TAP wird beim Heben des Stifts gesendet.<br/>                                                                                         | WM \_ LBUTTONDOWN und WM \_ LBUTTONUP werden gesendet, wenn der Stift gezauft wurde.<br/>                                                                    | Wählen Sie im Menü oder in der Symbolleiste den Befehl aus, ergreifen Sie eine Aktion, wenn Sie den Befehl ausgewählt haben, legen Sie die Einfügemarke (IP) fest, und zeigen Sie Auswahlfeedback an.<br/>                                                |
| Doppeltippen<br/>                        | Doppelklicken<br/>                                         | Tippen Sie zweimal in schneller Folge auf bildschirm.<br/>                                                                                                                                                                                    | ISG \_ DOUBLETAP wird beim zweiten Tippen (nach unten) gesendet. BEIM ersten Tippen gesendetes ISG \_ TAP-Ereignis.<br/>                                           | WM \_ LBUTTONDBLCLK gesendet beim zweiten Tippen (nach unten). WM \_ LBUTTONDOWN und WM LBUTTONUP, die beim ersten Tippen \_ (nach oben) gesendet werden, wie bei einem einzigen Tippen.<br/> | Wählen Sie Word aus, öffnen Sie die Datei oder den Ordner .<br/>                                                                                                                                     |
| Drücken und Halten<br/>                    | Klicken Sie mit der rechten Maustaste auf<br/>                                          | Tippen Sie auf den Bildschirm, halten Sie ihn gedrückt, bis ein Maussymbol angezeigt wird, und heben Sie dann den Stift, um ein Kontextmenü anzuzeigen. Eine Anwendung kann eine Aktion ausführen, die sich von der Anzeige eines Kontextmenüs beim Heben des Stifts abwählt.<br/> | ISG \_ HOLDENTER wird gesendet, wenn der Stift lang genug heruntergefahren ist. ISG \_ RIGHTTAP wird gesendet, wenn der Stift per Lifting und Rechtsklick angezeigt wird.<br/> | WM RBUTTONDOWN und WM RBUTTONUP werden gesendet, wenn ein Rechtsklick \_ \_ auftritt (wenn der Stift per Lifting aufgehoben wird).<br/>                                       | Kontextmenü anzeigen.<br/>                                                                                                                                                   |
| Zurückhalten<br/>                      | Linksklick<br/>                                           | Tippen Sie auf den Bildschirm, und halten Sie ihn gedrückt, bis das Maussymbol angezeigt und nicht mehr angezeigt wird. Benutzer werden dies wahrscheinlich tun, wenn sie versehentlich drücken und halten und einfach tippen möchten.<br/>                                                 | ISG \_ TAP wird beim Heben des Stifts gesendet.<br/>                                                                                         | WM \_ LBUTTONDOWN und WM \_ LBUTTONUP werden gesendet, wenn der Stift per Lifting aufgehoben wird.<br/>                                                                 | Klicken Sie lange mit der linken Maustaste. Es ist kein Mausäquivalent vorhanden. Dies ist ein Fallback für den Fall, dass ein Benutzer lange gedrückt hält. Das Ereignis wird wieder zu einem Tippen.<br/> |
| Ziehen<br/>                              | Ziehen nach links<br/>                                            | Tippen Sie auf den Bildschirm, um das objekt auszuwählen, das verschoben werden soll, und ziehen Sie dann, nachdem das Objekt ausgewählt wurde.<br/>                                                                                                                     | ISG\_DRAG sent when drag starts.<br/>                                                                                          | WM LBUTTONDOWN wird gesendet, wenn der Ziehbewegungsstart gestartet wird, gefolgt von einer Reihe von Mausbewegungsmeldungen, gefolgt von einem \_ \_ WM-LBUTTONUP-Ereignis.<br/> | Ziehen Sie die Auswahl, wie in Microsoft Word, wenn Sie mit einer IP-Adresse beginnen. Wählen Sie mehrere Wörter aus. ziehen, wie beim Ziehen eines Objekts in Windows; Scrollen.<br/>                            |
| Halten Sie gedrückt, gefolgt von einem Ziehziehze<br/> | Ziehen mit der rechten Seite<br/>                                           | Tippen Sie auf den Bildschirm, um das Objekt auszuwählen, das verschoben werden soll. Halten Sie gedrückt, bis das Maussymbol angezeigt wird, und ziehen Sie dann, um das Objekt zu verschieben. Heben Sie den Stift auf, um ein Kontextmenü anzuzeigen.<br/>                                                   | ISG \_ HOLDENTER wird gesendet, wenn der Stift seit einiger Zeit nicht mehr zur Hand ist. ISG\_RIGHTDRAG sent when drag starts.<br/>                           | WM RBUTTONDOWN wird gesendet, wenn der Ziehbewegungsstart gestartet wird, gefolgt von einer Reihe von Mausbewegungsmeldungen, gefolgt von \_ einem WM \_ RBUTTONUP-Ereignis.<br/>     | Ziehen Sie , wie beim Ziehen eines Objekts oder einer Auswahl gefolgt von einem Kontextmenü.<br/>                                                                                             |
| Stift mit dem Hover<br/>                         | Mauszeigerzeiger<br/>                                          | Halten Sie den Stift in einem kleinen Abstand vom Bildschirm fest.<br/>                                                                                                                                                                 | Das ISG \_ HOVERENTER-Ereignis wurde anfänglich gesendet. Wenn das Hoverintervall abgeschlossen ist, werden ISG \_ HOVERLEAVEis gesendet.<br/>                           | Keine entsprechende Mausmeldung.<br/>                                                                                               | Zeigt QuickInfo, Rollovereffekte und andere Mauszeigerbewegungsverhalten an.<br/>                                                                                                     |
| Schütteln in der Luft<br/>                      | Tablet **PC-Eingabebereich anzeigen.** Keine Entsprechende Maus.<br/> | Bewegen Sie den Stift schnell von Seite zu Seite, und halten Sie den Tipp oben, aber innerhalb des Bereichs des Bildschirms.<br/>                                                                                                                          | Das Ereignis wird nicht an die Anwendung übergeben.<br/>                                                                                   | Keine entsprechende Mausmeldung.<br/>                                                                                               | Neu, spezifisch für Tablet PC.<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>Angeben von Stift- und Touchinteraktionen

Standardmäßig erhält Ihr Fenster alle Systemgestenereignisse und verwendet das Standardinteraktionsmodell. Einige Teile dieses Modells können Ihre Anwendung beeinträchtigen, sodass Sie sie selektiv deaktivieren können, indem Sie auf die [**WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS-Nachricht**](wm-tablet-querysystemgesturestatus-message.md) in Ihrer WndProc reagieren.

 

 
