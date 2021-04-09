---
title: Steuern von Meldungen
description: Dieser Abschnitt enthält Informationen darüber, wie Windows-Meldungen für die Kommunikation mit-Steuerelementen verwendet werden.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858580"
---
# <a name="control-messages"></a><span data-ttu-id="3134a-103">Steuern von Meldungen</span><span class="sxs-lookup"><span data-stu-id="3134a-103">Control Messages</span></span>

<span data-ttu-id="3134a-104">Dieser Abschnitt enthält Informationen darüber, wie Windows-Meldungen für die Kommunikation mit-Steuerelementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3134a-104">This section contains information about how Windows messages are used to communicate with controls.</span></span>

<span data-ttu-id="3134a-105">Die folgenden Themen werden erörtert.</span><span class="sxs-lookup"><span data-stu-id="3134a-105">The following topics are discussed.</span></span>

-   [<span data-ttu-id="3134a-106">Nachrichten an allgemeine Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3134a-106">Messages to Common Controls</span></span>](#messages-to-common-controls)
-   [<span data-ttu-id="3134a-107">Benachrichtigungen von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="3134a-107">Notifications from Controls</span></span>](#notifications-from-controls)
-   [<span data-ttu-id="3134a-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3134a-108">Related topics</span></span>](#related-topics)

## <a name="messages-to-common-controls"></a><span data-ttu-id="3134a-109">Nachrichten an allgemeine Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3134a-109">Messages to Common Controls</span></span>

<span data-ttu-id="3134a-110">Da es sich bei den allgemeinen Steuerelementen um Windows handelt, kann eine Anwendung mit Ihnen kommunizieren, indem allgemeine Microsoft Win32-Nachrichten wie [**WM \_ getFont**](/windows/desktop/winmsg/wm-getfont) oder [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3134a-110">Because common controls are windows, an application can communicate with them by using common Microsoft Win32 messages such as [**WM\_GETFONT**](/windows/desktop/winmsg/wm-getfont) or [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span> <span data-ttu-id="3134a-111">Außerdem unterstützt die Fenster Klasse der einzelnen allgemeinen Steuerelemente eine Reihe von Steuerelement spezifischen Meldungen.</span><span class="sxs-lookup"><span data-stu-id="3134a-111">In addition, the window class of each common control supports a set of control-specific messages.</span></span> <span data-ttu-id="3134a-112">In der Regel verwendet eine Anwendung [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) oder [**SendDlgItemMess**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) , um Nachrichten an das Steuerelement zu übergeben (häufig werden Informationen im Rückgabewert empfangen).</span><span class="sxs-lookup"><span data-stu-id="3134a-112">Typically, an application uses [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) or [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) to pass messages to the control (often receiving information in the return value).</span></span>

<span data-ttu-id="3134a-113">Einige allgemeine Steuerelemente verfügen auch über eine Reihe von Makros, die eine Anwendung anstelle von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="3134a-113">Some common controls also have a set of macros that an application can use instead of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="3134a-114">Die Makros sind in der Regel einfacher zu verwenden als die Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3134a-114">The macros are typically easier to use than the functions.</span></span> <span data-ttu-id="3134a-115">Der folgende Beispielcode ruft den Text des ausgewählten Struktur Ansichts Elements ab, wobei zuerst die unformatierten Nachrichten verwendet werden, und zweitens, indem die entsprechenden Makros verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3134a-115">The following example code retrieves the text of the selected tree-view item, first by using the raw messages, and second by using the equivalent macros.</span></span> <span data-ttu-id="3134a-116">Nehmen Sie an, dass *HWND* das Handle des Steuerelement Fensters ist.</span><span class="sxs-lookup"><span data-stu-id="3134a-116">Assume that *hwnd* is the handle of the control window.</span></span>


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



<span data-ttu-id="3134a-117">Wenn an den System Farbeinstellungen eine Änderung vorgenommen wird, sendet Windows eine [**\_ System-syscolorchange**](/windows/desktop/gdi/wm-syscolorchange) -Meldung an alle Fenster der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="3134a-117">When a change is made to the system color settings, Windows sends a [**WM\_SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) message to all top-level windows.</span></span> <span data-ttu-id="3134a-118">Das Fenster der obersten Ebene muss die **System- \_ syscolorchange** -Nachricht an die allgemeinen Steuerelemente weiterleiten. andernfalls werden die Steuerelemente nicht über die Farbänderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="3134a-118">Your top-level window must forward the **WM\_SYSCOLORCHANGE** message to its common controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="3134a-119">Durch Weiterleiten der Nachricht wird sichergestellt, dass die von den allgemeinen Steuerelementen verwendeten Farben mit den von anderen Benutzeroberflächen Objekten verwendeten Farben konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="3134a-119">Forwarding the message ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="3134a-120">Beispielsweise verwendet ein ToolBar-Steuerelement die Farbe "3D-Objekte", um seine Schaltflächen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="3134a-120">For example, a toolbar control uses the "3-D Objects" color to draw its buttons.</span></span> <span data-ttu-id="3134a-121">Wenn der Benutzer die Farbe des 3D-Objekts ändert, aber die **WM- \_ syscolorchange** -Meldung nicht an die Symbolleiste weitergeleitet wird, bleiben die Schaltflächen der Symbolleiste in der ursprünglichen Farbe (oder sogar in eine Kombination aus alten und neuen Farben geändert), während sich die Farbe anderer Schaltflächen im System ändert.</span><span class="sxs-lookup"><span data-stu-id="3134a-121">If the user changes the 3-D Object's color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color (or even change to a combination of old and new colors) while the color of other buttons in the system changes.</span></span>

## <a name="notifications-from-controls"></a><span data-ttu-id="3134a-122">Benachrichtigungen von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="3134a-122">Notifications from Controls</span></span>

<span data-ttu-id="3134a-123">Steuerelemente sind untergeordnete Fenster, die Benachrichtigungs Meldungen an das übergeordnete Fenster senden, wenn Ereignisse, die normalerweise durch eine Eingabe des Benutzers ausgelöst werden, im-Steuerelement auftreten.</span><span class="sxs-lookup"><span data-stu-id="3134a-123">Controls are child windows that send notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="3134a-124">Die Anwendung nutzt diese Benachrichtigungs Meldungen, um zu bestimmen, welche Aktion der Benutzer ausführen möchte.</span><span class="sxs-lookup"><span data-stu-id="3134a-124">The application relies on these notification messages to determine what action the user wants it to take.</span></span> <span data-ttu-id="3134a-125">Mit Ausnahme von trackbars, die die [**"WM \_ HScroll**](wm-hscroll.md) "-und " [**WM \_ VScroll**](wm-vscroll.md) "-Meldungen verwenden, um das übergeordnete Element von Änderungen zu benachrichtigen, senden allgemeine Steuerelemente Benachrichtigungen als [**WM- \_ Befehl**](/windows/desktop/menurc/wm-command) oder [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen, wie im Referenz Thema für die Benachrichtigung angegeben.</span><span class="sxs-lookup"><span data-stu-id="3134a-125">Except for trackbars, which use the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to notify their parent of changes, common controls send notifications as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages, as specified in the reference topic for the notification.</span></span> <span data-ttu-id="3134a-126">In der Regel verwenden ältere Benachrichtigungen (die für einen langen Zeitraum in der API enthalten waren) **den \_ Befehl WM**.</span><span class="sxs-lookup"><span data-stu-id="3134a-126">Typically, older notifications (those that have been in the API for a long time) use **WM\_COMMAND**.</span></span>

<span data-ttu-id="3134a-127">Der *LPARAM* -Parameter von [**WM \_ Notify**](wm-notify.md) ist entweder die Adresse einer [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur oder die Adresse einer größeren Struktur, die **NMHDR** als ersten Member enthält.</span><span class="sxs-lookup"><span data-stu-id="3134a-127">The *lParam* parameter of [**WM\_NOTIFY**](wm-notify.md) is either the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure or the address of a larger structure that includes **NMHDR** as its first member.</span></span> <span data-ttu-id="3134a-128">Die-Struktur enthält den Benachrichtigungs Code und identifiziert das allgemeine Steuerelement, das die Benachrichtigungs Meldung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="3134a-128">The structure contains the notification code and identifies the common control that sent the notification message.</span></span> <span data-ttu-id="3134a-129">Die Bedeutung der übrigen Strukturmember variiert ggf. je nach Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="3134a-129">The meaning of the remaining structure members, if any, varies depending on the notification code.</span></span>

<span data-ttu-id="3134a-130">Jeder Typ von Common Control verfügt über einen entsprechenden Satz von Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="3134a-130">Each type of common control has a corresponding set of notification codes.</span></span> <span data-ttu-id="3134a-131">Die allgemeine Steuerelement Bibliothek bietet auch Benachrichtigungs Codes, die von mehreren Typen von allgemeinen Steuerelementen gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3134a-131">The common control library also provides notification codes that can be sent by more than one type of common control.</span></span> <span data-ttu-id="3134a-132">Sehen Sie sich die Dokumentation für das relevante Steuerelement an, um zu bestimmen, welche Benachrichtigungs Codes gesendet werden und welches Format Sie annehmen.</span><span class="sxs-lookup"><span data-stu-id="3134a-132">See the documentation for the control of interest to determine which notification codes it will send and what format they take.</span></span>

<span data-ttu-id="3134a-133">Beispielcode zum Behandeln von WM- [**\_ Benachrichtigungs**](wm-notify.md) Nachrichten finden Sie im Referenz Thema für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3134a-133">For example code showing how to handle [**WM\_NOTIFY**](wm-notify.md) messages, see the reference topic for that message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3134a-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3134a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3134a-135">Allgemeine Steuerungs Referenz</span><span class="sxs-lookup"><span data-stu-id="3134a-135">General Control Reference</span></span>](common-control-reference.md)
</dt> </dl>

 

 
