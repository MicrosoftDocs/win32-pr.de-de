---
description: Das taubemrefresh Sher-Objekt ist ein Container Objekt, das die Daten für alle hinzugefügten Objekte aktualisieren kann. Der Satz von hinzugefügten Objekten, wobei jedes Element, das von einer-Instanz von einer-Instanz dargestellt wird, als Auflistung und Enumeration behandelt werden kann.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Swap-Aktualisierungs Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961177"
---
# <a name="swbemrefresher-object"></a><span data-ttu-id="48ac8-104">Swap-Aktualisierungs Objekt</span><span class="sxs-lookup"><span data-stu-id="48ac8-104">SWbemRefresher object</span></span>

<span data-ttu-id="48ac8-105">Das **taubemrefresh Sher** -Objekt ist ein Container Objekt, das die Daten für alle hinzugefügten Objekte aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="48ac8-105">The **SWbemRefresher** object is a container object that can refresh the data for all the objects that are added to it.</span></span> <span data-ttu-id="48ac8-106">Einzelne Instanzen und instanzenumeratoren können dem Container hinzugefügt oder daraus entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="48ac8-106">Single instances and instance enumerators can be added or removed from the container.</span></span> <span data-ttu-id="48ac8-107">Der Satz von hinzugefügten Objekten, wobei jedes Element, das [**von einer-**](swbemrefreshableitem.md) Instanz von einer-Instanz dargestellt wird, als Auflistung und Enumeration behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="48ac8-107">The set of added objects, each item represented by an [**SWbemRefreshableItem**](swbemrefreshableitem.md) instance, can be treated as a collection and enumerated.</span></span> <span data-ttu-id="48ac8-108">WMI-Instanzen aus beliebigen Klassen können dem Objekt " **Swap** -Aktualisierungs Modul" hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="48ac8-108">WMI instances from any class can be added to the **SWbemRefresher** object.</span></span> <span data-ttu-id="48ac8-109">Auch wenn es sich bei dem Anbieter für die Instanzdaten nicht um einen Hochleistungs Anbieter handelt, kann das Aktualisier Ende Objekt die Daten nach dem Aktualisierungs-und [**Update aktualisieren.**](swbemrefresher-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="48ac8-109">Even if the provider for the instance data is not a high-performance provider, the refresher object can still update the data on the [**Refresh**](swbemrefresher-refresh.md) call.</span></span> <span data-ttu-id="48ac8-110">Wenn die Daten über einen Hochleistungs Anbieter bereitgestellt werden und die [**autoreconnetct**](swbemrefresher-autoreconnect.md) -Eigenschaft den Wert **true** hat, versucht das Objekt " **Swap** -Aktualisierungs", eine unterbrochene Verbindung mit dem Datenanbieter wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="48ac8-110">If the data is supplied through a high-performance provider and the [**AutoReconnect**](swbemrefresher-autoreconnect.md) property is **TRUE**, then the **SWbemRefresher** object attempts to reestablish a broken connection to the data provider.</span></span> <span data-ttu-id="48ac8-111">Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="48ac8-111">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="48ac8-112">Der Aktualisierungs Vorgang kann durch Aufrufen der Methode " [**Swap. Refresh**](swbemrefresher-refresh.md) " oder der Methode " [**\_ errbemubjectex. Refresh**](swbemobjectex-refresh-.md) " durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="48ac8-112">The refresh operation can be carried out by calling either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="48ac8-113">Member</span><span class="sxs-lookup"><span data-stu-id="48ac8-113">Members</span></span>

<span data-ttu-id="48ac8-114">Das Objekt " **Swap** -Aktualisierungs Programm" verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="48ac8-114">The **SWbemRefresher** object has these types of members:</span></span>

-   [<span data-ttu-id="48ac8-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="48ac8-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="48ac8-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48ac8-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48ac8-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="48ac8-117">Methods</span></span>

<span data-ttu-id="48ac8-118">Das **taubemaktualisierungs** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="48ac8-118">The **SWbemRefresher** object has these methods.</span></span>



| <span data-ttu-id="48ac8-119">Methode</span><span class="sxs-lookup"><span data-stu-id="48ac8-119">Method</span></span>                                        | <span data-ttu-id="48ac8-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48ac8-120">Description</span></span>                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48ac8-121">**Eren**</span><span class="sxs-lookup"><span data-stu-id="48ac8-121">**Add**</span></span>](swbemrefresher-add.md)             | <span data-ttu-id="48ac8-122">Fügt der Auflistung im Aktualisierungs Objekt ein neues Aktualisier bares Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="48ac8-122">Adds a new refreshable object to the collection in the refresher object.</span></span><br/>                   |
| [<span data-ttu-id="48ac8-123">**AddEnum**</span><span class="sxs-lookup"><span data-stu-id="48ac8-123">**AddEnum**</span></span>](swbemrefresher-addenum.md)     | <span data-ttu-id="48ac8-124">Fügt dem Aktualisierungs Objekt einen neuen Enumerator hinzu.</span><span class="sxs-lookup"><span data-stu-id="48ac8-124">Adds a new enumerator to the refresher object.</span></span><br/>                                             |
| [<span data-ttu-id="48ac8-125">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="48ac8-125">**DeleteAll**</span></span>](swbemrefresher-deleteall.md) | <span data-ttu-id="48ac8-126">Entfernt alle Elemente aus der Auflistung im Aktualisierungs-Objekt.</span><span class="sxs-lookup"><span data-stu-id="48ac8-126">Removes all items from the collection in the refresher object.</span></span><br/>                             |
| [<span data-ttu-id="48ac8-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="48ac8-127">**Item**</span></span>](swbemrefresher-item.md)           | <span data-ttu-id="48ac8-128">Gibt ein angegebenes Aktualisierungs Element aus der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="48ac8-128">Returns a specified refresher item from the collection.</span></span><br/>                                    |
| [<span data-ttu-id="48ac8-129">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="48ac8-129">**Refresh**</span></span>](swbemrefresher-refresh.md)     | <span data-ttu-id="48ac8-130">Aktualisiert alle Elemente, die im Aktualisierungs Objekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="48ac8-130">Updates all the items that are contained in the refresher object.</span></span><br/>                          |
| [<span data-ttu-id="48ac8-131">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="48ac8-131">**Remove**</span></span>](swbemrefresher-remove.md)       | <span data-ttu-id="48ac8-132">Entfernt das Aktualisierungs Element Objekt oder den Objekt Satz mit einem angegebenen Index aus dem Aktualisierungs Programm.</span><span class="sxs-lookup"><span data-stu-id="48ac8-132">Removes the refresher item object or object set with a specified index from the refresher.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="48ac8-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48ac8-133">Properties</span></span>

<span data-ttu-id="48ac8-134">Das **taubemaktualisierungs** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="48ac8-134">The **SWbemRefresher** object has these properties.</span></span>



| <span data-ttu-id="48ac8-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="48ac8-135">Property</span></span>                                                         | <span data-ttu-id="48ac8-136">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="48ac8-136">Access type</span></span>          | <span data-ttu-id="48ac8-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48ac8-137">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48ac8-138">**Automatische**</span><span class="sxs-lookup"><span data-stu-id="48ac8-138">**AutoReconnect**</span></span>](swbemrefresher-autoreconnect.md)<br/> | <span data-ttu-id="48ac8-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48ac8-139">Read-only</span></span><br/> | <span data-ttu-id="48ac8-140">Gibt an, ob das Aktualisierungs Programm automatisch erneut eine Verbindung mit einem Remote Anbieter herstellt, wenn die Verbindung getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="48ac8-140">Indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span><br/> |
| [<span data-ttu-id="48ac8-141">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="48ac8-141">**Count**</span></span>](swbemrefresher-count.md)<br/>                 | <span data-ttu-id="48ac8-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48ac8-142">Read-only</span></span><br/> | <span data-ttu-id="48ac8-143">Enthält die Anzahl der Elemente im Aktualisierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="48ac8-143">Contains the number of items in the refresher object.</span></span><br/>                                                      |



 

## <a name="examples"></a><span data-ttu-id="48ac8-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48ac8-144">Examples</span></span>

<span data-ttu-id="48ac8-145">Das folgende Beispiel veranschaulicht das Erstellen eines slibemaktualisierungs-Objekts mithilfe der [**Add**](swbemrefresher-add.md) -Methode und der [**AddEnum**](swbemrefresher-addenum.md) -Methode, um eine einzelne Instanz und eine Enumerationsinstanz zu speichern, die Aktualisierung der Daten und die Verwendung der Item-Eigenschaft zum Abrufen der " [**slibemfreshableitem**](swbemrefreshableitem.md) "-Objekte. </span><span class="sxs-lookup"><span data-stu-id="48ac8-145">The following example illustrates creating an **SWbemRefresher** object, using the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods to store a single instance and an enumeration instance, the refreshing of the data, and using the Item property to obtain the [**SWbemRefreshableItem**](swbemrefreshableitem.md) objects.</span></span>


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a><span data-ttu-id="48ac8-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48ac8-146">Requirements</span></span>



| <span data-ttu-id="48ac8-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48ac8-147">Requirement</span></span> | <span data-ttu-id="48ac8-148">Wert</span><span class="sxs-lookup"><span data-stu-id="48ac8-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48ac8-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48ac8-149">Minimum supported client</span></span><br/> | <span data-ttu-id="48ac8-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48ac8-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48ac8-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48ac8-151">Minimum supported server</span></span><br/> | <span data-ttu-id="48ac8-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48ac8-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48ac8-153">Header</span><span class="sxs-lookup"><span data-stu-id="48ac8-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="48ac8-154"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48ac8-154"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="48ac8-155">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="48ac8-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="48ac8-156"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="48ac8-156"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="48ac8-157">DLL</span><span class="sxs-lookup"><span data-stu-id="48ac8-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48ac8-158"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48ac8-158"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="48ac8-159">CLSID</span><span class="sxs-lookup"><span data-stu-id="48ac8-159">CLSID</span></span><br/>                    | <span data-ttu-id="48ac8-160">CLSID- \_ Austauschprogramm</span><span class="sxs-lookup"><span data-stu-id="48ac8-160">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="48ac8-161">IID</span><span class="sxs-lookup"><span data-stu-id="48ac8-161">IID</span></span><br/>                      | <span data-ttu-id="48ac8-162">IID \_ iswbemfreshsher</span><span class="sxs-lookup"><span data-stu-id="48ac8-162">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="48ac8-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48ac8-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ac8-164">**Swap-aktuableitem**</span><span class="sxs-lookup"><span data-stu-id="48ac8-164">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="48ac8-165">**Austauschen von "errbemubjectex"**</span><span class="sxs-lookup"><span data-stu-id="48ac8-165">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="48ac8-166">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="48ac8-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




