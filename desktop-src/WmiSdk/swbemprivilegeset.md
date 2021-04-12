---
description: Ein "taubemprivilegeset"-Objekt ist eine Sammlung von "taubemprivilege"-Objekten in einem "Swap Security"-Objekt, das bestimmte Berechtigungen für ein Windows-Verwaltungsinstrumentation (WMI)-Objekt anfordert.
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Taubemprivilegeset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344719"
---
# <a name="swbemprivilegeset-object"></a><span data-ttu-id="c0820-103">Swap-Objekt</span><span class="sxs-lookup"><span data-stu-id="c0820-103">SWbemPrivilegeSet object</span></span>

<span data-ttu-id="c0820-104">Ein " **taubemprivilegeset** "-Objekt ist eine Sammlung von " [**taubemprivilege**](swbemprivilege.md) "-Objekten in einem " [**Swap Security**](swbemsecurity.md) "-Objekt, das bestimmte Berechtigungen für ein Windows-Verwaltungsinstrumentation (WMI)-Objekt anfordert.</span><span class="sxs-lookup"><span data-stu-id="c0820-104">An **SWbemPrivilegeSet** object is a collection of [**SWbemPrivilege**](swbemprivilege.md) objects in an [**SWbemSecurity**](swbemsecurity.md) object that requests specific privileges for a Windows Management Instrumentation (WMI) object.</span></span> <span data-ttu-id="c0820-105">Weitere Informationen finden Sie in der Liste der Berechtigungen unter [**Berechtigungs Konstanten**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c0820-105">See the list of privileges in [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="c0820-106">Der Auflistung werden Elemente mithilfe der [**Add**](swbemprivilegeset-add.md) -Methode und der [**addasstring**](swbemprivilegeset-addasstring.md) -Methode hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c0820-106">Items are added to the collection using the [**Add**](swbemprivilegeset-add.md) and [**AddAsString**](swbemprivilegeset-addasstring.md) methods.</span></span> <span data-ttu-id="c0820-107">Elemente werden mithilfe der- [**Element**](swbemprivilegeset-item.md) Methode aus der-Auflistung abgerufen und mithilfe der [**Remove**](swbemprivilegeset-remove.md) -Methode entfernt.</span><span class="sxs-lookup"><span data-stu-id="c0820-107">Items are retrieved from the collection using the [**Item**](swbemprivilegeset-item.md) method, and removed using the [**Remove**](swbemprivilegeset-remove.md) method.</span></span> <span data-ttu-id="c0820-108">Dieses Objekt kann nicht durch den VBScript-Methoden aufgerufene " [samateobject](/previous-versions//xzysf6hc(v=vs.85)) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c0820-108">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method call.</span></span> <span data-ttu-id="c0820-109">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="c0820-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="c0820-110">Ein-Objekt vom typ' **Swap** ' ist ein Satz von Berechtigungs Überschreibungs Anforderungen für ein bestimmtes Objekt.</span><span class="sxs-lookup"><span data-stu-id="c0820-110">An **SWbemPrivilegeSet** object is a set of privilege override requests for a specific object.</span></span> <span data-ttu-id="c0820-111">Wenn ein API-Befehl mit diesem-Objekt ausgeführt wird, werden die Anforderungen zur außer Kraft Setzung von Berechtigungen versucht.</span><span class="sxs-lookup"><span data-stu-id="c0820-111">When an API call is made using this object, the privilege override requests are attempted.</span></span> <span data-ttu-id="c0820-112">Das Objekt " **taubemprivilegeset** " definiert nicht die für den aktuellen Benutzer oder den aktuellen Prozess verfügbaren Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="c0820-112">The **SWbemPrivilegeSet** object does not define the privileges available to the current user or process.</span></span> <span data-ttu-id="c0820-113">Anders ausgedrückt: durch das Abrufen der Berechtigungen für ein WMI-Objekt werden nicht die Berechtigungseinstellungen identifiziert, die für die Verbindung mit WMI hergestellt werden, oder die Berechtigungen, die beim Übermitteln eines Objekts an eine Senke wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="c0820-113">In other words, obtaining the privileges for any WMI object does not identify the privilege settings that are made on the connection to WMI, or the privileges in effect when an object is delivered to a sink.</span></span>

## <a name="members"></a><span data-ttu-id="c0820-114">Member</span><span class="sxs-lookup"><span data-stu-id="c0820-114">Members</span></span>

<span data-ttu-id="c0820-115">Das Objekt " **taubemprivilegeset** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c0820-115">The **SWbemPrivilegeSet** object has these types of members:</span></span>

-   [<span data-ttu-id="c0820-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="c0820-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0820-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0820-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0820-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="c0820-118">Methods</span></span>

<span data-ttu-id="c0820-119">Das **taubemprivilegeset** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c0820-119">The **SWbemPrivilegeSet** object has these methods.</span></span>



| <span data-ttu-id="c0820-120">Methode</span><span class="sxs-lookup"><span data-stu-id="c0820-120">Method</span></span>                                               | <span data-ttu-id="c0820-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0820-121">Description</span></span>                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0820-122">**Eren**</span><span class="sxs-lookup"><span data-stu-id="c0820-122">**Add**</span></span>](swbemprivilegeset-add.md)                 | <span data-ttu-id="c0820-123">Fügt der **slibemprivilegeset** -Auflistung mithilfe einer [wbemprivilegeenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) -Konstante ein " [**slibemprivilege**](swbemprivilege.md) "-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c0820-123">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) constant.</span></span><br/> |
| [<span data-ttu-id="c0820-124">**Addasstring**</span><span class="sxs-lookup"><span data-stu-id="c0820-124">**AddAsString**</span></span>](swbemprivilegeset-addasstring.md) | <span data-ttu-id="c0820-125">Fügt der-Auflistung von " **taubemprivilegeset** " mithilfe einer Berechtigungs Zeichenfolge ein "" [**-Objekt "**](swbemprivilege.md) ".</span><span class="sxs-lookup"><span data-stu-id="c0820-125">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a privilege string.</span></span><br/>                                    |
| [<span data-ttu-id="c0820-126">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="c0820-126">**DeleteAll**</span></span>](swbemprivilegeset-deleteall.md)     | <span data-ttu-id="c0820-127">Löscht alle Berechtigungen aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c0820-127">Deletes all the privileges from the collection.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="c0820-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0820-128">**Item**</span></span>](swbemprivilegeset-item.md)               | <span data-ttu-id="c0820-129">Ruft [**ein-**](swbemprivilege.md) Objekt aus der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="c0820-129">Retrieves an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="c0820-130">Dies ist die Standardmethode dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="c0820-130">This is the default method of this object.</span></span><br/>                                 |
| [<span data-ttu-id="c0820-131">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="c0820-131">**Remove**</span></span>](swbemprivilegeset-remove.md)           | <span data-ttu-id="c0820-132">Entfernt ein [**-**](swbemprivilege.md) Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c0820-132">Removes an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="c0820-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0820-133">Properties</span></span>

<span data-ttu-id="c0820-134">Das Objekt " **taubemprivilegeset** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c0820-134">The **SWbemPrivilegeSet** object has these properties.</span></span>



| <span data-ttu-id="c0820-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c0820-135">Property</span></span>                                            | <span data-ttu-id="c0820-136">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="c0820-136">Access type</span></span>          | <span data-ttu-id="c0820-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0820-137">Description</span></span>                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="c0820-138">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="c0820-138">**Count**</span></span>](swbemprivilegeset-count.md)<br/> | <span data-ttu-id="c0820-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0820-139">Read-only</span></span><br/> | <span data-ttu-id="c0820-140">Die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c0820-140">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="c0820-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0820-141">Examples</span></span>

<span data-ttu-id="c0820-142">Im folgenden VBScript-Codebeispiel wird ein Objekt vom Typ "slibemprivileges" abgerufen, und der Auflistung werden alle verfügbaren Berechtigungen gemäß dem Wert hinzugefügt, wie in [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)definiert.</span><span class="sxs-lookup"><span data-stu-id="c0820-142">The following VBScript code example obtains an SWbemPrivileges object and adds all the available privileges to the collection by privilege value, as defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



<span data-ttu-id="c0820-143">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Berechtigungen mithilfe des-Objekts von " **Swap** " hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c0820-143">The following VBScript code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



<span data-ttu-id="c0820-144">Im folgenden perl-Codebeispiel wird das Hinzufügen von Berechtigungen mithilfe des-Objekts " **Swap** " veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c0820-144">The following Perl code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="c0820-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0820-145">Requirements</span></span>



| <span data-ttu-id="c0820-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0820-146">Requirement</span></span> | <span data-ttu-id="c0820-147">Wert</span><span class="sxs-lookup"><span data-stu-id="c0820-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0820-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0820-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c0820-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0820-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0820-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0820-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c0820-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0820-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0820-152">Header</span><span class="sxs-lookup"><span data-stu-id="c0820-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0820-153"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0820-153"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0820-154">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c0820-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0820-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0820-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0820-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c0820-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0820-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0820-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0820-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="c0820-158">CLSID</span></span><br/>                    | <span data-ttu-id="c0820-159">CLSID- \_ Swap-taubemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="c0820-159">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="c0820-160">IID</span><span class="sxs-lookup"><span data-stu-id="c0820-160">IID</span></span><br/>                      | <span data-ttu-id="c0820-161">IID \_ iswbemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="c0820-161">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="c0820-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0820-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0820-163">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="c0820-163">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="c0820-164">Ausführen privilegierter Vorgänge mit VBScript</span><span class="sxs-lookup"><span data-stu-id="c0820-164">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="c0820-165">Wbemprivilegeumum</span><span class="sxs-lookup"><span data-stu-id="c0820-165">WbemPrivilegeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="c0820-166">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="c0820-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="c0820-167">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="c0820-167">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

