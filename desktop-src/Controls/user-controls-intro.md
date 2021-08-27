---
title: Benutzerdefinierte Steuerelemente
description: Dieser Abschnitt enthält Informationen zu anwendungsdefinierten oder benutzerdefinierten Steuerelementen.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d1a31a44f1f71d99088f7729c2de6d5fdb597e14507f5f994dfaca1b96613d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059710"
---
# <a name="custom-controls"></a>Benutzerdefinierte Steuerelemente

Dieser Abschnitt enthält Informationen zu anwendungsdefinierten oder benutzerdefinierten Steuerelementen.

Die folgenden Themen werden erläutert.

-   [Erstellen Owner-Drawn Steuerelementen](#creating-owner-drawn-controls)
-   [Unterklassen der Window-Klasse eines vorhandenen Steuerelements](#subclassing-the-window-class-of-an-existing-control)
-   [Implementieren einer Application-Defined Window-Klasse](#implementing-an-application-defined-window-class)
-   [Senden von Benachrichtigungen von einem Steuerelement](#sending-notifications-from-a-control)
-   [Bedienungshilfen](#accessibility)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Erstellen Owner-Drawn Steuerelementen

Schaltflächen, Menüs, statische Textsteuerelemente, Listenfelder und Kombinationsfelder können mit einem vom Besitzer gezeichneten Stilflag erstellt werden. Wenn ein Steuerelement über den vom Besitzer gezeichneten Stil verfügt, verarbeitet das System die Interaktion des Benutzers mit dem Steuerelement wie gewohnt. Dabei werden aufgaben wie das Erkennen, wenn ein Benutzer eine Schaltfläche ausgewählt hat, und der Besitzer des Ereignisses benachrichtigt. Da das Steuerelement jedoch vom Besitzer gezeichnet wird, ist das übergeordnete Fenster des Steuerelements für die visuelle Darstellung des Steuerelements verantwortlich. Das übergeordnete Fenster empfängt immer dann eine Meldung, wenn das Steuerelement gezeichnet werden muss.

Bei Schaltflächen und statischen Textsteuerelementen wirkt sich der vom Besitzer gezeichnete Stil darauf aus, wie das System das gesamte Steuerelement zeichnet. Bei Listen- und Kombinationsfeldern zeichnet das übergeordnete Fenster die Elemente im Steuerelement, und das Steuerelement zeichnet seine eigene Kontur. Beispielsweise kann eine Anwendung ein Listenfeld so anpassen, dass neben jedem Element in der Liste eine kleine Bitmap angezeigt wird.

Der folgende Beispielcode zeigt, wie ein vom Besitzer gezeichnetes statisches Textsteuerfeld erstellt wird. Angenommen, Unicode ist definiert.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



Im folgenden Beispiel wird in der Fensterprozedur für das Dialogfeld, das das im vorherigen Beispiel erstellte Steuerelement enthält, die [**WM \_ DRAWITEM-Meldung**](wm-drawitem.md) behandelt, indem der Text in einer benutzerdefinierten Farbe mithilfe der Standardschriftart angezeigt wird. Beachten Sie, dass Sie [**beginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) und [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) nicht aufrufen müssen, wenn Sie **WM \_ DRAWITEM behandeln.**


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



Weitere Informationen zu vom Besitzer gezeichneten Steuerelementen finden Sie unter [Creating an Owner-drawn List Box](using-list-boxes.md) and Owner Drawn Combo [Boxes](about-combo-boxes.md).

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Unterklassen der Window-Klasse eines vorhandenen Steuerelements

Die Unterklasse eines vorhandenen Steuerelements ist eine weitere Möglichkeit, ein benutzerdefiniertes Steuerelement zu erstellen. Die Unterklassenprozedur kann ausgewählte Verhaltensweisen des Steuerelements ändern, indem die Nachrichten verarbeitet werden, die sich auf das ausgewählte Verhalten auswirken. Alle anderen Meldungen werden an die ursprüngliche Fensterprozedur für das Steuerelement übergeben. Beispielsweise kann eine Anwendung eine kleine Bitmap neben dem Text in einem schreibgeschützten, einzeilenbasierten Bearbeitungssteuerfeld anzeigen, indem das Steuerelement untergliedert und die [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) verarbeitet wird. Weitere Informationen finden Sie unter [About Window Procedures](/windows/desktop/winmsg/about-window-procedures) and [Subclassing Controls](subclassing-overview.md).

## <a name="implementing-an-application-defined-window-class"></a>Implementieren einer Application-Defined Window-Klasse

Um ein Steuerelement zu erstellen, das nicht explizit auf einem vorhandenen Steuerelement basiert, muss die Anwendung eine Fensterklasse erstellen und registrieren. Der Prozess zum Registrieren einer anwendungsdefinierten Fensterklasse für ein benutzerdefiniertes Steuerelement ist mit dem Registrieren einer Klasse für ein normales Fenster identisch. Um ein benutzerdefiniertes Steuerelement zu erstellen, geben Sie den Namen der Fensterklasse in der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oder in einer Dialogfeldvorlage an. Jede Klasse muss einen eindeutigen Namen, eine entsprechende Fensterprozedur und andere Informationen haben.

Die Fensterprozedur zeichnet mindestens das -Steuerelement. Wenn eine Anwendung das -Steuerelement verwendet, um dem Benutzer die Eingabe von Informationen zu ermöglichen, verarbeitet die Fensterprozedur auch Eingabemeldungen von Tastatur und Maus und sendet Benachrichtigungsmeldungen an das übergeordnete Fenster. Darüber hinaus verarbeitet die Fensterprozedur Nachrichten, die vom übergeordneten Fenster oder anderen Fenstern an das Steuerelement gesendet werden, wenn das Steuerelement Steuerungsmeldungen unterstützt. Steuerelemente verarbeiten z. B. häufig die [**WM \_ GETDLGCODE-Nachricht,**](/windows/desktop/dlgbox/wm-getdlgcode) die von Dialogfeldern gesendet wird, um ein Dialogfeld an die Verarbeitung von Tastatureingaben auf eine bestimmte Weise zu richten.

Die Fensterprozedur für ein anwendungsdefiniertes Steuerelement sollte alle vordefinierten Steuernachrichten in der folgenden Tabelle verarbeiten, wenn die Meldung den Betrieb des Steuerelements beeinflusst.



| `Message`                                          | Empfehlung                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)       | Verarbeiten Sie , wenn das Steuerelement die EINGABETASTE, ESC, TAB ODER PFEILTASTE verwendet. Die [**IsDialogMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) sendet diese Nachricht an Steuerelemente in einem Dialogfeld, um zu bestimmen, ob die Schlüssel zu verarbeiten oder an das Steuerelement übergeben werden sollen. |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)             | Verarbeiten Sie, ob [**die WM \_ SETFONT-Nachricht**](/windows/desktop/winmsg/wm-setfont) ebenfalls verarbeitet wird.                                                                                                                                                                  |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)             | Verarbeiten Sie , wenn der Steuerelementtext nicht mit dem von der [**CreateWindowEx-Funktion angegebenen Titel identisch**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ist.                                                                                                                 |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) | Verarbeiten Sie , wenn der Steuerelementtext nicht mit dem von der [**CreateWindowEx-Funktion angegebenen Titel identisch**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ist.                                                                                                                 |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)       | Verarbeiten Sie , wenn das Steuerelement ein Caretelement, ein Fokusrechteck oder ein anderes Element anzeigt, um anzugeben, dass es den Eingabefokus besitzt.                                                                                                                            |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)         | Verarbeiten Sie , wenn das Steuerelement ein Caretelement, ein Fokusrechteck oder ein anderes Element anzeigt, um anzugeben, dass es den Eingabefokus besitzt.                                                                                                                            |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)             | Verarbeiten Sie , wenn der Steuerelementtext nicht mit dem von der [**CreateWindowEx-Funktion angegebenen Titel identisch**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ist.                                                                                                                 |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)             | Verarbeiten Sie , wenn das Steuerelement Text anzeigt. Das System sendet diese Meldung, wenn ein Dialogfeld mit dem DS \_ SETFONT-Format erstellt wird.                                                                                                                  |



 

Anwendungsdefinierte Steuerungsmeldungen sind spezifisch für das gegebene Steuerelement und müssen explizit mithilfe einer [**SendMessage-**](/windows/desktop/api/winuser/nf-winuser-sendmessage) oder [**SendDlgItemMessage-Funktion an**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) das Steuerelement gesendet werden. Der numerische Wert für jede Nachricht muss eindeutig sein und darf nicht mit den Werten anderer Fenstermeldungen in Konflikt stehen. Um sicherzustellen, dass anwendungsdefinierte Nachrichtenwerte nicht in Konflikt stehen, sollte eine Anwendung jeden Wert erstellen, indem dem [**WM \_ USER-Wert**](/windows/desktop/winmsg/wm-user) eine eindeutige Zahl hinzugefügt wird.

## <a name="sending-notifications-from-a-control"></a>Senden von Benachrichtigungen von einem Steuerelement

Möglicherweise sind benutzerdefinierte Steuerelemente erforderlich, um Benachrichtigungen über Ereignisse an das übergeordnete Fenster zu senden, damit die Hostanwendung auf diese Ereignisse reagieren kann. Beispielsweise kann eine benutzerdefinierte Listenansicht eine Benachrichtigung senden, wenn der Benutzer ein Element auswählt, und eine weitere Benachrichtigung, wenn auf ein Element doppelklickt wird.

Benachrichtigungen werden als [**WM \_ COMMAND- oder**](/windows/desktop/menurc/wm-command) WM [**\_ NOTIFY-Meldungen**](wm-notify.md) gesendet. **WM \_ NOTIFY-Nachrichten** enthalten mehr Informationen als **WM \_ COMMAND-Nachrichten.**

Der Steuerelementbezeichner ist eine eindeutige Zahl, mit der die Anwendung das Steuerelement identifiziert, das die Nachricht sendet. Die Anwendung legt beim Erstellen des Steuerelements den Bezeichner für ein Steuerelement fest. Die Anwendung gibt den Bezeichner entweder im *hMenu-Parameter* der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oder im **ID-Member** der [**DLGITEMTEMPLATEEX-Struktur**](/windows/desktop/dlgbox/dlgitemtemplateex) an.

Da das Steuerelement selbst den Steuerelementbezeichner nicht festgelegt, muss das Steuerelement den Bezeichner abrufen, bevor es Benachrichtigungsmeldungen senden kann. Ein Steuerelement muss die [**GetDlgCtrlID-Funktion**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) verwenden, um seinen eigenen Steuerelementbezeichner abzurufen. Obwohl der Steuerelementbezeichner beim Erstellen des Steuerelements als Menühand handle angegeben wird, kann die [**GetMenu-Funktion**](/windows/desktop/api/winuser/nf-winuser-getmenu) nicht zum Abrufen des Bezeichners verwendet werden. Alternativ kann ein Steuerelement den Bezeichner aus dem **hMenu-Member** in der [**CREATESTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-createstructa) abrufen, während die [**WM \_ CREATE-Nachricht verarbeitet**](/windows/desktop/winmsg/wm-create) wird.

Die folgenden Beispiele, in denen *hwndControl* das Handle des Steuerelementfensters und CN VALUECHANGED eine benutzerdefinierte Benachrichtigungsdefinition ist, zeigen die beiden Möglichkeiten zum Senden einer steuerelementspezifischen \_ Benachrichtigung.


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



Beachten Sie, [**dass die NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) Teil einer größeren steuerelementdefinierten Struktur sein kann, die zusätzliche Informationen enthält. Im Beispiel können die alten und neuen Werte des -Steuerelements in dieser -Struktur enthalten sein. (Solche erweiterten Strukturen werden mit vielen Standardbenachrichtigungen verwendet. Informationen dazu finden Sie beispielsweise unter [LVN \_ INSERTITEM](lvn-insertitem.md), das die [**NMLISTVIEW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) verwendet.)

## <a name="accessibility"></a>Zugriff

Alle gängigen Steuerelemente unterstützen Microsoft Active Accessibility (MSAA), die programmgesteuerten Zugriff über Anwendungen mit barrierefreier Technologie wie Sprachbildschirme ermöglicht. MSAA ermöglicht es Benutzeroberflächenautomatisierung, einer neueren Technologie, mit Steuerelementen zu interagieren.

Benutzerdefinierte Steuerelemente sollten entweder die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (zur Unterstützung von MSAA) oder die Benutzeroberflächenautomatisierung oder beides implementieren. Andernfalls können Barrierefreie Technologieprodukte nur sehr eingeschränkte Informationen über das Steuerfenster abrufen, haben keinen Zugriff auf die Eigenschaften des Steuerelements und können keine Ereignisse im Steuerelement auslösen.

Weitere Informationen zum Zugänglich machen Ihres Steuerelements finden Sie unter Windows [Automation-API.](/windows/desktop/WinAuto/windows-automation-api-portal)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Steuerelementreferenz](common-control-reference.md)
</dt> <dt>

[Anpassen der Darstellung eines Steuerelements mit benutzerdefiniertem Zeichnen](custom-draw.md)
</dt> <dt>

[Steuern von Nachrichten](control-messages.md)
</dt> <dt>

[Verwenden von visuellen Stilen mit Owner-Drawn Steuerelementen](using-visual-styles.md)
</dt> </dl>

 

 