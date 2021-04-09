---
title: Schaltflächenmeldungen
description: Eine Schaltfläche kann Nachrichten an das übergeordnete Fenster senden, und ein übergeordnetes Fenster kann Nachrichten an eine Schaltfläche Senden.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103734041"
---
# <a name="button-messages"></a><span data-ttu-id="d33d5-103">Schaltflächenmeldungen</span><span class="sxs-lookup"><span data-stu-id="d33d5-103">Button Messages</span></span>

<span data-ttu-id="d33d5-104">Eine Schaltfläche kann Nachrichten an das übergeordnete Fenster senden, und ein übergeordnetes Fenster kann Nachrichten an eine Schaltfläche Senden.</span><span class="sxs-lookup"><span data-stu-id="d33d5-104">A button can send messages to its parent window, and a parent window can send messages to a button.</span></span>

<span data-ttu-id="d33d5-105">Die folgenden Themen werden in diesem Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="d33d5-105">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="d33d5-106">Senden von Nachrichten an Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="d33d5-106">Sending Messages to Buttons</span></span>](#sending-messages-to-buttons)
-   [<span data-ttu-id="d33d5-107">Verarbeiten von Nachrichten über eine Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="d33d5-107">Handling Messages from a Button</span></span>](#handling-messages-from-a-button)
-   [<span data-ttu-id="d33d5-108">Benachrichtigungs Meldungen von Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="d33d5-108">Notification Messages from Buttons</span></span>](#notification-messages-from-buttons)
-   [<span data-ttu-id="d33d5-109">Schaltflächen-Farb Meldungen</span><span class="sxs-lookup"><span data-stu-id="d33d5-109">Button Color Messages</span></span>](#button-color-messages)
-   [<span data-ttu-id="d33d5-110">Schaltfläche Standard Nachrichtenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="d33d5-110">Button Default Message Processing</span></span>](#button-default-message-processing)
-   [<span data-ttu-id="d33d5-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d33d5-111">Related topics</span></span>](#related-topics)

## <a name="sending-messages-to-buttons"></a><span data-ttu-id="d33d5-112">Senden von Nachrichten an Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="d33d5-112">Sending Messages to Buttons</span></span>

<span data-ttu-id="d33d5-113">Ein übergeordnetes Fenster kann mithilfe der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion Meldungen an eine Schaltfläche in einem überlappenden oder untergeordneten Fenster senden oder Nachrichten mithilfe der Funktionen [**SendDlgItemMess**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**checkdlgbutton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**checkradio Button**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)und [**isdlgbuttoncheckan**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) eine Schaltfläche in einem Dialogfeld senden.</span><span class="sxs-lookup"><span data-stu-id="d33d5-113">A parent window can send messages to a button in an overlapped or child window by using the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, or it can send messages to a button in a dialog box by using the [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton), and [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) functions.</span></span>

<span data-ttu-id="d33d5-114">Eine Anwendung kann die [**BM \_ getcheck**](bm-getcheck.md) -Nachricht verwenden, um den Status der Überprüfung eines Kontrollkästchens oder Options Felds abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-114">An application can use the [**BM\_GETCHECK**](bm-getcheck.md) message to retrieve the check state of a check box or radio button.</span></span> <span data-ttu-id="d33d5-115">Eine Anwendung kann auch die [**BM \_ GetState**](bm-getstate.md) -Nachricht verwenden, um die aktuellen Status der Schaltfläche abzurufen (den Prüf Zustand, den pushzustand und den Fokus Zustand).</span><span class="sxs-lookup"><span data-stu-id="d33d5-115">An application can also use the [**BM\_GETSTATE**](bm-getstate.md) message to retrieve the button's current states (the check state, push state, and focus state).</span></span> <span data-ttu-id="d33d5-116">Um Informationen zu einem bestimmten Zustand zu erhalten, verwenden Sie eine Bitmaske für den zurückgegebenen Statuswert.</span><span class="sxs-lookup"><span data-stu-id="d33d5-116">To get information about a specific state, use a bitmask on the returned state value.</span></span>

<span data-ttu-id="d33d5-117">Die [**BM- \_ setcheck**](bm-setcheck.md) -Nachricht legt den Kontrollzustand eines Kontrollkästchens oder Options Felds fest. die Meldung gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d33d5-117">The [**BM\_SETCHECK**](bm-setcheck.md) message sets the check state of a check box or radio button; the message returns zero.</span></span> <span data-ttu-id="d33d5-118">Die [**BM- \_ SetState**](bm-setstate.md) -Meldung legt den pushzustand einer Schaltfläche fest. diese Meldung gibt auch 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d33d5-118">The [**BM\_SETSTATE**](bm-setstate.md) message sets the push state of a button; this message also returns zero.</span></span> <span data-ttu-id="d33d5-119">Die [**BM- \_ SetStyle**](bm-setstyle.md) -Nachricht ändert den Stil einer Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d33d5-119">The [**BM\_SETSTYLE**](bm-setstyle.md) message changes the style of a button.</span></span> <span data-ttu-id="d33d5-120">Er dient zum Ändern von Schaltflächen Formaten innerhalb eines Typs (z. b. Ändern eines Kontrollkästchens in ein automatisches Kontrollkästchen).</span><span class="sxs-lookup"><span data-stu-id="d33d5-120">It is designed for changing button styles within a type (for example, changing a check box to an automatic check box).</span></span> <span data-ttu-id="d33d5-121">Sie ist nicht für die Änderung zwischen Typen (z. b. Ändern eines Kontrollkästchens in ein Optionsfeld) konzipiert.</span><span class="sxs-lookup"><span data-stu-id="d33d5-121">It is not designed for changing between types (for example, changing a check box to a radio button).</span></span> <span data-ttu-id="d33d5-122">Eine Anwendung sollte keine Schaltfläche von einem Typ in einen anderen ändern.</span><span class="sxs-lookup"><span data-stu-id="d33d5-122">An application should not change a button from one type to another.</span></span>

<span data-ttu-id="d33d5-123">Eine Schaltfläche mit dem [**\_ Symbol**](button-styles.md) Stil " [**SB \_ Bitmap**](button-styles.md) " oder "SB" zeigt anstelle von Text eine Bitmap oder ein Symbol an.</span><span class="sxs-lookup"><span data-stu-id="d33d5-123">A button of the [**BS\_BITMAP**](button-styles.md) or [**BS\_ICON**](button-styles.md) style displays a bitmap or icon instead of text.</span></span> <span data-ttu-id="d33d5-124">Die [**BM \_**](bm-setimage.md) -abtader Nachricht verknüpft ein Handle mit einer Schaltfläche zu einer Bitmap oder einem Symbol.</span><span class="sxs-lookup"><span data-stu-id="d33d5-124">The [**BM\_SETIMAGE**](bm-setimage.md) message associates a handle to a bitmap or icon with a button.</span></span> <span data-ttu-id="d33d5-125">Die [**BM \_ GetImage**](bm-getimage.md) -Nachricht Ruft ein Handle für das Bitmap oder Symbol ab, das einer Schaltfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d33d5-125">The [**BM\_GETIMAGE**](bm-getimage.md) message retrieves a handle to the bitmap or icon associated with a button.</span></span>

<span data-ttu-id="d33d5-126">Eine Anwendung kann auch die [**DM \_ getdefid-**](/windows/desktop/dlgbox/dm-getdefid) Nachricht verwenden, um den Bezeichner des Standard Steuer Elements der Push-Schaltfläche in einem Dialogfeld abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-126">An application can also use the [**DM\_GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) message to retrieve the identifier of the default push button control in a dialog box.</span></span> <span data-ttu-id="d33d5-127">Eine Anwendung kann die " [**DM \_ setdefid"-**](/windows/desktop/dlgbox/dm-setdefid) Meldung verwenden, um die Standard-pushschaltfläche für ein Dialogfeld festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-127">An application can use the [**DM\_SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) message to set the default push button for a dialog box.</span></span>

<span data-ttu-id="d33d5-128">Das Aufrufen der [**checkdlgbutton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) -oder [**checkradiobutton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) -Funktion entspricht dem Senden einer [**BM- \_ setcheck**](bm-setcheck.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d33d5-128">Calling the [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) or [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) function is equivalent to sending a [**BM\_SETCHECK**](bm-setcheck.md) message.</span></span> <span data-ttu-id="d33d5-129">Das Aufrufen der [**isdlgbuttoncheck-**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) Funktion entspricht dem Senden einer [**BM \_ getcheck**](bm-getcheck.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d33d5-129">Calling the [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) function is equivalent to sending a [**BM\_GETCHECK**](bm-getcheck.md) message.</span></span>

## <a name="handling-messages-from-a-button"></a><span data-ttu-id="d33d5-130">Verarbeiten von Nachrichten über eine Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="d33d5-130">Handling Messages from a Button</span></span>

<span data-ttu-id="d33d5-131">Benachrichtigungen von einer Schaltfläche werden entweder als [**WM- \_ Befehl**](/windows/desktop/menurc/wm-command) oder als [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten gesendet.</span><span class="sxs-lookup"><span data-stu-id="d33d5-131">Notifications from a button are sent as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="d33d5-132">Informationen dazu, welche Nachricht verwendet wird, finden Sie auf der Referenzseite für jede Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="d33d5-132">Information about which message is used can be found on the reference page for each notification.</span></span>

<span data-ttu-id="d33d5-133">Weitere Informationen zum Verarbeiten von Nachrichten finden Sie unter [Control Messages](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d33d5-133">For more information on how to handle messages, see [Control Messages](control-messages.md).</span></span> <span data-ttu-id="d33d5-134">Siehe auch Schaltflächen Meldungen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-134">See also Button Messages.</span></span>

## <a name="notification-messages-from-buttons"></a><span data-ttu-id="d33d5-135">Benachrichtigungs Meldungen von Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="d33d5-135">Notification Messages from Buttons</span></span>

<span data-ttu-id="d33d5-136">Wenn der Benutzer auf eine Schaltfläche klickt, wird der Status geändert, und die Schaltfläche sendet Benachrichtigungs Codes in Form von [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen an das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="d33d5-136">When the user clicks a button, its state changes, and the button sends notification codes, in the form of [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages, to its parent window.</span></span> <span data-ttu-id="d33d5-137">Beispielsweise sendet ein Push-Schaltflächen-Steuerelement den auf der Benutzer auf die Schaltfläche [ \_ angeklickten](bn-clicked.md) Wert der Milliarde.</span><span class="sxs-lookup"><span data-stu-id="d33d5-137">For example, a push button control sends the [BN\_CLICKED](bn-clicked.md) notification code whenever the user chooses the button.</span></span> <span data-ttu-id="d33d5-138">In allen Fällen (mit Ausnahme von [BCN- \_ betitemchange](bcn-hotitemchange.md)) enthält das nieder wertige Wort des *wParam* -Parameters den Steuerelement Bezeichner, das hochwertige Wort von *wParam* enthält den Benachrichtigungs Code, und der *LPARAM* -Parameter enthält das Steuerelement Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="d33d5-138">In all cases (except for [BCN\_HOTITEMCHANGE](bcn-hotitemchange.md)), the low-order word of the *wParam* parameter contains the control identifier, the high-order word of *wParam* contains the notification code, and the *lParam* parameter contains the control window handle.</span></span>

<span data-ttu-id="d33d5-139">Sowohl die Nachricht als auch die Antwort des übergeordneten Fensters hängen vom Typ, Format und aktuellen Zustand der Schaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="d33d5-139">Both the message and the parent window's response depend on the type, style, and current state of the button.</span></span> <span data-ttu-id="d33d5-140">Im folgenden sind die Schaltflächen-Benachrichtigungs Codes, die eine Anwendung überwachen und verarbeiten soll</span><span class="sxs-lookup"><span data-stu-id="d33d5-140">Following are the button notification codes an application should monitor and process.</span></span>



| <span data-ttu-id="d33d5-141">Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d33d5-141">Notification code</span></span>                                                        | <span data-ttu-id="d33d5-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d33d5-142">Description</span></span>                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d33d5-143">BCN- \_ hubänderung</span><span class="sxs-lookup"><span data-stu-id="d33d5-143">BCN\_HOTITEMCHANGE</span></span>](bcn-hotitemchange.md)                              | <span data-ttu-id="d33d5-144">Die Maus hat den Client Bereich einer Schaltfläche eingegeben oder verlassen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-144">The mouse entered or left the client area of a button.</span></span> |
| [<span data-ttu-id="d33d5-145">auf BN \_ geklickt</span><span class="sxs-lookup"><span data-stu-id="d33d5-145">BN\_CLICKED</span></span>](bn-clicked.md)                                            | <span data-ttu-id="d33d5-146">Der Benutzer hat auf eine Schaltfläche geklickt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-146">The user clicked a button.</span></span>                             |
| <span data-ttu-id="d33d5-147">[BN \_ Dblclk](bn-dblclk.md) oder [BN- \_ Doppel](bn-doubleclicked.md) Klick</span><span class="sxs-lookup"><span data-stu-id="d33d5-147">[BN\_DBLCLK](bn-dblclk.md) or [BN\_DOUBLECLICKED](bn-doubleclicked.md)</span></span> | <span data-ttu-id="d33d5-148">Der Benutzer hat auf eine Schaltfläche Doppel geklickt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-148">The user double-clicked a button.</span></span>                      |
| [<span data-ttu-id="d33d5-149">BN \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="d33d5-149">BN\_DISABLE</span></span>](bn-disable.md)                                            | <span data-ttu-id="d33d5-150">Eine Schaltfläche ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d33d5-150">A button is disabled.</span></span>                                  |
| <span data-ttu-id="d33d5-151">[BN \_ Per pushübertragung](bn-pushed.md) oder [Milliarde \_ Hilite](bn-hilite.md)</span><span class="sxs-lookup"><span data-stu-id="d33d5-151">[BN\_PUSHED](bn-pushed.md) or [BN\_HILITE](bn-hilite.md)</span></span>               | <span data-ttu-id="d33d5-152">Der Benutzer hat eine Schaltfläche gedrückt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-152">The user pushed a button.</span></span>                              |
| [<span data-ttu-id="d33d5-153">BN- \_ killfokus</span><span class="sxs-lookup"><span data-stu-id="d33d5-153">BN\_KILLFOCUS</span></span>](bn-killfocus.md)                                        | <span data-ttu-id="d33d5-154">Die Schaltfläche hat den Tastaturfokus verloren.</span><span class="sxs-lookup"><span data-stu-id="d33d5-154">The button lost the keyboard focus.</span></span>                    |
| [<span data-ttu-id="d33d5-155">BN- \_ Paint</span><span class="sxs-lookup"><span data-stu-id="d33d5-155">BN\_PAINT</span></span>](bn-paint.md)                                                | <span data-ttu-id="d33d5-156">Die Schaltfläche sollte gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d33d5-156">The button should be painted.</span></span>                          |
| [<span data-ttu-id="d33d5-157">BN- \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="d33d5-157">BN\_SETFOCUS</span></span>](bn-setfocus.md)                                          | <span data-ttu-id="d33d5-158">Die Schaltfläche hat den Tastaturfokus erhalten.</span><span class="sxs-lookup"><span data-stu-id="d33d5-158">The button gained the keyboard focus.</span></span>                  |
| <span data-ttu-id="d33d5-159">[BN \_ Nicht per pushübertragung](bn-unpushed.md) oder [Milliarde \_ unhilite](bn-unhilite.md)</span><span class="sxs-lookup"><span data-stu-id="d33d5-159">[BN\_UNPUSHED](bn-unpushed.md) or [BN\_UNHILITE](bn-unhilite.md)</span></span>       | <span data-ttu-id="d33d5-160">Die Schaltfläche wird nicht mehr per pushübertragung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-160">The button is no longer pushed.</span></span>                        |



 

<span data-ttu-id="d33d5-161">Mit einer Schaltfläche werden die Benachrichtigungs Codes " [BN \_ deaktiviert](bn-disable.md)", " [BN \_ gepusht](bn-pushed.md)", " [BN- \_ killfocus](bn-killfocus.md)", "bn [ \_ Paint](bn-paint.md)", " [BN \_ SetFocus](bn-setfocus.md)" und " [BN \_](bn-unpushed.md) " nur dann gesendet, [**Wenn die \_**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="d33d5-161">A button sends the [BN\_DISABLE](bn-disable.md), [BN\_PUSHED](bn-pushed.md), [BN\_KILLFOCUS](bn-killfocus.md), [BN\_PAINT](bn-paint.md), [BN\_SETFOCUS](bn-setfocus.md), and [BN\_UNPUSHED](bn-unpushed.md) notification codes only if it has the [**BS\_NOTIFY**](button-styles.md) style.</span></span> <span data-ttu-id="d33d5-162">[BN \_ Dblclk](bn-dblclk.md) -Benachrichtigungs Codes werden automatisch für die Schaltflächen " [**\_ Benutzer Schaltfläche**](button-styles.md)", " [**SB- \_ RadioButton**](button-styles.md)" und " [**b \_**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="d33d5-162">[BN\_DBLCLK](bn-dblclk.md) notification codes are sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="d33d5-163">Andere Schaltflächen Typen senden \_ nur dann eine Milliarde dblclk, wenn Sie über das Format "Schriftarten **\_ Benachrichtigen** " verfügen</span><span class="sxs-lookup"><span data-stu-id="d33d5-163">Other button types send BN\_DBLCLK only if they have the **BS\_NOTIFY** style.</span></span> <span data-ttu-id="d33d5-164">Alle Schaltflächen senden den von der [Milliarde \_ angeklickten](bn-clicked.md) Benachrichtigungs Code unabhängig von den Schaltflächen Stilen</span><span class="sxs-lookup"><span data-stu-id="d33d5-164">All buttons send the [BN\_CLICKED](bn-clicked.md) notification code regardless of their button styles.</span></span>

<span data-ttu-id="d33d5-165">Für automatische Schaltflächen ändert das System den pushzustand und zeichnet die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d33d5-165">For automatic buttons, the system changes the push state and paints the button.</span></span> <span data-ttu-id="d33d5-166">In diesem Fall [verarbeitet die Anwendung \_ ](bn-clicked.md) i. [d. d. \_ d](bn-dblclk.md) . a</span><span class="sxs-lookup"><span data-stu-id="d33d5-166">In this case, the application typically processes only the [BN\_CLICKED](bn-clicked.md) and [BN\_DBLCLK](bn-dblclk.md) notification codes.</span></span> <span data-ttu-id="d33d5-167">Für Schaltflächen, die nicht automatisch sind, antwortet die Anwendung in der Regel auf den Benachrichtigungs Code, indem eine Nachricht gesendet wird, um den Zustand der Schaltfläche zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d33d5-167">For buttons that are not automatic, the application typically responds to the notification code by sending a message to change the state of the button.</span></span> <span data-ttu-id="d33d5-168">Informationen zum Senden von Nachrichten an Schaltflächen finden Sie unter [Senden von Nachrichten an Schalt](#sending-messages-to-buttons)Flächen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-168">For information about sending messages to buttons, see [Sending Messages to Buttons](#sending-messages-to-buttons).</span></span>

<span data-ttu-id="d33d5-169">Wenn der Benutzer eine vom Besitzer gezeichnete Schaltfläche auswählt, sendet die Schaltfläche seinem übergeordneten Fenster eine [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht, die den Bezeichner des Steuer Elements enthält, das gezeichnet werden soll, sowie Informationen zu den Dimensionen und dem Zustand</span><span class="sxs-lookup"><span data-stu-id="d33d5-169">When the user selects an owner-drawn button, the button sends its parent window a [**WM\_DRAWITEM**](wm-drawitem.md) message containing the identifier of the control to be drawn and information about its dimensions and state.</span></span>

## <a name="button-color-messages"></a><span data-ttu-id="d33d5-170">Schaltflächen-Farb Meldungen</span><span class="sxs-lookup"><span data-stu-id="d33d5-170">Button Color Messages</span></span>

<span data-ttu-id="d33d5-171">Das System stellt Standard Farbwerte für Schaltflächen bereit.</span><span class="sxs-lookup"><span data-stu-id="d33d5-171">The system provides default color values for buttons.</span></span> <span data-ttu-id="d33d5-172">Eine Anwendung kann die Standardwerte für diese Farben abrufen, indem Sie die [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) -Funktion aufruft, oder die Werte durch Aufrufen der Funktion [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) festlegen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-172">An application can retrieve the default values for these colors by calling the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) function, or set the values by calling the [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) function.</span></span> <span data-ttu-id="d33d5-173">In der folgenden Tabelle werden die Standardwerte für die Schaltflächen Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-173">The following table shows the default button-color values.</span></span>



| <span data-ttu-id="d33d5-174">Wert</span><span class="sxs-lookup"><span data-stu-id="d33d5-174">Value</span></span>               | <span data-ttu-id="d33d5-175">Farbiges Element</span><span class="sxs-lookup"><span data-stu-id="d33d5-175">Element colored</span></span>                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d33d5-176">Farbe ( \_ btnface)</span><span class="sxs-lookup"><span data-stu-id="d33d5-176">COLOR\_BTNFACE</span></span>      | <span data-ttu-id="d33d5-177">Schaltflächen Flächen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-177">Button faces.</span></span>                                                                                                              |
| <span data-ttu-id="d33d5-178">Farbe \_ btnhervorhebung</span><span class="sxs-lookup"><span data-stu-id="d33d5-178">COLOR\_BTNHIGHLIGHT</span></span> | <span data-ttu-id="d33d5-179">Markieren Sie den Bereich (die oberen und linken Kanten) einer Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d33d5-179">Highlight area (the top and left edges) of a button.</span></span>                                                                       |
| <span data-ttu-id="d33d5-180">Farbe \_ btnshadow</span><span class="sxs-lookup"><span data-stu-id="d33d5-180">COLOR\_BTNSHADOW</span></span>    | <span data-ttu-id="d33d5-181">Der Schattenbereich (der untere und der Rechte Rand) einer Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d33d5-181">Shadow area (the bottom and right edges) of a button.</span></span>                                                                      |
| <span data-ttu-id="d33d5-182">Farbe \_ btntext</span><span class="sxs-lookup"><span data-stu-id="d33d5-182">COLOR\_BTNTEXT</span></span>      | <span data-ttu-id="d33d5-183">Regulärer (nicht ausgegrauter) Text in Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-183">Regular (nongrayed) text in buttons.</span></span>                                                                                       |
| <span data-ttu-id="d33d5-184">Farbe \_ grau Text</span><span class="sxs-lookup"><span data-stu-id="d33d5-184">COLOR\_GRAYTEXT</span></span>     | <span data-ttu-id="d33d5-185">Deaktivierter (grauer) Text in Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-185">Disabled (gray) text in buttons.</span></span> <span data-ttu-id="d33d5-186">Diese Farbe wird auf 0 festgelegt, wenn der aktuelle Anzeigetreiber keine ausgefüllte graue Farbe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-186">This color is set to 0 if the current display driver does not support a solid gray color.</span></span> |
| <span data-ttu-id="d33d5-187">Farb \_ Fenster</span><span class="sxs-lookup"><span data-stu-id="d33d5-187">COLOR\_WINDOW</span></span>       | <span data-ttu-id="d33d5-188">Fenster Hintergründe.</span><span class="sxs-lookup"><span data-stu-id="d33d5-188">Window backgrounds.</span></span>                                                                                                        |
| <span data-ttu-id="d33d5-189">Color \_ WindowFrame</span><span class="sxs-lookup"><span data-stu-id="d33d5-189">COLOR\_WINDOWFRAME</span></span>  | <span data-ttu-id="d33d5-190">Fensterrahmen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-190">Window frames.</span></span>                                                                                                             |
| <span data-ttu-id="d33d5-191">\_WindowText-Farbe</span><span class="sxs-lookup"><span data-stu-id="d33d5-191">COLOR\_WINDOWTEXT</span></span>   | <span data-ttu-id="d33d5-192">Text in Windows.</span><span class="sxs-lookup"><span data-stu-id="d33d5-192">Text in windows.</span></span>                                                                                                           |



 

<span data-ttu-id="d33d5-193">Allerdings wirkt sich das Aufrufen von [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) auf alle Anwendungen aus. Daher sollten Sie diese Funktion nicht aufrufen, um die Schaltflächen für die Anwendung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-193">However, calling [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affects all applications, so you should not call this function to customize buttons for your application.</span></span>

<span data-ttu-id="d33d5-194">Das System sendet eine [**WM \_ ctlcolorbtn**](wm-ctlcolorbtn.md) -Meldung an das übergeordnete Fenster einer Schaltfläche, bevor eine Schaltfläche gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d33d5-194">The system sends a [**WM\_CTLCOLORBTN**](wm-ctlcolorbtn.md) message to a button's parent window before drawing a button.</span></span> <span data-ttu-id="d33d5-195">Diese Meldung enthält ein Handle für den Gerätekontext der Schaltfläche und ein Handle für das untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="d33d5-195">This message contains a handle to the button's device context and a handle to the child window.</span></span> <span data-ttu-id="d33d5-196">Das übergeordnete Fenster kann diese Handles verwenden, um die Text-und Hintergrundfarben der Schaltfläche zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d33d5-196">The parent window can use these handles to change the button's text and background colors.</span></span> <span data-ttu-id="d33d5-197">Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das die Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d33d5-197">However, only owner-drawn buttons respond to the parent window processing the message.</span></span>

## <a name="button-default-message-processing"></a><span data-ttu-id="d33d5-198">Schaltfläche Standard Nachrichtenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="d33d5-198">Button Default Message Processing</span></span>

<span data-ttu-id="d33d5-199">Die Fenster Prozedur für die vordefinierte Schaltflächen Steuerelement-Fenster Klasse führt die Standard Verarbeitung für alle Meldungen aus, die von der Schaltflächen-Steuerelement Prozedur nicht verarbeitet werden</span><span class="sxs-lookup"><span data-stu-id="d33d5-199">The window procedure for the predefined button control window class carries out default processing for all messages that the button control procedure does not process.</span></span> <span data-ttu-id="d33d5-200">Wenn die Schaltflächen-Steuerelement Prozedur für jede Nachricht **false** zurückgibt, prüft die vordefinierte Fenster Prozedur die Nachrichten und führt die in der folgenden Tabelle aufgeführten Standard Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="d33d5-200">When the button control procedure returns **FALSE** for any message, the predefined window procedure checks the messages and performs the default actions listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d33d5-201">`Message`</span><span class="sxs-lookup"><span data-stu-id="d33d5-201">Message</span></span></th>
<th><span data-ttu-id="d33d5-202">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="d33d5-202">Default action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d33d5-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-204">Sendet die Schaltfläche a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> und eine <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> Meldung und sendet dem übergeordneten Fenster einen <a href="bn-clicked.md">BN_CLICKED</a> Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="d33d5-204">Sends the button a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> and a <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> message, and sends the parent window a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-206">Gibt den Prüf Zustand der Schaltfläche zurück.</span><span class="sxs-lookup"><span data-stu-id="d33d5-206">Returns the check state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-208">Gibt ein Handle für das Bitmap oder Symbol zurück, das der Schaltfläche zugeordnet ist, oder <strong>null</strong> , wenn die Schaltfläche keine Bitmap oder ein Symbol aufweist.</span><span class="sxs-lookup"><span data-stu-id="d33d5-208">Returns a handle to the bitmap or icon associated with the button or <strong>NULL</strong> if the button has no bitmap or icon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-210">Gibt den aktuellen Prüf Zustand, den pushzustand und den Fokus Zustand der Schaltfläche zurück.</span><span class="sxs-lookup"><span data-stu-id="d33d5-210">Returns the current check state, push state, and focus state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-212">Legt den Status der Überprüfung für alle Stile von Options Feldern und Kontrollkästchen fest.</span><span class="sxs-lookup"><span data-stu-id="d33d5-212">Sets the check state for all styles of radio buttons and check boxes.</span></span> <span data-ttu-id="d33d5-213">Wenn der <em>wParam</em> -Parameter für options Felder größer als 0 (null) ist, erhält die Schaltfläche den <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> Stil.</span><span class="sxs-lookup"><span data-stu-id="d33d5-213">If the <em>wParam</em> parameter is greater than zero for radio buttons, the button is given the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> style.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-215">Ordnet die angegebene Bitmap oder das angegebene Symbol Handle der Schaltfläche zu und gibt ein Handle für das vorherige Bitmap oder Symbol zurück.</span><span class="sxs-lookup"><span data-stu-id="d33d5-215">Associates the specified bitmap or icon handle with the button and returns a handle to the previous bitmap or icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-217">Legt den pushzustand der Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="d33d5-217">Sets the push state of the button.</span></span> <span data-ttu-id="d33d5-218">Bei vom Besitzer gezeichneten Schaltflächen wird eine <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> Meldung an das übergeordnete Fenster gesendet, wenn sich der Zustand der Schaltfläche geändert hat.</span><span class="sxs-lookup"><span data-stu-id="d33d5-218">For owner-drawn buttons, a <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message is sent to the parent window if the state of the button has changed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-220">Legt den Schaltflächen Stil fest.</span><span class="sxs-lookup"><span data-stu-id="d33d5-220">Sets the button style.</span></span> <span data-ttu-id="d33d5-221">Wenn das nieder wertige Wort des <em>LPARAM</em> -Parameters <strong>true</strong>ist, wird die Schaltfläche neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d33d5-221">If the low-order word of the <em>lParam</em> parameter is <strong>TRUE</strong>, the button is redrawn.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-223">Prüft ein Kontrollkästchen oder ein automatisches Kontrollkästchen, wenn der Benutzer die Plus-(+) oder gleich (=)-Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-223">Checks a check box or automatic check box when the user presses the plus (+) or equal (=) keys.</span></span> <span data-ttu-id="d33d5-224">Löscht ein Kontrollkästchen oder ein automatisches Kontrollkästchen, wenn der Benutzer die Minus Taste (–) drückt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-224">Clears a check box or automatic check box when the user presses the minus (–) key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-226">Zeichnet die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d33d5-226">Paints the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-228">Löscht den Hintergrund für vom Besitzer gezeichnete Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-228">Erases the background for owner-drawn buttons.</span></span> <span data-ttu-id="d33d5-229">Die Hintergründe anderer Schaltflächen werden als Teil der <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> -und <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> Verarbeitung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d33d5-229">The backgrounds of other buttons are erased as part of the <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> and <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-231">Gibt Werte zurück, die den Typ der Eingabe angeben, die von der Standard Schaltfläche Prozedur verarbeitet wird, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-231">Returns values that indicate the type of input processed by the default button procedure, as shown in the following table.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d33d5-232">Schaltflächen Stil</span><span class="sxs-lookup"><span data-stu-id="d33d5-232">Button style</span></span></th>
<th><span data-ttu-id="d33d5-233">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="d33d5-233">Returns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d33d5-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-235">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d33d5-235">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d33d5-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-239">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d33d5-239">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d33d5-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-243">DLGC_STATIC</span><span class="sxs-lookup"><span data-stu-id="d33d5-243">DLGC_STATIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d33d5-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d33d5-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-249">Gibt ein Handle für die aktuelle Schriftart zurück.</span><span class="sxs-lookup"><span data-stu-id="d33d5-249">Returns a handle to the current font.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-251">Drückt die Schaltfläche, wenn der Benutzer die LEERTASTE drückt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-251">Pushes the button if the user presses the SPACEBAR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-253">Gibt die Maus Aufzeichnung für alle Fälle außer der Tab-Taste frei.</span><span class="sxs-lookup"><span data-stu-id="d33d5-253">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-255">Entfernt das Fokus Rechteck aus einer Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d33d5-255">Removes the focus rectangle from a button.</span></span> <span data-ttu-id="d33d5-256">Für pushschaltflächen und Standard-Push-Schaltflächen wird das Fokus Rechteck ungültig.</span><span class="sxs-lookup"><span data-stu-id="d33d5-256">For push buttons and default push buttons, the focus rectangle is invalidated.</span></span> <span data-ttu-id="d33d5-257">Wenn die Schaltfläche die Maus Aufzeichnung enthält, wird die Erfassung freigegeben, die Schaltfläche wird nicht geklickt, und jeder pushzustand wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-257">If the button has the mouse capture, the capture is released, the button is not clicked, and any push state is removed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-259">Sendet eine <a href="bn-dblclk.md">BN_DBLCLK</a> Benachrichtigungs Codes an das übergeordnete Fenster für options Felder und vom Besitzer gezeichnete Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="d33d5-259">Sends a <a href="bn-dblclk.md">BN_DBLCLK</a> notification code to the parent window for radio buttons and owner-drawn buttons.</span></span> <span data-ttu-id="d33d5-260">Bei anderen Schaltflächen wird ein Doppelklick als <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d33d5-260">For other buttons, a double-click is processed as a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-262">Hebt die Schaltfläche hervor, wenn sich die Position des Mauszeigers innerhalb des Client Rechtecks der Schaltfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="d33d5-262">Highlights the button if the position of the mouse cursor is within the button's client rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-264">Gibt die Maus Aufzeichnung frei, wenn die Schaltfläche die Maus Aufzeichnung aufwies.</span><span class="sxs-lookup"><span data-stu-id="d33d5-264">Releases the mouse capture if the button had the mouse capture.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-266">Führt dieselbe Aktion wie <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>aus, wenn die Schaltfläche die Maus Aufzeichnung aufweist.</span><span class="sxs-lookup"><span data-stu-id="d33d5-266">Performs the same action as <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, if the button has the mouse capture.</span></span> <span data-ttu-id="d33d5-267">Andernfalls wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d33d5-267">Otherwise, no action is performed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-269">Schaltet eine beliebige <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> Schaltfläche in eine Schaltfläche <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d33d5-269">Turns any <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> button into a <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> button.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-271">Gibt "httransparent" zurück, wenn das Schaltflächen-Steuerelement ein Gruppenfeld ist.</span><span class="sxs-lookup"><span data-stu-id="d33d5-271">Returns HTTRANSPARENT, if the button control is a group box.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-273">Zeichnet die Schaltfläche nach Ihrem Stil und dem aktuellen Zustand.</span><span class="sxs-lookup"><span data-stu-id="d33d5-273">Draws the button according to its style and current state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-275">Zeichnet ein Fokus Rechteck auf der Schaltfläche, die den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="d33d5-275">Draws a focus rectangle on the button getting the focus.</span></span> <span data-ttu-id="d33d5-276">Für options Felder und automatische Options Felder wird das übergeordnete Fenster als <a href="bn-clicked.md">BN_CLICKED</a> Benachrichtigungs Code gesendet.</span><span class="sxs-lookup"><span data-stu-id="d33d5-276">For radio buttons and automatic radio buttons, the parent window is sent a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-278">Legt eine neue Schriftart fest und aktualisiert optional das Fenster.</span><span class="sxs-lookup"><span data-stu-id="d33d5-278">Sets a new font and optionally updates the window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33d5-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-280">Legt den Text der Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="d33d5-280">Sets the text of the button.</span></span> <span data-ttu-id="d33d5-281">Im Fall eines Gruppen Felds zeichnet die Meldung den bereits vorhandenen Text, bevor das Gruppenfeld mit dem neuen Text neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d33d5-281">In the case of a group box, the message paints over the preexisting text before repainting the group box with the new text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33d5-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d33d5-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span></span></td>
<td><span data-ttu-id="d33d5-283">Gibt die Maus Aufzeichnung für alle Fälle außer der Tab-Taste frei.</span><span class="sxs-lookup"><span data-stu-id="d33d5-283">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d33d5-284">Die vordefinierte Fenster Prozedur übergibt alle anderen Nachrichten zur Standard Verarbeitung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d33d5-284">The predefined window procedure passes all other messages to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function for default processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d33d5-285">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d33d5-285">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d33d5-286">Steuern von Meldungen</span><span class="sxs-lookup"><span data-stu-id="d33d5-286">Control Messages</span></span>](control-messages.md)
</dt> </dl>

 

 