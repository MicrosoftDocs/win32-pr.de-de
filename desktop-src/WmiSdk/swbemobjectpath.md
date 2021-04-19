---
description: Verwenden Sie die Methoden und Eigenschaften des Objekts "errbemubjectpath", um einen Objekt Pfad zu erstellen und zu überprüfen. Dieses Objekt kann durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Errbemubjectpath-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360164"
---
# <a name="swbemobjectpath-object"></a><span data-ttu-id="5570a-104">Errbemubjectpath-Objekt</span><span class="sxs-lookup"><span data-stu-id="5570a-104">SWbemObjectPath object</span></span>

<span data-ttu-id="5570a-105">Verwenden Sie die Methoden und Eigenschaften des Objekts " **errbemubjectpath** ", um einen Objekt Pfad zu erstellen und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5570a-105">Use the methods and properties of the **SWbemObjectPath** object to construct and validate an object path.</span></span> <span data-ttu-id="5570a-106">Dieses Objekt kann durch den VBScript-Befehl "up- **Object** " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5570a-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="5570a-107">Member</span><span class="sxs-lookup"><span data-stu-id="5570a-107">Members</span></span>

<span data-ttu-id="5570a-108">Das Objekt " **errbeporbjectpath** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5570a-108">The **SWbemObjectPath** object has these types of members:</span></span>

-   [<span data-ttu-id="5570a-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="5570a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5570a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5570a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5570a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="5570a-111">Methods</span></span>

<span data-ttu-id="5570a-112">Das Objekt " **errbemubjectpath** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5570a-112">The **SWbemObjectPath** object has these methods.</span></span>



| <span data-ttu-id="5570a-113">Methode</span><span class="sxs-lookup"><span data-stu-id="5570a-113">Method</span></span>                                                   | <span data-ttu-id="5570a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5570a-114">Description</span></span>                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="5570a-115">**-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5570a-115">**SetAsClass**</span></span>](swbemobjectpath-setasclass.md)         | <span data-ttu-id="5570a-116">Erzwingt, dass der Pfad eine WMI-Klasse adressiert.</span><span class="sxs-lookup"><span data-stu-id="5570a-116">Forces the path to address a WMI class.</span></span><br/>              |
| [<span data-ttu-id="5570a-117">**"Ttassingleton"**</span><span class="sxs-lookup"><span data-stu-id="5570a-117">**SetAsSingleton**</span></span>](swbemobjectpath-setassingleton.md) | <span data-ttu-id="5570a-118">Erzwingt, dass der Pfad eine Singleton-WMI-Instanz adressiert.</span><span class="sxs-lookup"><span data-stu-id="5570a-118">Forces the path to address a singleton WMI instance.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5570a-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5570a-119">Properties</span></span>

<span data-ttu-id="5570a-120">Das Objekt " **errbemubjectpath** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5570a-120">The **SWbemObjectPath** object has these properties.</span></span>



| <span data-ttu-id="5570a-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5570a-121">Property</span></span>                                                              | <span data-ttu-id="5570a-122">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="5570a-122">Access type</span></span>           | <span data-ttu-id="5570a-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5570a-123">Description</span></span>                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5570a-124">**Autoritative Stelle**</span><span class="sxs-lookup"><span data-stu-id="5570a-124">**Authority**</span></span>](swbemobjectpath-authority.md)<br/>             | <span data-ttu-id="5570a-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5570a-125">Read/write</span></span><br/> | <span data-ttu-id="5570a-126">Eine Zeichenfolge, die die Autoritäts Komponente des Objekt Pfads definiert.</span><span class="sxs-lookup"><span data-stu-id="5570a-126">String that defines the Authority component of the object path.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="5570a-127">**Klasse**</span><span class="sxs-lookup"><span data-stu-id="5570a-127">**Class**</span></span>](swbemobjectpath-class.md)<br/>                     | <span data-ttu-id="5570a-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5570a-128">Read/write</span></span><br/> | <span data-ttu-id="5570a-129">Der Name der Klasse, die Teil des Objekt Pfads ist.</span><span class="sxs-lookup"><span data-stu-id="5570a-129">Name of the class that is part of the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="5570a-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="5570a-130">**DisplayName**</span></span>](swbemobjectpath-displayname.md)<br/>         | <span data-ttu-id="5570a-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5570a-131">Read/write</span></span><br/> | <span data-ttu-id="5570a-132">Eine Zeichenfolge, die den Pfad in einem Formular enthält, das als Moniker-Anzeige Name verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5570a-132">String that contains the path in a form that can be used as a moniker display name.</span></span> <span data-ttu-id="5570a-133">Siehe [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="5570a-133">See [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span><br/> |
| [<span data-ttu-id="5570a-134">**IsClass**</span><span class="sxs-lookup"><span data-stu-id="5570a-134">**IsClass**</span></span>](swbemobjectpath-isclass.md)<br/>                 | <span data-ttu-id="5570a-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5570a-135">Read-only</span></span><br/>  | <span data-ttu-id="5570a-136">Boolescher Wert, der angibt, ob dieser Pfad eine Klasse darstellt.</span><span class="sxs-lookup"><span data-stu-id="5570a-136">Boolean value that indicates if this path represents a class.</span></span> <span data-ttu-id="5570a-137">Dies entspricht der Eigenschaft " [ \_ \_ Eigenschaft" in der com](wmi-system-properties.md) -API.</span><span class="sxs-lookup"><span data-stu-id="5570a-137">This is analogous to the [\_\_Genus](wmi-system-properties.md) property in the COM API.</span></span><br/>                    |
| [<span data-ttu-id="5570a-138">**IsSingleton**</span><span class="sxs-lookup"><span data-stu-id="5570a-138">**IsSingleton**</span></span>](swbemobjectpath-issingleton.md)<br/>         | <span data-ttu-id="5570a-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5570a-139">Read-only</span></span><br/>  | <span data-ttu-id="5570a-140">Boolescher Wert, der angibt, ob dieser Pfad eine Singleton-Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="5570a-140">Boolean value that indicates if this path represents a singleton instance.</span></span><br/>                                                                                                |
| [<span data-ttu-id="5570a-141">**Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="5570a-141">**Keys**</span></span>](swbemobjectpath-keys.md)<br/>                       | <span data-ttu-id="5570a-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5570a-142">Read-only</span></span><br/>  | <span data-ttu-id="5570a-143">Ein [**-**](swbemnamedvalueset.md) Objekt, das die Schlüsselwert Bindungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5570a-143">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span><br/>                                                                          |
| [<span data-ttu-id="5570a-144">**Gebietsschema**</span><span class="sxs-lookup"><span data-stu-id="5570a-144">**Locale**</span></span>](swbemobjectpath-locale.md)<br/>                   | <span data-ttu-id="5570a-145">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5570a-145">Read/write</span></span><br/> | <span data-ttu-id="5570a-146">Eine Zeichenfolge, die das Gebiets Schema für diesen Objekt Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="5570a-146">String that contains the locale for this object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="5570a-147">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5570a-147">**Namespace**</span></span>](swbemobjectpath-namespace.md)<br/>             | <span data-ttu-id="5570a-148">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5570a-148">Read/write</span></span><br/> | <span data-ttu-id="5570a-149">Der Name des Namespace, der Teil des Objekt Pfads ist.</span><span class="sxs-lookup"><span data-stu-id="5570a-149">Name of the namespace that is part of the object path.</span></span> <span data-ttu-id="5570a-150">Dies entspricht der [ \_ \_ Namespace](wmi-system-properties.md) -Eigenschaft in der com-API.</span><span class="sxs-lookup"><span data-stu-id="5570a-150">This is the same as the [\_\_Namespace](wmi-system-properties.md) property in the COM API.</span></span><br/>                        |
| [<span data-ttu-id="5570a-151">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5570a-151">**ParentNamespace**</span></span>](swbemobjectpath-parentnamespace.md)<br/> | <span data-ttu-id="5570a-152">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5570a-152">Read-only</span></span><br/>  | <span data-ttu-id="5570a-153">Der Name des übergeordneten Elements des Namespace, der Teil des Objekt Pfads ist.</span><span class="sxs-lookup"><span data-stu-id="5570a-153">Name of the parent of the namespace that is part of the object path.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="5570a-154">**ADS**</span><span class="sxs-lookup"><span data-stu-id="5570a-154">**Path**</span></span>](swbemobjectpath-path.md)<br/>                       | <span data-ttu-id="5570a-155">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5570a-155">Read/write</span></span><br/> | <span data-ttu-id="5570a-156">Enthält den absoluten Pfad.</span><span class="sxs-lookup"><span data-stu-id="5570a-156">Contains the absolute path.</span></span> <span data-ttu-id="5570a-157">Dies entspricht der Eigenschaft [ \_ \_ path](wmi-system-properties.md) System in der com-API.</span><span class="sxs-lookup"><span data-stu-id="5570a-157">This is the same as the [\_\_Path](wmi-system-properties.md) system property in the COM API.</span></span> <span data-ttu-id="5570a-158">Dies ist die Standard Eigenschaft dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="5570a-158">This is the default property of this object.</span></span><br/>    |
| [<span data-ttu-id="5570a-159">**RelPath**</span><span class="sxs-lookup"><span data-stu-id="5570a-159">**Relpath**</span></span>](swbemobjectpath-relpath.md)<br/>                 | <span data-ttu-id="5570a-160">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5570a-160">Read/write</span></span><br/> | <span data-ttu-id="5570a-161">Enthält den relativen Pfad.</span><span class="sxs-lookup"><span data-stu-id="5570a-161">Contains the relative path.</span></span> <span data-ttu-id="5570a-162">Dies entspricht der Eigenschaft " [ \_ \_ RelPath](wmi-system-properties.md) System" in der com-API.</span><span class="sxs-lookup"><span data-stu-id="5570a-162">This is the same as the [\_\_Relpath](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                              |
| [<span data-ttu-id="5570a-163">**Sicherheit\_**</span><span class="sxs-lookup"><span data-stu-id="5570a-163">**Security\_**</span></span>](swbemobjectpath-security-.md)<br/>            | <span data-ttu-id="5570a-164">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5570a-164">Read-only</span></span><br/>  | <span data-ttu-id="5570a-165">Wird verwendet, um die Sicherheitseinstellungen zu lesen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5570a-165">Used to read or change the security settings.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="5570a-166">**Servers**</span><span class="sxs-lookup"><span data-stu-id="5570a-166">**Server**</span></span>](swbemobjectpath-server.md)<br/>                   | <span data-ttu-id="5570a-167">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5570a-167">Read/write</span></span><br/> | <span data-ttu-id="5570a-168">Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5570a-168">Name of the server.</span></span> <span data-ttu-id="5570a-169">Dies entspricht der [ \_ \_ Server](wmi-system-properties.md) System Eigenschaft in der com-API.</span><span class="sxs-lookup"><span data-stu-id="5570a-169">This is the same as the [\_\_Server](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                                       |



 

## <a name="examples"></a><span data-ttu-id="5570a-170">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5570a-170">Examples</span></span>

<span data-ttu-id="5570a-171">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Objekt Pfade erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5570a-171">The following VBScript code sample demonstrates how to build object paths.</span></span>


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



<span data-ttu-id="5570a-172">Im folgenden perl-Codebeispiel wird veranschaulicht, wie Objekt Pfade erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5570a-172">The following Perl code sample demonstrates how to build object paths.</span></span>


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
  }
  else
  {
   print STDERR Win32::OLE->LastError, "\n";
  }
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="5570a-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5570a-173">Requirements</span></span>



| <span data-ttu-id="5570a-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5570a-174">Requirement</span></span> | <span data-ttu-id="5570a-175">Wert</span><span class="sxs-lookup"><span data-stu-id="5570a-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5570a-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5570a-176">Minimum supported client</span></span><br/> | <span data-ttu-id="5570a-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5570a-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5570a-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5570a-178">Minimum supported server</span></span><br/> | <span data-ttu-id="5570a-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5570a-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5570a-180">Header</span><span class="sxs-lookup"><span data-stu-id="5570a-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="5570a-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5570a-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5570a-182">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5570a-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="5570a-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5570a-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5570a-184">DLL</span><span class="sxs-lookup"><span data-stu-id="5570a-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5570a-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5570a-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5570a-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="5570a-186">CLSID</span></span><br/>                    | <span data-ttu-id="5570a-187">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="5570a-187">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="5570a-188">IID</span><span class="sxs-lookup"><span data-stu-id="5570a-188">IID</span></span><br/>                      | <span data-ttu-id="5570a-189">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="5570a-189">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="5570a-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5570a-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5570a-191">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="5570a-191">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




