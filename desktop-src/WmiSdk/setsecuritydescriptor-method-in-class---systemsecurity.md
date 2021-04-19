---
description: Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Die Sicherheits Beschreibung wird durch eine Instanz von \_ \_ securityDescriptor dargestellt.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: SETSECURITYDESCRIPTOR-Methode der __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364053"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="c5c8c-104">SETSECURITYDESCRIPTOR-Methode der \_ \_ System Security-Klasse</span><span class="sxs-lookup"><span data-stu-id="c5c8c-104">SetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="c5c8c-105">Die [**SETSECURITYDESCRIPTOR**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) -Methode schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-105">The [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) method writes an updated version of the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="c5c8c-106">Die Sicherheits Beschreibung wird durch eine Instanz von [**\_ \_ securityDescriptor**](--securitydescriptor.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-106">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="c5c8c-107">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c5c8c-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c8c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5c8c-108">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="c5c8c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5c8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5c8c-110">*Deskriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5c8c-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5c8c-111">Die Sicherheits Beschreibung, die dem WMI-Namespace zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-111">The security descriptor associated with the WMI Namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5c8c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5c8c-112">Return value</span></span>

<span data-ttu-id="c5c8c-113">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="c5c8c-114">Weitere Informationen finden Sie unter [WMI-Rückgabe Codes](wmi-return-codes.md) oder [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c5c8c-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="c5c8c-115">**0**</span><span class="sxs-lookup"><span data-stu-id="c5c8c-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c5c8c-116">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="c5c8c-117">**2**</span><span class="sxs-lookup"><span data-stu-id="c5c8c-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c5c8c-118">Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="c5c8c-119">**8**</span><span class="sxs-lookup"><span data-stu-id="c5c8c-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c5c8c-120">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="c5c8c-121">**9**</span><span class="sxs-lookup"><span data-stu-id="c5c8c-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c5c8c-122">Der Benutzer verfügt nicht über die erforderlichen Berechtigungen, um die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="c5c8c-123">**21**</span><span class="sxs-lookup"><span data-stu-id="c5c8c-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c5c8c-124">Ein im Methoden Aufrufwert angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5c8c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5c8c-125">Remarks</span></span>

<span data-ttu-id="c5c8c-126">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Access Control Liste*](/windows/desktop/SecGloss/a-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="c5c8c-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*System Access Control List*](/windows/desktop/SecGloss/a-gly) (SACL).</span></span> <span data-ttu-id="c5c8c-127">Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="c5c8c-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="c5c8c-128">Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="c5c8c-129">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c5c8c-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="c5c8c-130">Wenn Sie diese Methode aufrufen, können Sie sowohl die DACL als auch die SACL in der [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz aktualisieren, aber Sie können auch nur die DACL oder nur die SACL aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-130">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="c5c8c-131">Die folgenden Werte im [**Sicherheits \_ \_ deskriptorsteuerelement**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL oder die SACL oder beides aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-131">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL or the SACL or both are updated.</span></span>

-   <span data-ttu-id="c5c8c-132">**SE \_ DACL \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="c5c8c-132">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="c5c8c-133">Gibt an, dass die DACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-133">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="c5c8c-134">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-134">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="c5c8c-135">**SE \_ SACL \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="c5c8c-135">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="c5c8c-136">Gibt an, dass die SACL aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-136">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="c5c8c-137">Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-137">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="c5c8c-138">Zum Aktualisieren der SACL muss für das Konto die Berechtigung " **SeSecurityPrivilege** " aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-138">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="c5c8c-139">Bei der Skripterstellung lautet der Berechtigungs Name " **SeSecurityPrivilege**".</span><span class="sxs-lookup"><span data-stu-id="c5c8c-139">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="c5c8c-140">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c5c8c-140">For more information, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="c5c8c-141">Wenn die Eigenschaften des Gruppen Vertrauens nehmers und des Besitzer Treuhänders nicht **null** sind, werden Sie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-141">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="c5c8c-142">Andernfalls behält WMI die ursprünglichen Werte bei.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-142">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="c5c8c-143">Weitere Informationen finden Sie unter [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c5c8c-143">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span>

<span data-ttu-id="c5c8c-144">Wenn eine neue SACL in einem Aufruf dieser Methode **null** ist, bleibt die SACL der Sicherheits Beschreibung für das Sicherungs fähige Zielobjekt unverändert.</span><span class="sxs-lookup"><span data-stu-id="c5c8c-144">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c8c-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5c8c-145">Requirements</span></span>



| <span data-ttu-id="c5c8c-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5c8c-146">Requirement</span></span> | <span data-ttu-id="c5c8c-147">Wert</span><span class="sxs-lookup"><span data-stu-id="c5c8c-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c5c8c-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5c8c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c8c-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5c8c-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c5c8c-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5c8c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c8c-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5c8c-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c5c8c-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5c8c-152">Namespace</span></span><br/>                | <span data-ttu-id="c5c8c-153">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="c5c8c-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c5c8c-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5c8c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c8c-155">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="c5c8c-155">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="c5c8c-156">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="c5c8c-156">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

