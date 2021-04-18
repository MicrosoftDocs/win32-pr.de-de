---
description: Ruft die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, bei denen die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: '__SystemSecurity:: Get9XUserList-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350804"
---
# <a name="__systemsecurityget9xuserlist-method"></a><span data-ttu-id="4800f-103">\_\_SystemSecurity:: Get9XUserList-Methode</span><span class="sxs-lookup"><span data-stu-id="4800f-103">\_\_SystemSecurity::Get9XUserList method</span></span>

<span data-ttu-id="4800f-104">Die [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) -Methode ruft die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4800f-104">The [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) method gets the remote access rights for a list of individual users on computers running obsolete versions of Windows , where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="4800f-105">Diese Funktion ähnelt der Sicherheits Beschreibung, ist aber eingeschränkter.</span><span class="sxs-lookup"><span data-stu-id="4800f-105">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="4800f-106">Gruppen werden nicht unterstützt, und es gibt keine Kontrolle über den lokalen Zugriff, da der lokale Benutzer immer über Vollzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="4800f-106">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="4800f-107">Sowohl Deny-als auch Zulassungs Zugriffs Steuerungs Einträge (ACE) sind zulässig, und aus diesem Grund ist die ACE-Reihenfolge in der freigegebenen Zugriffs Steuerungs Liste (DACL) wichtig.</span><span class="sxs-lookup"><span data-stu-id="4800f-107">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="4800f-108">Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="4800f-108">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="4800f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4800f-109">Syntax</span></span>


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="4800f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4800f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4800f-111">*UL* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4800f-111">*ul* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4800f-112">Array von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="4800f-112">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4800f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4800f-113">Return value</span></span>

<span data-ttu-id="4800f-114">Diese Methode gibt ein **HRESULT** zurück, das den Status des Methoden Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="4800f-114">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="4800f-115">In der folgenden Liste sind die Rückgabewerte aufgelistet, die für **Get9XUserList** von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="4800f-115">The following list lists the return values that are of significance to **Get9XUserList**.</span></span> <span data-ttu-id="4800f-116">Für Skript-und Visual Basic Anwendungen kann das Ergebnis [OutParameters. returnValue](parsing-outparameters-objects.md)sein.</span><span class="sxs-lookup"><span data-stu-id="4800f-116">For scripting and Visual Basic applications, the result can be [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="4800f-117">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4800f-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="4800f-118">**WBEM \_ E- \_ Methode \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="4800f-118">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="4800f-119">Diese Methode wird auf unterstützten Versionen von Windows nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4800f-119">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4800f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4800f-120">Requirements</span></span>



| <span data-ttu-id="4800f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4800f-121">Requirement</span></span> | <span data-ttu-id="4800f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4800f-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4800f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4800f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4800f-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4800f-124">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4800f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4800f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4800f-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4800f-126">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4800f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4800f-127">Namespace</span></span><br/>                | <span data-ttu-id="4800f-128">alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="4800f-128">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4800f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4800f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4800f-130">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="4800f-130">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4800f-131">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="4800f-131">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="4800f-132">**\_\_SystemSecurity:: getd**</span><span class="sxs-lookup"><span data-stu-id="4800f-132">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="4800f-133">**\_\_SystemSecurity::-ID**</span><span class="sxs-lookup"><span data-stu-id="4800f-133">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="4800f-134">**Win32- \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="4800f-134">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="4800f-135">**Win32- \_ securityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4800f-135">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="4800f-136">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="4800f-136">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="4800f-137">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="4800f-137">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

