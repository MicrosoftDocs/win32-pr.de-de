---
description: Leitet die von einem angegebenen shellfolderview-Objekt ausgelösten Ereignisse an entsprechende shellfolderviewoc-Ereignishandler weiter.
title: Shellfolderviewoc-Objekt (Shldisp. h)
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
ms.openlocfilehash: b9a2b76f48731bf4c7b515779122503fa2cb02f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960509"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="2fd69-103">Shellfolderviewoc-Objekt</span><span class="sxs-lookup"><span data-stu-id="2fd69-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="2fd69-104">Leitet die von einem angegebenen [**shellfolderview**](shellfolderview.md) -Objekt ausgelösten Ereignisse an entsprechende **shellfolderviewoc** -Ereignishandler weiter.</span><span class="sxs-lookup"><span data-stu-id="2fd69-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="2fd69-105">Member</span><span class="sxs-lookup"><span data-stu-id="2fd69-105">Members</span></span>

<span data-ttu-id="2fd69-106">Das **shellfolderviewoc** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2fd69-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="2fd69-107">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2fd69-107">Events</span></span>](#events)
-   [<span data-ttu-id="2fd69-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="2fd69-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="2fd69-109">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2fd69-109">Events</span></span>

<span data-ttu-id="2fd69-110">Das **shellfolderviewoc** -Objekt enthält diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="2fd69-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="2fd69-111">Ereignis</span><span class="sxs-lookup"><span data-stu-id="2fd69-111">Event</span></span>                                                          | <span data-ttu-id="2fd69-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fd69-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fd69-113">**Enumdone**</span><span class="sxs-lookup"><span data-stu-id="2fd69-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="2fd69-114">Gibt an, dass das [**shellfolderview**](shellfolderview.md) -Objekt das Auflisten des Ordner Inhalts abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="2fd69-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="2fd69-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="2fd69-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="2fd69-116">Gibt an, dass sich der Auswahl Zustand eines oder mehrerer Elemente in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2fd69-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="2fd69-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="2fd69-117">Methods</span></span>

<span data-ttu-id="2fd69-118">Das **shellfolderviewoc** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2fd69-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="2fd69-119">Methode</span><span class="sxs-lookup"><span data-stu-id="2fd69-119">Method</span></span>                                                   | <span data-ttu-id="2fd69-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fd69-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fd69-121">**Setfolderview**</span><span class="sxs-lookup"><span data-stu-id="2fd69-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="2fd69-122">Leitet die Ereignisse des angegebenen [**shellfolderview**](shellfolderview.md) -Objekts an den entsprechenden **shellfolderviewoc** -Ereignishandler weiter.</span><span class="sxs-lookup"><span data-stu-id="2fd69-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2fd69-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fd69-123">Remarks</span></span>

<span data-ttu-id="2fd69-124">Das [**shellfolderview**](shellfolderview.md) -Objekt löst zwei Ereignisse (" [**enumdone**](shellfolderviewoc-enumdone.md) " und " [**SelectionChanged**](shellfolderviewoc-selectionchanged.md)") aus, die in der Regel von Anwendungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2fd69-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="2fd69-125">Einige Anwendungen müssen jedoch Ereignisse aus einer Reihe von **shellfolderview** -Objekten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="2fd69-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="2fd69-126">Beispielsweise kann eine Anwendung ein Webbrowser-Steuerelement hosten, mit dem Benutzer durch eine Reihe von Ordnern navigieren können.</span><span class="sxs-lookup"><span data-stu-id="2fd69-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="2fd69-127">Jeder Ordner verfügt über ein eigenes **shellfolderview** -Objekt mit den zugehörigen Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="2fd69-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="2fd69-128">Die Behandlung dieser Ereignisse kann schwierig sein.</span><span class="sxs-lookup"><span data-stu-id="2fd69-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="2fd69-129">Das **shellfolderviewoc** -Objekt vereinfacht die Ereignis Behandlung in solchen Szenarien.</span><span class="sxs-lookup"><span data-stu-id="2fd69-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="2fd69-130">Sie ermöglicht Anwendungen das Behandeln von Ereignissen für alle [**shellfolderview**](shellfolderview.md) -Objekte mit einem einzigen Paar von **shellfolderviewoc** -Ereignis Handlern.</span><span class="sxs-lookup"><span data-stu-id="2fd69-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="2fd69-131">Jedes Mal, wenn der Benutzer zu einem neuen Ordner navigiert, übergibt die Anwendung das zugehörige **shellfolderview** -Objekt an das **shellfolderviewoc** -Objekt, indem [**setfolderview**](shellfolderviewoc-setfolderview.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2fd69-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="2fd69-132">Wenn dann ein [**enumdone**](shellfolderviewoc-enumdone.md) -oder [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) -Ereignis ausgelöst wird, leitet das **shellfolderviewoc** -Objekt das Ereignis zur Verarbeitung an den eigenen Handler weiter.</span><span class="sxs-lookup"><span data-stu-id="2fd69-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd69-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2fd69-133">Requirements</span></span>



| <span data-ttu-id="2fd69-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fd69-134">Requirement</span></span> | <span data-ttu-id="2fd69-135">Wert</span><span class="sxs-lookup"><span data-stu-id="2fd69-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd69-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fd69-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd69-137">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fd69-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2fd69-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fd69-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd69-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2fd69-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2fd69-140">Header</span><span class="sxs-lookup"><span data-stu-id="2fd69-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fd69-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd69-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2fd69-142">IDL</span><span class="sxs-lookup"><span data-stu-id="2fd69-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fd69-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fd69-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2fd69-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2fd69-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd69-145"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2fd69-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd69-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2fd69-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd69-147">**Shellfolderview**</span><span class="sxs-lookup"><span data-stu-id="2fd69-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 




