---
title: Benutzerdefinierte Steuerelemente
description: Dieser Abschnitt enthält Informationen zu Anwendungs definierten oder benutzerdefinierten Steuerelementen.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82ed9394ec06257e524153b86ef487f4507f35b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102374"
---
# <a name="custom-controls"></a>Benutzerdefinierte Steuerelemente

Dieser Abschnitt enthält Informationen zu Anwendungs definierten oder benutzerdefinierten Steuerelementen.

Die folgenden Themen werden erörtert.

-   [Erstellen von Owner-Drawn Steuerelementen](#creating-owner-drawn-controls)
-   [Unterklassen der Fenster Klasse eines vorhandenen Steuer Elements](#subclassing-the-window-class-of-an-existing-control)
-   [Implementieren einer Application-Defined Window-Klasse](#implementing-an-application-defined-window-class)
-   [Senden von Benachrichtigungen von einem Steuerelement](#sending-notifications-from-a-control)
-   [Bedienungshilfen](#accessibility)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Erstellen von Owner-Drawn Steuerelementen

Schaltflächen, Menüs, statische Text Steuerelemente, Listenfelder und Kombinations Felder können mit einem vom Besitzer gezeichneten stilflag erstellt werden. Wenn ein Steuerelement den vom Besitzer gezeichneten Stil hat, verarbeitet das System die Interaktion des Benutzers mit dem Steuerelement wie gewohnt und führt Aufgaben wie das erkennen aus, wenn ein Benutzer eine Schaltfläche ausgewählt hat und benachrichtigt den Besitzer des Ereignisses der Schaltfläche. Da das Steuerelement jedoch vom Besitzer gezeichnet wird, ist das übergeordnete Fenster des Steuer Elements für die visuelle Darstellung des Steuer Elements verantwortlich. Das übergeordnete Fenster empfängt eine Nachricht, wenn das Steuerelement gezeichnet werden muss.

Bei Schaltflächen und statischen Text Steuerelementen wirkt sich der vom Besitzer gezeichnete Stil darauf aus, wie das System das gesamte Steuerelement zeichnet. Für Listenfelder und Kombinations Felder zeichnet das übergeordnete Fenster die Elemente innerhalb des Steuer Elements, und das Steuerelement zeichnet seinen eigenen Umriss. Beispielsweise kann eine Anwendung ein Listenfeld so anpassen, dass neben den einzelnen Elementen in der Liste eine kleine Bitmap angezeigt wird.

Der folgende Beispielcode zeigt, wie ein vom Besitzer gezeichnetes statisches Text Steuerelement erstellt wird. Angenommen, Unicode ist definiert.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



Im folgenden Beispiel wird die [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht in der Fenster Prozedur für das Dialogfeld, das das im vorherigen Beispiel erstellte Steuerelement enthält, behandelt, indem der Text mit der Standard Schriftart in einer benutzerdefinierten Farbe angezeigt wird. Beachten Sie, dass Sie bei der Behandlung von **WM \_ DrawItem** nicht [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) und [**endpaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) aufrufen müssen.


```
case WM_DRAWITEM:
{
    LPDRAWITEMSTRUCT pDIS = (LPDRAWITEMSTRUCT)lParam;
    if (pDIS->hwndItem == g_myStatic)
    {
        SetTextColor(pDIS->hDC, RGB(100, 0, 100));
        WCHAR staticText[99];
        int len = SendMessage(myStatic, WM_GETTEXT, 
            ARRAYSIZE(staticText), (LPARAM)staticText);
        TextOut(pDIS->hDC, pDIS->rcItem.left, pDIS->rcItem.top, staticText, len);
    }
    return TRUE;
}
```



Weitere Informationen zu Steuerelementen, die von einem Besitzer gezeichnet werden, finden Sie unter [Erstellen eines von einem Besitzer gezeichneten Listen](using-list-boxes.md) Felds und von Besitzer gezeichneten Kombinations [Feldern](about-combo-boxes.md)

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Unterklassen der Fenster Klasse eines vorhandenen Steuer Elements

Ein vorhandenes Steuerelement zu erstellen, ist eine andere Möglichkeit, ein benutzerdefiniertes Steuerelement zu erstellen. Die Unterklassen Prozedur kann das ausgewählte Verhalten des Steuer Elements ändern, indem die Nachrichten verarbeitet werden, die das ausgewählte Verhalten beeinflussen. Alle anderen Nachrichten werden an die ursprüngliche Fenster Prozedur für das-Steuerelement übergeben. Beispielsweise kann eine Anwendung eine kleine Bitmap neben dem Text in einem schreibgeschützten, einzeiligen Bearbeitungs Steuerelement anzeigen, indem Sie das Steuerelement Unterklassen und die [**WM- \_**](/windows/desktop/gdi/wm-paint) Zeichnungs Nachricht verarbeitet. Weitere Informationen finden Sie unter Informationen [zu Fenster Prozeduren](/windows/desktop/winmsg/about-window-procedures) und [Unterklassen](subclassing-overview.md)-Steuerelementen.

## <a name="implementing-an-application-defined-window-class"></a>Implementieren einer Application-Defined Window-Klasse

Um ein Steuerelement zu erstellen, das nicht explizit auf einem vorhandenen Steuerelement basiert, muss die Anwendung eine Fenster Klasse erstellen und registrieren. Der Prozess zum Registrieren einer Anwendungs definierten Fenster Klasse für ein benutzerdefiniertes Steuerelement ist mit dem Registrieren einer Klasse für ein normales Fenster identisch. Um ein benutzerdefiniertes Steuerelement zu erstellen, geben Sie den Namen der Fenster Klasse in [**der Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) in der Funktion" "und" "in einer Dialogfeld Vorlage an. Jede Klasse muss einen eindeutigen Namen, eine entsprechende Fenster Prozedur und weitere Informationen aufweisen.

Die Fenster Prozedur zeichnet das Steuerelement mindestens. Wenn eine Anwendung das-Steuerelement verwendet, um den Benutzertyp Informationen zuzulassen, verarbeitet die Fenster Prozedur auch Eingabe Nachrichten von Tastatur und Maus und sendet Benachrichtigungs Meldungen an das übergeordnete Fenster. Wenn das Steuerelement außerdem Steuerungs Meldungen unterstützt, verarbeitet die Fenster Prozedur Nachrichten, die vom übergeordneten Fenster oder von anderen Fenstern an das Steuerelement gesendet werden. Beispielsweise verarbeiten Steuerelemente häufig die von Dialogfeldern gesendete [**WM \_ getdlgcode**](/windows/desktop/dlgbox/wm-getdlgcode) -Nachricht, um ein Dialogfeld zu leiten, um Tastatureingaben auf eine bestimmte Art und Weise zu verarbeiten.

Die Fenster Prozedur für ein von der Anwendung definiertes Steuerelement sollte jede vordefinierte Steuerelement Nachricht in der folgenden Tabelle verarbeiten, wenn sich die Nachricht auf den Betrieb des-Steuer Elements auswirkt.



| `Message`                                          | Empfehlung                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ getdlgcode**](/windows/desktop/dlgbox/wm-getdlgcode)       | Verarbeiten, wenn das Steuerelement die Tasten Eingabe, ESC, Tab oder Pfeil verwendet. Die [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) -Funktion sendet diese Nachricht an Steuerelemente in einem Dialogfeld, um zu bestimmen, ob die Schlüssel verarbeitet oder an das Steuerelement übergeben werden sollen. |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)             | Verarbeiten, wenn die [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont) -Nachricht ebenfalls verarbeitet wird.                                                                                                                                                                  |
| [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)             | Process, wenn der Steuerelement Text nicht mit dem Titel übereinstimmt [**, der durch die Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Funktion" von "Funktion" festgelegt wurde.                                                                                                                 |
| [**WM \_ getTextLength**](/windows/desktop/winmsg/wm-gettextlength) | Process, wenn der Steuerelement Text nicht mit dem Titel übereinstimmt [**, der durch die Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Funktion" von "Funktion" festgelegt wurde.                                                                                                                 |
| [**WM- \_ killfokus**](/windows/desktop/inputdev/wm-killfocus)       | Verarbeiten, wenn das Steuerelement eine Einfügemarke, ein Fokus Rechteck oder ein anderes Element anzeigt, um anzugeben, dass es den Eingabefokus besitzt.                                                                                                                            |
| [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)         | Verarbeiten, wenn das Steuerelement eine Einfügemarke, ein Fokus Rechteck oder ein anderes Element anzeigt, um anzugeben, dass es den Eingabefokus besitzt.                                                                                                                            |
| [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext)             | Process, wenn der Steuerelement Text nicht mit dem Titel übereinstimmt [**, der durch die Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Funktion" von "Funktion" festgelegt wurde.                                                                                                                 |
| [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont)             | Verarbeiten, wenn das Steuerelement Text anzeigt. Das System sendet diese Meldung, wenn ein Dialogfeld mit dem DS- \_ setFont-Stil erstellt wird.                                                                                                                  |



 

Anwendungs definierte Steuerungs Meldungen sind spezifisch für das angegebene Steuerelement und müssen explizit mithilfe einer [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -oder [**SendDlgItemMess**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) -Funktion an das Steuerelement gesendet werden. Der numerische Wert für jede Nachricht muss eindeutig sein und darf nicht mit den Werten anderer Fenster Meldungen in Konflikt stehen. Um sicherzustellen, dass Anwendungs definierte Nachrichten Werte nicht in Konflikt stehen, sollte eine Anwendung jeden Wert erstellen, indem Sie dem Wert des [**WM- \_ Benutzers**](/windows/desktop/winmsg/wm-user) eine eindeutige Nummer hinzufügt.

## <a name="sending-notifications-from-a-control"></a>Senden von Benachrichtigungen von einem Steuerelement

Möglicherweise sind benutzerdefinierte Steuerelemente erforderlich, um Benachrichtigungen von Ereignissen an das übergeordnete Fenster zu senden, damit die Host Anwendung auf diese Ereignisse reagieren kann. Beispielsweise kann eine benutzerdefinierte Listenansicht eine Benachrichtigung senden, wenn der Benutzer ein Element auswählt, und eine weitere Benachrichtigung, wenn auf ein Element Doppel geklickt wird.

Benachrichtigungen werden als [**WM- \_ Befehl**](/windows/desktop/menurc/wm-command) oder [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen gesendet. **WM \_ Benachrichtigungs** Meldungen enthalten mehr Informationen als **WM- \_ Befehls** Nachrichten.

Der Steuerelement Bezeichner ist eine eindeutige Zahl, mit der die Anwendung das Steuerelement identifiziert, das die Nachricht sendet. Die Anwendung legt den Bezeichner für ein Steuerelement fest, wenn das Steuerelement erstellt wird. Die Anwendung gibt den Bezeichner entweder im *HMENU* -Parameter der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder im **ID** -Member der [**dlgitemtemplateex**](/windows/desktop/dlgbox/dlgitemtemplateex) -Struktur an.

Da das Steuerelement selbst den Steuerelement Bezeichner nicht festgelegt hat, muss das Steuerelement den Bezeichner abrufen, bevor er Benachrichtigungs Meldungen senden kann. Ein Steuerelement muss die [**getdlgctrlid**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) -Funktion verwenden, um seinen eigenen Steuerelement Bezeichner abzurufen. Obwohl der Steuerelement Bezeichner bei der Erstellung des Steuer Elements als Menü handle angegeben ist, kann die [**getMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) -Funktion nicht zum Abrufen des Bezeichners verwendet werden. Alternativ kann ein Steuerelement während der Verarbeitung der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht den Bezeichner aus dem **HMENU** -Member in [**der Struktur "**](/windows/win32/api/winuser/ns-winuser-createstructa) Struktur erstellen" abrufen.

In den folgenden Beispielen, in denen *hwndcontrol* das Handle des Steuerelement Fensters ist und CN \_ ValueChanged eine benutzerdefinierte Benachrichtigungs Definition ist, werden die beiden Möglichkeiten zum Senden einer Steuerelement spezifischen Benachrichtigung angezeigt.


```
 // Send as WM_COMMAND.
SendMessage(GetParent(hwndControl), 
    WM_COMMAND,
    MAKEWPARAM(GetDlgCtrlID(hwndControl), CN_VALUECHANGED),
    (LPARAM)hwndControl);

// Send as WM_NOTIFY.           
NMHDR nmh;
nmh.code = CN_VALUECHANGED;
nmh.idFrom = GetDlgCtrlID(hwndControl);
nmh.hwndFrom = hwndControl;
SendMessage(GetParent(hwndControl), 
    WM_NOTIFY, 
    (WPARAM)hwndControl, 
    (LPARAM)&nmh);
```



Beachten Sie, dass die [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur Teil einer größeren Steuerelement definierten Struktur sein kann, die zusätzliche Informationen enthält. In diesem Beispiel können der alte und der neue Wert des-Steuer Elements in dieser Struktur enthalten sein. (Solche erweiterten Strukturen werden mit vielen Standard Benachrichtigungen verwendet, z. b. unter [LVN \_ InsertItem](lvn-insertitem.md), das die [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur verwendet.)

## <a name="accessibility"></a>Eingabehilfen

Alle allgemeinen Steuerelemente unterstützen Microsoft Active Accessibility (MSAA), wodurch der programmgesteuerte Zugriff durch barrierefreie Anwendungen wie z. b. Bildschirm Ausgaben ermöglicht wird. MSAA ermöglicht außerdem die Benutzeroberflächen Automatisierung, eine neuere Technologie, um mit Steuerelementen zu interagieren.

Benutzerdefinierte Steuerelemente müssen entweder die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle (zur Unterstützung von MSAA) oder die Benutzeroberflächenautomatisierungs-Schnittstellen implementieren. Andernfalls können barrierefreie Technologie Produkte nur sehr eingeschränkte Informationen über das Steuerelement Fenster abrufen, haben keinen Zugriff auf die Eigenschaften des Steuer Elements und können keine Ereignisse im Steuerelement auslöst.

Weitere Informationen zum Zugriff auf das Steuerelement finden Sie unter [Windows Automation-API](/windows/desktop/WinAuto/windows-automation-api-portal).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Allgemeine Steuerungs Referenz](common-control-reference.md)
</dt> <dt>

[Anpassen des Erscheinungs Bilds eines Steuer Elements mithilfe von benutzerdefiniertem zeichnen](custom-draw.md)
</dt> <dt>

[Steuern von Meldungen](control-messages.md)
</dt> <dt>

[Verwenden von visuellen Stilen mit Owner-Drawn Steuerelementen](using-visual-styles.md)
</dt> </dl>

 

 