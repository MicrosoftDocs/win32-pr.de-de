---
title: Fensterrahmen
description: Die meisten Programme sollten Standardfenster Rahmen verwenden. Immersive Anwendungen können über einen Vollbildmodus verfügen, der den Fensterrahmen verbirgt. Sie sollten Glas strategisch für ein einfacheres, helleres aussehen in Erwägung gezogen werden.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552831"
---
# <a name="window-frames"></a><span data-ttu-id="aea7e-105">Fensterrahmen</span><span class="sxs-lookup"><span data-stu-id="aea7e-105">Window Frames</span></span>

> [!NOTE]
> <span data-ttu-id="aea7e-106">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aea7e-106">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="aea7e-107">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="aea7e-107">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="aea7e-108">Die meisten Programme sollten Standardfenster Rahmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-108">Most programs should use standard window frames.</span></span> <span data-ttu-id="aea7e-109">Immersive Anwendungen können über einen Vollbildmodus verfügen, der den Fensterrahmen verbirgt.</span><span class="sxs-lookup"><span data-stu-id="aea7e-109">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="aea7e-110">Sie sollten Glas strategisch für ein einfacheres, helleres aussehen in Erwägung gezogen werden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-110">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span>

<span data-ttu-id="aea7e-111">Mit einem Fensterrahmen können Benutzer ein Fenster bearbeiten und den Titel und das Symbol anzeigen, um dessen Inhalte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="aea7e-111">With a window frame, users can manipulate a window and view the title and icon to identify its contents.</span></span>

![<span data-ttu-id="aea7e-112">Screenshot des Fensterrahmens um das Editor Fenster</span><span class="sxs-lookup"><span data-stu-id="aea7e-112">screen shot of window frame around notepad window</span></span> ](images/win-window-frames-image1.png)

<span data-ttu-id="aea7e-113">Ein typischer Fensterrahmen.</span><span class="sxs-lookup"><span data-stu-id="aea7e-113">A typical window frame.</span></span>

<span data-ttu-id="aea7e-114">**Hinweis:** Richtlinien für die [Fensterverwaltung](win-window-mgt.md) und das [Branding](exper-branding.md) werden in separaten Artikeln dargestellt.</span><span class="sxs-lookup"><span data-stu-id="aea7e-114">**Note:** Guidelines related to [window management](win-window-mgt.md) and [branding](exper-branding.md) are presented in separate articles.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="aea7e-115">Entwurfskonzepte</span><span class="sxs-lookup"><span data-stu-id="aea7e-115">Design concepts</span></span>

### <a name="glass-window-frames"></a><span data-ttu-id="aea7e-116">Glasfenster Rahmen</span><span class="sxs-lookup"><span data-stu-id="aea7e-116">Glass window frames</span></span>

<span data-ttu-id="aea7e-117">Die Glasfenster Rahmen sind ein neuer Aspekt der Microsoft Windows-Ästhetik, der sowohl ansprechend als auch leicht zu sein ist.</span><span class="sxs-lookup"><span data-stu-id="aea7e-117">The glass window frames are a striking new aspect of the Microsoft Windows aesthetic, aiming to be both attractive and lightweight.</span></span> <span data-ttu-id="aea7e-118">Diese Durchschnitt stellen ermöglichen Windows ein offenes, weniger eindringliches Erscheinungsbild, das es Benutzern ermöglicht, sich auf Inhalte und Funktionen zu konzentrieren und nicht auf die Schnittstelle, die</span><span class="sxs-lookup"><span data-stu-id="aea7e-118">These translucent frames give windows an open, less intrusive appearance, helping users focus on content and functionality rather than the interface surrounding it.</span></span>

![<span data-ttu-id="aea7e-119">Screenshot des Glasrahmens um den Rechner</span><span class="sxs-lookup"><span data-stu-id="aea7e-119">screen shot of glass frame around calculator</span></span> ](images/win-window-frames-image2.png)

<span data-ttu-id="aea7e-120">Glasfenster Rahmen.</span><span class="sxs-lookup"><span data-stu-id="aea7e-120">Glass window frames.</span></span>

<span data-ttu-id="aea7e-121">Sie können Glas in kleinen Regionen in einem Fenster, das den Fensterrahmen berührt, strategisch strategisch verwenden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-121">You can use glass strategically in small regions within a window that touch the window frame.</span></span> <span data-ttu-id="aea7e-122">Diese Bereiche scheinen Teil des Fensterrahmens zu sein, auch wenn Sie technisch gesehen Teil des Client Bereichs des Fensters sind.</span><span class="sxs-lookup"><span data-stu-id="aea7e-122">Such regions appear to be part of the window frame, even though technically they are part of the window's client area.</span></span>

![<span data-ttu-id="aea7e-123">Screenshot des Fensters mit der durchlässigen Kante</span><span class="sxs-lookup"><span data-stu-id="aea7e-123">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)

<span data-ttu-id="aea7e-124">In diesem Beispiel wird Glas im Client Bereich verwendet, um einen Teil des Frames zu sehen.</span><span class="sxs-lookup"><span data-stu-id="aea7e-124">In this example, glass is used in the client area to make it look like part of the frame.</span></span>

### <a name="hidden-frames"></a><span data-ttu-id="aea7e-125">Verborgene Frames</span><span class="sxs-lookup"><span data-stu-id="aea7e-125">Hidden frames</span></span>

<span data-ttu-id="aea7e-126">Manchmal ist der beste Fensterrahmen überhaupt kein Frame.</span><span class="sxs-lookup"><span data-stu-id="aea7e-126">Sometimes the best window frame is no frame at all.</span></span> <span data-ttu-id="aea7e-127">Dies ist häufig der Fall für das [primäre Fenster](glossary.md) von immersiven [Vollbild](glossary.md) -Anwendungen, die nicht zusammen mit anderen Programmen verwendet werden, wie z. b. Medien Player, Spiele und Kiosk Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="aea7e-127">This is often the case for the [primary window](glossary.md) of immersive [full screen](glossary.md) applications that aren't used in conjunction with other programs, such as media players, games, and kiosk applications.</span></span>

<span data-ttu-id="aea7e-128">Inhalts Betrachter profitieren häufig von der Option, Inhalte voll Bildschirm anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aea7e-128">Content viewers often benefit from having the option to show content full screen.</span></span> <span data-ttu-id="aea7e-129">Beispiele hierfür sind Windows Internet Explorer, Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint und Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="aea7e-129">Examples include Windows Internet Explorer , Windows Live Photo Gallery, Windows Movie Maker HD, Microsoft PowerPoint , and Microsoft Word.</span></span>

![<span data-ttu-id="aea7e-130">Screenshot von Media Player in der Vollbildansicht</span><span class="sxs-lookup"><span data-stu-id="aea7e-130">screen shot of media player in full-screen view</span></span> ](images/win-window-frames-image4.png)

<span data-ttu-id="aea7e-131">In diesem Beispiel kann der Inhalt des Windows-Media Player voll Bildschirms angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-131">In this example, Windows Media Player can display its content full screen.</span></span>

### <a name="custom-frames"></a><span data-ttu-id="aea7e-132">Benutzerdefinierte Frames</span><span class="sxs-lookup"><span data-stu-id="aea7e-132">Custom frames</span></span>

<span data-ttu-id="aea7e-133">Die meisten Windows-Anwendungen sollten die Standardfenster Rahmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-133">Most Windows applications should use the standard window frames.</span></span> <span data-ttu-id="aea7e-134">Bei immersiven, eigenständigen, eigenständigen Anwendungen wie spielen und Kiosk Anwendungen kann es jedoch sinnvoll sein, benutzerdefinierte Frames für alle Fenster zu verwenden, die nicht voll Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-134">However, for immersive, full screen, stand-alone applications like games and kiosk applications, it may be appropriate to use custom frames for any windows that aren't shown full screen.</span></span> <span data-ttu-id="aea7e-135">Die Motivation für die Verwendung von benutzerdefinierten Frames sollte darin bestehen, die allgemeine Darstellung zu einem einzigartigen Verhalten zu machen, nicht nur für [Branding](exper-branding.md).</span><span class="sxs-lookup"><span data-stu-id="aea7e-135">The motivation to use custom frames should be to give the overall experience a unique feel, not just for [branding](exper-branding.md).</span></span>

![<span data-ttu-id="aea7e-136">Abbildung von Durcheinander und Frame des zusammen gewürelten Bilds</span><span class="sxs-lookup"><span data-stu-id="aea7e-136">illustration of scrambled picture puzzle and frame</span></span> ](images/win-window-frames-image5.png)

<span data-ttu-id="aea7e-137">Benutzerdefinierte Frames eignen sich für immersive, voll Bild-und eigenständige Anwendungen, wie z. b. Spiele.</span><span class="sxs-lookup"><span data-stu-id="aea7e-137">Custom frames are appropriate for immersive, full screen, stand-alone applications such as games.</span></span>

## <a name="guidelines"></a><span data-ttu-id="aea7e-138">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="aea7e-138">Guidelines</span></span>

### <a name="window-frames"></a><span data-ttu-id="aea7e-139">Fensterrahmen</span><span class="sxs-lookup"><span data-stu-id="aea7e-139">Window frames</span></span>

-   <span data-ttu-id="aea7e-140">Standardfenster Rahmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-140">Use standard window frames.</span></span>
    -   <span data-ttu-id="aea7e-141">**Ausnahme:** Um immersive Vollbild-, eigenständige Anwendungen zu einem einzigartigen Gefühl zu machen:</span><span class="sxs-lookup"><span data-stu-id="aea7e-141">**Exception:** To give immersive full screen, stand-alone applications a unique feel:</span></span>
        -   <span data-ttu-id="aea7e-142">Sie sollten den Fensterrahmen des [primären Fensters](glossary.md)ausblenden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-142">Consider hiding the window frame of the [primary window](glossary.md).</span></span>
        -   <span data-ttu-id="aea7e-143">Verwenden Sie benutzerdefinierte Frames für ein [sekundäres Fenster](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="aea7e-143">Consider using custom frames for [secondary window](glossary.md).</span></span>
        -   <span data-ttu-id="aea7e-144">Wenn ein benutzerdefinierter Frame geeignet ist, wählen Sie einen Entwurf aus, der einfach ist und nicht zu viel Aufmerksamkeit auf sich selbst zeichnet.</span><span class="sxs-lookup"><span data-stu-id="aea7e-144">If a custom frame is appropriate, choose a design that is lightweight and doesn't draw too much attention to itself.</span></span>

            <span data-ttu-id="aea7e-145">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="aea7e-145">**Incorrect:**</span></span>

            ![<span data-ttu-id="aea7e-146">Screenshot des abfragende Frames</span><span class="sxs-lookup"><span data-stu-id="aea7e-146">screen shot of distracting frame</span></span> ](images/win-window-frames-image6.png)

            <span data-ttu-id="aea7e-147">In diesem Beispiel zeichnet der benutzerdefinierte Frame eine zu große Aufmerksamkeit auf sich selbst.</span><span class="sxs-lookup"><span data-stu-id="aea7e-147">In this example, the custom frame draws too much attention to itself.</span></span>
-   <span data-ttu-id="aea7e-148">Fügen Sie einem Fensterrahmen keine Steuerelemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="aea7e-148">Don't add controls to a window frame.</span></span> <span data-ttu-id="aea7e-149">Fügen Sie die Steuerelemente stattdessen in das Fenster ein.</span><span class="sxs-lookup"><span data-stu-id="aea7e-149">Put the controls within the window instead.</span></span>

    <span data-ttu-id="aea7e-150">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="aea7e-150">**Incorrect:**</span></span>

    ![<span data-ttu-id="aea7e-151">Screenshot des Steuer Elements im Fensterrahmen</span><span class="sxs-lookup"><span data-stu-id="aea7e-151">screen shot of control in window frame</span></span> ](images/win-window-frames-image7.png)

    <span data-ttu-id="aea7e-152">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="aea7e-152">**Correct:**</span></span>

    ![<span data-ttu-id="aea7e-153">Screenshot des Steuer Elements im Client Bereich</span><span class="sxs-lookup"><span data-stu-id="aea7e-153">screen shot of control in client area</span></span> ](images/win-window-frames-image8.png)

    <span data-ttu-id="aea7e-154">Im richtigen Beispiel befindet sich das Steuerelement innerhalb des Client Bereichs anstelle des Fensterrahmens.</span><span class="sxs-lookup"><span data-stu-id="aea7e-154">In the correct example, the control is within the client area instead of the window frame.</span></span>

### <a name="full-screen-mode"></a><span data-ttu-id="aea7e-155">Vollbildmodus</span><span class="sxs-lookup"><span data-stu-id="aea7e-155">Full screen mode</span></span>

-   <span data-ttu-id="aea7e-156">Für Programme, die einen optionalen Vollbildmodus aufweisen, um den Vollbildmodus zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="aea7e-156">For programs that have an optional full screen mode, to enable full screen mode:</span></span>
    -   <span data-ttu-id="aea7e-157">Sie haben einen modalen Vollbild-Befehl in der Menüleiste oder in der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="aea7e-157">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="aea7e-158">Wenn der Benutzer auf den Befehl klickt, wird der Befehl im ausgewählten Zustand angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aea7e-158">When the user clicks the command, show the command in its selected state.</span></span>

        ![<span data-ttu-id="aea7e-159">Screenshot des Fensters mit dem Menü Element "Vollbild"</span><span class="sxs-lookup"><span data-stu-id="aea7e-159">screen shot of window with full screen menu item</span></span> ](images/win-window-frames-image9.png)

        <span data-ttu-id="aea7e-160">In diesem Beispiel wird der Vollbild-Befehl zusammen mit der Standard-Tastenkombination angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aea7e-160">This example shows the full screen command along with its standard shortcut key.</span></span>

-   <span data-ttu-id="aea7e-161">Verwenden Sie F11 für die Tastenkombination für den Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="aea7e-161">Use F11 for the full screen shortcut key.</span></span>
-   <span data-ttu-id="aea7e-162">Wenn eine Symbolleiste und der Vollbildmodus häufig verwendet werden, haben Sie auch eine Grafik Symbolleisten-Schaltfläche mit einer Vollbild-QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="aea7e-162">If there is a toolbar and full screen mode is commonly used, also have a graphic toolbar button with a Full screen tooltip.</span></span>

    ![<span data-ttu-id="aea7e-163">Screenshot der Schaltflächen zum Vollbildmodus und zum Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="aea7e-163">screen shot of full screen and revert buttons</span></span> ](images/win-window-frames-image10.png)

    <span data-ttu-id="aea7e-164">Beispiele für Vollbild-Symbolleisten-Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="aea7e-164">Examples of full screen toolbar buttons.</span></span>

-   <span data-ttu-id="aea7e-165">So kehren Sie den Vollbildmodus wieder her:</span><span class="sxs-lookup"><span data-stu-id="aea7e-165">To revert back from full screen mode:</span></span>
    -   <span data-ttu-id="aea7e-166">Sie haben einen modalen Vollbild-Befehl in der Menüleiste oder in der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="aea7e-166">Have a modal full screen command in the menu bar or toolbar.</span></span> <span data-ttu-id="aea7e-167">Wenn der Benutzer auf den Befehl klickt, zeigen Sie den Befehl im Zustand "gelöscht" an.</span><span class="sxs-lookup"><span data-stu-id="aea7e-167">When the user clicks the command, show the command in its cleared state.</span></span>
    -   <span data-ttu-id="aea7e-168">Verwenden Sie F11 für die Tastenkombination für den Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="aea7e-168">Use F11 for the full screen shortcut key.</span></span> <span data-ttu-id="aea7e-169">Wenn die Zuordnung nicht bereits erfolgt ist, kann ESC auch zu diesem Zweck verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aea7e-169">If not already assigned, Esc can also be used for this purpose.</span></span>

### <a name="glass"></a><span data-ttu-id="aea7e-170">Glas</span><span class="sxs-lookup"><span data-stu-id="aea7e-170">Glass</span></span>

<span data-ttu-id="aea7e-171">Standard Fensterrahmen verwenden in Windows automatisch Glas, Sie können jedoch auch Glas in Regionen verwenden, die den Fensterrahmen berühren.</span><span class="sxs-lookup"><span data-stu-id="aea7e-171">Standard window frames use glass automatically in Windows, but you can also use glass in regions that touch the window frame.</span></span>

-   <span data-ttu-id="aea7e-172">**Es empfiehlt sich, Glas strategisch in kleinen Regionen zu verwenden, die den Fensterrahmen ohne Text berühren.**</span><span class="sxs-lookup"><span data-stu-id="aea7e-172">**Consider using glass strategically in small regions touching the window frame without text.**</span></span> <span data-ttu-id="aea7e-173">Dies kann einem Programm ein einfacheres, helleres aussehen ermöglichen, indem die Region als Teil des Frames angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aea7e-173">Doing so can give a program a simpler, lighter, more cohesive look by making the region appear to be part of the frame.</span></span>
-   ![<span data-ttu-id="aea7e-174">Screenshot des Fensters mit der durchlässigen Kante</span><span class="sxs-lookup"><span data-stu-id="aea7e-174">screen shot of window with translucent edge</span></span> ](images/win-window-frames-image3.png)
-   <span data-ttu-id="aea7e-175">In diesem Beispiel konzentriert sich die Aufmerksamkeit des Benutzers auf den Inhalt und nicht auf die Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="aea7e-175">In this example, glass focuses the user's attention on the content instead of the controls.</span></span>
-   <span data-ttu-id="aea7e-176">**Verwenden Sie kein Glas in Situationen, in denen ein einfacher Fenster Hintergrund attraktiver oder leichter zu verwenden wäre.**</span><span class="sxs-lookup"><span data-stu-id="aea7e-176">**Don't use glass in situations where a plain window background would be more attractive or easier to use.**</span></span>

<span data-ttu-id="aea7e-177">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="aea7e-177">**Correct:**</span></span>

![<span data-ttu-id="aea7e-178">Screenshot des Fensters mit vier Grafiken und Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="aea7e-178">screen shot of window with four graphics and label</span></span> ](images/win-window-frames-image11.png)

<span data-ttu-id="aea7e-179">In diesem Beispiel wird Glas verwendet, um dem Alt + Tab-Fenster ein schlankes aussehen zu geben.</span><span class="sxs-lookup"><span data-stu-id="aea7e-179">In this example, glass is used to give the Alt+Tab window a lightweight appearance.</span></span> <span data-ttu-id="aea7e-180">Glas funktioniert für dieses Fenster, weil es aus Grafiken und einer einzelnen, starken Text Bezeichnung besteht.</span><span class="sxs-lookup"><span data-stu-id="aea7e-180">Glass works for this window because it consists of graphics and a single, strong text label.</span></span>

<span data-ttu-id="aea7e-181">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="aea7e-181">**Incorrect:**</span></span>

![<span data-ttu-id="aea7e-182">Screenshot des Fensters mit zwölf Grafiken</span><span class="sxs-lookup"><span data-stu-id="aea7e-182">screen shot of window with twelve graphics</span></span> ](images/win-window-frames-image12.png)

<span data-ttu-id="aea7e-183">In diesem falschen Beispiel ist die Verwendung von Glas ablenkend.</span><span class="sxs-lookup"><span data-stu-id="aea7e-183">In this incorrect example, the use of glass is distracting.</span></span> <span data-ttu-id="aea7e-184">Ein einfacher Hintergrund ist eine bessere Wahl.</span><span class="sxs-lookup"><span data-stu-id="aea7e-184">A plain window background would be a better choice.</span></span>

 

 