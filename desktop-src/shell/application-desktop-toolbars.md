---
description: Eine Anwendungs Desktop-Symbolleiste (auch als appbar bezeichnet) ist ein Fenster, das der Windows-Taskleiste ähnelt.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Verwenden von Anwendungs Desktop-Symbolleisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128469"
---
# <a name="using-application-desktop-toolbars"></a><span data-ttu-id="e9712-103">Verwenden von Anwendungs Desktop-Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="e9712-103">Using Application Desktop Toolbars</span></span>

<span data-ttu-id="e9712-104">Eine *Anwendungs Desktop-Symbolleiste* (auch als appbar bezeichnet) ist ein Fenster, das der Windows-Taskleiste ähnelt.</span><span class="sxs-lookup"><span data-stu-id="e9712-104">An *application desktop toolbar* (also called an appbar) is a window that is similar to the Windows taskbar.</span></span> <span data-ttu-id="e9712-105">Er ist an einem Bildschirmrand verankert und enthält in der Regel Schaltflächen, die dem Benutzer einen schnellen Zugriff auf andere Anwendungen und Windows ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e9712-105">It is anchored to an edge of the screen, and it typically contains buttons that give the user quick access to other applications and windows.</span></span> <span data-ttu-id="e9712-106">Das System verhindert, dass andere Anwendungen den von einer appbar verwendeten Desktop Bereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9712-106">The system prevents other applications from using the desktop area used by an appbar.</span></span> <span data-ttu-id="e9712-107">Eine beliebige Anzahl von appbars kann zu einem beliebigen Zeitpunkt auf dem Desktop vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e9712-107">Any number of appbars can exist on the desktop at any given time.</span></span>

<span data-ttu-id="e9712-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="e9712-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e9712-109">Informationen zu Anwendungs Desktop-Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="e9712-109">About Application Desktop Toolbars</span></span>](#about-application-desktop-toolbars)
    -   [<span data-ttu-id="e9712-110">Senden von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e9712-110">Sending Messages</span></span>](#sending-messages)
    -   [<span data-ttu-id="e9712-111">Registrierung</span><span class="sxs-lookup"><span data-stu-id="e9712-111">Registration</span></span>](#registration)
    -   [<span data-ttu-id="e9712-112">Größe und Position von appbar</span><span class="sxs-lookup"><span data-stu-id="e9712-112">Appbar Size and Position</span></span>](#appbar-size-and-position)
    -   [<span data-ttu-id="e9712-113">Anwendungs Desktop-Symbolleisten automatisch ausblenden</span><span class="sxs-lookup"><span data-stu-id="e9712-113">Autohide Application Desktop Toolbars</span></span>](#autohide-application-desktop-toolbars)
    -   [<span data-ttu-id="e9712-114">Appbar-Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="e9712-114">Appbar Notification Messages</span></span>](#appbar-notification-messages)
-   [<span data-ttu-id="e9712-115">Registrieren einer Anwendungs Desktop-Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="e9712-115">Registering an Application Desktop Toolbar</span></span>](#registering-an-application-desktop-toolbar)
-   [<span data-ttu-id="e9712-116">Festlegen der Größe und Position der appbar</span><span class="sxs-lookup"><span data-stu-id="e9712-116">Setting the Appbar Size and Position</span></span>](#setting-the-appbar-size-and-position)
-   [<span data-ttu-id="e9712-117">Verarbeiten von appbar-Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="e9712-117">Processing Appbar Notification Messages</span></span>](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a><span data-ttu-id="e9712-118">Informationen zu Anwendungs Desktop-Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="e9712-118">About Application Desktop Toolbars</span></span>

<span data-ttu-id="e9712-119">Windows bietet eine API, mit der Sie die vom System bereitgestellten appbar-Dienste nutzen können.</span><span class="sxs-lookup"><span data-stu-id="e9712-119">Windows provides an API that lets you take advantage of appbar services provided by the system.</span></span> <span data-ttu-id="e9712-120">Mithilfe der-Dienste wird sichergestellt, dass Anwendungs definierte appbars problemlos miteinander und mit der Taskleiste funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e9712-120">The services help ensure that application-defined appbars operate smoothly with one another and with the taskbar.</span></span> <span data-ttu-id="e9712-121">Das System verwaltet Informationen zu den einzelnen appbars und sendet die appbars-Meldungen, um Sie über Ereignisse zu benachrichtigen, die ihre Größe, Position und Darstellung beeinflussen können.</span><span class="sxs-lookup"><span data-stu-id="e9712-121">The system maintains information about each appbar and sends the appbars messages to notify them about events that can affect their size, position, and appearance.</span></span>

### <a name="sending-messages"></a><span data-ttu-id="e9712-122">Senden von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e9712-122">Sending Messages</span></span>

<span data-ttu-id="e9712-123">Eine Anwendung verwendet einen speziellen Satz von Nachrichten, die als appbar-Meldungen bezeichnet werden, um eine appbar hinzuzufügen oder zu entfernen, die Größe und Position einer appbar festzulegen und Informationen über Größe, Position und Zustand der Taskleiste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e9712-123">An application uses a special set of messages, called appbar messages, to add or remove an appbar, set an appbar's size and position, and retrieve information about the size, position, and state of the taskbar.</span></span> <span data-ttu-id="e9712-124">Zum Senden einer appbar-Nachricht muss eine Anwendung die [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9712-124">To send an appbar message, an application must use the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function.</span></span> <span data-ttu-id="e9712-125">Die Parameter der Funktion enthalten einen Nachrichten Bezeichner, z. b. " [**ABM \_ New**](abm-new.md)", und die Adresse einer [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e9712-125">The function's parameters include a message identifier, such as [**ABM\_NEW**](abm-new.md), and the address of an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="e9712-126">Die Strukturmember enthalten Informationen, die das System benötigt, um die angegebene Nachricht zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e9712-126">The structure members contain information that the system needs to process the given message.</span></span>

<span data-ttu-id="e9712-127">Für jede angegebene appbar-Nachricht verwendet das System einige Member der [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur und ignoriert die anderen.</span><span class="sxs-lookup"><span data-stu-id="e9712-127">For any given appbar message, the system uses some members of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure and ignores the others.</span></span> <span data-ttu-id="e9712-128">Das System verwendet jedoch immer die Member **CBSIZE** und **HWND** , sodass eine Anwendung diese Member für jede appbar-Nachricht ausfüllen muss.</span><span class="sxs-lookup"><span data-stu-id="e9712-128">However, the system always uses the **cbSize** and **hWnd** members, so an application must fill these members for every appbar message.</span></span> <span data-ttu-id="e9712-129">Der **CBSIZE** -Member gibt die Größe der Struktur an, und der **HWND** -Member ist das Handle für das Fenster der appbar.</span><span class="sxs-lookup"><span data-stu-id="e9712-129">The **cbSize** member specifies the size of the structure, and the **hWnd** member is the handle to the appbar's window.</span></span>

<span data-ttu-id="e9712-130">Einige appbar-Meldungen fordern Informationen vom System an.</span><span class="sxs-lookup"><span data-stu-id="e9712-130">Some appbar messages request information from the system.</span></span> <span data-ttu-id="e9712-131">Bei der Verarbeitung dieser Nachrichten kopiert das System die angeforderten Informationen in die [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e9712-131">When processing these messages, the system copies the requested information into the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

### <a name="registration"></a><span data-ttu-id="e9712-132">Registrierung</span><span class="sxs-lookup"><span data-stu-id="e9712-132">Registration</span></span>

<span data-ttu-id="e9712-133">Das System behält eine interne Liste von appbars bei und verwaltet Informationen zu den einzelnen Balken in der Liste.</span><span class="sxs-lookup"><span data-stu-id="e9712-133">The system keeps an internal list of appbars and maintains information about each bar in the list.</span></span> <span data-ttu-id="e9712-134">Das System verwendet die Informationen, um appbars zu verwalten, Dienste für diese auszuführen und Benachrichtigungs Meldungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="e9712-134">The system uses the information to manage appbars, perform services for them, and send them notification messages.</span></span>

<span data-ttu-id="e9712-135">Eine Anwendung muss eine appbar registrieren (d. h., Sie wird der internen Liste hinzugefügt), bevor appbar-Dienste vom System empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="e9712-135">An application must register an appbar (that is, add it to the internal list) before it can receive appbar services from the system.</span></span> <span data-ttu-id="e9712-136">Zum Registrieren einer appbar sendet eine Anwendung die [**\_ neue ABM**](abm-new.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e9712-136">To register an appbar, an application sends the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="e9712-137">Die zugehörige [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur enthält das Handle für das Fenster der appbar und einen Anwendungs definierten Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e9712-137">The accompanying [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure includes the handle to the appbar's window and an application-defined message identifier.</span></span> <span data-ttu-id="e9712-138">Das System verwendet den Nachrichten Bezeichner, um Benachrichtigungs Meldungen an die Fenster Prozedur des appbar-Fensters zu senden.</span><span class="sxs-lookup"><span data-stu-id="e9712-138">The system uses the message identifier to send notification messages to the window procedure of the appbar window.</span></span> <span data-ttu-id="e9712-139">Weitere Informationen finden Sie unter appbar-Benachrichtigungs Meldungen.</span><span class="sxs-lookup"><span data-stu-id="e9712-139">For more information, see Appbar Notification Messages.</span></span>

<span data-ttu-id="e9712-140">Eine Anwendung hebt die Registrierung einer appbar auf, indem Sie die [**ABM- \_ Entfernungs**](abm-remove.md) Meldung sendet.</span><span class="sxs-lookup"><span data-stu-id="e9712-140">An application unregisters an appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="e9712-141">Durch das Aufheben der Registrierung einer appbar wird diese aus der internen Liste der appbars des Systems entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9712-141">Unregistering an appbar removes it from the system's internal list of appbars.</span></span> <span data-ttu-id="e9712-142">Das System sendet keine Benachrichtigungs Meldungen mehr an die appbar oder verhindert, dass andere Anwendungen den von der appbar verwendeten Bildschirmbereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9712-142">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span> <span data-ttu-id="e9712-143">Eine Anwendung sollte vor dem zerstören einer appbar immer **ABM \_ Entfernen** senden.</span><span class="sxs-lookup"><span data-stu-id="e9712-143">An application should always send **ABM\_REMOVE** before destroying an appbar.</span></span>

### <a name="appbar-size-and-position"></a><span data-ttu-id="e9712-144">Größe und Position von appbar</span><span class="sxs-lookup"><span data-stu-id="e9712-144">Appbar Size and Position</span></span>

<span data-ttu-id="e9712-145">Eine Anwendung sollte die Größe und Position einer appbar so festlegen, dass Sie keine Auswirkung auf andere appbars oder die Taskleiste hat.</span><span class="sxs-lookup"><span data-stu-id="e9712-145">An application should set an appbar's size and position so that it does not interfere with any other appbars or the taskbar.</span></span> <span data-ttu-id="e9712-146">Jede appbar muss an einer bestimmten Bildschirm Kante verankert werden, und mehrere appbars können an einer Kante verankert werden.</span><span class="sxs-lookup"><span data-stu-id="e9712-146">Every appbar must be anchored to a particular edge of the screen, and multiple appbars can be anchored to an edge.</span></span> <span data-ttu-id="e9712-147">Wenn eine appbar jedoch am gleichen Rand wie die Taskleiste verankert ist, stellt das System sicher, dass sich die Taskleiste immer am äußersten Rand befindet.</span><span class="sxs-lookup"><span data-stu-id="e9712-147">However, if an appbar is anchored to the same edge as the taskbar, the system ensures that the taskbar is always on the outermost edge.</span></span>

<span data-ttu-id="e9712-148">Zum Festlegen der Größe und Position einer appbar wird von einer Anwendung zunächst ein Bildschirmrand und ein Begrenzungs Rechteck für die appbar vorgeschlagen, indem die [**ABM- \_ querypos**](abm-querypos.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-148">To set the size and position of an appbar, an application first proposes a screen edge and bounding rectangle for the appbar by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="e9712-149">Das System bestimmt, ob ein Teil des Bildschirmbereichs innerhalb des vorgeschlagenen Rechtecks von der Taskleiste oder einer anderen appbar verwendet wird, das Rechteck (falls erforderlich) anpasst und das angepasste Rechteck an die Anwendung zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e9712-149">The system determines whether any part of the screen area within the proposed rectangle is used by the taskbar or another appbar, adjusts the rectangle (if necessary), and returns the adjusted rectangle to the application.</span></span>

<span data-ttu-id="e9712-150">Anschließend sendet die Anwendung die [**ABM- \_ SetPos**](abm-setpos.md) -Nachricht, um das neue Begrenzungs Rechteck für die appbar festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e9712-150">Next, the application sends the [**ABM\_SETPOS**](abm-setpos.md) message to set the new bounding rectangle for the appbar.</span></span> <span data-ttu-id="e9712-151">Auch hier kann das System das Rechteck anpassen, bevor es an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-151">Again, the system may adjust the rectangle before returning it to the application.</span></span> <span data-ttu-id="e9712-152">Aus diesem Grund sollte die Anwendung das angepasste Rechteck verwenden, das von **ABM- \_ SetPos** zurückgegeben wird, um die endgültige Größe und Position festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e9712-152">For this reason, the application should use the adjusted rectangle returned by **ABM\_SETPOS** to set the final size and position.</span></span> <span data-ttu-id="e9712-153">Die Anwendung kann die [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) -Funktion verwenden, um die appbar in die Position zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="e9712-153">The application can use the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="e9712-154">Durch die Verwendung eines zweistufigen Prozesses zum Festlegen der Größe und Position ermöglicht das System der Anwendung das Bereitstellen von zwischen Feedback für den Benutzer während des Verschiebungs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e9712-154">By using a two-step process to set the size and position, the system enables the application to provide intermediate feedback to the user during the move operation.</span></span> <span data-ttu-id="e9712-155">Wenn der Benutzer z. b. eine appbar zieht, zeigt die Anwendung möglicherweise ein schattiertes Rechteck an, das die neue Position anzeigt, bevor die appbar tatsächlich verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-155">For example, if the user drags an appbar, the application might display a shaded rectangle indicating the new position before the appbar actually moves.</span></span>

<span data-ttu-id="e9712-156">Eine Anwendung sollte die Größe und Position der appbar nach der Registrierung festlegen und immer dann, wenn die appbar die [**ABN \_ -Benachrichtigungs**](abn-poschanged.md) Meldung erhält.</span><span class="sxs-lookup"><span data-stu-id="e9712-156">An application should set the size and position of its appbar after registering it and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="e9712-157">Eine appbar empfängt diese Benachrichtigungs Meldung immer dann, wenn eine Änderung in der Größe, Position oder Sichtbarkeit der Taskleiste auftritt und wenn die Größe einer anderen appbar auf der gleichen Seite des Bildschirms geändert, hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-157">An appbar receives this notification message whenever a change occurs in the taskbar's size, position, or visibility state and whenever another appbar on the same side of the screen is resized, added, or removed.</span></span>

<span data-ttu-id="e9712-158">Wenn eine appbar die WM- \_ Aktivierungs Nachricht empfängt, sollte Sie die [**ABM- \_ Aktivierungs**](abm-activate.md) Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="e9712-158">Whenever an appbar receives the WM\_ACTIVATE message, it should send the [**ABM\_ACTIVATE**](abm-activate.md) message.</span></span> <span data-ttu-id="e9712-159">Wenn eine appbar eine "WM \_ Windows Message Message"-Nachricht empfängt, muss Sie auch " [**ABM \_ windowposchge**](abm-windowposchanged.md)" aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e9712-159">Similarly, when an appbar receives a WM\_WINDOWPOSCHANGED message, it must call [**ABM\_WINDOWPOSCHANGED**](abm-windowposchanged.md).</span></span> <span data-ttu-id="e9712-160">Wenn diese Nachrichten gesendet werden, wird sichergestellt, dass das System die z-Reihenfolge der automatisch Ausblend enden appbars am gleichen Rand ordnungsgemäß festlegt.</span><span class="sxs-lookup"><span data-stu-id="e9712-160">Sending these messages ensures that the system properly sets the z-order of any autohide appbars on the same edge.</span></span>

### <a name="autohide-application-desktop-toolbars"></a><span data-ttu-id="e9712-161">Anwendungs Desktop-Symbolleisten automatisch ausblenden</span><span class="sxs-lookup"><span data-stu-id="e9712-161">Autohide Application Desktop Toolbars</span></span>

<span data-ttu-id="e9712-162">Eine appbar zum automatischen Ausblenden ist eine, die normalerweise ausgeblendet ist, aber sichtbar wird, wenn der Benutzer den Mauszeiger auf den Bildschirmrand bewegt, dem die appbar zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e9712-162">An autohide appbar is one that is normally hidden but becomes visible when the user moves the mouse cursor to the screen edge with which the appbar is associated.</span></span> <span data-ttu-id="e9712-163">Die appbar verbirgt sich wieder, wenn der Benutzer den Mauszeiger aus dem umgebenden Rechteck des Balkens bewegt.</span><span class="sxs-lookup"><span data-stu-id="e9712-163">The appbar hides itself again when the user moves the mouse cursor out of the bar's bounding rectangle.</span></span>

<span data-ttu-id="e9712-164">Obwohl das System eine Reihe von verschiedenen appbars zu einem beliebigen Zeitpunkt zulässt, lässt es jeweils nur eine automatische Ausblend-appbar für jeden Bildschirmrand zu.</span><span class="sxs-lookup"><span data-stu-id="e9712-164">Although the system allows a number of different appbars at any given time, it allows only one autohide appbar at a time for each screen edge on a first-come, first-served basis.</span></span> <span data-ttu-id="e9712-165">Das System behält automatisch die z-Reihenfolge einer automatischen Ausblend-appbar bei (nur in der z-Reihen folgen Gruppe).</span><span class="sxs-lookup"><span data-stu-id="e9712-165">The system automatically maintains the z-order of an autohide appbar (within its z-order group only).</span></span>

<span data-ttu-id="e9712-166">Eine Anwendung verwendet die [**ABM \_ setaudehidebar**](abm-setautohidebar.md) -Nachricht, um eine automatisch Ausgeblend Bare appbar zu registrieren oder die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="e9712-166">An application uses the [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) message to register or unregister an autohide appbar.</span></span> <span data-ttu-id="e9712-167">Die Meldung gibt den Edge für die appbar und ein Flag an, das angibt, ob die appbar registriert oder die Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9712-167">The message specifies the edge for the appbar and a flag that specifies whether the appbar is to be registered or unregistered.</span></span> <span data-ttu-id="e9712-168">Die Meldung schlägt fehl, wenn eine APP-Leiste zum automatischen Ausblenden registriert wird, aber eine bereits mit dem angegebenen Edge verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e9712-168">The message fails if an autohide appbar is being registered but one is already associated with the specified edge.</span></span> <span data-ttu-id="e9712-169">Eine Anwendung kann das Handle für die automatisch Ausblend Ende appbar abrufen, die einem Edge zugeordnet ist, indem die [**ABM \_ getautohidebar**](abm-getautohidebar.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-169">An application can retrieve the handle to the autohide appbar associated with an edge by sending the [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) message.</span></span>

<span data-ttu-id="e9712-170">Eine APP-Leiste zum automatischen Ausblenden muss nicht als normale appbar registriert werden. Dies bedeutet, dass Sie nicht durch Senden der [**\_ neuen ABM**](abm-new.md) -Nachricht registriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e9712-170">An autohide appbar does not need to register as a normal appbar; that is, it does not need to be registered by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="e9712-171">Eine appbar, die nicht von **ABM \_ neu** registriert ist, überlappt alle an der gleichen Bildschirm Kante verankerten appbars.</span><span class="sxs-lookup"><span data-stu-id="e9712-171">An appbar that is not registered by **ABM\_NEW** overlaps any appbars anchored on the same edge of the screen.</span></span>

### <a name="appbar-notification-messages"></a><span data-ttu-id="e9712-172">Appbar-Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="e9712-172">Appbar Notification Messages</span></span>

<span data-ttu-id="e9712-173">Das System sendet Nachrichten, um eine appbar über Ereignisse zu benachrichtigen, die ihre Position und Darstellung beeinflussen können.</span><span class="sxs-lookup"><span data-stu-id="e9712-173">The system sends messages to notify an appbar about events that can affect its position and appearance.</span></span> <span data-ttu-id="e9712-174">Die Nachrichten werden im Kontext einer Anwendungs definierten Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="e9712-174">The messages are sent in the context of an application-defined message.</span></span> <span data-ttu-id="e9712-175">Die Anwendung gibt den Bezeichner der Nachricht an, wenn Sie die [**\_ neue ABM**](abm-new.md) -Nachricht zum Registrieren der appbar sendet.</span><span class="sxs-lookup"><span data-stu-id="e9712-175">The application specifies the identifier of the message when it sends the [**ABM\_NEW**](abm-new.md) message to register the appbar.</span></span> <span data-ttu-id="e9712-176">Der Benachrichtigungs Code befindet sich im *wParam* -Parameter der von der Anwendung definierten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e9712-176">The notification code is in the *wParam* parameter of the application-defined message.</span></span>

<span data-ttu-id="e9712-177">Eine appbar empfängt die [**ABN \_**](abn-poschanged.md) -Benachrichtigungs Meldung, wenn sich die Größe, Position oder Sichtbarkeit der Taskleiste ändert, wenn eine andere appbar zum gleichen Bildschirmrand hinzugefügt wird oder wenn die Größe einer anderen appbar am gleichen Bildschirmrand geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-177">An appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message when the taskbar's size, position, or visibility state changes, when another appbar is added to the same edge of the screen, or when another appbar on the same edge of the screen is resized or removed.</span></span> <span data-ttu-id="e9712-178">Eine appbar sollte auf diese Benachrichtigungs Meldung reagieren, indem [**ABM \_ querypos**](abm-querypos.md) und [**ABM- \_ SetPos**](abm-setpos.md) -Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9712-178">An appbar should respond to this notification message by sending [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="e9712-179">Wenn sich die Position einer appbar geändert hat, sollte Sie die [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) -Funktion zum Verschieben an die neue Position abrufen.</span><span class="sxs-lookup"><span data-stu-id="e9712-179">If an appbar's position has changed, it should call the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

<span data-ttu-id="e9712-180">Das System sendet die [**ABN \_ StateChange**](abn-statechange.md) -Benachrichtigungs Meldung immer dann, wenn der Zustand "automatisch ausblenden" oder "Always on-Top" der Taskleiste geändert wurde – d. h. wenn der Benutzer das Kontrollkästchen " **Always on-Top** " oder " **automatisch ausblenden** " auf der Eigenschaften Seite der Taskleiste aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9712-180">The system sends the [**ABN\_STATECHANGE**](abn-statechange.md) notification message whenever the taskbar's autohide or always-on-top state has changed—that is, when the user selects or clears the **Always on top** or **Auto hide** check box on the taskbar's property sheet.</span></span> <span data-ttu-id="e9712-181">Eine appbar kann diese Benachrichtigungs Meldung verwenden, um den Status der Taskleiste, wenn gewünscht, auf die Konformität festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e9712-181">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

<span data-ttu-id="e9712-182">Wenn eine Vollbildanwendung gestartet wird oder wenn die letzte Vollbildanwendung geschlossen wird, empfängt eine appbar die [**ABN \_ fullscreenapp**](abn-fullscreenapp.md) -Benachrichtigungs Meldung.</span><span class="sxs-lookup"><span data-stu-id="e9712-182">When a full-screen application is started or when the last full-screen application is closed, an appbar receives the [**ABN\_FULLSCREENAPP**](abn-fullscreenapp.md) notification message.</span></span> <span data-ttu-id="e9712-183">Der *LPARAM* -Parameter gibt an, ob die Vollbildanwendung geöffnet oder geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-183">The *lParam* parameter indicates whether the full-screen application is opening or closing.</span></span> <span data-ttu-id="e9712-184">Wenn Sie geöffnet wird, muss die appbar am Ende der z-Reihenfolge ablegen.</span><span class="sxs-lookup"><span data-stu-id="e9712-184">If it is opening, the appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="e9712-185">Die appbar sollte die Position der z-Reihenfolge wiederherstellen, wenn die letzte Vollbildanwendung geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e9712-185">The appbar should restore its z-order position when the last full-screen application has closed.</span></span>

<span data-ttu-id="e9712-186">Eine appbar empfängt die [**ABN- \_ windowarrange**](abn-windowarrange.md) -Benachrichtigungs Meldung, wenn der Benutzer im Kontextmenü der Taskleiste den vertikal kaskadierten, nebeneinander-oder Kachel Befehl auswählt.</span><span class="sxs-lookup"><span data-stu-id="e9712-186">An appbar receives the [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) notification message when the user selects the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span> <span data-ttu-id="e9712-187">Das System sendet die Nachricht zweimal – vor der Neuanordnung der Fenster (*LPARAM* ist **true**) und nach dem Anordnen der Fenster (*LPARAM* ist **false**).</span><span class="sxs-lookup"><span data-stu-id="e9712-187">The system sends the message two times—before rearranging the windows (*lParam* is **TRUE**) and after arranging the windows (*lParam* is **FALSE**).</span></span>

<span data-ttu-id="e9712-188">Eine appbar kann [**ABN \_ windowarrange**](abn-windowarrange.md) -Nachrichten verwenden, um sich selbst vom kaskadierenden oder Kachel Vorgang auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="e9712-188">An appbar can use [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) messages to exclude itself from the cascade or tile operation.</span></span> <span data-ttu-id="e9712-189">Um sich selbst auszuschließen, sollte die appbar ausgeblendet werden, wenn *LPARAM* den Wert **true** hat, und sich Selbstanzeigen, wenn *LPARAM* den Wert **false** hat.</span><span class="sxs-lookup"><span data-stu-id="e9712-189">To exclude itself, the appbar should hide itself when *lParam* is **TRUE** and show itself when *lParam* is **FALSE**.</span></span> <span data-ttu-id="e9712-190">Wenn eine appbar als Reaktion auf diese Meldung ausgeblendet wird, ist es nicht erforderlich, die [**ABM- \_ querypos**](abm-querypos.md) -und [**ABM- \_ SetPos**](abm-setpos.md) -Nachrichten als Antwort auf den Cascade-oder Tile-Vorgang zu senden.</span><span class="sxs-lookup"><span data-stu-id="e9712-190">If an appbar hides itself in response to this message, it does not need to send the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages in response to the cascade or tile operation.</span></span>

## <a name="registering-an-application-desktop-toolbar"></a><span data-ttu-id="e9712-191">Registrieren einer Anwendungs Desktop-Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="e9712-191">Registering an Application Desktop Toolbar</span></span>

<span data-ttu-id="e9712-192">Eine Anwendung muss eine appbar registrieren, indem Sie die [**\_ neue ABM**](abm-new.md) -Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="e9712-192">An application must register an appbar by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="e9712-193">Beim Registrieren einer appbar wird Sie der internen Liste des Systems hinzugefügt, und dem System wird eine Nachrichten-ID für das Senden von Benachrichtigungs Meldungen an die appbar bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e9712-193">Registering an appbar adds it to the system's internal list and provides the system with a message identifier to use to send notification messages to the appbar.</span></span> <span data-ttu-id="e9712-194">Bevor die Anwendung beendet wird, muss die Registrierung der appbar aufgehoben werden, indem die [**ABM- \_ Entfernungs**](abm-remove.md) Meldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-194">Before exiting, an application must unregister the appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="e9712-195">Durch das Aufheben der Registrierung wird die appbar aus der internen Liste des Systems entfernt und verhindert, dass der Balken appbar-Benachrichtigungs Meldungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="e9712-195">Unregistering removes the appbar from the system's internal list and prevents the bar from receiving appbar notification messages.</span></span>

<span data-ttu-id="e9712-196">Die Funktion im folgenden Beispiel registriert oder hebt die Registrierung einer appbar auf, abhängig vom Wert eines booleschen Flag-Parameters.</span><span class="sxs-lookup"><span data-stu-id="e9712-196">The function in the following example either registers or unregisters an appbar, depending on the value of a Boolean flag parameter.</span></span>


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a><span data-ttu-id="e9712-197">Festlegen der Größe und Position der appbar</span><span class="sxs-lookup"><span data-stu-id="e9712-197">Setting the Appbar Size and Position</span></span>

<span data-ttu-id="e9712-198">Eine Anwendung sollte die Größe und Position einer appbar nach dem Registrieren der appbar festlegen, nachdem der Benutzer die appbar bewegt oder mit der Größe losgt hat und wenn die APP-Leiste die [**ABN \_ -Benachrichtigungs**](abn-poschanged.md) Meldung erhält.</span><span class="sxs-lookup"><span data-stu-id="e9712-198">An application should set an appbar's size and position after registering the appbar, after the user user moves or sizes the appbar, and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="e9712-199">Vor dem Festlegen der Größe und Position der appbar fragt die Anwendung das System nach einem genehmigten umgebenden Rechteck ab, indem die [**ABM \_ querypos**](abm-querypos.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9712-199">Before setting the size and position of the appbar, the application queries the system for an approved bounding rectangle by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="e9712-200">Das System gibt ein umgebenden Rechteck zurück, das die Taskleiste oder andere appbar nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="e9712-200">The system returns a bounding rectangle that does not interfere with the taskbar or any other appbar.</span></span> <span data-ttu-id="e9712-201">Das System passt das Rechteck ausschließlich durch die rechtesubtraktion an; Es wird nicht versucht, die anfängliche Größe des Rechtecks beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e9712-201">The system adjusts the rectangle purely by rectangle subtraction; it makes no effort to preserve the rectangle's initial size.</span></span> <span data-ttu-id="e9712-202">Aus diesem Grund sollte die appbar nach dem Senden von **ABM- \_ querypos** das Rechteck nach Bedarf einlesen.</span><span class="sxs-lookup"><span data-stu-id="e9712-202">For this reason, the appbar should readjust the rectangle, as necessary, after sending **ABM\_QUERYPOS**.</span></span>

<span data-ttu-id="e9712-203">Als nächstes übergibt die Anwendung das umgebende Rechteck mithilfe der [**ABM- \_ SetPos**](abm-setpos.md) -Nachricht an das System zurück.</span><span class="sxs-lookup"><span data-stu-id="e9712-203">Next, the application passes the bounding rectangle back to the system by using the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span> <span data-ttu-id="e9712-204">Anschließend wird die Funktion [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) aufgerufen, um die appbar in die Position zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="e9712-204">Then it calls the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="e9712-205">Im folgenden Beispiel wird gezeigt, wie Sie die Größe und Position einer appbar festlegen.</span><span class="sxs-lookup"><span data-stu-id="e9712-205">The following example shows how to set an appbar's size and position.</span></span>


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a><span data-ttu-id="e9712-206">Verarbeiten von appbar-Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="e9712-206">Processing Appbar Notification Messages</span></span>

<span data-ttu-id="e9712-207">Eine appbar empfängt eine Benachrichtigungs Meldung, wenn sich der Zustand der Taskleiste ändert, wenn eine Vollbildanwendung gestartet wird (oder der letzte Vorgang geschlossen wird) oder wenn ein Ereignis auftritt, das die Größe und Position der appbar beeinflussen kann.</span><span class="sxs-lookup"><span data-stu-id="e9712-207">An appbar receives a notification message when the state of the taskbar changes, when a full-screen application starts (or the last one closes), or when an event occurs that can affect the appbar's size and position.</span></span> <span data-ttu-id="e9712-208">Im folgenden Beispiel wird gezeigt, wie die verschiedenen Benachrichtigungs Meldungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e9712-208">The following example shows how to process the various notification messages.</span></span>


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



<span data-ttu-id="e9712-209">Die folgende Funktion passt das umgebende Rechteck einer appbar an und ruft dann die Anwendungs definierte appbarquerysetpos-Funktion (im vorherigen Abschnitt enthalten) auf, um die Größe und Position der Leiste entsprechend festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e9712-209">The following function adjusts an appbar's bounding rectangle and then calls the application-defined AppBarQuerySetPos function (included in the previous section) to set the bar's size and position accordingly.</span></span>


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
