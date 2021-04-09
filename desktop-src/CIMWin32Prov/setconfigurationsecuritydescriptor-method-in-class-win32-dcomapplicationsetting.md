---
description: Aktualisiert die Konfigurations Sicherheits Beschreibung der DCOM-Anwendung mit einer neuen Sicherheits Beschreibung, die durch eine Instanz einer Win32 \_ securityDescriptor-Klasse definiert wird.
ms.assetid: e0fe3d2f-7641-4cae-972d-888e800548de
ms.tgt_platform: multiple
title: Setconfigurationsecuritydescriptor-Methode der Win32_DCOMApplicationSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8556e49d2e87e12763e3f0699bcff1f786ac1e72
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860704"
---
# <a name="setconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="3d3a8-103">Setconfigurationsecuritydescriptor-Methode der Win32 \_ dcomapplicationsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="3d3a8-103">SetConfigurationSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="3d3a8-104">Die **setconfigurationsecuritydescriptor** -Methode aktualisiert die Konfigurations Sicherheits Beschreibung der DCOM-Anwendung mit einer neuen Sicherheits Beschreibung, die durch eine Instanz einer [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-104">The **SetConfigurationSecurityDescriptor** method updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="3d3a8-105">Diese Sicherheits Beschreibung steuert, wer die Anwendung konfigurieren darf.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-105">This security descriptor controls who is allowed to configure the application.</span></span> <span data-ttu-id="3d3a8-106">Das Konto, auf dem das Skript oder die Anwendung ausgeführt wird, das diese Methode aufruft, muss über die Berechtigungen **SeSecurityPrivilege** und **SeRestorePrivilege** verfügen.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="3d3a8-107">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="3d3a8-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3a8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d3a8-108">Syntax</span></span>


```mof
uint32 SetConfigurationSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="3d3a8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d3a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d3a8-110">*Deskriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d3a8-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3a8-111">Die Sicherheits Beschreibung, die für die DCOM-Anwendung festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d3a8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d3a8-112">Return value</span></span>

<span data-ttu-id="3d3a8-113">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="3d3a8-114">Weitere Informationen finden Sie unter [WMI-Rückgabe Codes](/windows/desktop/WmiSdk/wmi-return-codes) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3d3a8-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="3d3a8-115">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3d3a8-116">0</span><span class="sxs-lookup"><span data-stu-id="3d3a8-116">0</span></span>

<span data-ttu-id="3d3a8-117">Erfolgreicher Abschluss</span><span class="sxs-lookup"><span data-stu-id="3d3a8-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="3d3a8-118">**2**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3d3a8-119">Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="3d3a8-120">**8**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3d3a8-121">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="3d3a8-122">**9**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3d3a8-123">Der Benutzer verfügt nicht über die erforderlichen Berechtigungen zum Ausführen der Methode.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="3d3a8-124">**21**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3d3a8-125">Ein im Methoden Aufrufwert angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="3d3a8-126">**Andere**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3d3a8-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="3d3a8-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d3a8-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d3a8-128">Remarks</span></span>

<span data-ttu-id="3d3a8-129">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="3d3a8-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="3d3a8-130">Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="3d3a8-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="3d3a8-131">Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="3d3a8-132">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="3d3a8-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="3d3a8-133">Wenn Sie diese Methode aufrufen, können Sie sowohl die DACL als auch die SACL in der [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz aktualisieren, aber Sie können auch nur die DACL oder nur die SACL aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-133">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="3d3a8-134">Die folgenden Werte im [**Sicherheits \_ Deskriptor- \_ Steuer**](/windows/desktop/SecAuthZ/security-descriptor-control) Element bestimmen, ob die DACL, die SACL oder beides aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-134">The following values in the [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="3d3a8-135">**SE \_ DACL \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-135">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="3d3a8-136">Gibt an, dass die DACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-136">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="3d3a8-137">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-137">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="3d3a8-138">**SE \_ SACL \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-138">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="3d3a8-139">Gibt an, dass die SACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-139">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="3d3a8-140">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-140">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="3d3a8-141">Zum Aktualisieren der SACL muss für das Konto die Berechtigung " **SeSecurityPrivilege** " aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-141">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="3d3a8-142">Bei der Skripterstellung lautet der Berechtigungs Name " **SeSecurityPrivilege**".</span><span class="sxs-lookup"><span data-stu-id="3d3a8-142">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="3d3a8-143">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="3d3a8-143">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="3d3a8-144">Wenn die Eigenschaften des Gruppen Vertrauens nehmers und des Besitzer Treuhänders nicht **null** sind, werden Sie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-144">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="3d3a8-145">Andernfalls behält WMI die ursprünglichen Werte bei.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-145">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="3d3a8-146">Weitere Informationen finden Sie unter [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="3d3a8-146">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="3d3a8-147">Wenn eine neue SACL bei einem Aufruf dieser Methode **null** ist, bleibt die SACL der Sicherheits Beschreibung für das Sicherungs fähige Zielobjekt unverändert.</span><span class="sxs-lookup"><span data-stu-id="3d3a8-147">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3a8-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d3a8-148">Requirements</span></span>



| <span data-ttu-id="3d3a8-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d3a8-149">Requirement</span></span> | <span data-ttu-id="3d3a8-150">Wert</span><span class="sxs-lookup"><span data-stu-id="3d3a8-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3a8-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d3a8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3a8-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d3a8-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d3a8-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d3a8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3a8-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d3a8-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d3a8-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d3a8-155">Namespace</span></span><br/>                | <span data-ttu-id="3d3a8-156">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3d3a8-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d3a8-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3d3a8-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d3a8-158"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3d3a8-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d3a8-159">DLL</span><span class="sxs-lookup"><span data-stu-id="3d3a8-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d3a8-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d3a8-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d3a8-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d3a8-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3a8-162">**Win32- \_ dcomapplicationsetting**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-162">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="3d3a8-163">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="3d3a8-163">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="3d3a8-164">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="3d3a8-164">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="3d3a8-165">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="3d3a8-165">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

