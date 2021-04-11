---
description: Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Drucker steuert.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: SETSECURITYDESCRIPTOR-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1572919d0ac0b5c18a6fc5084636c52b9b3ea1c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214298"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="07a6b-103">SETSECURITYDESCRIPTOR-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="07a6b-103">SetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="07a6b-104">Die **SETSECURITYDESCRIPTOR** -Methode schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Drucker steuert.</span><span class="sxs-lookup"><span data-stu-id="07a6b-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="07a6b-105">Die Sicherheits Beschreibung ist eine Instanz der Win32- [**\_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="07a6b-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="07a6b-106">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="07a6b-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="07a6b-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="07a6b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07a6b-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="07a6b-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07a6b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="07a6b-109">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="07a6b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07a6b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07a6b-111">*Deskriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07a6b-111">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07a6b-112">Die Sicherheits Beschreibung, die dem Drucker zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="07a6b-112">The security descriptor that is associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07a6b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07a6b-113">Return value</span></span>

<span data-ttu-id="07a6b-114">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="07a6b-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="07a6b-115">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="07a6b-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="07a6b-116">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="07a6b-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="07a6b-117">**0**</span><span class="sxs-lookup"><span data-stu-id="07a6b-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="07a6b-118">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="07a6b-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="07a6b-119">**2**</span><span class="sxs-lookup"><span data-stu-id="07a6b-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="07a6b-120">Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="07a6b-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="07a6b-121">**8**</span><span class="sxs-lookup"><span data-stu-id="07a6b-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="07a6b-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="07a6b-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="07a6b-123">**9**</span><span class="sxs-lookup"><span data-stu-id="07a6b-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="07a6b-124">Der Benutzer verfügt nicht über die erforderlichen Berechtigungen, um die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="07a6b-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="07a6b-125">**21**</span><span class="sxs-lookup"><span data-stu-id="07a6b-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="07a6b-126">Ein im Methoden Aufrufwert angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="07a6b-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07a6b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07a6b-127">Remarks</span></span>

<span data-ttu-id="07a6b-128">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="07a6b-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="07a6b-129">Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="07a6b-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="07a6b-130">Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="07a6b-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="07a6b-131">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="07a6b-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="07a6b-132">Wenn Sie diese Methode aufrufen, können Sie sowohl die DACL als auch die SACL in der [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz aktualisieren, aber Sie können auch nur die DACL oder nur die SACL aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="07a6b-132">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you can also update only the DACL or only the SACL.</span></span>

<span data-ttu-id="07a6b-133">Die folgenden Werte im [**\_ \_ sicherheitsdeskriptorsteuerelement**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL, die SACL oder beides aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="07a6b-133">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="07a6b-134">**SE \_ DACL \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="07a6b-134">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="07a6b-135">Gibt an, dass die DACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07a6b-135">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="07a6b-136">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.</span><span class="sxs-lookup"><span data-stu-id="07a6b-136">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="07a6b-137">**SE \_ SACL \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="07a6b-137">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="07a6b-138">Gibt an, dass die SACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07a6b-138">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="07a6b-139">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei.</span><span class="sxs-lookup"><span data-stu-id="07a6b-139">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="07a6b-140">Zum Aktualisieren der SACL muss für das Konto die Berechtigung " **SeSecurityPrivilege** " aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="07a6b-140">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="07a6b-141">Bei der Skripterstellung lautet der Berechtigungs Name " **SeSecurityPrivilege**".</span><span class="sxs-lookup"><span data-stu-id="07a6b-141">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="07a6b-142">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="07a6b-142">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="07a6b-143">Wenn die Eigenschaften des Gruppen Vertrauens nehmers und des Besitzer Treuhänders nicht **null** sind, werden Sie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="07a6b-143">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="07a6b-144">Andernfalls behält WMI die ursprünglichen Werte bei.</span><span class="sxs-lookup"><span data-stu-id="07a6b-144">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="07a6b-145">Weitere Informationen finden Sie unter [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="07a6b-145">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="07a6b-146">Wenn eine neue SACL bei einem Aufruf dieser Methode **null** ist, bleibt die SACL der Sicherheits Beschreibung für das Sicherungs fähige Zielobjekt unverändert.</span><span class="sxs-lookup"><span data-stu-id="07a6b-146">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="examples"></a><span data-ttu-id="07a6b-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07a6b-147">Examples</span></span>

<span data-ttu-id="07a6b-148">Das PowerShell [-Beispiel Copy-acltoprinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) ersetzt die Berechtigungen (ACL) von einem Drucker zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="07a6b-148">The [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell sample Replace the permissions (ACL) from one printer to another.</span></span>

<span data-ttu-id="07a6b-149">Im folgenden PowerShell-Codebeispiel wird beschrieben, wie die Sicherheits Beschreibung für einen Drucker festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="07a6b-149">The following PowerShell code sample describes how to set the security descriptor for a printer.</span></span>


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a><span data-ttu-id="07a6b-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07a6b-150">Requirements</span></span>



| <span data-ttu-id="07a6b-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07a6b-151">Requirement</span></span> | <span data-ttu-id="07a6b-152">Wert</span><span class="sxs-lookup"><span data-stu-id="07a6b-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a6b-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07a6b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="07a6b-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07a6b-154">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="07a6b-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07a6b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="07a6b-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07a6b-156">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="07a6b-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="07a6b-157">Namespace</span></span><br/>                | <span data-ttu-id="07a6b-158">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07a6b-158">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="07a6b-159">MOF</span><span class="sxs-lookup"><span data-stu-id="07a6b-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07a6b-160"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="07a6b-160"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="07a6b-161">DLL</span><span class="sxs-lookup"><span data-stu-id="07a6b-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07a6b-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07a6b-162"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="07a6b-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07a6b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a6b-164">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="07a6b-164">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="07a6b-165">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="07a6b-165">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="07a6b-166">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="07a6b-166">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="07a6b-167">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="07a6b-167">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

