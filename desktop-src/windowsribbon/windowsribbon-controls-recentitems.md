---
title: Zuletzt verwendete Elemente
description: Die Liste der zuletzt verwendeten Elemente ist ein Bereich im Anwendungsmenü, in dem die zuletzt verwendeten Elemente (MRU) für eine Anwendung angezeigt werden.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104571556"
---
# <a name="recent-items"></a><span data-ttu-id="1ce1b-103">Zuletzt verwendete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ce1b-103">Recent Items</span></span>

<span data-ttu-id="1ce1b-104">Die Liste der zuletzt verwendeten Elemente ist ein Bereich im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) , in dem die zuletzt verwendeten Elemente (MRU) für eine Anwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-104">The Recent Items list is a pane in the [Application Menu](windowsribbon-controls-applicationmenu.md) that displays the most recently used (MRU) items for an application.</span></span>

-   [<span data-ttu-id="1ce1b-105">Details</span><span class="sxs-lookup"><span data-stu-id="1ce1b-105">Details</span></span>](#details)
-   [<span data-ttu-id="1ce1b-106">Eigenschaften für zuletzt verwendete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ce1b-106">Recent Items Properties</span></span>](#recent-items-properties)
-   [<span data-ttu-id="1ce1b-107">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="1ce1b-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="1ce1b-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ce1b-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="1ce1b-109">Details</span><span class="sxs-lookup"><span data-stu-id="1ce1b-109">Details</span></span>

<span data-ttu-id="1ce1b-110">Der folgende Screenshot veranschaulicht eine Liste zuletzt verwendeter Elemente aus WordPad für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-110">The following screen shot illustrates a Recent Items list from WordPad for Windows 7).</span></span>

![Screenshot der Liste der zuletzt verwendeten Elemente im Microsoft Paint-Menüband.](images/controls/recentitems.png)

<span data-ttu-id="1ce1b-112">Das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) kann höchstens eine [**applicationmenu. recentitems**](windowsribbon-element-applicationmenu-recentitems.md) -Liste enthalten, die durch ein **applicationmenu. recentitems** -Element dargestellt wird, um aktuelle Dokumente, Bilder, Filme und andere Projekte anzuzeigen, an denen ein Benutzer gearbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-112">The [Application Menu](windowsribbon-controls-applicationmenu.md) can have at most one [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) list, represented by an **ApplicationMenu.RecentItems** element, for displaying recent documents, pictures, movies, and other projects a user has been working on.</span></span> <span data-ttu-id="1ce1b-113">Die Anzahl der aufgelisteten Elemente liegt zwischen 0 (null) und der maximalen Anzahl, die im Markup angegeben ist. der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-113">The number of listed items ranges from zero to the maximum number specified in markup, with a default value of ten.</span></span> <span data-ttu-id="1ce1b-114">Die zuletzt verwendeten Elemente werden als eine nummerierte Liste von Zeichen folgen angezeigt, die Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-114">The recent items are displayed as a numbered list of strings indicating file names.</span></span> <span data-ttu-id="1ce1b-115">Es wird empfohlen, die [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md) -Eigenschaft zu verwenden, um den vollständigen Pfad für den Datei Speicherort anzugeben, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-115">It is recommended that the [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) property be used to give the full path for the file location, as shown in the following screen shot .</span></span>

![Screenshot einer Liste zuletzt verwendeter Elemente in einem Anwendungsmenü.](images/overviews/applicationmenu-menurecentitems.png)

<span data-ttu-id="1ce1b-117">Das [**recentitems**](windowsribbon-element-recentitems.md) -Element verfügt über ein *enablepinning* -Attribut, das, wenn es auf festgelegt `true` ist, auf der rechten Seite jedes Elements in der Liste ein Pin-Symbol anzeigt, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-117">The [**RecentItems**](windowsribbon-element-recentitems.md) element has an *EnablePinning* attribute that, if set to `true`, displays a pin icon to the right of each item in the list, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="1ce1b-118">Das anhepup ist standardmäßig aktiviert, wenn das Attribut " *enablepinning* " nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-118">Pinning is enabled by default if the *EnablePinning* attribute is not specified.</span></span>

 

![Screenshot der letzten Elemente, die in einem Anwendungsmenü fixiert werden.](images/overviews/applicationmenu-menurecentitemspinned.png)

<span data-ttu-id="1ce1b-120">Der Fixierungs Algorithmus soll verhindern, dass Elemente aus der Liste der **zuletzt verwendeten Elemente** entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-120">The pinning algorithm is intended to keep items from falling off the **Recent items** list.</span></span> <span data-ttu-id="1ce1b-121">Der Algorithmus erzeugt das folgende Verhalten:</span><span class="sxs-lookup"><span data-stu-id="1ce1b-121">The algorithm produces the following behavior:</span></span>

-   <span data-ttu-id="1ce1b-122">Ein neues Element wird immer am oberen Rand der Liste **zuletzt geöffnete Elemente** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-122">A new item is always added at the top of the **Recent items** list.</span></span>
-   <span data-ttu-id="1ce1b-123">Elemente werden im Laufe der Zeit in der Liste nach unten verschoben.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-123">Items will move down in the list over time.</span></span> <span data-ttu-id="1ce1b-124">Sobald die Liste voll ist (erreicht die maximale Anzahl der im Markup angegebenen Elemente), werden ältere Elemente am Ende der Liste entfernt, wenn neue Elemente am Anfang der Liste hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-124">Once the list is full (reaches the maximum number of items specified in markup), older items fall off the bottom of the list as new items are added to the top of the list.</span></span>
-   <span data-ttu-id="1ce1b-125">Wenn ein Element bereits irgendwo in der Liste angezeigt wird, aber wieder darauf zugegriffen wird, wird es wieder an den Anfang der Liste verschoben.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-125">If an item already appears somewhere in the list but is accessed again, it moves back to the top of the list.</span></span>
-   <span data-ttu-id="1ce1b-126">Wenn ein Element fixiert ist, wird es immer noch in der Liste nach unten angezeigt, aber es wird nicht vom unteren Rand entfernt.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-126">If an item is pinned, it will still travel down the list, but it will not fall off the bottom.</span></span> <span data-ttu-id="1ce1b-127">Wenn die Liste voll ist, wird stattdessen das erste nicht angeheftete Element oberhalb des fixierten Elements entfernt, wenn der Liste ein neues Element hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-127">Instead, once the list is full, the first unpinned item above the pinned item will fall off when a new item is added to the list.</span></span>
-   <span data-ttu-id="1ce1b-128">Wenn die Anzahl der fixierten Elemente jemals die maximal zulässige Anzahl von Elementen erreicht, werden der Liste keine neuen Elemente hinzugefügt, bis ein Element gelöst wird.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-128">If the number of pinned items ever reaches the maximum number of items, then no new items will get added to the list until an item is unpinned.</span></span>

## <a name="recent-items-properties"></a><span data-ttu-id="1ce1b-129">Eigenschaften für zuletzt verwendete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ce1b-129">Recent Items Properties</span></span>

<span data-ttu-id="1ce1b-130">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Steuerelement "zuletzt verwendete Elemente".</span><span class="sxs-lookup"><span data-stu-id="1ce1b-130">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Recent Items control.</span></span>

<span data-ttu-id="1ce1b-131">In der Regel wird die Eigenschaft "zuletzt verwendete Elemente" in der Multifunktionsleisten-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der Methode [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-131">Typically, a Recent Items property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="1ce1b-132">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-132">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="1ce1b-133">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-133">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="1ce1b-134">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-134">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="1ce1b-135">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-135">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="1ce1b-136">In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Steuerelement zuletzt verwendete Elemente zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-136">The following table lists the property keys that are associated with the Recent Items control.</span></span>



| <span data-ttu-id="1ce1b-137">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="1ce1b-137">Property Key</span></span>                                                                       | <span data-ttu-id="1ce1b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ce1b-138">Notes</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="1ce1b-139">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="1ce1b-139">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)           | <span data-ttu-id="1ce1b-140">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-140">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="1ce1b-141">Benutzeroberflächen- \_ pkey- \_ entitems</span><span class="sxs-lookup"><span data-stu-id="1ce1b-141">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md) | <span data-ttu-id="1ce1b-142">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-142">Can only be updated through invalidation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1ce1b-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ce1b-143">Remarks</span></span>

<span data-ttu-id="1ce1b-144">Die [iapplicationdocumentlists:: GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) -Methode kann verwendet werden, um die MRU-Liste der Windows-Shell für die Menüband-Anwendung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-144">The [IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) method can be used to retrieve the Windows Shell MRU list for the Ribbon application.</span></span> <span data-ttu-id="1ce1b-145">Das von dieser Methode abgerufene-Objekt kann dann von der Anwendung verwendet werden, um die Daten zu erstellen, die für das Menüband-Framework zum Auffüllen der Liste zuletzt verwendeter **Elemente** im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ce1b-145">The object retrieved by this method can then be used by the application to create the data required by the Ribbon framework to populate the **Recent items** list of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

> [!Note]  
> <span data-ttu-id="1ce1b-146">Wenn Sie diese Methode verwenden, sollte *Listentyp* den Wert aufweisen `ADLT_RECENT` .</span><span class="sxs-lookup"><span data-stu-id="1ce1b-146">When using this method, *listtype* should have the value `ADLT_RECENT`.</span></span>

 

<span data-ttu-id="1ce1b-147">Ein Beispiel für das Implementieren einer MRU-Elementliste in einer Menüband-Framework-Anwendung finden Sie im [Beispiel htmleditribbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="1ce1b-147">For an example of how to implement an MRU items list in a Ribbon framework application, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ce1b-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ce1b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ce1b-149">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ce1b-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="1ce1b-150">**Zuletzt verwendete Elemente (Markup Element)**</span><span class="sxs-lookup"><span data-stu-id="1ce1b-150">**Recent items markup element**</span></span>](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 