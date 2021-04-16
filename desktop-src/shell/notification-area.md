---
description: Der Benachrichtigungsbereich ist ein Teil der Taskleiste, der eine temporäre Quelle für Benachrichtigungen und Status bereitstellt.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Benachrichtigungen und Benachrichtigungsbereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344139"
---
# <a name="notifications-and-the-notification-area"></a><span data-ttu-id="a516e-103">Benachrichtigungen und Benachrichtigungsbereich</span><span class="sxs-lookup"><span data-stu-id="a516e-103">Notifications and the Notification Area</span></span>

<span data-ttu-id="a516e-104">Der Benachrichtigungsbereich ist ein Teil der Taskleiste, der eine temporäre Quelle für Benachrichtigungen und Status bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a516e-104">The notification area is a portion of the taskbar that provides a temporary source for notifications and status.</span></span> <span data-ttu-id="a516e-105">Es kann auch verwendet werden, um Symbole für System-und Programm Features anzuzeigen, die auf dem Desktop nicht vorhanden sind, z. b. Akku-, volumesteuer-und Netzwerkstatus.</span><span class="sxs-lookup"><span data-stu-id="a516e-105">It can also be used to display icons for system and program features that have no presence on the desktop, such as battery level, volume control, and network status.</span></span> <span data-ttu-id="a516e-106">Der Benachrichtigungsbereich wurde in der Vergangenheit als Systemleiste oder Statusbereich bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a516e-106">The notification area has been known historically as the system tray or status area.</span></span>

<span data-ttu-id="a516e-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="a516e-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="a516e-108">Richtlinien für Benachrichtigungen und Benachrichtigungsbereich</span><span class="sxs-lookup"><span data-stu-id="a516e-108">Notification and Notification Area Guidelines</span></span>](#notification-and-notification-area-guidelines)
-   [<span data-ttu-id="a516e-109">Erstellen und Anzeigen einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a516e-109">Creating and Displaying a Notification</span></span>](#notifications-and-the-notification-area)
    -   [<span data-ttu-id="a516e-110">Benachrichtigungssymbol hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a516e-110">Add a Notification Icon</span></span>](#add-a-notification-icon)
    -   [<span data-ttu-id="a516e-111">Legen Sie die notisyiendata-Version fest.</span><span class="sxs-lookup"><span data-stu-id="a516e-111">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
    -   [<span data-ttu-id="a516e-112">Definieren von Benachrichtigungs Aussehen und-Inhalten</span><span class="sxs-lookup"><span data-stu-id="a516e-112">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
    -   [<span data-ttu-id="a516e-113">Überprüfen des Benutzer Status</span><span class="sxs-lookup"><span data-stu-id="a516e-113">Check the User Status</span></span>](#check-the-user-status)
    -   [<span data-ttu-id="a516e-114">Anzeigen der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a516e-114">Display the Notification</span></span>](#display-the-notification)
    -   [<span data-ttu-id="a516e-115">Entfernen eines Symbols</span><span class="sxs-lookup"><span data-stu-id="a516e-115">Removing an Icon</span></span>](#removing-an-icon)
-   [<span data-ttu-id="a516e-116">SDK-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a516e-116">SDK Sample</span></span>](#sdk-sample)
-   [<span data-ttu-id="a516e-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a516e-117">Related topics</span></span>](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a><span data-ttu-id="a516e-118">Richtlinien für Benachrichtigungen und Benachrichtigungsbereich</span><span class="sxs-lookup"><span data-stu-id="a516e-118">Notification and Notification Area Guidelines</span></span>

<span data-ttu-id="a516e-119">Informationen zu bewährten Methoden bei der Verwendung von Benachrichtigungen und dem Benachrichtigungsbereich finden Sie in den Abschnitten zu den Benachrichtigungs [-und](../uxguide/mess-notif.md) [Benachrichtigungs Bereichen](../uxguide/winenv-notification.md) der Windows-Interaktions Richtlinien für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a516e-119">See the [Notifications](../uxguide/mess-notif.md) and [Notification Area](../uxguide/winenv-notification.md) sections of the Windows User Experience Interaction Guidelines for best practices in the use of notifications and the notification area.</span></span> <span data-ttu-id="a516e-120">Das Ziel besteht darin, den Benutzer Vorteil durch die angemessene Verwendung von Benachrichtigungen bereitzustellen, ohne dass Sie lästig oder ablenkend sind.</span><span class="sxs-lookup"><span data-stu-id="a516e-120">The goal is to provide user benefit through appropriate use of notifications, without being annoying or distracting.</span></span>

<span data-ttu-id="a516e-121">Der Benachrichtigungsbereich ist nicht für wichtige Informationen vorgesehen, auf die sofort reagiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a516e-121">The notification area is not for critical information that must be acted on immediately.</span></span> <span data-ttu-id="a516e-122">Es ist auch nicht für den schnellen Programm-oder Befehls Zugriff vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a516e-122">It is also not intended for quick program or command access.</span></span> <span data-ttu-id="a516e-123">Ab Windows 7 wird ein Großteil dieser Funktionen am besten über die Task leisten Schaltfläche einer Anwendung erreicht.</span><span class="sxs-lookup"><span data-stu-id="a516e-123">As of Windows 7, much of that functionality is best accomplished through an application's taskbar button.</span></span>

<span data-ttu-id="a516e-124">Windows 7 ermöglicht es Benutzern, alle Benachrichtigungen von einer Anwendung zu unterdrücken, wenn Sie sich entscheiden. durchdachte Benachrichtigungs Entwürfe und-Verwendung wird der Benutzer daher geneigt, die Anwendung weiterhin anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="a516e-124">Windows 7 allows a user to suppress all notifications from an application if they choose, so thoughtful notification design and use will incline the user to allow your application to continue to display them.</span></span> <span data-ttu-id="a516e-125">Benachrichtigungen sind eine Unterbrechung. Stellen Sie sicher, dass Sie den Wert haben.</span><span class="sxs-lookup"><span data-stu-id="a516e-125">Notifications are an interruption; ensure that they are worth it.</span></span>

<span data-ttu-id="a516e-126">Mit Windows 7 wird das Konzept der "stillen Zeit" eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a516e-126">Windows 7 introduces the concept of "quiet time".</span></span> <span data-ttu-id="a516e-127">Die quiet-Zeit wird als erste Stunde definiert, nachdem ein neuer Benutzer sich zum ersten Mal bei seinem Konto anmeldet, oder zum ersten Mal nach einem Betriebssystem Upgrade oder einer Neuinstallation.</span><span class="sxs-lookup"><span data-stu-id="a516e-127">Quiet time is defined as the first hour after a new user logs into his or her account either for the first time or for the first time after an operating system upgrade or clean installation.</span></span> <span data-ttu-id="a516e-128">Diese Zeit wird reserviert, um dem Benutzer die Möglichkeit zu geben, sich mit der neuen Umgebung vertraut zu machen, ohne die Benachrichtigungen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="a516e-128">This time is set aside to allow the user to explore and familiarize themselves with the new environment without the distraction of notifications.</span></span> <span data-ttu-id="a516e-129">Während dieser Zeit sollten die meisten Benachrichtigungen nicht gesendet oder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a516e-129">During this time, most notifications should not be sent or shown.</span></span> <span data-ttu-id="a516e-130">Ausnahmen enthalten Feedback, das der Benutzer als Reaktion auf eine Benutzeraktion erwarten würde, z. b. wenn er ein USB-Gerät einfügt oder ein Dokument druckt.</span><span class="sxs-lookup"><span data-stu-id="a516e-130">Exceptions include feedback that the user would expect to see in response to a user action, such as when he or she plugs in a USB device or prints a document.</span></span> <span data-ttu-id="a516e-131">API-Besonderheiten von bezüglich der stillen Zeit werden weiter unten in diesem Thema erläutert.</span><span class="sxs-lookup"><span data-stu-id="a516e-131">API specifics of regarding quiet time are discussed later in this topic.</span></span>

## <a name="creating-and-displaying-a-notification"></a><span data-ttu-id="a516e-132">Erstellen und Anzeigen einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a516e-132">Creating and Displaying a Notification</span></span>

<span data-ttu-id="a516e-133">In den restlichen Abschnitten dieses Themas wird das grundlegende Verfahren erläutert, das Sie befolgen müssen, um eine Benachrichtigung von Ihrer Anwendung an den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a516e-133">The remaining sections in this topic outline the basic procedure to follow to display a notification from your application to the user.</span></span>

1.  [<span data-ttu-id="a516e-134">Benachrichtigungssymbol hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a516e-134">Add a Notification Icon</span></span>](#add-a-notification-icon)
2.  [<span data-ttu-id="a516e-135">Legen Sie die notisyiendata-Version fest.</span><span class="sxs-lookup"><span data-stu-id="a516e-135">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
3.  [<span data-ttu-id="a516e-136">Definieren von Benachrichtigungs Aussehen und-Inhalten</span><span class="sxs-lookup"><span data-stu-id="a516e-136">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
4.  [<span data-ttu-id="a516e-137">Überprüfen des Benutzer Status</span><span class="sxs-lookup"><span data-stu-id="a516e-137">Check the User Status</span></span>](#check-the-user-status)
5.  [<span data-ttu-id="a516e-138">Anzeigen der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a516e-138">Display the Notification</span></span>](#display-the-notification)
6.  [<span data-ttu-id="a516e-139">Entfernen eines Symbols</span><span class="sxs-lookup"><span data-stu-id="a516e-139">Removing an Icon</span></span>](#removing-an-icon)

### <a name="add-a-notification-icon"></a><span data-ttu-id="a516e-140">Benachrichtigungssymbol hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a516e-140">Add a Notification Icon</span></span>

<span data-ttu-id="a516e-141">Um eine Benachrichtigung anzuzeigen, müssen Sie über ein Symbol im Benachrichtigungsbereich verfügen.</span><span class="sxs-lookup"><span data-stu-id="a516e-141">To display a notification, you must have an icon in the notification area.</span></span> <span data-ttu-id="a516e-142">In bestimmten Fällen, wie z. b. Microsoft Communicator oder Akku Ebene, ist dieses Symbol bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a516e-142">In certain cases, such as Microsoft Communicator or battery level, that icon will already be present.</span></span> <span data-ttu-id="a516e-143">In vielen anderen Fällen fügen Sie jedoch dem Benachrichtigungsbereich nur so lange ein Symbol hinzu, wie es zum Anzeigen der Benachrichtigung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a516e-143">In many other cases, however, you will add an icon to the notification area only as long as is needed to show the notification.</span></span> <span data-ttu-id="a516e-144">In beiden Fällen wird dies mithilfe der [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) -Funktion erreicht.</span><span class="sxs-lookup"><span data-stu-id="a516e-144">In either case, this is accomplished using the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) function.</span></span> <span data-ttu-id="a516e-145">**Shell \_ NotifyIcon** ermöglicht das Hinzufügen, ändern oder Löschen eines Symbols im Benachrichtigungsbereich.</span><span class="sxs-lookup"><span data-stu-id="a516e-145">**Shell\_NotifyIcon** allows you to add, modify, or delete an icon in the notification area.</span></span>

![Benachrichtigungsbereich, der drei Symbole enthält](images/taskbar/notificationareaicons.png)

<span data-ttu-id="a516e-147">Wenn ein Symbol zum Infobereich unter Windows 7 hinzugefügt wird, wird es standardmäßig dem Überlauf Abschnitt des Benachrichtigungs Bereichs hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a516e-147">When an icon is added to the notification area on Windows 7, it is added to the overflow section of the notification area by default.</span></span> <span data-ttu-id="a516e-148">Dieser Bereich enthält Benachrichtigungs Bereichs Symbole, die aktiv sind, aber nicht im Benachrichtigungsbereich sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="a516e-148">This area contains notification area icons that are active, but not visible in the notification area.</span></span> <span data-ttu-id="a516e-149">Nur der Benutzer kann ein Symbol vom Überlauf in den Benachrichtigungsbereich herauf Stufen, obwohl das System unter bestimmten Umständen ein Symbol vorübergehend als kurze Vorschau (in einer Minute) in den Benachrichtigungsbereich herauf Stufen kann.</span><span class="sxs-lookup"><span data-stu-id="a516e-149">Only the user can promote an icon from the overflow to the notification area, although in certain circumstances the system can temporarily promote an icon into the notification area as a short preview (under one minute).</span></span>

> [!Note]  
> <span data-ttu-id="a516e-150">Der Benutzer sollte in seinem Benachrichtigungsbereich das letzte Mal über die gewünschten Symbole verfügen.</span><span class="sxs-lookup"><span data-stu-id="a516e-150">The user should have the final say on which icons they want to see in their notification area.</span></span> <span data-ttu-id="a516e-151">Vor der Installation eines nicht vorübergehenden Symbols im Benachrichtigungsbereich sollte der Benutzer zur Berechtigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a516e-151">Before installing a non-transient icon in the notification area, the user should be asked for permission.</span></span> <span data-ttu-id="a516e-152">Außerdem sollte Ihnen die Option (normalerweise das Kontextmenü) zugewiesen werden, um das Symbol aus dem Benachrichtigungsbereich zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a516e-152">They should also be given the option (normally though its shortcut menu) to remove the icon from the notification area.</span></span>

 

<span data-ttu-id="a516e-153">Die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur, die im aufrufungsshellbenachrichtigungshub gesendet wird, enthält Informationen, die sowohl das Benachrichtigungs Bereichs Symbol als auch die Benachrichtigung selbst angeben. [**\_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)</span><span class="sxs-lookup"><span data-stu-id="a516e-153">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification itself.</span></span> <span data-ttu-id="a516e-154">Die folgenden Elemente sind für das Benachrichtigungs Bereichs Symbol selbst spezifisch, das über **notifyiendata** festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a516e-154">The following are those items specific to the notification area icon itself that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="a516e-155">Die Ressource, aus der das Symbol entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="a516e-155">The resource from which the icon is taken.</span></span>
-   <span data-ttu-id="a516e-156">Ein eindeutiger Bezeichner für das Symbol.</span><span class="sxs-lookup"><span data-stu-id="a516e-156">A unique identifier for the icon.</span></span>
-   <span data-ttu-id="a516e-157">Der Stil der QuickInfo des Symbols.</span><span class="sxs-lookup"><span data-stu-id="a516e-157">The style of the icon's tooltip.</span></span>
-   <span data-ttu-id="a516e-158">Der Zustand des Symbols (ausgeblendet, freigegeben oder beides) im Benachrichtigungsbereich.</span><span class="sxs-lookup"><span data-stu-id="a516e-158">The icon's state (hidden, shared, or both) in the notification area.</span></span>
-   <span data-ttu-id="a516e-159">Das Handle eines Anwendungsfensters, das dem Symbol zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a516e-159">The handle of an application window associated with the icon.</span></span>
-   <span data-ttu-id="a516e-160">Ein Rückruf Nachrichten Bezeichner, der es dem Symbol ermöglicht, Ereignisse, die innerhalb des umgebenden Rechtecks des Symbols auftreten, und die Sprechblasen Benachrichtigung mit dem zugeordneten Anwendungsfenster zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a516e-160">A callback message identifier that allows the icon to communicate events that occur within the icon's bounding rectangle and balloon notification with the associated application window.</span></span> <span data-ttu-id="a516e-161">Das umgebende Rechteck des Symbols kann über die [**Shell \_ notifyicyienrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a516e-161">The icon's bounding rectangle can be retrieved through [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span></span>

<span data-ttu-id="a516e-162">Jedes Symbol im Benachrichtigungsbereich kann auf zwei Arten identifiziert werden:</span><span class="sxs-lookup"><span data-stu-id="a516e-162">Each icon in the notification area can be identified in two ways:</span></span>

-   <span data-ttu-id="a516e-163">Die GUID, mit der das Symbol in der Registrierung deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="a516e-163">The GUID with which the icon is declared in the registry.</span></span> <span data-ttu-id="a516e-164">Dies ist die bevorzugte Methode unter Windows 7 und höher.</span><span class="sxs-lookup"><span data-stu-id="a516e-164">This is the preferred method on Windows 7 and later.</span></span>
-   <span data-ttu-id="a516e-165">Das Handle eines Fensters, das mit dem Symbol für den Benachrichtigungsbereich verknüpft ist, sowie ein Anwendungs definierter Symbol Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a516e-165">The handle of a window associated with the notification area icon, plus an application-defined icon identifier.</span></span> <span data-ttu-id="a516e-166">Diese Methode wird unter Windows Vista und früheren Versionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a516e-166">This method is used on Windows Vista and earlier.</span></span>

<span data-ttu-id="a516e-167">Symbole im Benachrichtigungsbereich können eine QuickInfo aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a516e-167">Icons in the notification area can have a tooltip.</span></span> <span data-ttu-id="a516e-168">Die QuickInfo kann entweder eine Standard-QuickInfo (bevorzugt) oder eine von der Anwendung gezeichnete Popup-Benutzeroberfläche sein.</span><span class="sxs-lookup"><span data-stu-id="a516e-168">The tooltip can be either a standard tooltip (preferred) or an application-drawn, pop-up UI.</span></span> <span data-ttu-id="a516e-169">Eine QuickInfo ist zwar nicht erforderlich, es wird jedoch empfohlen.</span><span class="sxs-lookup"><span data-stu-id="a516e-169">While a tooltip is not required, it is recommended.</span></span>

<span data-ttu-id="a516e-170">Benachrichtigungs Bereichs Symbole sollten hoch dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="a516e-170">Notification area icons should be high-DPI aware.</span></span> <span data-ttu-id="a516e-171">Eine Anwendung sollte sowohl ein 16x16-Pixel-Symbol als auch ein 32 x 32-Symbol in der Ressourcen Datei bereitstellen. verwenden Sie dann [**loadiinmetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) , um sicherzustellen, dass das korrekte Symbol geladen und entsprechend skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="a516e-171">An application should provide both a 16x16 pixel icon and a 32x32 icon in its resource file, and then use [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) to ensure that the correct icon is loaded and scaled appropriately.</span></span>

<span data-ttu-id="a516e-172">Die Anwendung, die für das Benachrichtigungs Bereichs Symbol zuständig ist, sollte für dieses Symbol einen Mausklick verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a516e-172">The application responsible for the notification area icon should handle a mouse click for that icon.</span></span> <span data-ttu-id="a516e-173">Wenn ein Benutzer mit der rechten Maustaste auf das Symbol klickt, sollte ein normales Kontextmenü angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a516e-173">When a user right-clicks the icon, it should bring up a normal shortcut menu.</span></span> <span data-ttu-id="a516e-174">Das Ergebnis eines einzelnen Klicks mit der linken Maustaste unterscheidet sich jedoch von der Funktion des Symbols.</span><span class="sxs-lookup"><span data-stu-id="a516e-174">However, the result of a single click with the left mouse button will vary with the function of the icon.</span></span> <span data-ttu-id="a516e-175">Es sollte angezeigt werden, was der Benutzer in dem Formular sehen würde, das sich am besten für diesen Inhalt eignet – ein Popup Fenster, ein Dialogfeld oder das Programmfenster selbst.</span><span class="sxs-lookup"><span data-stu-id="a516e-175">It should display what the user would expect to see in the form best suited to that content—a popup window, a dialog box or the program window itself.</span></span> <span data-ttu-id="a516e-176">Beispielsweise kann der Status Text für ein Statussymbol oder ein Schieberegler für das volumesteuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a516e-176">For instance, it could show status text for a status icon, or a slider for the volume control.</span></span>

<span data-ttu-id="a516e-177">Die Platzierung eines Popup Fensters oder eines Dialog Felds, das sich aus dem Klick ergibt, sollte sich in der Nähe der Koordinaten des Click im Benachrichtigungsbereich befinden.</span><span class="sxs-lookup"><span data-stu-id="a516e-177">The placement of a popup window or dialog box that results from the click should be placed near the coordinate of the click in the notification area.</span></span> <span data-ttu-id="a516e-178">Verwenden Sie [**calculatepopupwindowposition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) , um den Speicherort zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a516e-178">Use the [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) to determine its location.</span></span>

<span data-ttu-id="a516e-179">Das Symbol kann dem Benachrichtigungsbereich hinzugefügt werden, ohne dass eine Benachrichtigung angezeigt wird, indem nur die Symbol spezifischen Member von [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) definiert werden (oben erläutert) und die [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufgerufen wird, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="a516e-179">The icon can be added to the notification area without displaying a notification by defining only the icon-specific members of [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discussed above) and calling [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) as shown here:</span></span>


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



<span data-ttu-id="a516e-180">Sie können das Symbol auch dem Benachrichtigungsbereich hinzufügen und eine Benachrichtigung in einem einzigen aufrufsbenachrichtigungs-Befehl [**anzeigen. \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)</span><span class="sxs-lookup"><span data-stu-id="a516e-180">You can also add the icon to the notification area and display a notification all in one call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="a516e-181">Fahren Sie zu diesem Zweck mit den Anweisungen in diesem Thema fort.</span><span class="sxs-lookup"><span data-stu-id="a516e-181">To do so, continue with the instructions in this topic.</span></span>

### <a name="define-the-notifyicondata-version"></a><span data-ttu-id="a516e-182">Legen Sie die notisyiendata-Version fest.</span><span class="sxs-lookup"><span data-stu-id="a516e-182">Define the NOTIFYICONDATA Version</span></span>

<span data-ttu-id="a516e-183">Wenn Windows fortgeschritten ist, wurde die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur erweitert, sodass Sie mehr Mitglieder enthält, um mehr Funktionalität zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a516e-183">As Windows has progressed, the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure has expanded to include more members to define more functionality.</span></span> <span data-ttu-id="a516e-184">Konstanten werden verwendet, um zu deklarieren, welche Version von **notifyiendata** mit dem Benachrichtigungs Bereichs Symbol verwendet werden soll, um Abwärtskompatibilität zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a516e-184">Constants are used to declare which version of **NOTIFYICONDATA** to use with your notification area icon, to allow for backward compatibility.</span></span> <span data-ttu-id="a516e-185">Es wird dringend empfohlen, dass Sie die Version 4 der NotifyIcon \_ Version \_ 4 verwenden, die in Windows Vista eingeführt wurde, es sei denn, es gibt einen überzeugenden Grund dafür.</span><span class="sxs-lookup"><span data-stu-id="a516e-185">Unless there is a compelling reason to do otherwise, it is strongly recommended that you use the NOTIFYICON\_VERSION\_4 version, introduced in Windows Vista.</span></span> <span data-ttu-id="a516e-186">Diese Version bietet die vollständige verfügbare Funktionalität, einschließlich der bevorzugten Fähigkeit, das Benachrichtigungs Bereichs Symbol, aber eine registrierte GUID, einen übergeordneten Rückrufmechanismus und eine bessere Barrierefreiheit zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a516e-186">This version provides the full available functionality, including the preferred ability to identify the notification area icon though a registered GUID, a superior callback mechanism, and better accessibility.</span></span>

<span data-ttu-id="a516e-187">Legen Sie die Version mit den folgenden Aufrufen fest:</span><span class="sxs-lookup"><span data-stu-id="a516e-187">Set the version through the following calls:</span></span>


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



<span data-ttu-id="a516e-188">Beachten Sie, dass beim Aufrufen von [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) keine Benachrichtigung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a516e-188">Note that this call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) does not display a notification.</span></span>

### <a name="define-the-notification-look-and-contents"></a><span data-ttu-id="a516e-189">Definieren von Benachrichtigungs Aussehen und-Inhalten</span><span class="sxs-lookup"><span data-stu-id="a516e-189">Define the Notification Look and Contents</span></span>

<span data-ttu-id="a516e-190">Eine Benachrichtigung ist eine besondere Art von QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a516e-190">A notification is a special type of balloon tooltip control.</span></span> <span data-ttu-id="a516e-191">Sie enthält einen Titel, Textkörper und ein Symbol.</span><span class="sxs-lookup"><span data-stu-id="a516e-191">It contains a title, body text, and an icon.</span></span> <span data-ttu-id="a516e-192">Ebenso wie ein Fenster befindet sich die Schaltfläche **Schließen** in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="a516e-192">Like a window, it has a **Close** button in its upper right corner.</span></span> <span data-ttu-id="a516e-193">Sie enthält auch eine **options** Schaltfläche, die das Info Bereichs Symbol-Element in der Systemsteuerung öffnet, das es dem Benutzer ermöglicht, das Symbol anzuzeigen oder auszublenden oder nur Benachrichtigungen ohne Symbol anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a516e-193">It also contains a **Options** button that opens the Notification Area Icons item in the Control Panel, which allows the user to show or hide the icon or show only notifications without an icon.</span></span>

![Screenshot der Benachrichtigungs Sprechblase, die anzeigt, dass die Stromversorgung gering ist](images/taskbar/notificationballoon.png)

<span data-ttu-id="a516e-195">Die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur, die im aufrufungsshellbenachrichtigungshub gesendet wird, enthält Informationen, die sowohl das Benachrichtigungs Bereichs Symbol als auch die Benachrichtigungs Sprechblase selbst angeben. [**\_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)</span><span class="sxs-lookup"><span data-stu-id="a516e-195">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification balloon itself.</span></span> <span data-ttu-id="a516e-196">Im folgenden finden Sie die für die Benachrichtigung spezifischen Elemente, die über **notifyitendata** festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="a516e-196">The following are those items specific to the notification that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="a516e-197">Ein Symbol, das in der Benachrichtigungs Sprechblase angezeigt wird, die durch den Benachrichtigungstyp angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a516e-197">An icon to display in the notification balloon, which is specified by the notification type.</span></span> <span data-ttu-id="a516e-198">Die Größe des Symbols sowie benutzerdefinierte Symbole können angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a516e-198">The size of the icon can be specified, as well as custom icons.</span></span>
-   <span data-ttu-id="a516e-199">Ein Benachrichtigungs Titel.</span><span class="sxs-lookup"><span data-stu-id="a516e-199">A notification title.</span></span> <span data-ttu-id="a516e-200">Dieser Titel sollte maximal 48 Zeichen lang sein (um die Lokalisierung zu ermöglichen).</span><span class="sxs-lookup"><span data-stu-id="a516e-200">This title should be a maximum of 48 characters long in English (to accommodate localization).</span></span> <span data-ttu-id="a516e-201">Der Titel ist die erste Zeile der Benachrichtigung und wird durch die Verwendung von Schriftart Größe, Farbe und Gewichtung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a516e-201">The title is the first line of the notification, and set apart through the use of font size, color, and weight.</span></span>
-   <span data-ttu-id="a516e-202">Text zur Verwendung im Text der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a516e-202">Text for use in the body of the notification.</span></span> <span data-ttu-id="a516e-203">Dieser Text sollte maximal 200 Zeichen lang sein (um die Lokalisierung zu ermöglichen).</span><span class="sxs-lookup"><span data-stu-id="a516e-203">This text should be a maximum of 200 characters in English (to accommodate localization).</span></span>
-   <span data-ttu-id="a516e-204">Gibt an, ob die Benachrichtigung verworfen werden soll, wenn Sie nicht sofort angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a516e-204">Whether the notification should be discarded if it cannot be displayed immediately.</span></span>
-   <span data-ttu-id="a516e-205">Ein Timeout für die Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a516e-205">A timeout for the notification.</span></span> <span data-ttu-id="a516e-206">Diese Einstellung wird in Windows Vista-Systemen und neueren Systemen zugunsten einer systemweiten Einstellung für das Barrierefreiheits Timeout ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a516e-206">This setting is ignored in Windows Vista and later systems in favor of a system-wide accessibility timeout setting.</span></span>
-   <span data-ttu-id="a516e-207">Gibt an, ob die Benachrichtigung eine Stille Zeit beachten sollte, festgelegt über das Flag " [**NIIF \_ Respect \_ quiet \_ time**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) ".</span><span class="sxs-lookup"><span data-stu-id="a516e-207">Whether the notification should respect quiet time, set through the [**NIIF\_RESPECT\_QUIET\_TIME**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) flag.</span></span>

> [!Note]  
> <span data-ttu-id="a516e-208">Die [**iusernotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) -und [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) -Schnittstellen sind Component Object Model (com)-Wrapper für [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="a516e-208">The [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) and [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) interfaces are Component Object Model (COM) wrappers for [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="a516e-209">Zu diesem Zeitpunkt stellen Sie jedoch nicht die vollständige NotifyIcon- \_ Version \_ 4-Funktionalität bereit, die über **Shell \_ NotifyIcon** direkt verfügbar ist, einschließlich der Verwendung einer GUID, um das Symbol für den Benachrichtigungsbereich zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a516e-209">However, at this time, they do not provide the full NOTIFYICON\_VERSION\_4 functionality available through **Shell\_NotifyIcon** directly, including the use of a GUID to identify the notification area icon.</span></span>

 

### <a name="check-the-user-status"></a><span data-ttu-id="a516e-210">Überprüfen des Benutzer Status</span><span class="sxs-lookup"><span data-stu-id="a516e-210">Check the User Status</span></span>

<span data-ttu-id="a516e-211">Das System verwendet die Funktion " [**shqueryusernotificationstate**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) ", um zu überprüfen, ob sich der Benutzer in der stillen Zeit, vom Computer oder in einem nicht unter brechbaren Zustand wie dem Präsentationsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="a516e-211">The system uses the [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) function is used to check whether the user is in quiet time, away from the computer, or in an uninterruptable state such as Presentation mode.</span></span> <span data-ttu-id="a516e-212">Ob das System Ihre Benachrichtigung anzeigt, hängt von diesem Zustand ab.</span><span class="sxs-lookup"><span data-stu-id="a516e-212">Whether the system displays your notification depends on this state.</span></span>

> [!Note]  
> <span data-ttu-id="a516e-213">Wenn Ihre Anwendung eine benutzerdefinierte Benachrichtigungs Methode verwendet, die [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**iusernotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)oder [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)nicht verwendet, sollte Sie immer explizit [**shqueryusernotificationstate**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) aufrufen, um zu bestimmen, ob die Benutzeroberfläche zu diesem Zeitpunkt angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a516e-213">If your application is using a custom notification method that does not use [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification), or [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), it should always explicitly call [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) to determine whether it should display notification UI at that time.</span></span>

 

<span data-ttu-id="a516e-214">Benachrichtigungen, die gesendet werden, wenn der Benutzer nicht mehr verfügbar ist, werden zur Anzeige in die Warteschlange eingereiht, aber da Sie nicht wissen, wann der Benutzer zurückgibt oder ob die Benachrichtigung zu diesem Zeitpunkt weiterhin gültig ist, sollten Sie die Benachrichtigung später erneut senden.</span><span class="sxs-lookup"><span data-stu-id="a516e-214">Notifications sent when the user is away are queued for display, but because you cannot know when the user will return or whether the notification will still be valid at that time, you might consider resending the notification later.</span></span>

<span data-ttu-id="a516e-215">Während der stillen Zeit gesendete Benachrichtigungen werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a516e-215">Notifications sent during quiet time are discarded unshown.</span></span> <span data-ttu-id="a516e-216">Entwurfs Richtlinien stellen fest, dass alle Benachrichtigungen ignoriert werden können.</span><span class="sxs-lookup"><span data-stu-id="a516e-216">Design guidelines ask that all notifications be ignorable.</span></span> <span data-ttu-id="a516e-217">Sie sollten keine sofortige Benutzeraktion erfordern.</span><span class="sxs-lookup"><span data-stu-id="a516e-217">They should not require immediate user action.</span></span> <span data-ttu-id="a516e-218">Daher ist keine Benachrichtigung so wichtig, dass Sie eine Stille Zeit überschreiben sollte.</span><span class="sxs-lookup"><span data-stu-id="a516e-218">Therefore, no notification is so important that it should override quiet time.</span></span>

### <a name="display-the-notification"></a><span data-ttu-id="a516e-219">Anzeigen der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a516e-219">Display the Notification</span></span>

<span data-ttu-id="a516e-220">Nachdem Sie die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Version festgelegt und die Benachrichtigung in einer **notifyiendata** -Struktur definiert haben, können Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufrufen, um das Symbol anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a516e-220">Once you have set the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) version and defined the notification in a **NOTIFYICONDATA** structure, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to display the icon.</span></span>

-   <span data-ttu-id="a516e-221">Wenn das Benachrichtigungs Bereichs Symbol nicht vorhanden ist, können Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufzurufen, um das Symbol hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a516e-221">If the notification area icon is not present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to add the icon.</span></span> <span data-ttu-id="a516e-222">Dies geschieht sowohl für vorübergehende als auch für nicht vorübergehende Symbole.</span><span class="sxs-lookup"><span data-stu-id="a516e-222">Do this for both transient and non-transient icons.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   <span data-ttu-id="a516e-223">Wenn das Benachrichtigungs Bereichs Symbol bereits vorhanden ist, müssen Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufzurufen, um das Symbol zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a516e-223">If the notification area icon is already present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to modify the icon.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

<span data-ttu-id="a516e-224">Der folgende Code zeigt ein Beispiel für das Festlegen von [**notisyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Daten und das Senden der Daten über die [**\_ shellbenachrichtigung**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="a516e-224">The following code shows an example of setting [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) data and sending it through [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="a516e-225">Beachten Sie, dass in diesem Beispiel das Benachrichtigungssymbol über eine GUID (bevorzugt in Windows 7) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a516e-225">Note that this example identifies the notification icon through a GUID (preferred in Windows 7).</span></span>


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a><span data-ttu-id="a516e-226">Entfernen eines Symbols</span><span class="sxs-lookup"><span data-stu-id="a516e-226">Removing an Icon</span></span>

<span data-ttu-id="a516e-227">So entfernen Sie ein Symbol – Wenn Sie z. b. das Symbol nur vorübergehend hinzugefügt haben, um eine Benachrichtigung zu übertragen – nennen Sie die [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a516e-227">To remove an icon—for instance, when you have only added the icon temporarily to broadcast a notification—call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)as shown here.</span></span> <span data-ttu-id="a516e-228">In diesem-Befehl wird nur eine minimale [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur, die das Symbol identifiziert, benötigt.</span><span class="sxs-lookup"><span data-stu-id="a516e-228">Only a minimal [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure that identifies the icon is needed in this call.</span></span>


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> <span data-ttu-id="a516e-229">Wenn eine Anwendung deinstalliert wird, kann der Benutzer das Benachrichtigungs Bereichs Symbol für bis zu sieben Tage weiterhin als Option auf der Seite "Info Bereichs Symbole" in der Systemsteuerung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a516e-229">When an application is uninstalled, its notification area icon can still appear to the user as an option in the Notification Area Icons page in the Control Panel for up to seven days.</span></span> <span data-ttu-id="a516e-230">Alle Änderungen, die Sie vorgenommen haben, haben jedoch keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="a516e-230">However, any changes made there will have no effect.</span></span>

 

## <a name="sdk-sample"></a><span data-ttu-id="a516e-231">SDK-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a516e-231">SDK Sample</span></span>

<span data-ttu-id="a516e-232">Ein vollständiges Beispiel für die Verwendung von [**Shell \_ notioyicon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)finden Sie unter [notificationicon Sample](samples-notificationicon.md) Sample im Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a516e-232">See the [NotificationIcon Sample](samples-notificationicon.md) sample in the Windows Software Development Kit (SDK) for a full example of the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a516e-233">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a516e-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a516e-234">**Benachrichtigung zur Shell \_**</span><span class="sxs-lookup"><span data-stu-id="a516e-234">**Shell\_NotifyIcon**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[<span data-ttu-id="a516e-235">**Shell \_ notityitrect**</span><span class="sxs-lookup"><span data-stu-id="a516e-235">**Shell\_NotifyIconGetRect**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[<span data-ttu-id="a516e-236">**Notier\data**</span><span class="sxs-lookup"><span data-stu-id="a516e-236">**NOTIFYICONDATA**</span></span>](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[<span data-ttu-id="a516e-237">**Shqueryusernotificationstate**</span><span class="sxs-lookup"><span data-stu-id="a516e-237">**SHQueryUserNotificationState**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[<span data-ttu-id="a516e-238">**Iusernotification**</span><span class="sxs-lookup"><span data-stu-id="a516e-238">**IUserNotification**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[<span data-ttu-id="a516e-239">**IUserNotification2**</span><span class="sxs-lookup"><span data-stu-id="a516e-239">**IUserNotification2**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[<span data-ttu-id="a516e-240">Die Taskleiste</span><span class="sxs-lookup"><span data-stu-id="a516e-240">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="a516e-241">Task leisten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="a516e-241">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
