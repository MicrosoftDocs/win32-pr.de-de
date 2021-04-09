---
description: Initiiert die Freigabe für eine Server Ressource.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Create-Methode der Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958623"
---
# <a name="create-method-of-the-win32_share-class"></a><span data-ttu-id="a2287-103">Create-Methode der Win32- \_ Freigabe Klasse</span><span class="sxs-lookup"><span data-stu-id="a2287-103">Create method of the Win32\_Share class</span></span>

<span data-ttu-id="a2287-104">Die Methode **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) initiiert die Freigabe für eine Server Ressource.</span><span class="sxs-lookup"><span data-stu-id="a2287-104">The **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method initiates sharing for a server resource.</span></span>

<span data-ttu-id="a2287-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2287-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a2287-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a2287-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2287-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2287-107">Syntax</span></span>


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="a2287-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2287-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2287-109">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2287-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2287-110">Lokaler Pfad der Windows-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="a2287-110">Local path of the Windows share.</span></span>

<span data-ttu-id="a2287-111">Beispiel: "C: \\ Program Files".</span><span class="sxs-lookup"><span data-stu-id="a2287-111">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="a2287-112">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2287-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2287-113">Übergibt den Alias an einen Pfad, der auf einem Computersystem, auf dem Windows ausgeführt wird, als Freigabe eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="a2287-113">Passes the alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="a2287-114">Beispiel: "Public".</span><span class="sxs-lookup"><span data-stu-id="a2287-114">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="a2287-115">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2287-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2287-116">Übergibt den Typ der freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="a2287-116">Passes the type of resource being shared.</span></span> <span data-ttu-id="a2287-117">Zu den Typen zählen Laufwerke, Druck Warteschlangen, prozessübergreifende Kommunikation (prozessübergreifende Communications, IPC) und allgemeine Geräte.</span><span class="sxs-lookup"><span data-stu-id="a2287-117">Types includes disk drives, print queues, interprocess communications (IPC), and general devices.</span></span> <span data-ttu-id="a2287-118">Kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a2287-118">Can be one of the following values.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="a2287-119">**Laufwerk (0** )</span><span class="sxs-lookup"><span data-stu-id="a2287-119">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="a2287-120">**Druck Warteschlange** (1)</span><span class="sxs-lookup"><span data-stu-id="a2287-120">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="a2287-121">**Gerät** (2)</span><span class="sxs-lookup"><span data-stu-id="a2287-121">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="a2287-122">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="a2287-122">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="a2287-123">**Laufwerks Administrator** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="a2287-123">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="a2287-124">**Administrator der Druck Warteschlange** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="a2287-124">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="a2287-125">**Geräte Administrator** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="a2287-125">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="a2287-126">**IPC admin** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="a2287-126">**IPC Admin** (2147483651)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a2287-127">*MaximumAllowed* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a2287-127">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2287-128">Limit für die maximale Anzahl von Benutzern, die gleichzeitig diese Ressource verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="a2287-128">Limit on the maximum number of users allowed to concurrently use this resource.</span></span>

<span data-ttu-id="a2287-129">Beispiel: 10.</span><span class="sxs-lookup"><span data-stu-id="a2287-129">Example: 10.</span></span> <span data-ttu-id="a2287-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a2287-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a2287-131">*Beschreibung* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a2287-131">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2287-132">Optionaler Kommentar zum Beschreiben der freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="a2287-132">Optional comment to describe the resource being shared.</span></span> <span data-ttu-id="a2287-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a2287-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a2287-134">*Kennwort* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a2287-134">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2287-135">Kennwort (bei Ausführung des Servers mit Sicherheit auf Freigabe Ebene) für die freigegebene Ressource.</span><span class="sxs-lookup"><span data-stu-id="a2287-135">Password (when the server is running with share-level security) for the shared resource.</span></span> <span data-ttu-id="a2287-136">Wenn der Server mit Sicherheit auf Benutzerebene ausgeführt wird, wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a2287-136">If the server is running with user-level security, this parameter is ignored.</span></span> <span data-ttu-id="a2287-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a2287-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a2287-138">*Zugriff* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a2287-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2287-139">Sicherheits Beschreibung für Berechtigungen auf Benutzerebene.</span><span class="sxs-lookup"><span data-stu-id="a2287-139">Security descriptor for user level permissions.</span></span> <span data-ttu-id="a2287-140">Eine Sicherheits Beschreibung enthält Informationen über die Berechtigungen, den Besitzer und die Zugriffs Funktionen der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a2287-140">A security descriptor contains information about the permissions, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="a2287-141">Wenn dieser Parameter nicht angegeben wird oder den Wert **null** aufweist, verfügt jeder über Lesezugriff auf die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="a2287-141">If this parameter is not supplied or is **NULL**, then Everyone has read access to the share.</span></span> <span data-ttu-id="a2287-142">Weitere Informationen finden Sie unter [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="a2287-142">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) and [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2287-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2287-143">Return value</span></span>

<span data-ttu-id="a2287-144">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a2287-144">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a2287-145">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a2287-145">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a2287-146">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a2287-146">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a2287-147">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="a2287-147">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-148">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="a2287-148">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-149">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="a2287-149">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-150">**Ungültiger Name** (9)</span><span class="sxs-lookup"><span data-stu-id="a2287-150">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-151">**Ungültige Ebene** (10)</span><span class="sxs-lookup"><span data-stu-id="a2287-151">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-152">**Ungültiger Parameter** (21)</span><span class="sxs-lookup"><span data-stu-id="a2287-152">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-153">**Doppelte Freigabe** (22)</span><span class="sxs-lookup"><span data-stu-id="a2287-153">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-154">**Umgeleiteter Pfad** (23)</span><span class="sxs-lookup"><span data-stu-id="a2287-154">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-155">**Unbekanntes Gerät oder Verzeichnis** (24)</span><span class="sxs-lookup"><span data-stu-id="a2287-155">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-156">Der **Netzwerkname wurde nicht gefunden** (25).</span><span class="sxs-lookup"><span data-stu-id="a2287-156">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="a2287-157">**Sonstige** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="a2287-157">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a2287-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2287-158">Remarks</span></span>

<span data-ttu-id="a2287-159">**Create** ist eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="a2287-159">**Create** is a static method.</span></span>

<span data-ttu-id="a2287-160">Nur Mitglieder der lokalen Gruppe "Administratoren" oder "Konto-Operatoren" oder die Gruppenmitgliedschaften "Kommunikation", "Drucken" oder "Server Operator" können " **Create**"</span><span class="sxs-lookup"><span data-stu-id="a2287-160">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **Create**.</span></span> <span data-ttu-id="a2287-161">Der Druck Operator kann nur Drucker Warteschlangen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2287-161">The Print operator can only add printer queues.</span></span> <span data-ttu-id="a2287-162">Der Kommunikations Operator kann nur Kommunikationsgeräte Warteschlangen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2287-162">The Communication operator can only add communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="a2287-163">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2287-163">Examples</span></span>

<span data-ttu-id="a2287-164">Das PowerShell-Beispiel [exportieren und Importieren von Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) exportiert und importiert Dateifreigaben und legt Freigabe Berechtigungen fest.</span><span class="sxs-lookup"><span data-stu-id="a2287-164">The [Export and Import Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell sample exports and imports file shares and sets share permissions.</span></span> <span data-ttu-id="a2287-165">Entsprechend erstellt das Beispiel [Create a share und Set-Berechtigungen](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) auch eine neue Freigabe und legt die Freigabe Berechtigungen fest.</span><span class="sxs-lookup"><span data-stu-id="a2287-165">Similarly, the [Create a Share and Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) sample also creates a new share and sets the share permissions.</span></span>

<span data-ttu-id="a2287-166">Mit dem folgenden PowerShell-Code wird eine Freigabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2287-166">The following PowerShell code creates a share.</span></span>


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



<span data-ttu-id="a2287-167">Im vorherigen Codebeispiel wird Folgendes zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="a2287-167">The previous code sample returns the following:</span></span>

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

<span data-ttu-id="a2287-168">Im folgenden C- \# Codebeispiel wird beschrieben, wie die Create-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a2287-168">The following C\# code sample describe how to call the create method.</span></span>


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



## <a name="requirements"></a><span data-ttu-id="a2287-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2287-169">Requirements</span></span>



| <span data-ttu-id="a2287-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2287-170">Requirement</span></span> | <span data-ttu-id="a2287-171">Wert</span><span class="sxs-lookup"><span data-stu-id="a2287-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2287-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2287-172">Minimum supported client</span></span><br/> | <span data-ttu-id="a2287-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2287-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2287-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2287-174">Minimum supported server</span></span><br/> | <span data-ttu-id="a2287-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2287-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2287-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2287-176">Namespace</span></span><br/>                | <span data-ttu-id="a2287-177">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2287-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2287-178">MOF</span><span class="sxs-lookup"><span data-stu-id="a2287-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2287-179"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a2287-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2287-180">DLL</span><span class="sxs-lookup"><span data-stu-id="a2287-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2287-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2287-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2287-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2287-182">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2287-183">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2287-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a2287-184">**Win32- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="a2287-184">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

