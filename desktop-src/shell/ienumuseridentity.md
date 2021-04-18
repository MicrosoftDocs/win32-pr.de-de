---
description: Ienumumuseridentity wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Ienumumuseridentity-Schnittstelle (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979504"
---
# <a name="ienumuseridentity-interface"></a><span data-ttu-id="c6758-104">Ienumumuseridentity-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c6758-104">IEnumUserIdentity interface</span></span>

<span data-ttu-id="c6758-105">\[**Ienumumuseridentity** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c6758-105">\[**IEnumUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="c6758-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="c6758-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="c6758-107">Stellt eine Enumeration aller Benutzer Identitäten bereit, die auf dem System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c6758-107">Provides enumeration of all user identities present on the system.</span></span>

## <a name="members"></a><span data-ttu-id="c6758-108">Member</span><span class="sxs-lookup"><span data-stu-id="c6758-108">Members</span></span>

<span data-ttu-id="c6758-109">Die **ienumumuseridentity** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c6758-109">The **IEnumUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c6758-110">**Ienumuseridentity** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c6758-110">**IEnumUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="c6758-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c6758-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c6758-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c6758-112">Methods</span></span>

<span data-ttu-id="c6758-113">Die **ienumumuseridentity** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c6758-113">The **IEnumUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="c6758-114">Methode</span><span class="sxs-lookup"><span data-stu-id="c6758-114">Method</span></span>                                         | <span data-ttu-id="c6758-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6758-115">Description</span></span>                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6758-116">**Klon**</span><span class="sxs-lookup"><span data-stu-id="c6758-116">**Clone**</span></span>](ienumuseridentity-clone.md)       | <span data-ttu-id="c6758-117">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c6758-117">Deprecated.</span></span> <span data-ttu-id="c6758-118">Ruft eine Kopie der aktuellen Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="c6758-118">Gets a copy of the current enumeration.</span></span><br/>                                                               |
| [<span data-ttu-id="c6758-119">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="c6758-119">**GetCount**</span></span>](ienumuseridentity-getcount.md) | <span data-ttu-id="c6758-120">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c6758-120">Deprecated.</span></span> <span data-ttu-id="c6758-121">Ruft die Anzahl der Benutzer Identitäten ab, die sich zurzeit im System befinden.</span><span class="sxs-lookup"><span data-stu-id="c6758-121">Gets the count of user identities currently on the system.</span></span><br/>                                            |
| [<span data-ttu-id="c6758-122">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="c6758-122">**Next**</span></span>](ienumuseridentity-next.md)         | <span data-ttu-id="c6758-123">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c6758-123">Deprecated.</span></span> <span data-ttu-id="c6758-124">Ruft ein Array von Benutzer Identitäts Schnittstellen aus der-Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="c6758-124">Retrieves an array of user identity interfaces from the enumeration.</span></span><br/>                                  |
| [<span data-ttu-id="c6758-125">**Festlegen**</span><span class="sxs-lookup"><span data-stu-id="c6758-125">**Reset**</span></span>](ienumuseridentity-reset.md)       | <span data-ttu-id="c6758-126">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c6758-126">Deprecated.</span></span> <span data-ttu-id="c6758-127">Setzt die interne Anzahl der abgerufenen Schnittstellen in der-Enumeration zurück.</span><span class="sxs-lookup"><span data-stu-id="c6758-127">Resets the internal count of retrieved interfaces in the enumeration.</span></span><br/>                                 |
| [<span data-ttu-id="c6758-128">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="c6758-128">**Skip**</span></span>](ienumuseridentity-skip.md)         | <span data-ttu-id="c6758-129">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c6758-129">Deprecated.</span></span> <span data-ttu-id="c6758-130">Überspringt eine angegebene Anzahl von Benutzer Identitäts Schnittstellen in der-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="c6758-130">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="c6758-131">Wird beim Abrufen von Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6758-131">Used when retrieving interfaces.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6758-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6758-132">Remarks</span></span>

<span data-ttu-id="c6758-133">Zum Abrufen von Informationen zu Benutzer Identitäten, die auf dem System vorhanden sind, können Sie diese Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6758-133">To retrieve information about user identities present on the system, you can use this interface.</span></span> <span data-ttu-id="c6758-134">Über eine [**iuseridentitymanager**](iuseridentitymanager.md) -Schnittstelle können Sie [**iuseridentitymanager:: tumidentities**](iuseridentitymanager-enumidentities.md) aufrufen, um diese Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6758-134">From a [**IUserIdentityManager**](iuseridentitymanager.md) interface, you can call [**IUserIdentityManager::EnumIdentities**](iuseridentitymanager-enumidentities.md) to retrieve this interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6758-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c6758-135">Requirements</span></span>



| <span data-ttu-id="c6758-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6758-136">Requirement</span></span> | <span data-ttu-id="c6758-137">Wert</span><span class="sxs-lookup"><span data-stu-id="c6758-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6758-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6758-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c6758-139">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6758-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c6758-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6758-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c6758-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6758-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c6758-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c6758-142">End of client support</span></span><br/>    | <span data-ttu-id="c6758-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6758-143">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="c6758-144">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c6758-144">End of server support</span></span><br/>    | <span data-ttu-id="c6758-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6758-145">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c6758-146">Header</span><span class="sxs-lookup"><span data-stu-id="c6758-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6758-147"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6758-147"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6758-148">IDL</span><span class="sxs-lookup"><span data-stu-id="c6758-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6758-149"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6758-149"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="c6758-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c6758-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6758-151"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6758-151"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6758-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6758-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6758-153">**Iuseridentitymanager**</span><span class="sxs-lookup"><span data-stu-id="c6758-153">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> </dl>

 

 
