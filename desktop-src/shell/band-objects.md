---
description: Die Explorer-Leiste wurde mit Microsoft Internet Explorer 4,0 eingeführt, um einen Anzeigebereich neben dem Browserbereich bereitzustellen.
title: Erstellen von benutzerdefinierten Explorer-Leisten, Tool-Bändern und Desk-Bändern
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104571323"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a><span data-ttu-id="2a882-103">Erstellen von benutzerdefinierten Explorer-leisten, Toolbands und Desk-Bändern</span><span class="sxs-lookup"><span data-stu-id="2a882-103">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</span></span>

<span data-ttu-id="2a882-104">Die Explorer-Leiste wurde mit Microsoft Internet Explorer 4,0 eingeführt, um einen Anzeigebereich neben dem Browserbereich bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2a882-104">The Explorer Bar was introduced with Microsoft Internet Explorer 4.0 to provide a display area adjacent to the browser pane.</span></span> <span data-ttu-id="2a882-105">Es handelt sich im Grunde um ein untergeordnetes Fenster innerhalb des Windows Internet Explorer-Fensters, das zum Anzeigen von Informationen und zum interagieren mit dem Benutzer auf die gleiche Weise verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a882-105">It is basically a child window within the Windows Internet Explorer window, and it can be used to display information and interact with the user in much the same way.</span></span> <span data-ttu-id="2a882-106">Explorer-Balken werden am häufigsten als vertikaler Bereich auf der linken Seite des Browser Bereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-106">Explorer Bars are most commonly displayed as a vertical pane on the left side of the browser pane.</span></span> <span data-ttu-id="2a882-107">Eine Explorer-Leiste kann jedoch auch horizontal unter dem Browserbereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-107">However, an Explorer Bar can also be displayed horizontally, below the browser pane.</span></span>

![Screenshot, in dem die vertikalen und horizontalen Explorer-Leisten angezeigt werden.](images/expl1.jpg)

<span data-ttu-id="2a882-109">Es gibt eine breite Palette möglicher Verwendungsmöglichkeiten für die Explorer-Leiste.</span><span class="sxs-lookup"><span data-stu-id="2a882-109">There is a wide range of possible uses for the Explorer Bar.</span></span> <span data-ttu-id="2a882-110">Benutzer können auf verschiedene Arten auswählen, welche Option angezeigt werden soll. Sie können Sie auch im Untermenü der **Explorer-Leiste** des Menüs **Ansicht** auswählen oder auf eine Symbolleisten Schaltfläche klicken.</span><span class="sxs-lookup"><span data-stu-id="2a882-110">Users can select which option they want to see in several different ways, including selecting it from the **Explorer Bar** submenu of the **View** menu, or clicking a toolbar button.</span></span> <span data-ttu-id="2a882-111">Internet Explorer bietet einige Standard-Explorer-leisten, einschließlich Favoriten und suchen.</span><span class="sxs-lookup"><span data-stu-id="2a882-111">Internet Explorer provides several standard Explorer Bars, including Favorites and Search.</span></span>

<span data-ttu-id="2a882-112">Eine der Möglichkeiten, wie Sie Internet Explorer anpassen können, besteht darin, eine benutzerdefinierte Explorer-Leiste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2a882-112">One of the ways you can customize Internet Explorer is by adding a custom Explorer Bar.</span></span> <span data-ttu-id="2a882-113">Wenn Sie implementiert und registriert ist, wird Sie dem Untermenü der **Explorer-Leiste** im Menü **Ansicht** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2a882-113">When implemented and registered, it will be added to the **Explorer Bar** submenu of the **View** menu.</span></span> <span data-ttu-id="2a882-114">Wenn Sie vom Benutzer ausgewählt wird, kann der Anzeigebereich der Explorer-Leiste verwendet werden, um Informationen anzuzeigen und die Benutzereingaben auf die gleiche Weise wie ein normales Fenster zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="2a882-114">When selected by the user, the Explorer Bar's display area can then be used to display information and take user input in much the same way as a normal window.</span></span>

![Screenshot der Explorer-leisten](images/expl2.jpg)

<span data-ttu-id="2a882-116">Um eine benutzerdefinierte Explorer-Leiste zu erstellen, müssen Sie ein *Band Objekt* implementieren und registrieren.</span><span class="sxs-lookup"><span data-stu-id="2a882-116">To create a custom Explorer Bar, you must implement and register a *band object*.</span></span> <span data-ttu-id="2a882-117">Band Objekte wurden mit Version 4,71 der Shell eingeführt und bieten ähnliche Funktionen wie normale Fenster.</span><span class="sxs-lookup"><span data-stu-id="2a882-117">Band objects were introduced with version 4.71 of the Shell and provide capabilities similar to those of normal windows.</span></span> <span data-ttu-id="2a882-118">Da es sich jedoch um Component Object Model (com)-Objekte handelt, die entweder in Internet Explorer oder in der Shell enthalten sind, werden Sie etwas anders implementiert.</span><span class="sxs-lookup"><span data-stu-id="2a882-118">However, because they are Component Object Model (COM) objects and contained by either Internet Explorer or the Shell, they are implemented somewhat differently.</span></span> <span data-ttu-id="2a882-119">Einfache Band Objekte wurden verwendet, um die Beispiel-Explorer-leisten zu erstellen, die in der ersten Grafik angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-119">Simple band objects were used to create the sample Explorer Bars displayed in the first graphic.</span></span> <span data-ttu-id="2a882-120">Die Implementierung des Beispiels für die vertikale Explorer-Leiste wird in einem späteren Abschnitt ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a882-120">The implementation of the vertical Explorer Bar sample will be discussed in detail in a later section.</span></span>

## <a name="tool-bands"></a><span data-ttu-id="2a882-121">Tool Bänder</span><span class="sxs-lookup"><span data-stu-id="2a882-121">Tool Bands</span></span>

<span data-ttu-id="2a882-122">Ein *Toolband* ist ein Band Objekt, das mit Microsoft Internet Explorer 5 eingeführt wurde, um die Windows Radio Toolbar-Funktion zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2a882-122">A *tool band* is a band object that was introduced with Microsoft Internet Explorer 5 to support the Windows radio toolbar feature.</span></span> <span data-ttu-id="2a882-123">Die Internet Explorer-Symbolleiste ist tatsächlich ein Grund leisten-Steuerelement, das mehrere Toolbar- [Steuer](../controls/rebar-controls.md) [Elemente](../controls/toolbar-control-reference.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="2a882-123">The Internet Explorer toolbar is actually a [rebar control](../controls/rebar-controls.md) that contains several [toolbar controls](../controls/toolbar-control-reference.md).</span></span> <span data-ttu-id="2a882-124">Wenn Sie ein Toolband erstellen, können Sie ein Band zu diesem Grund leisten-Steuerelement hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2a882-124">By creating a tool band, you can add a band to that rebar control.</span></span> <span data-ttu-id="2a882-125">Ähnlich wie Explorer-Balken ist ein Toolband jedoch ein allgemeines Fenster.</span><span class="sxs-lookup"><span data-stu-id="2a882-125">However, like Explorer Bars, a tool band is a general purpose window.</span></span>

![Screenshot der Tool Bänder](images/toolband1.jpg)

<span data-ttu-id="2a882-127">Benutzer zeigen eine Symbolleiste an, indem Sie Sie im Untermenü "Symbolleisten" des Menüs **Ansicht** oder im Kontextmenü auswählen, das angezeigt wird, indem Sie mit der rechten Maustaste auf den Symbol **leisten** Bereich klicken.</span><span class="sxs-lookup"><span data-stu-id="2a882-127">Users display a toolbar by selecting it from the **Toolbars** submenu of the **View** menu or from the shortcut menu that is displayed by right-clicking the toolbar area.</span></span>

## <a name="desk-bands"></a><span data-ttu-id="2a882-128">Desk-Bänder</span><span class="sxs-lookup"><span data-stu-id="2a882-128">Desk Bands</span></span>

<span data-ttu-id="2a882-129">Mithilfe von Band Objekten können auch Desk- *Bänder* erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-129">Band objects can also be used to create *desk bands*.</span></span> <span data-ttu-id="2a882-130">Während die grundlegende Implementierung von Explorer-leisten vergleichbar ist, sind die Desk-Bänder nicht mit Internet Explorer verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2a882-130">While their basic implementation is similar to Explorer Bars, desk bands are unrelated to Internet Explorer.</span></span> <span data-ttu-id="2a882-131">Ein Desk-Band ist im Grunde genommen eine Möglichkeit, ein Andock bares Fenster auf dem Desktop zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2a882-131">A desk band is basically a way to create a dockable window on the desktop.</span></span> <span data-ttu-id="2a882-132">Der Benutzer wählt ihn aus, indem er mit der rechten Maustaste auf die Taskleiste klickt und ihn aus dem Untermenü **Symbolleisten** auswählt.</span><span class="sxs-lookup"><span data-stu-id="2a882-132">The user selects it by right-clicking the taskbar and selecting it from the **Toolbars** submenu.</span></span>

![Screenshot, der ein Beispiel für einen Desk-Band anzeigt.](images/desk2.png)

<span data-ttu-id="2a882-134">Anfänglich werden die Desk-Bänder auf der Taskleiste angedockt.</span><span class="sxs-lookup"><span data-stu-id="2a882-134">Initially, desk bands are docked on the taskbar.</span></span>

![Screenshot, in dem die in der Taskleiste angedockten Desk-Bänder angezeigt werden.](images/desk1.jpg)

<span data-ttu-id="2a882-136">Der Benutzer kann dann das Desk-Band auf den Desktop ziehen und als normales Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-136">The user can then drag the desk band to the desktop, and it will appear as a normal window.</span></span>

![Screenshot der Desk-Bänder](images/desk3.png)

## <a name="implementing-band-objects"></a><span data-ttu-id="2a882-138">Implementieren von Band Objekten</span><span class="sxs-lookup"><span data-stu-id="2a882-138">Implementing Band Objects</span></span>

<span data-ttu-id="2a882-139">Die folgenden Themen werden erörtert.</span><span class="sxs-lookup"><span data-stu-id="2a882-139">The following topics are discussed.</span></span>

-   [<span data-ttu-id="2a882-140">Grundlagen zu Band Objekten</span><span class="sxs-lookup"><span data-stu-id="2a882-140">Band Object Basics</span></span>](#band-object-basics)
-   [<span data-ttu-id="2a882-141">Band Registrierung</span><span class="sxs-lookup"><span data-stu-id="2a882-141">Band Registration</span></span>](#band-registration)
-   [<span data-ttu-id="2a882-142">Ein einfaches Beispiel für eine benutzerdefinierte Explorer-Leiste</span><span class="sxs-lookup"><span data-stu-id="2a882-142">A Simple Example of a Custom Explorer Bar</span></span>](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a><span data-ttu-id="2a882-143">Grundlagen zu Band Objekten</span><span class="sxs-lookup"><span data-stu-id="2a882-143">Band Object Basics</span></span>

<span data-ttu-id="2a882-144">Obwohl Sie ähnlich wie normale Fenster verwendet werden können, handelt es sich bei Band Objekten um COM-Objekte, die in einem Container vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2a882-144">Although they can be used much like normal windows, band objects are COM objects that exist within a container.</span></span> <span data-ttu-id="2a882-145">Explorer-Balken sind in Internet Explorer enthalten, und Desk-Bänder sind in der Shell enthalten.</span><span class="sxs-lookup"><span data-stu-id="2a882-145">Explorer Bars are contained by Internet Explorer, and desk bands are contained by the Shell.</span></span> <span data-ttu-id="2a882-146">Obwohl Sie unterschiedliche Funktionen bedienen, ist Ihre grundlegende Implementierung sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="2a882-146">While they serve different functions, their basic implementation is very similar.</span></span> <span data-ttu-id="2a882-147">Der Hauptunterschied besteht darin, wie das Band Objekt registriert wird, das wiederum den Objekttyp und den zugehörigen Container steuert.</span><span class="sxs-lookup"><span data-stu-id="2a882-147">The primary difference is in how the band object is registered, which in turn controls the type of object and its container.</span></span> <span data-ttu-id="2a882-148">In diesem Abschnitt werden die Aspekte der Implementierung erläutert, die allen Band Objekten gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="2a882-148">This section discusses those aspects of implementation that are common to all band objects.</span></span> <span data-ttu-id="2a882-149">Weitere Implementierungsdetails finden Sie [in einem einfachen Beispiel für eine benutzerdefinierte Explorer-Leiste](#a-simple-example-of-a-custom-explorer-bar) .</span><span class="sxs-lookup"><span data-stu-id="2a882-149">See [A Simple Example of a Custom Explorer Bar](#a-simple-example-of-a-custom-explorer-bar) for additional implementation details.</span></span>

<span data-ttu-id="2a882-150">Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) und [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)müssen alle Band Objekte die folgenden Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="2a882-150">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), all band objects must implement the following interfaces.</span></span>

-   [<span data-ttu-id="2a882-151">**Ideskband**</span><span class="sxs-lookup"><span data-stu-id="2a882-151">**IDeskBand**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [<span data-ttu-id="2a882-152">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="2a882-152">**IObjectWithSite**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [<span data-ttu-id="2a882-153">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="2a882-153">**IPersistStream**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersiststream)

<span data-ttu-id="2a882-154">Zusätzlich zum Registrieren Ihres Klassen Bezeichners (CLSID) müssen die Explorer-Leiste und die Desk-Band-Objekte auch für die entsprechende Komponenten Kategorie registriert werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-154">In addition to registering their class identifier (CLSID), the Explorer Bar and desk band objects must also be registered for the appropriate component category.</span></span> <span data-ttu-id="2a882-155">Beim Registrieren der Komponenten Kategorie wird der Objekttyp und der zugehörige Container bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2a882-155">Registering the component category determines the object type and its container.</span></span> <span data-ttu-id="2a882-156">Toolbänder verwenden eine andere Registrierungs Prozedur und verfügen nicht über einen Kategoriebezeichner (CATID).</span><span class="sxs-lookup"><span data-stu-id="2a882-156">Tool bands use a different registration procedure and do not have a category identifier (CATID).</span></span> <span data-ttu-id="2a882-157">Die CATIDs für die drei-Band-Objekte, die Sie benötigen, sind:</span><span class="sxs-lookup"><span data-stu-id="2a882-157">The CATIDs for the three band objects that require them are:</span></span>



| <span data-ttu-id="2a882-158">Bandtyp</span><span class="sxs-lookup"><span data-stu-id="2a882-158">Band Type</span></span>               | <span data-ttu-id="2a882-159">Komponentenkategorie</span><span class="sxs-lookup"><span data-stu-id="2a882-159">Component Category</span></span> |
|-------------------------|--------------------|
| <span data-ttu-id="2a882-160">Vertikale Explorer-Leiste</span><span class="sxs-lookup"><span data-stu-id="2a882-160">Vertical Explorer Bar</span></span>   | <span data-ttu-id="2a882-161">CATID- \_ Infoband</span><span class="sxs-lookup"><span data-stu-id="2a882-161">CATID\_InfoBand</span></span>    |
| <span data-ttu-id="2a882-162">Horizontale Explorer-Leiste</span><span class="sxs-lookup"><span data-stu-id="2a882-162">Horizontal Explorer Bar</span></span> | <span data-ttu-id="2a882-163">CATID- \_ Kommas</span><span class="sxs-lookup"><span data-stu-id="2a882-163">CATID\_CommBand</span></span>    |
| <span data-ttu-id="2a882-164">Desk-Band</span><span class="sxs-lookup"><span data-stu-id="2a882-164">Desk Band</span></span>               | <span data-ttu-id="2a882-165">CATID \_ Desktop</span><span class="sxs-lookup"><span data-stu-id="2a882-165">CATID\_DeskBand</span></span>    |



 

<span data-ttu-id="2a882-166">Weitere Informationen zum Registrieren von Band Objekten finden Sie unter [Band Registrierung](#band-registration) .</span><span class="sxs-lookup"><span data-stu-id="2a882-166">See [Band Registration](#band-registration) for further discussion of how to register band objects.</span></span>

<span data-ttu-id="2a882-167">Wenn das Band Objekt Benutzereingaben akzeptieren soll, muss auch [**iinputobject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-167">If the band object is to accept user input, it must also implement [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span></span> <span data-ttu-id="2a882-168">Zum Hinzufügen von Elementen zum Kontextmenü für Explorer-oder-Desk-Bänder muss das Band Objekt [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)exportieren.</span><span class="sxs-lookup"><span data-stu-id="2a882-168">To add items to the shortcut menu for Explorer Bar or desk bands, the band object must export [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="2a882-169">Tool Bänder unterstützen keine Kontextmenüs.</span><span class="sxs-lookup"><span data-stu-id="2a882-169">Tool bands do not support shortcut menus.</span></span>

<span data-ttu-id="2a882-170">Da ein untergeordnetes Fenster von Band Objekten implementiert wird, müssen Sie auch eine Fenster Prozedur zum Verarbeiten von Windows-Messaging implementieren.</span><span class="sxs-lookup"><span data-stu-id="2a882-170">Because band objects implement a child window, they must also implement a window procedure to handle Windows messaging.</span></span>

<span data-ttu-id="2a882-171">Band Objekte können über die [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) -Schnittstelle des Containers Befehle an ihren Container senden.</span><span class="sxs-lookup"><span data-stu-id="2a882-171">Band objects can send commands to their container through the container's [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) interface.</span></span> <span data-ttu-id="2a882-172">Um den Schnittstellen Zeiger zu erhalten, rufen Sie die [**iinputobjectsite:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode des Containers auf, und Fragen Sie IID \_ IOleCommandTarget.</span><span class="sxs-lookup"><span data-stu-id="2a882-172">To obtain the interface pointer, call the container's [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method and ask for IID\_IOleCommandTarget.</span></span> <span data-ttu-id="2a882-173">Anschließend senden Sie mit [**IOleCommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec)Befehle an den Container.</span><span class="sxs-lookup"><span data-stu-id="2a882-173">You then send commands to the container with [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span></span> <span data-ttu-id="2a882-174">Die Befehlsgruppe ist "cgid \_ Deskband".</span><span class="sxs-lookup"><span data-stu-id="2a882-174">The command group is CGID\_DeskBand.</span></span> <span data-ttu-id="2a882-175">Wenn die [**ideskband:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) -Methode eines Band Objekts aufgerufen wird, verwendet der Container den *dwbandid* -Parameter, um dem Band Objekt einen Bezeichner zuzuweisen, der für drei der Befehle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a882-175">When a band object's [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) method is called, the container uses the *dwBandID* parameter to assign the band object an identifier that is used for three of the commands.</span></span> <span data-ttu-id="2a882-176">Vier **IOleCommandTarget:: exec** -Befehls-IDs werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a882-176">Four **IOleCommandTarget::Exec** command IDs are supported.</span></span>

-   <span data-ttu-id="2a882-177">DBID \_ bandinfochanged</span><span class="sxs-lookup"><span data-stu-id="2a882-177">DBID\_BANDINFOCHANGED</span></span>

    <span data-ttu-id="2a882-178">Die Informationen des Bands wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="2a882-178">The band's information has changed.</span></span> <span data-ttu-id="2a882-179">Legen Sie den *pvaIn* -Parameter auf den Bezeichner des Bands fest, der beim letzten Aufruf von [**ideskband:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="2a882-179">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="2a882-180">Der Container Ruft die **ideskband:: GetBandInfo** -Methode des Band Objekts auf, um die aktualisierten Informationen anzufordern.</span><span class="sxs-lookup"><span data-stu-id="2a882-180">The container will call the band object's **IDeskBand::GetBandInfo** method to request the updated information.</span></span>

-   <span data-ttu-id="2a882-181">DBID \_ maximizeband</span><span class="sxs-lookup"><span data-stu-id="2a882-181">DBID\_MAXIMIZEBAND</span></span>

    <span data-ttu-id="2a882-182">Maximieren Sie das Band.</span><span class="sxs-lookup"><span data-stu-id="2a882-182">Maximize the band.</span></span> <span data-ttu-id="2a882-183">Legen Sie den *pvaIn* -Parameter auf den Bezeichner des Bands fest, der beim letzten Aufruf von [**ideskband:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="2a882-183">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span>

-   <span data-ttu-id="2a882-184">DBID \_ showonly</span><span class="sxs-lookup"><span data-stu-id="2a882-184">DBID\_SHOWONLY</span></span>

    <span data-ttu-id="2a882-185">Schalten Sie andere Bänder im Container ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="2a882-185">Turn other bands in the container on or off.</span></span> <span data-ttu-id="2a882-186">Legen Sie den *pvaIn* -Parameter auf den unbekannten VT- \_ Typ mit einem der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="2a882-186">Set the *pvaIn* parameter to the VT\_UNKNOWN type with one of the following values:</span></span>

    

    | <span data-ttu-id="2a882-187">Wert</span><span class="sxs-lookup"><span data-stu-id="2a882-187">Value</span></span> | <span data-ttu-id="2a882-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a882-188">Description</span></span>                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2a882-189">Kro</span><span class="sxs-lookup"><span data-stu-id="2a882-189">pUnk</span></span>  | <span data-ttu-id="2a882-190">Ein Zeiger auf die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Band Objekts.</span><span class="sxs-lookup"><span data-stu-id="2a882-190">A pointer to the band object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2a882-191">Alle anderen Desk-Bänder werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2a882-191">All other desk bands will be hidden.</span></span> |
    | <span data-ttu-id="2a882-192">0</span><span class="sxs-lookup"><span data-stu-id="2a882-192">0</span></span>     | <span data-ttu-id="2a882-193">Alle Desk-Bänder ausblenden.</span><span class="sxs-lookup"><span data-stu-id="2a882-193">Hide all desk bands.</span></span>                                                                                        |
    | <span data-ttu-id="2a882-194">1</span><span class="sxs-lookup"><span data-stu-id="2a882-194">1</span></span>     | <span data-ttu-id="2a882-195">Alle Desk-Bänder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2a882-195">Show all desk bands.</span></span>                                                                                        |

    

     

-   <span data-ttu-id="2a882-196">DBID- \_ pushchevron</span><span class="sxs-lookup"><span data-stu-id="2a882-196">DBID\_PUSHCHEVRON</span></span>

    <span data-ttu-id="2a882-197">[Version 5](versions.md).</span><span class="sxs-lookup"><span data-stu-id="2a882-197">[Version 5](versions.md).</span></span> <span data-ttu-id="2a882-198">Zeigen Sie ein Chevron-Menü an.</span><span class="sxs-lookup"><span data-stu-id="2a882-198">Display a chevron menu.</span></span> <span data-ttu-id="2a882-199">Der Container sendet eine [**RB- \_ pushchevron**](../controls/rb-pushchevron.md) -Nachricht, und das Band Objekt empfängt eine [RBN \_ chevronpush](../controls/rbn-chevronpushed.md) -Benachrichtigung, die ihn auffordert, das Chevron-Menü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2a882-199">The container sends an [**RB\_PUSHCHEVRON**](../controls/rb-pushchevron.md) message, and the band object receives an [RBN\_CHEVRONPUSHED](../controls/rbn-chevronpushed.md) notification that prompts it to display the chevron menu.</span></span> <span data-ttu-id="2a882-200">Legen Sie den *nCmdexecopt* -Parameter der [**IOleCommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) -Methode auf den Band Bezeichner fest, der beim letzten Aufruf von [**ideskband:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="2a882-200">Set the [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) method's *nCmdExecOpt* parameter to the band identifier received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="2a882-201">Legen Sie den *pvaIn* -Parameter der **IOleCommandTarget:: exec** -Methode auf den VT \_ I4-Typ mit einem von der Anwendung definierten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="2a882-201">Set the **IOleCommandTarget::Exec** method's *pvaIn* parameter to the VT\_I4 type with an application-defined value.</span></span> <span data-ttu-id="2a882-202">Es wird als Wert des *lappvalue* der RBN-chevronpushbenachrichtigung an das Band Objekt übergeben \_ .</span><span class="sxs-lookup"><span data-stu-id="2a882-202">It passes back to the band object as the *lAppValue* value of the RBN\_CHEVRONPUSHED notification.</span></span>

### <a name="band-registration"></a><span data-ttu-id="2a882-203">Band Registrierung</span><span class="sxs-lookup"><span data-stu-id="2a882-203">Band Registration</span></span>

<span data-ttu-id="2a882-204">Ein Band Objekt muss als OLE-Prozess interner Server registriert werden, der das Apartment Threading unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a882-204">A band object must be registered as an OLE in-process server that supports apartment threading.</span></span> <span data-ttu-id="2a882-205">Der Standardwert für den Server ist eine Menü Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2a882-205">The default value for the server is a menu text string.</span></span> <span data-ttu-id="2a882-206">Bei Explorer-leisten wird diese im Untermenü der **Explorer-Leiste** im Internet Explorer- **Ansichts** Menü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-206">For Explorer Bars, it will appear in the **Explorer Bar** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="2a882-207">Für Tool Bänder wird es im Menü " **Symbolleisten** " im Menü " **Ansicht** " von Internet Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-207">For tool bands, it will appear in the **Toolbars** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="2a882-208">Für Desk-Bänder wird Sie im Untermenü **Symbolleisten** des Kontextmenüs der Taskleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-208">For desk bands, it will appear in the **Toolbars** submenu of the taskbar's shortcut menu.</span></span> <span data-ttu-id="2a882-209">Wie bei Menü Ressourcen führt das Platzieren eines kaufmännischen und-Zeichens (&) vor einem Buchstaben zu unterstrichen und ermöglicht Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="2a882-209">As with menu resources, placing an ampersand (&) in front of a letter will cause it to be underlined and enable keyboard shortcuts.</span></span> <span data-ttu-id="2a882-210">Beispielsweise ist die Menü Zeichenfolge für die vertikale Explorer-Leiste, die in der ersten Grafik angezeigt wird, "Sample &Vertical Explorer Bar".</span><span class="sxs-lookup"><span data-stu-id="2a882-210">For example, the menu string for the vertical Explorer Bar shown in the first graphic is "Sample &Vertical Explorer Bar".</span></span>

<span data-ttu-id="2a882-211">Zunächst ruft Internet Explorer mithilfe der Komponenten Kategorien eine Enumeration der registrierten Explorer-Balken Objekte aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2a882-211">Initially, Internet Explorer retrieves an enumeration of the registered Explorer Bar objects from the registry using the component categories.</span></span> <span data-ttu-id="2a882-212">Um die Leistung zu verbessern, wird diese Enumeration zwischengespeichert, sodass anschließend die hinzugefügten Explorer-leisten übersehen werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-212">To increase performance, it then caches this enumeration, causing subsequently added Explorer Bars to be overlooked.</span></span> <span data-ttu-id="2a882-213">Wenn Sie erzwingen möchten, dass Windows Internet Explorer den Cache neu erstellt und eine neue Explorer-Leiste erkennt, löschen Sie die folgenden Registrierungsschlüssel während der Registrierung der neuen Explorer-Leiste:</span><span class="sxs-lookup"><span data-stu-id="2a882-213">To force Windows Internet Explorer to rebuild the cache and recognize a new Explorer Bar, delete the following registry keys during the registration of the new Explorer Bar:</span></span>

<span data-ttu-id="2a882-214">**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **verwerfbare** \\ **postsetup**- \\ **Komponenten Kategorien** \\ **{00021493-0000-0000-C000-000000000046}-Aufzählung** \\ </span><span class="sxs-lookup"><span data-stu-id="2a882-214">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021493-0000-0000-C000-000000000046}**\\**Enum**</span></span>

<span data-ttu-id="2a882-215">**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **verwerfbare** \\ **postsetup**- \\ **Komponenten Kategorien** \\ **{00021494-0000-0000-C000-000000000046}-Aufzählung** \\ </span><span class="sxs-lookup"><span data-stu-id="2a882-215">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021494-0000-0000-C000-000000000046}**\\**Enum**</span></span>

> [!Note]  
> <span data-ttu-id="2a882-216">Da für jeden Benutzer ein Explorer-leisten Cache erstellt wird, muss Ihre Setup Anwendung möglicherweise alle Benutzer Registrierungs Strukturen auflisten oder einen Stub pro Benutzer hinzufügen, der ausgeführt wird, wenn sich der Benutzer zum ersten Mal anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2a882-216">Because an Explorer Bar cache is created for each user, your setup application may need to enumerate all the user registry hives or add a per-user stub to run when the user first logs on.</span></span>

 

<span data-ttu-id="2a882-217">Im Allgemeinen wird der grundlegende Registrierungs Eintrag für ein Band Objekt folgendermaßen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-217">In general, the basic registry entry for a band object will appear as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

<span data-ttu-id="2a882-218">Bei Toolbands muss auch die CLSID Ihres Objekts bei Internet Explorer registriert sein.</span><span class="sxs-lookup"><span data-stu-id="2a882-218">Tool bands must also have their object's CLSID registered with Internet Explorer.</span></span> <span data-ttu-id="2a882-219">Weisen Sie zu diesem Zweck einen Wert unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Toolbar** mit dem Namen der CLSID-GUID des toolbandobjekts zu, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-219">To do this, assign a value under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Toolbar** named with the tool band object's CLSID GUID as shown here.</span></span> <span data-ttu-id="2a882-220">Der Datenwert wird ignoriert, sodass der Werttyp unwichtig ist.</span><span class="sxs-lookup"><span data-stu-id="2a882-220">Its data value is ignored, so the value type is unimportant.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

<span data-ttu-id="2a882-221">Es gibt mehrere optionale Werte, die auch der Registrierung hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="2a882-221">There are several optional values that can also be added to the registry.</span></span> <span data-ttu-id="2a882-222">Der folgende Wert ist z. b. erforderlich, wenn Sie die Explorer-Leiste zum Anzeigen von HTML verwenden möchten. der angezeigte Wert ist kein Beispiel, sondern der tatsächliche Wert, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a882-222">For instance, the following value is necessary if you want to use the Explorer Bar to display HTML The value shown is not an example, but the actual value that should be used.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

<span data-ttu-id="2a882-223">Wenn Sie in Verbindung mit dem oben gezeigten Wert verwendet werden, ist auch der folgende optionale Wert erforderlich, wenn Sie die Explorer-Leiste zum Anzeigen von HTML verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="2a882-223">Used in conjunction with the value shown above, the following optional value is also necessary if you want to use the Explorer Bar to display HTML.</span></span> <span data-ttu-id="2a882-224">Dieser Wert sollte auf den Speicherort der Datei festgelegt werden, die den HTML-Inhalt für die Explorer-Leiste enthält.</span><span class="sxs-lookup"><span data-stu-id="2a882-224">This value should be set to the location of the file that contains the HTML content for the Explorer Bar.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

<span data-ttu-id="2a882-225">Ein weiterer Optionaler Wert definiert die Standardbreite oder Höhe der Explorer-Leiste, je nachdem, ob es sich um vertikal bzw. horizontal handelt.</span><span class="sxs-lookup"><span data-stu-id="2a882-225">Another optional value defines the default width or height of the Explorer Bar, depending on whether it is vertical or horizontal, respectively.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

<span data-ttu-id="2a882-226">Der barsize-Wert muss auf die Breite oder Höhe des Balkens festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-226">The BarSize value should be set to the width or height of the bar.</span></span> <span data-ttu-id="2a882-227">Der Wert erfordert acht Bytes und wird in der Registrierung als binärer Wert abgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a882-227">The value requires eight bytes and is placed in the registry as a binary value.</span></span> <span data-ttu-id="2a882-228">Die ersten vier Bytes geben die Größe im Hexadezimal Format in Pixel an, beginnend ab dem äußersten linken Byte.</span><span class="sxs-lookup"><span data-stu-id="2a882-228">The first four bytes specify the size in pixels, in hexadecimal format, starting from the leftmost byte.</span></span> <span data-ttu-id="2a882-229">Die letzten vier Bytes sind reserviert und sollten auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-229">The last four bytes are reserved and should be set to zero.</span></span>

<span data-ttu-id="2a882-230">Beispielsweise werden hier die vollständigen Registrierungseinträge für eine HTML-fähige Explorer-Leiste mit einer Standardbreite von 291 (0x123) Pixel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-230">As an example, the full registry entries for an HTML-capable Explorer Bar with a default width of 291 (0x123) pixels are shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

<span data-ttu-id="2a882-231">Die Registrierung der CATID eines Band Objekts kann Programm gesteuert behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-231">You can handle registration of a band object's CATID programmatically.</span></span> <span data-ttu-id="2a882-232">Erstellen Sie ein Komponenten Kategorien-Manager-Objekt (CLSID \_ stdcomponentcategoriesmgr), und fordern Sie einen Zeiger auf seine [**ikatregister**](/windows/win32/api/comcat/nn-comcat-icatregister) -Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="2a882-232">Create a component categories manager object (CLSID\_StdComponentCategoriesMgr) and request a pointer to its [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) interface.</span></span> <span data-ttu-id="2a882-233">Übergeben Sie die CLSID und die CATID des Band Objekts an [**iskiregister:: registerclassimplcategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span><span class="sxs-lookup"><span data-stu-id="2a882-233">Pass the band object's CLSID and CATID to [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span></span>

### <a name="a-simple-example-of-a-custom-explorer-bar"></a><span data-ttu-id="2a882-234">Ein einfaches Beispiel für eine benutzerdefinierte Explorer-Leiste</span><span class="sxs-lookup"><span data-stu-id="2a882-234">A Simple Example of a Custom Explorer Bar</span></span>

<span data-ttu-id="2a882-235">Dieses Beispiel durchläuft die Implementierung der vertikalen Beispiel-Explorer-Leiste, die in der Einführung gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2a882-235">This example goes through the implementation of the sample vertical Explorer Bar shown in the introduction.</span></span>

<span data-ttu-id="2a882-236">Das grundlegende Verfahren zum Erstellen einer benutzerdefinierten Explorer-Leiste sieht wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="2a882-236">The basic procedure for creating a custom Explorer Bar is as follows.</span></span>

1.  <span data-ttu-id="2a882-237">[Implementieren Sie die Funktionen, die von der DLL benötigt werden](#dll-functions).</span><span class="sxs-lookup"><span data-stu-id="2a882-237">[Implement the functions needed by the DLL](#dll-functions).</span></span>
2.  [<span data-ttu-id="2a882-238">Implementieren Sie die erforderlichen COM-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="2a882-238">Implement the required COM interfaces.</span></span>](#required-interface-implementations)
3.  [<span data-ttu-id="2a882-239">Implementieren Sie alle gewünschten optionalen com-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="2a882-239">Implement any desired optional COM interfaces.</span></span>](#optional-interface-implementations)
4.  [<span data-ttu-id="2a882-240">Registrieren Sie die CLSID des Objekts und ggf. die Komponenten Kategorie.</span><span class="sxs-lookup"><span data-stu-id="2a882-240">Register the object's CLSID and, if required, component category.</span></span>](#clsid-registration)
5.  <span data-ttu-id="2a882-241">Erstellen Sie ein untergeordnetes Fenster von Internet Explorer, dessen Größenanpassung an den Anzeigebereich der Explorer-Leiste angepasst ist.</span><span class="sxs-lookup"><span data-stu-id="2a882-241">Create a child window of Internet Explorer, sized to fit the Explorer Bar's display region.</span></span>
6.  [<span data-ttu-id="2a882-242">Verwenden Sie das untergeordnete Fenster, um Informationen anzuzeigen und mit dem Benutzer zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="2a882-242">Use the child window to display information and interact with the user.</span></span>](#the-window-procedure)

<span data-ttu-id="2a882-243">Die sehr einfache Implementierung, die im Explorer-leisten Beispiel verwendet wird, kann tatsächlich für den Typ der Explorer-Leiste oder einen Desk-Band verwendet werden, indem Sie Sie einfach für die entsprechende Komponenten Kategorie registrieren.</span><span class="sxs-lookup"><span data-stu-id="2a882-243">The very simple implementation used in the Explorer Bar sample could actually be used for either type of Explorer Bar, or a desk band, by simply registering it for the appropriate component category.</span></span> <span data-ttu-id="2a882-244">Anspruchsvollere Implementierungen müssen für den Anzeigebereich und Container jedes Objekt Typs angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-244">More sophisticated implementations will need to be customized for each object type's display region and container.</span></span> <span data-ttu-id="2a882-245">Allerdings kann ein Großteil dieser Anpassung erreicht werden, indem der Beispielcode übernommen und erweitert wird, indem vertraute Windows-Programmiertechniken auf das untergeordnete Fenster angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-245">However, much of this customization can be accomplished by taking the sample code and extending it by applying familiar Windows programming techniques to the child window.</span></span> <span data-ttu-id="2a882-246">Beispielsweise können Sie Steuerelemente für Benutzerinteraktion oder Grafiken hinzufügen, um eine umfassendere Anzeige zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a882-246">For example, you can add controls for user interaction, or graphics for a richer display.</span></span>

### <a name="dll-functions"></a><span data-ttu-id="2a882-247">DLL-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2a882-247">DLL Functions</span></span>

<span data-ttu-id="2a882-248">Alle drei Objekte werden in einer einzelnen DLL verpackt, die die folgenden Funktionen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="2a882-248">All three objects are packaged in a single DLL, which exposes the following functions.</span></span>

-   [<span data-ttu-id="2a882-249">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="2a882-249">**DllMain**</span></span>](../dlls/dllmain.md)
-   [<span data-ttu-id="2a882-250">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="2a882-250">**DllCanUnloadNow**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [<span data-ttu-id="2a882-251">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="2a882-251">**DllGetClassObject**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [<span data-ttu-id="2a882-252">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="2a882-252">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

<span data-ttu-id="2a882-253">Die ersten drei Funktionen sind Standard Implementierungen und werden hier nicht erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a882-253">The first three functions are standard implementations and will not be discussed here.</span></span> <span data-ttu-id="2a882-254">Die Klassenfactoryimplementierung ist auch Standard.</span><span class="sxs-lookup"><span data-stu-id="2a882-254">The Class Factory implementation is also standard.</span></span>

### <a name="required-interface-implementations"></a><span data-ttu-id="2a882-255">Erforderliche Schnittstellen Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2a882-255">Required Interface Implementations</span></span>

<span data-ttu-id="2a882-256">Das Beispiel für die vertikale Explorer-Leiste implementiert die vier erforderlichen Schnittstellen: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)und [**ideskband**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) als Teil der cexplorerbar-Klasse.</span><span class="sxs-lookup"><span data-stu-id="2a882-256">The vertical Explorer Bar sample implements the four required interfaces: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream), and [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) as part of the CExplorerBar class.</span></span> <span data-ttu-id="2a882-257">Die Implementierungen Konstruktor, Dekonstruktor und **IUnknown** sind unkompliziert und werden hier nicht erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a882-257">The constructor, destructor, and **IUnknown** implementations are straightforward, and will not be discussed here.</span></span> <span data-ttu-id="2a882-258">Sehen Sie sich den Beispielcode an, um ausführliche Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a882-258">See the sample code for details.</span></span>

<span data-ttu-id="2a882-259">Die folgenden Schnittstellen werden ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a882-259">The following interfaces are discussed in detail.</span></span>

-   [<span data-ttu-id="2a882-260">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="2a882-260">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="2a882-261">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="2a882-261">IPersistStream</span></span>](#ipersiststream)
-   [<span data-ttu-id="2a882-262">Ideskband</span><span class="sxs-lookup"><span data-stu-id="2a882-262">IDeskBand</span></span>](#ideskband)

### <a name="iobjectwithsite"></a><span data-ttu-id="2a882-263">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="2a882-263">IObjectWithSite</span></span>

<span data-ttu-id="2a882-264">Wenn der Benutzer eine Explorer-Leiste auswählt, ruft der Container die [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) -Methode des entsprechenden Band Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="2a882-264">When the user selects an Explorer Bar, the container calls the corresponding band object's [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) method.</span></span> <span data-ttu-id="2a882-265">Der Parameter " *pUnkSite* " wird auf den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger der Site festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a882-265">The *punkSite* parameter will be set to the site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="2a882-266">Im Allgemeinen sollte eine [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) -Implementierung die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="2a882-266">In general, a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) implementation should perform the following steps:</span></span>

1.  <span data-ttu-id="2a882-267">Geben Sie einen beliebigen Website Zeiger frei, der derzeit aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="2a882-267">Release any site pointer that is currently being held.</span></span>
2.  <span data-ttu-id="2a882-268">Wenn der an [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) über gegebene Zeiger auf **null** festgelegt ist, wird das Band entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a882-268">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is set to **NULL**, the band is being removed.</span></span> <span data-ttu-id="2a882-269">**SetSite** kann S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="2a882-269">**SetSite** can return S\_OK.</span></span>
3.  <span data-ttu-id="2a882-270">Wenn der an [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) über gegebene Zeiger nicht **null** ist, wird eine neue Site festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a882-270">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is non-**NULL**, a new site is being set.</span></span> <span data-ttu-id="2a882-271">**SetSite** sollte folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="2a882-271">**SetSite** should do the following:</span></span>
    1.  <span data-ttu-id="2a882-272">Ruft [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der Site für die [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="2a882-272">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) interface.</span></span>
    2.  <span data-ttu-id="2a882-273">Rufen Sie [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) auf, um das Handle des übergeordneten Fensters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a882-273">Call [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) to obtain the parent window's handle.</span></span> <span data-ttu-id="2a882-274">Speichern Sie das Handle für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="2a882-274">Save the handle for later use.</span></span> <span data-ttu-id="2a882-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) , wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2a882-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) if it is no longer needed.</span></span>
    3.  <span data-ttu-id="2a882-276">Erstellen Sie das Fenster des Band Objekts als untergeordnetes Element des Fensters, das Sie im vorherigen Schritt abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="2a882-276">Create the band object's window as a child of the window obtained in the previous step.</span></span> <span data-ttu-id="2a882-277">Erstellen Sie Sie nicht als sichtbares Fenster.</span><span class="sxs-lookup"><span data-stu-id="2a882-277">Do not create it as a visible window.</span></span>
    4.  <span data-ttu-id="2a882-278">Wenn das Band Objekt [**iinputobject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)implementiert, nennen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die [**iinputobjectsite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) -Schnittstelle auf der Website.</span><span class="sxs-lookup"><span data-stu-id="2a882-278">If the band object implements [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) interface.</span></span> <span data-ttu-id="2a882-279">Speichern Sie den Zeiger auf diese Schnittstelle, um Sie später zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2a882-279">Store the pointer to this interface for use later.</span></span>
    5.  <span data-ttu-id="2a882-280">Wenn alle Schritte erfolgreich sind, geben Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2a882-280">If all steps are successful, return S\_OK.</span></span> <span data-ttu-id="2a882-281">Andernfalls wird der OLE-definierte Fehlercode zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="2a882-281">If not, return the OLE-defined error code indicating what failed.</span></span>

<span data-ttu-id="2a882-282">Das Beispiel für eine Explorer-Leiste implementiert [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) auf folgende Weise.</span><span class="sxs-lookup"><span data-stu-id="2a882-282">The Explorer Bar sample implements [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) in the following way.</span></span> <span data-ttu-id="2a882-283">Im folgenden Code ist " *m \_ psite* " eine private Member-Variable, die den [**iinputobjectsite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) -Zeiger enthält und *m \_ hwndParent* das Handle des übergeordneten Fensters enthält.</span><span class="sxs-lookup"><span data-stu-id="2a882-283">In the following code *m\_pSite* is a private member variable that holds the [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) pointer and *m\_hwndParent* holds the parent window's handle.</span></span> <span data-ttu-id="2a882-284">In diesem Beispiel wird auch die Fenster Erstellung behandelt.</span><span class="sxs-lookup"><span data-stu-id="2a882-284">In this sample, window creation is also handled.</span></span> <span data-ttu-id="2a882-285">Wenn das Fenster nicht vorhanden ist, erstellt diese Methode das Fenster der Explorer-Leiste als untergeordnetes Element des übergeordneten Fensters, das von **SetSite** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2a882-285">If the window does not exist, this method creates the Explorer Bar's window as an appropriately sized child of the parent window obtained by **SetSite**.</span></span> <span data-ttu-id="2a882-286">Das Handle des untergeordneten Fensters wird in *m \_ HWND* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2a882-286">The child window's handle is stored in *m\_hwnd*.</span></span>


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



<span data-ttu-id="2a882-287">Die [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) -Implementierung des Beispiels umschließt einfach einen Aufrufen der [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode der Site und verwendet dabei den von [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)gespeicherten Website Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2a882-287">The sample's [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) implementation simply wraps a call to the site's [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, using the site pointer saved by [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span></span>


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a><span data-ttu-id="2a882-288">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="2a882-288">IPersistStream</span></span>

<span data-ttu-id="2a882-289">Internet Explorer Ruft die [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle der Explorer-Leiste auf, damit die Explorer-Leiste persistente Daten laden oder speichern kann.</span><span class="sxs-lookup"><span data-stu-id="2a882-289">Internet Explorer will call the Explorer Bar's [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to allow the Explorer Bar to load or save persistent data.</span></span> <span data-ttu-id="2a882-290">Wenn keine persistenten Daten vorhanden sind, müssen die Methoden weiterhin einen Erfolgs Code zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2a882-290">If there is no persistent data, the methods must still return a success code.</span></span> <span data-ttu-id="2a882-291">Die **IPersistStream** -Schnittstelle erbt von [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist), sodass fünf Methoden implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2a882-291">The **IPersistStream** interface inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), so five methods must be implemented.</span></span>

-   [<span data-ttu-id="2a882-292">**Ipersistent:: GetClassID**</span><span class="sxs-lookup"><span data-stu-id="2a882-292">**IPersist::GetClassID**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [<span data-ttu-id="2a882-293">**IPersistStream:: IsDirty**</span><span class="sxs-lookup"><span data-stu-id="2a882-293">**IPersistStream::IsDirty**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [<span data-ttu-id="2a882-294">**IPersistStream:: Load**</span><span class="sxs-lookup"><span data-stu-id="2a882-294">**IPersistStream::Load**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [<span data-ttu-id="2a882-295">**IPersistStream:: Save**</span><span class="sxs-lookup"><span data-stu-id="2a882-295">**IPersistStream::Save**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [<span data-ttu-id="2a882-296">**IPersistStream:: GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="2a882-296">**IPersistStream::GetSizeMax**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

<span data-ttu-id="2a882-297">Im Beispiel für eine Explorer-Leiste werden keine persistenten Daten verwendet, und es ist nur eine minimale Implementierung von [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2a882-297">The Explorer Bar sample does not use any persistent data and has only a minimal implementation of [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="2a882-298">[**Ipersistent:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) gibt die CLSID des Objekts (CLSID \_ sampleexplor\) zurück, und der Rest gibt entweder s \_ OK, s \_ false oder E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="2a882-298">[**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) returns the object's CLSID (CLSID\_SampleExplorerBar), and the remainder return either S\_OK, S\_FALSE, or E\_NOTIMPL.</span></span>

### <a name="ideskband"></a><span data-ttu-id="2a882-299">Ideskband</span><span class="sxs-lookup"><span data-stu-id="2a882-299">IDeskBand</span></span>

<span data-ttu-id="2a882-300">Die [**ideskband**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) -Schnittstelle ist spezifisch für Band Objekte.</span><span class="sxs-lookup"><span data-stu-id="2a882-300">The [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) interface is specific to band objects.</span></span> <span data-ttu-id="2a882-301">Zusätzlich zu seiner einzigen Methode erbt sie von [**idockingwindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), das wiederum von [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)erbt.</span><span class="sxs-lookup"><span data-stu-id="2a882-301">In addition to its one method, it inherits from [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), which in turn inherits from [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span></span>

<span data-ttu-id="2a882-302">Es gibt zwei [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) -Methoden: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) und [**IOleWindow:: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span><span class="sxs-lookup"><span data-stu-id="2a882-302">There are two [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) methods: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) and [**IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span></span> <span data-ttu-id="2a882-303">Die Implementierung von **GetWindow** in der Explorer-Leiste gibt das untergeordnete Fenster Handle der Explorer-Leiste ( *m \_ HWND*) zurück.</span><span class="sxs-lookup"><span data-stu-id="2a882-303">The Explorer Bar sample's implementation of **GetWindow** returns the Explorer Bar's child window handle, *m\_hwnd*.</span></span> <span data-ttu-id="2a882-304">Die kontextbezogene Hilfe ist nicht implementiert, sodass **ContextSensitiveHelp** **E \_ notimpl** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2a882-304">Context-sensitive Help is not implemented, so **ContextSensitiveHelp** returns **E\_NOTIMPL**.</span></span>

<span data-ttu-id="2a882-305">Die [**idockingwindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) -Schnittstelle verfügt über drei Methoden.</span><span class="sxs-lookup"><span data-stu-id="2a882-305">The [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface has three methods.</span></span>

-   [<span data-ttu-id="2a882-306">**Idockingwindow:: showdw**</span><span class="sxs-lookup"><span data-stu-id="2a882-306">**IDockingWindow::ShowDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [<span data-ttu-id="2a882-307">**Idockingwindow:: closedw**</span><span class="sxs-lookup"><span data-stu-id="2a882-307">**IDockingWindow::CloseDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [<span data-ttu-id="2a882-308">**Idockingwindow:: resizeborderdw**</span><span class="sxs-lookup"><span data-stu-id="2a882-308">**IDockingWindow::ResizeBorderDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

<span data-ttu-id="2a882-309">Die [**resizeborderdw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) -Methode wird nicht mit einem beliebigen Typ von Band Objekt verwendet und sollte immer E \_ notimpl zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2a882-309">The [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) method is not used with any type of band object and should always return E\_NOTIMPL.</span></span> <span data-ttu-id="2a882-310">Die [**showdw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) -Methode zeigt das Fenster der Explorer-Leiste an oder blendet es aus, abhängig vom Wert des Parameters.</span><span class="sxs-lookup"><span data-stu-id="2a882-310">The [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) method either shows or hides the Explorer Bar's window, depending on the value of its parameter.</span></span>


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



<span data-ttu-id="2a882-311">Die [**closedw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) -Methode zerstört das Fenster der Explorer-Leiste.</span><span class="sxs-lookup"><span data-stu-id="2a882-311">The [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) method destroys the Explorer Bar's window.</span></span>


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



<span data-ttu-id="2a882-312">Die verbleibende Methode [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)ist für **ideskband** spezifisch.</span><span class="sxs-lookup"><span data-stu-id="2a882-312">The remaining method, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), is specific to **IDeskBand**.</span></span> <span data-ttu-id="2a882-313">Internet Explorer verwendet es, um den Bezeichner und den Anzeigemodus der Explorer-Leiste anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2a882-313">Internet Explorer uses it to specify the Explorer Bar's identifier and viewing mode.</span></span> <span data-ttu-id="2a882-314">Internet Explorer kann auch eine oder mehrere Informationen von der Explorer-Leiste anfordern, indem er den **dwMask** -Member der [**deskbandinfo**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) -Struktur ausfüllt, der als dritter Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2a882-314">Internet Explorer also may request one or more pieces of information from the Explorer Bar by filling the **dwMask** member of the [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) structure that is passed as the third parameter.</span></span> <span data-ttu-id="2a882-315">**GetBandInfo** sollte den Bezeichner und den Anzeigemodus speichern und die **deskbandinfo** -Struktur mit den angeforderten Daten ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="2a882-315">**GetBandInfo** should store the identifier and viewing mode and fill the **DESKBANDINFO** structure with the requested data.</span></span> <span data-ttu-id="2a882-316">Das Beispiel für eine Explorer-Leiste implementiert **GetBandInfo** , wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-316">The Explorer Bar sample implements **GetBandInfo** as shown in the following code example.</span></span>


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a><span data-ttu-id="2a882-317">Optionale Schnittstellen Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2a882-317">Optional Interface Implementations</span></span>

<span data-ttu-id="2a882-318">Es gibt zwei Schnittstellen, die nicht erforderlich sind. Dies kann jedoch nützlich sein, um Folgendes zu implementieren: [**iinputobject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) und [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="2a882-318">There are two interfaces that are not required, but that may be useful to implement: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) and [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="2a882-319">Das Beispiel für eine Explorer-Leiste implementiert **iinputobject**.</span><span class="sxs-lookup"><span data-stu-id="2a882-319">The Explorer Bar sample implements **IInputObject**.</span></span> <span data-ttu-id="2a882-320">Informationen zum Implementieren von **IContextMenu** finden Sie in der Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2a882-320">Refer to the documentation for information on how to implement **IContextMenu**.</span></span>

### <a name="iinputobject"></a><span data-ttu-id="2a882-321">Iinputobject</span><span class="sxs-lookup"><span data-stu-id="2a882-321">IInputObject</span></span>

<span data-ttu-id="2a882-322">Die [**iinputobject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) -Schnittstelle muss implementiert werden, wenn ein Band Objekt Benutzereingaben akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2a882-322">The [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) interface must be implemented if a band object accepts user input.</span></span> <span data-ttu-id="2a882-323">Internet Explorer implementiert [**iinputobjectsite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) und verwendet **iinputobject** , um den richtigen Benutzereingabe Fokus zu erhalten, wenn es mehr als ein eigenständiges Fenster hat.</span><span class="sxs-lookup"><span data-stu-id="2a882-323">Internet Explorer implements [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) and uses **IInputObject** to maintain proper user input focus when it has more than one contained window.</span></span> <span data-ttu-id="2a882-324">Es gibt drei Methoden, die von einer Explorer-Leiste implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2a882-324">There are three methods that need to be implemented by an Explorer Bar.</span></span>

-   [<span data-ttu-id="2a882-325">**Iinputobject:: uiactivateio**</span><span class="sxs-lookup"><span data-stu-id="2a882-325">**IInputObject::UIActivateIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [<span data-ttu-id="2a882-326">**Iinputobject:: hasfocusio**</span><span class="sxs-lookup"><span data-stu-id="2a882-326">**IInputObject::HasFocusIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [<span data-ttu-id="2a882-327">**Iinputobject:: translateacceleratorio**</span><span class="sxs-lookup"><span data-stu-id="2a882-327">**IInputObject::TranslateAcceleratorIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

<span data-ttu-id="2a882-328">Internet Explorer ruft [**uiactivateio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) auf, um der Explorer-Leiste mitzuteilen, dass Sie aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="2a882-328">Internet Explorer calls [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) to inform the Explorer Bar that it is being activated or deactivated.</span></span> <span data-ttu-id="2a882-329">Wenn diese aktiviert ist, ruft das Explorer-Balken Beispiel [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) auf, um den Fokus auf das Fenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2a882-329">When activated, the Explorer Bar sample calls [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) to set the focus to its window.</span></span>

<span data-ttu-id="2a882-330">Internet Explorer ruft [**hasfocusio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) auf, wenn versucht wird, zu bestimmen, welches Fenster den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="2a882-330">Internet Explorer calls [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) when it is attempting to determine which window has focus.</span></span> <span data-ttu-id="2a882-331">Wenn das Fenster der Explorer-Leiste oder einer der untergeordneten Elemente den Fokus besitzt, sollte **hasfocusio** den Wert s OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="2a882-331">If the Explorer Bar's window or one of its descendants has focus, **HasFocusIO** should return S\_OK.</span></span> <span data-ttu-id="2a882-332">Wenn dies nicht der Fall ist, sollte der Wert S false zurückgeben \_</span><span class="sxs-lookup"><span data-stu-id="2a882-332">If not, it should return S\_FALSE.</span></span>

<span data-ttu-id="2a882-333">[**Translateacceleratorio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) ermöglicht dem Objekt die Verarbeitung von Tastatur Accelerators.</span><span class="sxs-lookup"><span data-stu-id="2a882-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) allows the object to process keyboard accelerators.</span></span> <span data-ttu-id="2a882-334">Das Beispiel für eine Explorer-Leiste implementiert diese Methode nicht, daher gibt es "false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="2a882-334">The Explorer Bar sample does not implement this method, so it returns S\_FALSE.</span></span>

<span data-ttu-id="2a882-335">Die Implementierung von [**iinputobjectsite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) in der Beispiel Leiste sieht wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="2a882-335">The sample bar's implementation of [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) is as follows.</span></span>


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a><span data-ttu-id="2a882-336">CLSID-Registrierung</span><span class="sxs-lookup"><span data-stu-id="2a882-336">CLSID Registration</span></span>

<span data-ttu-id="2a882-337">Wie bei allen COM-Objekten muss die CLSID der Explorer-Leiste registriert werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-337">As with all COM objects, the Explorer Bar's CLSID must be registered.</span></span> <span data-ttu-id="2a882-338">Damit das-Objekt ordnungsgemäß mit Internet Explorer funktioniert, muss es auch für die entsprechende Komponenten Kategorie (CATID \_ Infoband) registriert werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-338">For the object to function properly with Internet Explorer, it must also be registered for the appropriate component category (CATID\_InfoBand).</span></span> <span data-ttu-id="2a882-339">Der relevante Code Abschnitt für die Explorer-Leiste wird im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-339">The relevant code section for the Explorer Bar is shown in the following code example.</span></span>


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="2a882-340">Bei der Registrierung von Band Objekten im Beispiel werden normale com-Prozeduren verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a882-340">Registration of band objects in the sample uses normal COM procedures.</span></span>

<span data-ttu-id="2a882-341">Zusätzlich zur CLSID muss der-Band Objekt Server auch für eine oder mehrere Komponenten Kategorien registriert werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-341">In addition to the CLSID, the band object server must also be registered for one or more component categories.</span></span> <span data-ttu-id="2a882-342">Dies ist der Hauptunterschied in der Implementierung zwischen vertikalen und horizontalen Explorer-Balken Beispielen.</span><span class="sxs-lookup"><span data-stu-id="2a882-342">This is actually the main difference in implementation between the vertical and horizontal Explorer Bar samples.</span></span> <span data-ttu-id="2a882-343">Dieser Prozess wird durch das Erstellen eines Komponenten Kategorien-Manager-Objekts (CLSID \_ stdcomponentcategoriesmgr) und das Verwenden der [**icatregister:: registerclassimplcategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) -Methode zum Registrieren des Band Objekt Servers behandelt.</span><span class="sxs-lookup"><span data-stu-id="2a882-343">This process is handled by creating a component categories manager object (CLSID\_StdComponentCategoriesMgr) and using the [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) method to register the band object server.</span></span> <span data-ttu-id="2a882-344">In diesem Beispiel wird die Registrierung der Komponenten Kategorie behandelt, indem die CLSID und die CATID des Explorer-Balken Beispiels an eine private Funktion –**registercomcat**– übergeben werden, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a882-344">In this example, component category registration is handled by passing the Explorer Bar sample's CLSID and CATID to a private function—**RegisterComCat**—as shown in the following code example.</span></span>


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a><span data-ttu-id="2a882-345">Die Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="2a882-345">The Window Procedure</span></span>

<span data-ttu-id="2a882-346">Da ein Band Objekt ein untergeordnetes Fenster für seine Anzeige verwendet, muss es eine Fenster Prozedur zum Verarbeiten von Windows-Messaging implementieren.</span><span class="sxs-lookup"><span data-stu-id="2a882-346">Because a band object uses a child window for its display, it must implement a window procedure to handle Windows messaging.</span></span> <span data-ttu-id="2a882-347">Das Band Beispiel verfügt über minimale Funktionalität, sodass die Fenster Prozedur nur fünf Nachrichten verarbeitet:</span><span class="sxs-lookup"><span data-stu-id="2a882-347">The band sample has minimal functionality, so its window procedure only handles five messages:</span></span>

-   [<span data-ttu-id="2a882-348">**WM- \_ nccreate**</span><span class="sxs-lookup"><span data-stu-id="2a882-348">**WM\_NCCREATE**</span></span>](../winmsg/wm-nccreate.md)
-   [<span data-ttu-id="2a882-349">**WM- \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="2a882-349">**WM\_PAINT**</span></span>](../gdi/wm-paint.md)
-   [<span data-ttu-id="2a882-350">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="2a882-350">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)
-   [<span data-ttu-id="2a882-351">**WM- \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="2a882-351">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)
-   [<span data-ttu-id="2a882-352">**WM- \_ killfokus**</span><span class="sxs-lookup"><span data-stu-id="2a882-352">**WM\_KILLFOCUS**</span></span>](../inputdev/wm-killfocus.md)

<span data-ttu-id="2a882-353">Die Prozedur kann problemlos erweitert werden, um weitere Nachrichten zur Unterstützung weiterer Funktionen zu bieten.</span><span class="sxs-lookup"><span data-stu-id="2a882-353">The procedure can easily be expanded to accommodate additional messages to support more features.</span></span>


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



<span data-ttu-id="2a882-354">Der WM- \_ Befehls Handler gibt einfach NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="2a882-354">The WM\_COMMAND handler simply returns zero.</span></span> <span data-ttu-id="2a882-355">Der WM-Zeichnungs \_ Handler erstellt die einfache Textanzeige, die im Beispiel der Explorer-Leiste in der Einführung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2a882-355">The WM\_PAINT handler creates the simple text display shown in the Explorer Bar example in the introduction.</span></span>


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="2a882-356">Die "WM \_ SetFocus"-und "WM \_ killfocus"-Handler informieren die Website über eine Fokus Änderung, indem Sie die [**iinputobjectsite:: onfocuschangeis**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) -Methode der Site aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2a882-356">The WM\_SETFOCUS and WM\_KILLFOCUS handlers inform the site of a focus change by calling the site's [**IInputObjectSite::OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) method.</span></span>


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



<span data-ttu-id="2a882-357">Band Objekte bieten eine flexible und leistungsstarke Möglichkeit, die Funktionen von Internet Explorer zu erweitern, indem benutzerdefinierte Explorer-leisten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2a882-357">Band objects provide a flexible and powerful way to extend the capabilities of Internet Explorer by creating custom Explorer Bars.</span></span> <span data-ttu-id="2a882-358">Durch die Implementierung eines Desk-Bands können Sie die Funktionen von normalen Fenstern erweitern.</span><span class="sxs-lookup"><span data-stu-id="2a882-358">Implementing a desk band enables you to extend the capabilities of normal windows.</span></span> <span data-ttu-id="2a882-359">Obwohl einige COM-Programmierung erforderlich ist, ist es letztendlich, ein untergeordnetes Fenster für Ihre Benutzeroberfläche bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2a882-359">Although some COM programming is required, it ultimately serves to provide a child window for your user interface.</span></span> <span data-ttu-id="2a882-360">Von dort aus kann der Großteil der Implementierung vertraute Windows-Programmiertechniken verwenden.</span><span class="sxs-lookup"><span data-stu-id="2a882-360">From there, the bulk of the implementation can use familiar Windows programming techniques.</span></span> <span data-ttu-id="2a882-361">Das hier beschriebene Beispiel verfügt zwar nur über eingeschränkte Funktionalität, veranschaulicht aber alle notwendigen Features eines Band Objekts und kann problemlos erweitert werden, um eine eindeutige und leistungsstarke Benutzeroberfläche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2a882-361">While the example discussed here has only limited functionality, it illustrates all the necessary features of a band object and it can be readily extended to create a unique and powerful user interface.</span></span>

 

 
