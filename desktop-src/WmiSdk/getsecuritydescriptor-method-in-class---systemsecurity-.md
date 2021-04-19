---
description: Ruft die Sicherheits Beschreibung ab, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind. Die Sicherheits Beschreibung wird als Instanz von \_ \_ securityDescriptor zurückgegeben.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Getsecuritydescriptor-Methode der __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363615"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="ccf49-104">Getsecuritydescriptor-Methode der \_ \_ System Security-Klasse</span><span class="sxs-lookup"><span data-stu-id="ccf49-104">GetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="ccf49-105">Die **getsecuritydescriptor** -Methode ruft die Sicherheits Beschreibung ab, die den Zugriff auf den WMI-Namespace steuert, mit dem Sie verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="ccf49-105">The **GetSecurityDescriptor** method gets the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="ccf49-106">Die Sicherheits Beschreibung wird als Instanz von [**\_ \_ securityDescriptor**](--securitydescriptor.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ccf49-106">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="ccf49-107">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ccf49-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf49-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccf49-108">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="ccf49-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccf49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf49-110">*Deskriptor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ccf49-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf49-111">Die Sicherheits Beschreibung, die dem WMI-Namespace zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ccf49-111">The security descriptor associated with the WMI namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf49-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccf49-112">Return value</span></span>

<span data-ttu-id="ccf49-113">Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ccf49-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="ccf49-114">Weitere Informationen finden Sie unter [WMI-Rückgabe Codes](wmi-return-codes.md) oder [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ccf49-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="ccf49-115">**0**</span><span class="sxs-lookup"><span data-stu-id="ccf49-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ccf49-116">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="ccf49-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="ccf49-117">**2**</span><span class="sxs-lookup"><span data-stu-id="ccf49-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ccf49-118">Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="ccf49-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ccf49-119">**8**</span><span class="sxs-lookup"><span data-stu-id="ccf49-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ccf49-120">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ccf49-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ccf49-121">**9**</span><span class="sxs-lookup"><span data-stu-id="ccf49-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ccf49-122">Der Benutzer verfügt nicht über die erforderlichen Berechtigungen, um die Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ccf49-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="ccf49-123">**21**</span><span class="sxs-lookup"><span data-stu-id="ccf49-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ccf49-124">Ein im Methoden Aufrufwert angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ccf49-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccf49-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccf49-125">Remarks</span></span>

<span data-ttu-id="ccf49-126">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="ccf49-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="ccf49-127">Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="ccf49-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="ccf49-128">Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ccf49-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="ccf49-129">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md) und [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ccf49-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf49-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccf49-130">Requirements</span></span>



| <span data-ttu-id="ccf49-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccf49-131">Requirement</span></span> | <span data-ttu-id="ccf49-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ccf49-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ccf49-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccf49-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf49-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccf49-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ccf49-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccf49-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf49-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccf49-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ccf49-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccf49-137">Namespace</span></span><br/>                | <span data-ttu-id="ccf49-138">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="ccf49-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ccf49-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccf49-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf49-140">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="ccf49-140">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="ccf49-141">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="ccf49-141">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

