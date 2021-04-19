---
description: Die-Methoden und-Eigenschaften des-Objekts von "taubemlasterror" enthalten Fehler Objekte und bearbeiten diese.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Taubemlasterror-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348885"
---
# <a name="swbemlasterror-object"></a><span data-ttu-id="063c3-103">Taubemlasterror-Objekt</span><span class="sxs-lookup"><span data-stu-id="063c3-103">SWbemLastError object</span></span>

<span data-ttu-id="063c3-104">Die-Methoden und-Eigenschaften des-Objekts von " **taubemlasterror** " enthalten Fehler Objekte und bearbeiten diese.</span><span class="sxs-lookup"><span data-stu-id="063c3-104">The methods and properties of the **SWbemLastError** object contain and manipulate error objects.</span></span> <span data-ttu-id="063c3-105">Die Methoden und Eigenschaften dieses Objekts sind identisch mit denen des WS [**-Objekts,**](swbemobject.md) werden jedoch verwendet, um Fehlerinformationen anstelle von WMI-Klassen Informationen zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="063c3-105">The methods and properties of this object are exactly the same as those of the [**SWbemObject**](swbemobject.md) object, but are used to contain error information instead of WMI class information.</span></span> <span data-ttu-id="063c3-106">Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="063c3-106">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="063c3-107">Sie können das Fehler Objekt " **taubemlasterror** " erstellen, um die erweiterten Fehlerinformationen zu überprüfen, die einem vorherigen Methoden Aufruftyp zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="063c3-107">You can create an **SWbemLastError** error object to inspect the extended error information that is associated with a previous method call.</span></span> <span data-ttu-id="063c3-108">Wenn keine Fehlerinformationen verfügbar sind, tritt beim Versuch, ein Fehler Objekt zu erstellen, ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="063c3-108">If error information is not available, an attempt to create an error object will fail.</span></span> <span data-ttu-id="063c3-109">Wenn der-Vorgang erfolgreich ist und ein Fehler Objekt zurückgibt, wird der Status des Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="063c3-109">If the call succeeds and an error object returns, the status of the object is reset.</span></span> <span data-ttu-id="063c3-110">Weitere Versuche, ein Fehler Objekt abzurufen, schlagen fehl, bis ein neuer Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="063c3-110">Further attempts to retrieve an error object will fail until a new error occurs.</span></span> <span data-ttu-id="063c3-111">Wenn Sie einen asynchronen-Rückruf ausführen, der fehlschlägt, kann ein " **slibemlasterror** "-Objekt vom Ereignis " [**slibemsink. onabgeschlossene**](swbemsink-oncompleted.md) " im Parameter " *objWbemErrorObject* " zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="063c3-111">If you make an asynchronous call that fails, an **SWbemLastError** object may be returned to you by the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event in the *objWbemErrorObject* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="063c3-112">Member</span><span class="sxs-lookup"><span data-stu-id="063c3-112">Members</span></span>

<span data-ttu-id="063c3-113">Das Objekt " **taubemlasterror** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="063c3-113">The **SWbemLastError** object has these types of members:</span></span>

-   [<span data-ttu-id="063c3-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="063c3-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="063c3-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="063c3-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="063c3-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="063c3-116">Methods</span></span>

<span data-ttu-id="063c3-117">Das **taubemlasterror** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="063c3-117">The **SWbemLastError** object has these methods.</span></span>



| <span data-ttu-id="063c3-118">Methode</span><span class="sxs-lookup"><span data-stu-id="063c3-118">Method</span></span>                                                   | <span data-ttu-id="063c3-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="063c3-119">Description</span></span>                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="063c3-120">**ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-120">**Associators\_**</span></span>                                        | <span data-ttu-id="063c3-121">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-121">Not used.</span></span> <span data-ttu-id="063c3-122">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-122">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-123">**Associatorsasync\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-123">**AssociatorsAsync\_**</span></span>                                   | <span data-ttu-id="063c3-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-124">Not used.</span></span> <span data-ttu-id="063c3-125">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-125">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="063c3-126">**Klon\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-126">**Clone\_**</span></span>](swbemlasterror-clone-.md)                 | <span data-ttu-id="063c3-127">Erstellt eine Kopie des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="063c3-127">Makes a copy of the current object.</span></span><br/>                                               |
| [<span data-ttu-id="063c3-128">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-128">**CompareTo\_**</span></span>](swbemlasterror-compareto-.md)         | <span data-ttu-id="063c3-129">Testet zwei-Objekte auf Gleichheit.</span><span class="sxs-lookup"><span data-stu-id="063c3-129">Tests two objects for equality.</span></span><br/>                                                   |
| <span data-ttu-id="063c3-130">**Lösch\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-130">**Delete\_**</span></span>                                             | <span data-ttu-id="063c3-131">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-131">Not used.</span></span> <span data-ttu-id="063c3-132">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-132">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-133">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-133">**DeleteAsync\_**</span></span>                                        | <span data-ttu-id="063c3-134">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-134">Not used.</span></span> <span data-ttu-id="063c3-135">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-135">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-136">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-136">**ExecMethod\_**</span></span>                                         | <span data-ttu-id="063c3-137">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-137">Not used.</span></span> <span data-ttu-id="063c3-138">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-138">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-139">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-139">**ExecMethodAsync\_**</span></span>                                    | <span data-ttu-id="063c3-140">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-140">Not used.</span></span> <span data-ttu-id="063c3-141">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-141">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="063c3-142">**Getobjecttext\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-142">**GetObjectText\_**</span></span>](swbemlasterror-getobjecttext-.md) | <span data-ttu-id="063c3-143">Ruft die Textdarstellung des-Objekts ab, das mit der MOF-Syntax geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="063c3-143">Retrieves the textual representation of the object written with MOF syntax.</span></span><br/>       |
| <span data-ttu-id="063c3-144">**Instanzen\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-144">**Instances\_**</span></span>                                          | <span data-ttu-id="063c3-145">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-145">Not used.</span></span> <span data-ttu-id="063c3-146">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-146">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-147">**Instancesasync\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-147">**InstancesAsync\_**</span></span>                                     | <span data-ttu-id="063c3-148">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-148">Not used.</span></span> <span data-ttu-id="063c3-149">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-149">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-150">**Stellte\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-150">**Put\_**</span></span>                                                | <span data-ttu-id="063c3-151">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-151">Not used.</span></span> <span data-ttu-id="063c3-152">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-152">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-153">**Putasync\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-153">**PutAsync\_**</span></span>                                           | <span data-ttu-id="063c3-154">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-154">Not used.</span></span> <span data-ttu-id="063c3-155">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-155">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-156">**References\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-156">**References\_**</span></span>                                         | <span data-ttu-id="063c3-157">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-157">Not used.</span></span> <span data-ttu-id="063c3-158">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-158">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-159">**Referencesasync\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-159">**ReferencesAsync\_**</span></span>                                    | <span data-ttu-id="063c3-160">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-160">Not used.</span></span> <span data-ttu-id="063c3-161">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-161">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-162">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-162">**SpawnDerivedClass\_**</span></span>                                  | <span data-ttu-id="063c3-163">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-163">Not used.</span></span> <span data-ttu-id="063c3-164">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-164">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-165">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-165">**SpawnInstance\_**</span></span>                                      | <span data-ttu-id="063c3-166">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-166">Not used.</span></span> <span data-ttu-id="063c3-167">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-167">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-168">**Unterklassen von  werden erstellt.\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-168">**Subclasses\_**</span></span>                                         | <span data-ttu-id="063c3-169">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-169">Not used.</span></span> <span data-ttu-id="063c3-170">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-170">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="063c3-171">**Subclassesasync\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-171">**SubclassesAsync\_**</span></span>                                    | <span data-ttu-id="063c3-172">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-172">Not used.</span></span> <span data-ttu-id="063c3-173">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-173">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="063c3-174">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="063c3-174">Properties</span></span>

<span data-ttu-id="063c3-175">Das **taubemlasterror** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="063c3-175">The **SWbemLastError** object has these properties.</span></span>



| <span data-ttu-id="063c3-176">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="063c3-176">Property</span></span>                                                      | <span data-ttu-id="063c3-177">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="063c3-177">Access type</span></span>          | <span data-ttu-id="063c3-178">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="063c3-178">Description</span></span>                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="063c3-179">**Ableitung\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-179">**Derivation\_**</span></span><br/>                                   | <span data-ttu-id="063c3-180">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="063c3-180">Read-only</span></span><br/> | <span data-ttu-id="063c3-181">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-181">Not used.</span></span> <span data-ttu-id="063c3-182">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-182">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="063c3-183">**Methoden\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-183">**Methods\_**</span></span> <br/>                                     | <span data-ttu-id="063c3-184">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="063c3-184">Read-only</span></span><br/> | <span data-ttu-id="063c3-185">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-185">Not used.</span></span> <span data-ttu-id="063c3-186">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-186">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| [<span data-ttu-id="063c3-187">**ADS\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-187">**Path\_**</span></span>](swbemlasterror-path-.md)<br/>             | <span data-ttu-id="063c3-188">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="063c3-188">Read-only</span></span><br/> | <span data-ttu-id="063c3-189">Enthält ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="063c3-189">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/>                    |
| [<span data-ttu-id="063c3-190">**Eigenschaften\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-190">**Properties\_**</span></span>](swbemlasterror-properties-.md)<br/> | <span data-ttu-id="063c3-191">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="063c3-191">Read-only</span></span><br/> | <span data-ttu-id="063c3-192">Stellt die Auflistung von Eigenschaften des-Objekts von " **Swap LastError** " dar.</span><span class="sxs-lookup"><span data-stu-id="063c3-192">Represents the collection of properties of the **SWbemLastError** object.</span></span> <span data-ttu-id="063c3-193">Bei dieser Eigenschaft handelt es sich um ein Objekt vom [**typaustausch**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="063c3-193">This property is an [**SWbemPropertySet**](swbempropertyset.md) object.</span></span><br/> |
| <span data-ttu-id="063c3-194">**Qualifikation\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-194">**Qualifiers\_**</span></span><br/>                                   | <span data-ttu-id="063c3-195">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="063c3-195">Read-only</span></span><br/> | <span data-ttu-id="063c3-196">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-196">Not used.</span></span> <span data-ttu-id="063c3-197">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-197">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="063c3-198">**Sicherheit\_**</span><span class="sxs-lookup"><span data-stu-id="063c3-198">**Security\_**</span></span><br/>                                     | <span data-ttu-id="063c3-199">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="063c3-199">Read-only</span></span><br/> | <span data-ttu-id="063c3-200">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="063c3-200">Not used.</span></span> <span data-ttu-id="063c3-201">Das [**errbemujeject**](swbemobject.md) -Objekt bietet dieselbe Methode.</span><span class="sxs-lookup"><span data-stu-id="063c3-201">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |



 

## <a name="examples"></a><span data-ttu-id="063c3-202">Beispiele</span><span class="sxs-lookup"><span data-stu-id="063c3-202">Examples</span></span>

<span data-ttu-id="063c3-203">Das folgende VBScript-Beispiel veranschaulicht, wie Fehler-und Fehler Objektinformationen überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="063c3-203">The following VBScript sample demonstrates how to inspect error and error object information.</span></span>


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



<span data-ttu-id="063c3-204">Das folgende perl-Beispiel veranschaulicht, wie Fehler-und Fehler Objektinformationen überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="063c3-204">The following Perl sample demonstrates how to inspect error and error object information.</span></span>


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a><span data-ttu-id="063c3-205">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="063c3-205">Requirements</span></span>



| <span data-ttu-id="063c3-206">Anforderung</span><span class="sxs-lookup"><span data-stu-id="063c3-206">Requirement</span></span> | <span data-ttu-id="063c3-207">Wert</span><span class="sxs-lookup"><span data-stu-id="063c3-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="063c3-208">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="063c3-208">Minimum supported client</span></span><br/> | <span data-ttu-id="063c3-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="063c3-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="063c3-210">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="063c3-210">Minimum supported server</span></span><br/> | <span data-ttu-id="063c3-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="063c3-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="063c3-212">Header</span><span class="sxs-lookup"><span data-stu-id="063c3-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="063c3-213"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="063c3-213"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="063c3-214">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="063c3-214">Type library</span></span><br/>             | <dl> <span data-ttu-id="063c3-215"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="063c3-215"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="063c3-216">DLL</span><span class="sxs-lookup"><span data-stu-id="063c3-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="063c3-217"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="063c3-217"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="063c3-218">CLSID</span><span class="sxs-lookup"><span data-stu-id="063c3-218">CLSID</span></span><br/>                    | <span data-ttu-id="063c3-219">CLSID- \_ Austausch Fehler</span><span class="sxs-lookup"><span data-stu-id="063c3-219">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="063c3-220">IID</span><span class="sxs-lookup"><span data-stu-id="063c3-220">IID</span></span><br/>                      | <span data-ttu-id="063c3-221">IID \_ iswbemlasterror</span><span class="sxs-lookup"><span data-stu-id="063c3-221">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="063c3-222">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="063c3-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="063c3-223">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="063c3-223">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




