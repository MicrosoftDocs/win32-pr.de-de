---
description: Sie können die Methoden und Eigenschaften des Objekts "errbewbject" verwenden, um eine Windows-Verwaltungsinstrumentation (WMI)-Klassendefinition oder-Objektinstanz darzustellen.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Errbebobject-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360165"
---
# <a name="swbemobject-object"></a><span data-ttu-id="11d77-103">Errbejebject-Objekt</span><span class="sxs-lookup"><span data-stu-id="11d77-103">SWbemObject object</span></span>

<span data-ttu-id="11d77-104">Sie können die Methoden und Eigenschaften des Objekts " **errbewbject** " verwenden, um eine Windows-Verwaltungsinstrumentation (WMI)-Klassendefinition oder-Objektinstanz darzustellen.</span><span class="sxs-lookup"><span data-stu-id="11d77-104">You can use the methods and properties of the **SWbemObject** object to represent one Windows Management Instrumentation (WMI) class definition or object instance.</span></span> <span data-ttu-id="11d77-105">Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](/previous-versions//xzysf6hc(v=vs.85)) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="11d77-105">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

<span data-ttu-id="11d77-106">Dieses Objekt unterstützt zwei Typen von Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="11d77-106">This object supports two types of properties and methods.</span></span> <span data-ttu-id="11d77-107">Die in diesem Abschnitt definierten generischen Eigenschaften und Methoden, die für alle WMI-Objekte gelten.</span><span class="sxs-lookup"><span data-stu-id="11d77-107">Those defined in this section are generic properties and methods that apply to all WMI objects.</span></span> <span data-ttu-id="11d77-108">Darüber hinaus macht dieses-Objekt die Eigenschaften und Methoden des zugrunde liegenden Objekts als dynamische Automatisierungs Eigenschaften und-Methoden von " **errbemubject**" verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11d77-108">In addition, this object exposes the properties and methods of the underlying object as dynamic automation properties and methods of **SWbemObject**.</span></span> <span data-ttu-id="11d77-109">Die Namen und Typen dieser Eigenschaften und Methoden hängen vom zugrunde liegenden WMI-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="11d77-109">The names and types of these properties and methods depend on the underlying WMI object.</span></span> <span data-ttu-id="11d77-110">Weitere Informationen darüber, wie diese dynamischen Eigenschaften und Methoden verfügbar gemacht werden, finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="11d77-110">For more information about how these dynamic properties and methods are exposed, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="11d77-111">In der WMI-Client Perspektive ist dieses Objekt immer in Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="11d77-111">From the WMI client perspective, this object is always in-process.</span></span> <span data-ttu-id="11d77-112">Schreibvorgänge wirken sich nur auf die lokale Kopie des Objekts aus, und Lesevorgänge rufen immer Werte aus der lokalen Kopie ab.</span><span class="sxs-lookup"><span data-stu-id="11d77-112">Write operations only affect the local copy of the object, and read operations always retrieve values from the local copy.</span></span> <span data-ttu-id="11d77-113">Updates für WMI werden nur ausgeführt, wenn ganze Objekte mithilfe eines Aufrufes der Methode " [**errbemubject \_ . Put**](swbemobject-put-.md) " geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="11d77-113">Updates to WMI are performed only when entire objects are written using a call to the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span> <span data-ttu-id="11d77-114">Wenn Sie die Eigenschaften oder Methoden in einem " **errbemubject** "-Objekt ändern, werden die Änderungen erst in WMI geschrieben, wenn Sie " **errbemubject. Put \_**" aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="11d77-114">If you modify the properties or methods in an **SWbemObject** object, your changes are not written to WMI until you call **SWbemObject.Put\_**.</span></span>

<span data-ttu-id="11d77-115">Die in diesem Abschnitt definierten generischen Methoden-und Eigenschaftsnamen enden immer mit einem nachfolgenden Unterstrich (" \_ "), um Sie von den dynamischen WMI-Methoden und-Eigenschaften des zugrunde liegenden Objekts zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="11d77-115">The generic method and property names defined in this section always end with a trailing underscore ("\_") to differentiate them from the dynamic WMI methods and properties of the underlying object.</span></span>

<span data-ttu-id="11d77-116">Beachten Sie **, dass das-** Objekt mit der VBScript-Methode " [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). Method" nicht erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="11d77-116">Note that **SWbemObject** cannot be created using the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).method.</span></span> <span data-ttu-id="11d77-117">Wenn Sie eine neue, leere Klasse erstellen möchten [**, verwenden Sie**](swbemservices-get.md) die-Klasse mit einem leeren path-Parameter.</span><span class="sxs-lookup"><span data-stu-id="11d77-117">If you want to create a new, empty class use [**SWbemServices.Get**](swbemservices-get.md) with an empty path parameter.</span></span> <span data-ttu-id="11d77-118">Dieser Befehl gibt ein leeres **errbejebject** -Objekt zurück, das eine Klasse werden kann.</span><span class="sxs-lookup"><span data-stu-id="11d77-118">This call returns an empty **SWbemObject** object that can become a class.</span></span> <span data-ttu-id="11d77-119">Sie können dann einen Klassennamen für die [**Class**](swbemobjectpath-class.md) -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts angeben, das vom [**path \_**](swbemobject-path-.md) -Befehl zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="11d77-119">You can then supply a class name for the [**Class**](swbemobjectpath-class.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the [**Path\_**](swbemobject-path-.md) call.</span></span> <span data-ttu-id="11d77-120">Fügen Sie der neuen Klasse mithilfe der [**Properties \_**](swbemobject-properties-.md) -Methode Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="11d77-120">Add properties to the new class by the [**Properties\_**](swbemobject-properties-.md) method.</span></span> <span data-ttu-id="11d77-121">Um eine Instanz zu erstellen, rufen Sie **GetObject** für die neue Klasse auf.</span><span class="sxs-lookup"><span data-stu-id="11d77-121">To create an instance, call **GetObject** on the new class.</span></span>

<span data-ttu-id="11d77-122">Im folgenden Codebeispiel wird gezeigt, wie Sie eine neue Klasse abrufen und ihr eine Eigenschaft hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="11d77-122">The following code example shows how to obtain a new class and add a property to it.</span></span> <span data-ttu-id="11d77-123">Das-Objekt, das die-Klasse darstellt, muss durch einen- **Befehl** [**Put \_**](swbemobject-put-.md)zurück in das WMI-Repository geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="11d77-123">The **SWbemObject** object that represents the class must be written back to the WMI repository by a call to [**Put\_**](swbemobject-put-.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



<span data-ttu-id="11d77-124">Sie können das Repository mit einem Anzeige Tool wie [CIM Studio](further-information.md) untersuchen, um zu überprüfen, ob die neue Klasse und Instanz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="11d77-124">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="11d77-125">Ein Beispiel für das Entfernen einer Klasse und einer Instanz aus dem Repository finden Sie unter " [**errbemservices. Delete**](swbemservices-delete.md) " oder " [**errbemubject. Delete \_**](swbemobject-delete-.md)".</span><span class="sxs-lookup"><span data-stu-id="11d77-125">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="members"></a><span data-ttu-id="11d77-126">Member</span><span class="sxs-lookup"><span data-stu-id="11d77-126">Members</span></span>

<span data-ttu-id="11d77-127">Das " **errbemubject** "-Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11d77-127">The **SWbemObject** object has these types of members:</span></span>

-   [<span data-ttu-id="11d77-128">Methoden</span><span class="sxs-lookup"><span data-stu-id="11d77-128">Methods</span></span>](#methods)
-   [<span data-ttu-id="11d77-129">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11d77-129">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="11d77-130">Methoden</span><span class="sxs-lookup"><span data-stu-id="11d77-130">Methods</span></span>

<span data-ttu-id="11d77-131">Das Objekt " **errbemubject** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="11d77-131">The **SWbemObject** object has these methods.</span></span>



| <span data-ttu-id="11d77-132">Methode</span><span class="sxs-lookup"><span data-stu-id="11d77-132">Method</span></span>                                                        | <span data-ttu-id="11d77-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11d77-133">Description</span></span>                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11d77-134">**ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-134">**Associators\_**</span></span>](swbemobject-associators-.md)             | <span data-ttu-id="11d77-135">Ruft die assoziatoren des-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="11d77-135">Retrieves the associators of the object.</span></span><br/>                                                     |
| [<span data-ttu-id="11d77-136">**Associatorsasync\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-136">**AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)   | <span data-ttu-id="11d77-137">Ruft die assoziatoren des-Objekts asynchron ab.</span><span class="sxs-lookup"><span data-stu-id="11d77-137">Asynchronously retrieves the associators of the object.</span></span><br/>                                      |
| [<span data-ttu-id="11d77-138">**Klon\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-138">**Clone\_**</span></span>](swbemobject-clone-.md)                         | <span data-ttu-id="11d77-139">Erstellt eine Kopie des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="11d77-139">Makes a copy of the current object.</span></span><br/>                                                          |
| [<span data-ttu-id="11d77-140">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-140">**CompareTo\_**</span></span>](swbemobject-compareto-.md)                 | <span data-ttu-id="11d77-141">Testet zwei-Objekte auf Gleichheit.</span><span class="sxs-lookup"><span data-stu-id="11d77-141">Tests two objects for equality.</span></span><br/>                                                              |
| [<span data-ttu-id="11d77-142">**Lösch\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-142">**Delete\_**</span></span>](swbemobject-delete-.md)                       | <span data-ttu-id="11d77-143">Löscht das-Objekt aus WMI.</span><span class="sxs-lookup"><span data-stu-id="11d77-143">Deletes the object from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="11d77-144">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-144">**DeleteAsync\_**</span></span>](swbemobject-deleteasync-.md)             | <span data-ttu-id="11d77-145">Löscht das Objekt asynchron aus WMI.</span><span class="sxs-lookup"><span data-stu-id="11d77-145">Asynchronously deletes the object from WMI.</span></span><br/>                                                  |
| [<span data-ttu-id="11d77-146">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-146">**ExecMethod\_**</span></span>](swbemobject-execmethod-.md)               | <span data-ttu-id="11d77-147">Führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="11d77-147">Executes a method exported by a method provider.</span></span><br/>                                             |
| [<span data-ttu-id="11d77-148">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-148">**ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)     | <span data-ttu-id="11d77-149">Führt eine Methode, die von einem Methoden Anbieter exportiert wurde, asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="11d77-149">Asynchronously executes a method exported by a method provider.</span></span><br/>                              |
| [<span data-ttu-id="11d77-150">**Getobjecttext\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-150">**GetObjectText\_**</span></span>](swbemobject-getobjecttext-.md)         | <span data-ttu-id="11d77-151">Ruft die Textdarstellung des-Objekts (MOF-Syntax) ab.</span><span class="sxs-lookup"><span data-stu-id="11d77-151">Retrieves the textual representation of the object (MOF syntax).</span></span><br/>                             |
| [<span data-ttu-id="11d77-152">**Instanzen\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-152">**Instances\_**</span></span>](swbemobject-instances-.md)                 | <span data-ttu-id="11d77-153">Gibt eine Auflistung von Instanzen des-Objekts zurück (bei der es sich um eine WMI-Klasse handeln muss).</span><span class="sxs-lookup"><span data-stu-id="11d77-153">Returns a collection of instances of the object (which must be a WMI class).</span></span><br/>                 |
| [<span data-ttu-id="11d77-154">**Instancesasync\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-154">**InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)       | <span data-ttu-id="11d77-155">Gibt asynchron eine Auflistung von Instanzen des-Objekts zurück (bei der es sich um eine WMI-Klasse handeln muss).</span><span class="sxs-lookup"><span data-stu-id="11d77-155">Asynchronously returns a collection of instances of the object (which must be a WMI class).</span></span><br/>  |
| [<span data-ttu-id="11d77-156">**Stellte\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-156">**Put\_**</span></span>](swbemobject-put-.md)                             | <span data-ttu-id="11d77-157">Erstellt oder aktualisiert das Objekt in WMI.</span><span class="sxs-lookup"><span data-stu-id="11d77-157">Creates or updates the object in WMI.</span></span><br/>                                                        |
| [<span data-ttu-id="11d77-158">**Putasync\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-158">**PutAsync\_**</span></span>](swbemobject-putasync-.md)                   | <span data-ttu-id="11d77-159">Erstellt oder aktualisiert das Objekt asynchron in WMI.</span><span class="sxs-lookup"><span data-stu-id="11d77-159">Asynchronously creates or updates the object in WMI.</span></span><br/>                                         |
| [<span data-ttu-id="11d77-160">**References\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-160">**References\_**</span></span>](swbemobject-references-.md)               | <span data-ttu-id="11d77-161">Gibt Verweise auf das-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="11d77-161">Returns references to the object.</span></span><br/>                                                            |
| [<span data-ttu-id="11d77-162">**Referencesasync\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-162">**ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)     | <span data-ttu-id="11d77-163">Gibt Verweise auf das-Objekt asynchron zurück.</span><span class="sxs-lookup"><span data-stu-id="11d77-163">Asynchronously returns references to the object.</span></span><br/>                                             |
| [<span data-ttu-id="11d77-164">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-164">**SpawnDerivedClass\_**</span></span>](swbemobject-spawnderivedclass-.md) | <span data-ttu-id="11d77-165">Erstellt eine neue abgeleitete Klasse aus dem aktuellen-Objekt (das eine WMI-Klasse sein muss).</span><span class="sxs-lookup"><span data-stu-id="11d77-165">Creates a new derived class from the current object (which must be a WMI class).</span></span><br/>             |
| [<span data-ttu-id="11d77-166">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-166">**SpawnInstance\_**</span></span>](swbemobject-spawninstance-.md)         | <span data-ttu-id="11d77-167">Erstellt eine neue-Instanz aus dem aktuellen-Objekt.</span><span class="sxs-lookup"><span data-stu-id="11d77-167">Creates a new instance from the current object.</span></span><br/>                                              |
| [<span data-ttu-id="11d77-168">**Unterklassen von  werden erstellt.\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-168">**Subclasses\_**</span></span>](swbemobject-subclasses-.md)               | <span data-ttu-id="11d77-169">Gibt eine Auflistung von Unterklassen des-Objekts zurück (bei dem es sich um eine WMI-Klasse handeln muss).</span><span class="sxs-lookup"><span data-stu-id="11d77-169">Returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/>                |
| [<span data-ttu-id="11d77-170">**Subclassesasync\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-170">**SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)     | <span data-ttu-id="11d77-171">Gibt asynchron eine Auflistung von Unterklassen des-Objekts zurück (bei der es sich um eine WMI-Klasse handeln muss).</span><span class="sxs-lookup"><span data-stu-id="11d77-171">Asynchronously returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="11d77-172">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11d77-172">Properties</span></span>

<span data-ttu-id="11d77-173">Das " **errbemubject** "-Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="11d77-173">The **SWbemObject** object has these properties.</span></span>



| <span data-ttu-id="11d77-174">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="11d77-174">Property</span></span>                                                   | <span data-ttu-id="11d77-175">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="11d77-175">Access type</span></span>          | <span data-ttu-id="11d77-176">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11d77-176">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11d77-177">**Ableitung\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-177">**Derivation\_**</span></span>](swbemobject-derivation-.md)<br/> | <span data-ttu-id="11d77-178">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11d77-178">Read-only</span></span><br/> | <span data-ttu-id="11d77-179">Enthält ein Array von Zeichen folgen, das die abderivations Hierarchie für die-Klasse beschreibt.</span><span class="sxs-lookup"><span data-stu-id="11d77-179">Contains an array of strings that describes the derivation hierarchy for the class.</span></span><br/>                                             |
| [<span data-ttu-id="11d77-180">**Methoden\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-180">**Methods\_**</span></span>](swbemobject-methods-.md)<br/>       | <span data-ttu-id="11d77-181">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11d77-181">Read-only</span></span><br/> | <span data-ttu-id="11d77-182">Ein " [**taubemmethodset**](swbemmethodset.md) "-Objekt, das die Auflistung von Methoden für dieses-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="11d77-182">An [**SWbemMethodSet**](swbemmethodset.md) object that is the collection of methods for this object.</span></span><br/>                           |
| [<span data-ttu-id="11d77-183">**ADS\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-183">**Path\_**</span></span>](swbemobject-path-.md)<br/>             | <span data-ttu-id="11d77-184">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11d77-184">Read-only</span></span><br/> | <span data-ttu-id="11d77-185">Enthält ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="11d77-185">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/> |
| [<span data-ttu-id="11d77-186">**Eigenschaften\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-186">**Properties\_**</span></span>](swbemobject-properties-.md)<br/> | <span data-ttu-id="11d77-187">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11d77-187">Read-only</span></span><br/> | <span data-ttu-id="11d77-188">Ein-Objekt, das die Auflistung von Eigenschaften für [**dieses Objekt ist**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="11d77-188">An [**SWbemPropertySet**](swbempropertyset.md) object that is the collection of properties for this object.</span></span><br/>                    |
| [<span data-ttu-id="11d77-189">**Qualifikation\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-189">**Qualifiers\_**</span></span>](swbemobject-qualifiers-.md)<br/> | <span data-ttu-id="11d77-190">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11d77-190">Read-only</span></span><br/> | <span data-ttu-id="11d77-191">Ein " [**taubemqualifierset**](swbemqualifierset.md) "-Objekt, das die Auflistung der Qualifizierer für dieses Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="11d77-191">An [**SWbemQualifierSet**](swbemqualifierset.md) object that is the collection of qualifiers for this object.</span></span><br/>                  |
| [<span data-ttu-id="11d77-192">**Sicherheit\_**</span><span class="sxs-lookup"><span data-stu-id="11d77-192">**Security\_**</span></span>](swbemobject-security-.md)<br/>     | <span data-ttu-id="11d77-193">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11d77-193">Read-only</span></span><br/> | <span data-ttu-id="11d77-194">Enthält ein " [**Swap Security**](swbemsecurity.md) "-Objekt, das zum Lesen oder Ändern der Sicherheitseinstellungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11d77-194">Contains an [**SWbemSecurity**](swbemsecurity.md) object used to read or change the security settings.</span></span><br/>                         |



 

## <a name="examples"></a><span data-ttu-id="11d77-195">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11d77-195">Examples</span></span>

<span data-ttu-id="11d77-196">Die [Liste alle Eigenschaften und Methoden für ein WMI-Klassen](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) -VBScript-Codebeispiel in der TechNet Gallery verwendet das "slibemubject", um alle Methoden und Eigenschaften für eine angegebene WMI-Klasse aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="11d77-196">The [List All the Properties and Methods for a WMI Class](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) VBScript code sample on TechNet Gallery uses the SWbemObject to list all of the methods and properties for a specified WMI class.</span></span>

## <a name="requirements"></a><span data-ttu-id="11d77-197">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11d77-197">Requirements</span></span>



| <span data-ttu-id="11d77-198">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11d77-198">Requirement</span></span> | <span data-ttu-id="11d77-199">Wert</span><span class="sxs-lookup"><span data-stu-id="11d77-199">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11d77-200">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11d77-200">Minimum supported client</span></span><br/> | <span data-ttu-id="11d77-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11d77-201">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11d77-202">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11d77-202">Minimum supported server</span></span><br/> | <span data-ttu-id="11d77-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11d77-203">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11d77-204">Header</span><span class="sxs-lookup"><span data-stu-id="11d77-204">Header</span></span><br/>                   | <dl> <span data-ttu-id="11d77-205"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d77-205"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="11d77-206">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="11d77-206">Type library</span></span><br/>             | <dl> <span data-ttu-id="11d77-207"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="11d77-207"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="11d77-208">DLL</span><span class="sxs-lookup"><span data-stu-id="11d77-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11d77-209"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11d77-209"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="11d77-210">CLSID</span><span class="sxs-lookup"><span data-stu-id="11d77-210">CLSID</span></span><br/>                    | <span data-ttu-id="11d77-211">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="11d77-211">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="11d77-212">IID</span><span class="sxs-lookup"><span data-stu-id="11d77-212">IID</span></span><br/>                      | <span data-ttu-id="11d77-213">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="11d77-213">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="11d77-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11d77-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d77-215">**Austauschen von "errbemubjectex"**</span><span class="sxs-lookup"><span data-stu-id="11d77-215">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="11d77-216">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="11d77-216">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

