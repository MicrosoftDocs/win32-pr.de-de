---
description: Legt die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern fest, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: '__SystemSecurity:: Set9XUserList-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: dd377da3adf55aef6a78576e1c978196f349f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362893"
---
# <a name="__systemsecurityset9xuserlist-method"></a><span data-ttu-id="e98e2-103">\_\_SystemSecurity:: Set9XUserList-Methode</span><span class="sxs-lookup"><span data-stu-id="e98e2-103">\_\_SystemSecurity::Set9XUserList method</span></span>

<span data-ttu-id="e98e2-104">Die **\_ \_ SystemSecurity:: Set9XUserList** -Methode legt die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern fest, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e98e2-104">The **\_\_SystemSecurity::Set9XUserList** method sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="e98e2-105">Die Liste wird als Array von eingebetteten Objekten angegeben, wobei jedes Objekt eine Instanz der [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) -Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="e98e2-105">The list is specified as an array of embedded objects where each object is an instance of the [**\_\_NTLMUser9X**](--ntlmuser9x.md) class.</span></span> <span data-ttu-id="e98e2-106">Diese Funktion ähnelt der Sicherheits Beschreibung, ist aber eingeschränkter.</span><span class="sxs-lookup"><span data-stu-id="e98e2-106">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="e98e2-107">Gruppen werden nicht unterstützt, und es gibt keine Kontrolle über den lokalen Zugriff, da der lokale Benutzer immer über Vollzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="e98e2-107">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="e98e2-108">Sowohl Deny-als auch Zulassungs Zugriffs Steuerungs Einträge (ACE) sind zulässig, und aus diesem Grund ist die ACE-Reihenfolge in der freigegebenen Zugriffs Steuerungs Liste (DACL) wichtig.</span><span class="sxs-lookup"><span data-stu-id="e98e2-108">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="e98e2-109">Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="e98e2-109">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="e98e2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e98e2-110">Syntax</span></span>


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="e98e2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e98e2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e98e2-112">*UL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e98e2-112">*ul* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e98e2-113">Array von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="e98e2-113">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e98e2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e98e2-114">Return value</span></span>

<span data-ttu-id="e98e2-115">Diese Methode gibt ein **HRESULT** zurück, das den Status des Methoden Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="e98e2-115">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="e98e2-116">In der folgenden Liste sind die Rückgabewerte aufgelistet, die für **Set9XUserList** von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="e98e2-116">The following list lists the return values that are of significance to **Set9XUserList**.</span></span> <span data-ttu-id="e98e2-117">Für Skript-und Visual Basic Anwendungen kann das Ergebnis aus " [OutParameters. returnValue](parsing-outparameters-objects.md)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e98e2-117">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="e98e2-118">Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e98e2-118">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="e98e2-119">**WBEM \_ E- \_ Methode \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="e98e2-119">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="e98e2-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e98e2-120">This method is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e98e2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e98e2-121">Requirements</span></span>



| <span data-ttu-id="e98e2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e98e2-122">Requirement</span></span> | <span data-ttu-id="e98e2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e98e2-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e98e2-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e98e2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e98e2-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e98e2-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e98e2-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e98e2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e98e2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e98e2-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e98e2-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e98e2-128">Namespace</span></span><br/>                | <span data-ttu-id="e98e2-129">alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="e98e2-129">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e98e2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e98e2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98e2-131">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="e98e2-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e98e2-132">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="e98e2-132">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="e98e2-133">**\_\_SystemSecurity:: getd**</span><span class="sxs-lookup"><span data-stu-id="e98e2-133">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="e98e2-134">**\_\_SystemSecurity::-ID**</span><span class="sxs-lookup"><span data-stu-id="e98e2-134">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="e98e2-135">**Win32- \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="e98e2-135">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="e98e2-136">**Win32- \_ securityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e98e2-136">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="e98e2-137">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="e98e2-137">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="e98e2-138">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="e98e2-138">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

