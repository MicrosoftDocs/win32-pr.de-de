---
description: Ruft die Sicherheits Beschreibung ab, die steuert, wer eine DCOM-Anwendung konfigurieren darf.
ms.assetid: 2858a7a0-1e5b-47aa-9967-0f578c3c22c1
ms.tgt_platform: multiple
title: Getconfigurationsecuritydescriptor-Methode der Win32_DCOMApplicationSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 320af05b352641c812c51353c2e7bda0da046bb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748129"
---
# <a name="getconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="be679-103">Getconfigurationsecuritydescriptor-Methode der Win32 \_ dcomapplicationsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="be679-103">GetConfigurationSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="be679-104">Die WMI-Methode **getconfigurationsecuritydescriptor** Ruft die Sicherheits Beschreibung ab, die steuert, wer eine DCOM-Anwendung konfigurieren darf.</span><span class="sxs-lookup"><span data-stu-id="be679-104">The **GetConfigurationSecurityDescriptor** WMI method gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span> <span data-ttu-id="be679-105">Die Sicherheits Beschreibung ist eine Instanz der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="be679-105">The security descriptor is a instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="be679-106">Das Konto, auf dem das Skript oder die Anwendung ausgeführt wird, das diese Methode aufruft, muss über die Berechtigungen **SeSecurityPrivilege** und **SeRestorePrivilege** verfügen.</span><span class="sxs-lookup"><span data-stu-id="be679-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="be679-107">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="be679-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="be679-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="be679-108">Syntax</span></span>


```mof
uint32 GetConfigurationSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="be679-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="be679-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be679-110">*Deskriptor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be679-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be679-111">Die Sicherheits Beschreibung, die für die DCOM-Anwendung festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="be679-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be679-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be679-112">Return value</span></span>

<span data-ttu-id="be679-113">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="be679-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="be679-114">Weitere Informationen finden Sie unter [WMI-Rückgabe Codes](/windows/desktop/WmiSdk/wmi-return-codes) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="be679-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="be679-115">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="be679-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="be679-116">0</span><span class="sxs-lookup"><span data-stu-id="be679-116">0</span></span>

<span data-ttu-id="be679-117">Erfolgreicher Abschluss</span><span class="sxs-lookup"><span data-stu-id="be679-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="be679-118">**2**</span><span class="sxs-lookup"><span data-stu-id="be679-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="be679-119">Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="be679-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="be679-120">**8**</span><span class="sxs-lookup"><span data-stu-id="be679-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="be679-121">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="be679-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="be679-122">**9**</span><span class="sxs-lookup"><span data-stu-id="be679-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="be679-123">Der Benutzer verfügt nicht über die erforderlichen Berechtigungen zum Ausführen der Methode.</span><span class="sxs-lookup"><span data-stu-id="be679-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="be679-124">**21**</span><span class="sxs-lookup"><span data-stu-id="be679-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="be679-125">Ein im Methoden Aufrufwert angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="be679-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="be679-126">**Andere**</span><span class="sxs-lookup"><span data-stu-id="be679-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="be679-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="be679-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be679-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be679-128">Remarks</span></span>

<span data-ttu-id="be679-129">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="be679-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="be679-130">Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="be679-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="be679-131">Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="be679-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="be679-132">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="be679-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="be679-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be679-133">Requirements</span></span>



| <span data-ttu-id="be679-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be679-134">Requirement</span></span> | <span data-ttu-id="be679-135">Wert</span><span class="sxs-lookup"><span data-stu-id="be679-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be679-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be679-136">Minimum supported client</span></span><br/> | <span data-ttu-id="be679-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be679-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be679-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be679-138">Minimum supported server</span></span><br/> | <span data-ttu-id="be679-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be679-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be679-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="be679-140">Namespace</span></span><br/>                | <span data-ttu-id="be679-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="be679-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be679-142">MOF</span><span class="sxs-lookup"><span data-stu-id="be679-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be679-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="be679-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be679-144">DLL</span><span class="sxs-lookup"><span data-stu-id="be679-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be679-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be679-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be679-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be679-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be679-147">**Win32- \_ dcomapplicationsetting**</span><span class="sxs-lookup"><span data-stu-id="be679-147">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="be679-148">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="be679-148">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="be679-149">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="be679-149">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="be679-150">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="be679-150">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

