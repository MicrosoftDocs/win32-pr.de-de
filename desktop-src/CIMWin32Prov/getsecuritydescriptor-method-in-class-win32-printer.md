---
description: Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Drucker steuert.
ms.assetid: c12ca35c-07b3-41ad-98c4-48ee584059d1
ms.tgt_platform: multiple
title: Getsecuritydescriptor-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c74d79430d15fa136c6edeb2a6e77e79e76b02ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344951"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="bc36c-103">Getsecuritydescriptor-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="bc36c-103">GetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="bc36c-104">Die **getsecuritydescriptor** -Methode gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Drucker steuert.</span><span class="sxs-lookup"><span data-stu-id="bc36c-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="bc36c-105">Der Deskriptor wird als eine Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc36c-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="bc36c-106">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="bc36c-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="bc36c-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc36c-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bc36c-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bc36c-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc36c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc36c-109">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="bc36c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc36c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc36c-111">*Deskriptor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc36c-111">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc36c-112">Die dem Drucker zugeordnete Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="bc36c-112">The security descriptor associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc36c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc36c-113">Return value</span></span>

<span data-ttu-id="bc36c-114">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc36c-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="bc36c-115">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bc36c-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bc36c-116">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="bc36c-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bc36c-117">**0**</span><span class="sxs-lookup"><span data-stu-id="bc36c-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="bc36c-118">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="bc36c-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="bc36c-119">**2**</span><span class="sxs-lookup"><span data-stu-id="bc36c-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="bc36c-120">Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="bc36c-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="bc36c-121">**8**</span><span class="sxs-lookup"><span data-stu-id="bc36c-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="bc36c-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bc36c-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="bc36c-123">**9**</span><span class="sxs-lookup"><span data-stu-id="bc36c-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="bc36c-124">Der Benutzer verfügt nicht über die erforderlichen Berechtigungen, um die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bc36c-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="bc36c-125">**21**</span><span class="sxs-lookup"><span data-stu-id="bc36c-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="bc36c-126">Ein im Methoden Aufrufwert angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bc36c-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc36c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc36c-127">Remarks</span></span>

<span data-ttu-id="bc36c-128">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="bc36c-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="bc36c-129">Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="bc36c-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="bc36c-130">Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc36c-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="bc36c-131">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="bc36c-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="bc36c-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc36c-132">Examples</span></span>

<span data-ttu-id="bc36c-133">Im folgenden VBScript-Codebeispiel werden die Drucker aufgelistet, die mit dem lokalen Computer verbunden sind, und die Sicherheits Beschreibung für jeden Drucker abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bc36c-133">The following VBScript code example lists the printers attached to the local computer and gets the security descriptor for each printer.</span></span> <span data-ttu-id="bc36c-134">Anschließend werden die [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACE) in der freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) extrahiert, um zu bestimmen, welche Benutzer auf den Drucker zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="bc36c-134">Then the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACE) in the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) are extracted to determine which users have access to the printer.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set objWMIService = GetObject("winmgmts:")
Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        arrACEs = objSD.DACL
    For Each objACE in arrACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="requirements"></a><span data-ttu-id="bc36c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc36c-135">Requirements</span></span>



| <span data-ttu-id="bc36c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc36c-136">Requirement</span></span> | <span data-ttu-id="bc36c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="bc36c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc36c-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc36c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bc36c-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc36c-139">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="bc36c-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc36c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bc36c-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc36c-141">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="bc36c-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc36c-142">Namespace</span></span><br/>                | <span data-ttu-id="bc36c-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bc36c-143">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="bc36c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="bc36c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc36c-145"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bc36c-145"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc36c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="bc36c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc36c-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc36c-147"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bc36c-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc36c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc36c-149">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="bc36c-149">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="bc36c-150">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="bc36c-150">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="bc36c-151">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="bc36c-151">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="bc36c-152">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="bc36c-152">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

