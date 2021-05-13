---
description: Gibt die Ereignisse weiter, die von einem angegebenen ShellFolderView-Objekt ausgelöst werden, an die entsprechenden ShellFolderViewOC-Ereignishandler.
title: ShellFolderViewOC-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: 2670578417dc616d30f319887f5281fa5d0615f5
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840871"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="fd440-103">ShellFolderViewOC-Objekt</span><span class="sxs-lookup"><span data-stu-id="fd440-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="fd440-104">Gibt die Ereignisse weiter, die von einem angegebenen [**ShellFolderView-Objekt**](shellfolderview.md) ausgelöst werden, an die entsprechenden **ShellFolderViewOC-Ereignishandler.**</span><span class="sxs-lookup"><span data-stu-id="fd440-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="fd440-105">Member</span><span class="sxs-lookup"><span data-stu-id="fd440-105">Members</span></span>

<span data-ttu-id="fd440-106">Das **ShellFolderViewOC-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="fd440-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="fd440-107">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="fd440-107">Events</span></span>](#events)
-   [<span data-ttu-id="fd440-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="fd440-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="fd440-109">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="fd440-109">Events</span></span>

<span data-ttu-id="fd440-110">Das **ShellFolderViewOC-Objekt** verfügt über diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="fd440-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="fd440-111">Ereignis</span><span class="sxs-lookup"><span data-stu-id="fd440-111">Event</span></span>                                                          | <span data-ttu-id="fd440-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd440-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd440-113">**EnumDone**</span><span class="sxs-lookup"><span data-stu-id="fd440-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="fd440-114">Gibt an, [**dass das ShellFolderView-Objekt**](shellfolderview.md) das Aufzählen des Ordnerinhalts abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="fd440-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="fd440-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="fd440-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="fd440-116">Gibt an, dass sich der Auswahlzustand eines oder mehrere Elemente in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="fd440-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="fd440-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="fd440-117">Methods</span></span>

<span data-ttu-id="fd440-118">Das **ShellFolderViewOC-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fd440-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="fd440-119">Methode</span><span class="sxs-lookup"><span data-stu-id="fd440-119">Method</span></span>                                                   | <span data-ttu-id="fd440-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd440-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd440-121">**SetFolderView**</span><span class="sxs-lookup"><span data-stu-id="fd440-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="fd440-122">Gibt die Ereignisse des angegebenen [**ShellFolderView-Objekts**](shellfolderview.md) an den entsprechenden **ShellFolderViewOC-Ereignishandler** weiter.</span><span class="sxs-lookup"><span data-stu-id="fd440-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd440-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd440-123">Remarks</span></span>

<span data-ttu-id="fd440-124">Das [**ShellFolderView-Objekt**](shellfolderview.md) gibt zwei Ereignisse aus, [**EnumDone**](shellfolderviewoc-enumdone.md) und [**SelectionChanged,**](shellfolderviewoc-selectionchanged.md)die in der Regel von Anwendungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="fd440-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="fd440-125">Einige Anwendungen müssen jedoch Ereignisse aus einer Reihe von **ShellFolderView-Objekten** verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fd440-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="fd440-126">Beispielsweise kann eine Anwendung ein WebBrowser-Steuerelement hosten, mit dem Benutzer durch eine Reihe von Ordnern navigieren können.</span><span class="sxs-lookup"><span data-stu-id="fd440-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="fd440-127">Jeder Ordner verfügt über ein **eigenes ShellFolderView-Objekt** mit den zugehörigen Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="fd440-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="fd440-128">Die Behandlung dieser Ereignisse kann schwierig sein.</span><span class="sxs-lookup"><span data-stu-id="fd440-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="fd440-129">Das **ShellFolderViewOC-Objekt** vereinfacht die Ereignisbehandlung für solche Szenarien.</span><span class="sxs-lookup"><span data-stu-id="fd440-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="fd440-130">Dadurch können Anwendungen Ereignisse für alle [**ShellFolderView-Objekte**](shellfolderview.md) mit einem einzelnen Paar von **ShellFolderViewOC-Ereignishandlern** behandeln.</span><span class="sxs-lookup"><span data-stu-id="fd440-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="fd440-131">Jedes Mal, wenn der Benutzer zu einem neuen Ordner navigiert, übergibt die Anwendung das zugeordnete **ShellFolderView-Objekt** durch Aufrufen von [**SetFolderView**](shellfolderviewoc-setfolderview.md)an das **ShellFolderViewOC-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="fd440-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="fd440-132">Wenn dann ein [**EnumDone-**](shellfolderviewoc-enumdone.md) oder [**SelectionChanged-Ereignis**](shellfolderviewoc-selectionchanged.md) ausgelöst wird, leitet das **ShellFolderViewOC-Objekt** das Ereignis zur Verarbeitung an seinen eigenen Handler weiter.</span><span class="sxs-lookup"><span data-stu-id="fd440-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd440-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd440-133">Requirements</span></span>



| <span data-ttu-id="fd440-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd440-134">Requirement</span></span> | <span data-ttu-id="fd440-135">Wert</span><span class="sxs-lookup"><span data-stu-id="fd440-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd440-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd440-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fd440-137">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd440-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd440-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd440-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fd440-139">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd440-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd440-140">Header</span><span class="sxs-lookup"><span data-stu-id="fd440-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd440-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="fd440-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fd440-142">Idl</span><span class="sxs-lookup"><span data-stu-id="fd440-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd440-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd440-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fd440-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fd440-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd440-145"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fd440-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd440-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd440-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd440-147">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="fd440-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 




