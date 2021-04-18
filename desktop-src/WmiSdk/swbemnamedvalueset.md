---
description: Ein "taubemnamedvalueset"-Objekt ist eine Sammlung von "taubemnamedvalue"-Objekten.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Taubemnamedvalueset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343411"
---
# <a name="swbemnamedvalueset-object"></a><span data-ttu-id="0a9ee-103">Swap-namedvalueset-Objekt</span><span class="sxs-lookup"><span data-stu-id="0a9ee-103">SWbemNamedValueSet object</span></span>

<span data-ttu-id="0a9ee-104">Ein " **taubemnamedvalueset** "-Objekt ist eine Sammlung von " [**taubemnamedvalue**](swbemnamedvalue.md) "-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-104">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) objects.</span></span> <span data-ttu-id="0a9ee-105">Die Methoden und Eigenschaften von " **Austausch Name** " werden im Wesentlichen verwendet, um weitere Informationen an Anbieter zu senden, wenn bestimmte WMI-Aufrufe übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-105">The methods and properties of **SWbemNamedValueSet** are used principally to send more information to providers when submitting certain calls to WMI.</span></span> <span data-ttu-id="0a9ee-106">Alle Aufrufe in " [**Swap Services**](swbemservices.md)" und einige Aufrufe in " [**errbemujeject**](swbemobject.md)" akzeptieren einen optionalen Parameter, bei dem es sich um ein Objekt dieses Typs handelt.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-106">All calls in [**SWbemServices**](swbemservices.md), and some calls in [**SWbemObject**](swbemobject.md), take an optional parameter that is an object of this type.</span></span> <span data-ttu-id="0a9ee-107">Ein Client kann einem "Swap- **namedvalueset** "-Objektinformationen hinzufügen und das " **austaubemnamedvalueset** "-Objekt mit dem-Parameter als einen der-Parameter senden.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-107">A client can add information to an **SWbemNamedValueSet** object, and send the **SWbemNamedValueSet** object with the call as one of the parameters.</span></span> <span data-ttu-id="0a9ee-108">Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-108">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="0a9ee-109">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="0a9ee-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

> [!Note]  
> <span data-ttu-id="0a9ee-110">Wichtig: Wenn möglich, verwenden Sie diesen Mechanismus nicht, da er das einheitliche Zugriffs Modell, das die Basis von WMI ist, unterbrechen kann.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-110">Important - If possible, do not use this mechanism because it can break the uniform access model that is the basis of WMI.</span></span> <span data-ttu-id="0a9ee-111">Wenn ein Anbieter diesen Mechanismus verwendet, ist es wichtig, dass dieser Mechanismus so sparsam wie möglich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-111">If a provider does use this mechanism, it is important that this mechanism is used as sparingly as possible.</span></span> <span data-ttu-id="0a9ee-112">Wenn ein Anbieter eine große Menge hochspezifischer Kontextinformationen erfordert, um auf eine Anforderung zu reagieren, müssen alle Clients so codiert sein, dass diese Informationen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-112">If a provider requires a large amount of highly specific context information to respond to a request, all clients must be coded to provide this information.</span></span> <span data-ttu-id="0a9ee-113">Mit diesem Mechanismus können Sie bei Bedarf auf solche Anbieter zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-113">This mechanism allows you to access such providers, if necessary.</span></span>

 

<span data-ttu-id="0a9ee-114">Ein " **taubemnamedvalueset** "-Objekt ist eine Sammlung von " [**taubemnamedvalue**](swbemnamedvalue.md) "-Elementen.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-114">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) elements.</span></span> <span data-ttu-id="0a9ee-115">Diese Elemente werden der Auflistung mithilfe der Methode " [**Swap. Add**](swbemnamedvalueset-add.md) " hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-115">These items are added to the collection using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span> <span data-ttu-id="0a9ee-116">Sie werden mithilfe der Methode " [**Swap Name. Remove**](swbemnamedvalueset-remove.md) " entfernt und mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-116">They are removed using the [**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md) method and retrieved using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="0a9ee-117">Sie können auf die-Methoden zugreifen, um alle Kontextinformationen auszufüllen, die von einem dynamischen Anbieter benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-117">You can access the methods to fill in any context information that is required by a dynamic provider.</span></span> <span data-ttu-id="0a9ee-118">Nachdem Sie eine der Methode " [**Swap Services**](swbemservices.md) " aufgerufen haben, können Sie das Objekt " **taubemnamedvalueset** " für einen anderen-Befehl wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-118">After you call one of the [**SWbemServices**](swbemservices.md) methods, you can reuse the **SWbemNamedValueSet** object for another call.</span></span>

<span data-ttu-id="0a9ee-119">Der zugrunde liegende Anbieter bestimmt die Informationen, die in einem " **Swap namedvalueset** "-Objekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-119">The underlying provider determines the information that is contained in an **SWbemNamedValueSet** object.</span></span> <span data-ttu-id="0a9ee-120">WMI verwendet die Informationen nicht, sondern leitet Sie einfach an den Anbieter weiter.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-120">WMI makes no use of the information, but simply forwards it to the provider.</span></span> <span data-ttu-id="0a9ee-121">Anbieter müssen die erforderlichen Kontextinformationen für die Dienst Anforderungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-121">Providers must publish the context information they require to service requests.</span></span>

## <a name="members"></a><span data-ttu-id="0a9ee-122">Member</span><span class="sxs-lookup"><span data-stu-id="0a9ee-122">Members</span></span>

<span data-ttu-id="0a9ee-123">Das Objekt " **taubemnamedvalueset** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0a9ee-123">The **SWbemNamedValueSet** object has these types of members:</span></span>

-   [<span data-ttu-id="0a9ee-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="0a9ee-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="0a9ee-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a9ee-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0a9ee-126">Methoden</span><span class="sxs-lookup"><span data-stu-id="0a9ee-126">Methods</span></span>

<span data-ttu-id="0a9ee-127">Das Objekt " **Swap namedvalueset** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-127">The **SWbemNamedValueSet** object has these methods.</span></span>



| <span data-ttu-id="0a9ee-128">Methode</span><span class="sxs-lookup"><span data-stu-id="0a9ee-128">Method</span></span>                                            | <span data-ttu-id="0a9ee-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a9ee-129">Description</span></span>                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a9ee-130">**Eren**</span><span class="sxs-lookup"><span data-stu-id="0a9ee-130">**Add**</span></span>](swbemnamedvalueset-add.md)             | <span data-ttu-id="0a9ee-131">Fügt der Auflistung ein-Objekt mit dem [**Namen**](swbemnamedvalue.md) "-Objekt" hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-131">Adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span><br/>                                                  |
| [<span data-ttu-id="0a9ee-132">**Klon**</span><span class="sxs-lookup"><span data-stu-id="0a9ee-132">**Clone**</span></span>](swbemnamedvalueset-clone.md)         | <span data-ttu-id="0a9ee-133">Erstellt eine Kopie dieser " **Swap namedvalueset** "-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-133">Makes a copy of this **SWbemNamedValueSet** collection.</span></span><br/>                                                                       |
| [<span data-ttu-id="0a9ee-134">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="0a9ee-134">**DeleteAll**</span></span>](swbemnamedvalueset-deleteall.md) | <span data-ttu-id="0a9ee-135">Entfernt alle Elemente aus der Auflistung, sodass das Objekt " **taubemnamedvalueset** " leer ist.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-135">Removes all items from the collection, making the **SWbemNamedValueSet** object empty.</span></span><br/>                                        |
| [<span data-ttu-id="0a9ee-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a9ee-136">**Item**</span></span>](swbemnamedvalueset-item.md)           | <span data-ttu-id="0a9ee-137">Ruft [**ein-**](swbemnamedvalue.md) Objekt aus der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-137">Retrieves an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span> <span data-ttu-id="0a9ee-138">Dies ist die Standardmethode des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-138">This is the default method of the object.</span></span><br/> |
| [<span data-ttu-id="0a9ee-139">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="0a9ee-139">**Remove**</span></span>](swbemnamedvalueset-remove.md)       | <span data-ttu-id="0a9ee-140">Entfernt ein " [**pulbemnamedvalue**](swbemnamedvalue.md) "-Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-140">Removes an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span><br/>                                             |



 

### <a name="properties"></a><span data-ttu-id="0a9ee-141">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a9ee-141">Properties</span></span>

<span data-ttu-id="0a9ee-142">Das Objekt " **Swap namedvalueset** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-142">The **SWbemNamedValueSet** object has these properties.</span></span>



| <span data-ttu-id="0a9ee-143">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0a9ee-143">Property</span></span>                                             | <span data-ttu-id="0a9ee-144">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="0a9ee-144">Access type</span></span>          | <span data-ttu-id="0a9ee-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a9ee-145">Description</span></span>                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="0a9ee-146">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="0a9ee-146">**Count**</span></span>](swbemnamedvalueset-count.md)<br/> | <span data-ttu-id="0a9ee-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a9ee-147">Read-only</span></span><br/> | <span data-ttu-id="0a9ee-148">Die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-148">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="0a9ee-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a9ee-149">Examples</span></span>

<span data-ttu-id="0a9ee-150">Das folgende VBScript-Beispiel veranschaulicht die Bearbeitung von benannten Wert Sätzen, falls der benannte Wert ein Arraytyp ist.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-150">The following VBScript sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="0a9ee-151">Das folgende perl-Beispiel veranschaulicht die Bearbeitung von benannten Wert Sätzen, falls der benannte Wert ein Arraytyp ist.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-151">The following Perl sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="0a9ee-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a9ee-152">Requirements</span></span>



| <span data-ttu-id="0a9ee-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a9ee-153">Requirement</span></span> | <span data-ttu-id="0a9ee-154">Wert</span><span class="sxs-lookup"><span data-stu-id="0a9ee-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9ee-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a9ee-155">Minimum supported client</span></span><br/> | <span data-ttu-id="0a9ee-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a9ee-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a9ee-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a9ee-157">Minimum supported server</span></span><br/> | <span data-ttu-id="0a9ee-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a9ee-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a9ee-159">Header</span><span class="sxs-lookup"><span data-stu-id="0a9ee-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a9ee-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a9ee-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a9ee-161">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0a9ee-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a9ee-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0a9ee-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0a9ee-163">DLL</span><span class="sxs-lookup"><span data-stu-id="0a9ee-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a9ee-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a9ee-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a9ee-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a9ee-165">CLSID</span></span><br/>                    | <span data-ttu-id="0a9ee-166">CLSID- \_ Swap-namedvalueset</span><span class="sxs-lookup"><span data-stu-id="0a9ee-166">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="0a9ee-167">IID</span><span class="sxs-lookup"><span data-stu-id="0a9ee-167">IID</span></span><br/>                      | <span data-ttu-id="0a9ee-168">IID \_ iswbemnamedvalueset</span><span class="sxs-lookup"><span data-stu-id="0a9ee-168">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="0a9ee-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a9ee-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9ee-170">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="0a9ee-170">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




