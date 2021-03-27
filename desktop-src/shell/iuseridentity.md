---
description: Iuseridentity wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Iuseridentity-Schnittstelle (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979481"
---
# <a name="iuseridentity-interface"></a><span data-ttu-id="5958e-104">Iuseridentity-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5958e-104">IUserIdentity interface</span></span>

<span data-ttu-id="5958e-105">\[**Iuseridentity** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5958e-105">\[**IUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5958e-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="5958e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5958e-107">Macht Methoden verfügbar, die Identifikations-, Registrierungs-und Ordner Daten für eine bestimmte Benutzeridentität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5958e-107">Exposes methods that provide identification, registry, and folder data for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="5958e-108">Member</span><span class="sxs-lookup"><span data-stu-id="5958e-108">Members</span></span>

<span data-ttu-id="5958e-109">Die **iuseridentity** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5958e-109">The **IUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5958e-110">**Iuseridentity** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5958e-110">**IUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="5958e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="5958e-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5958e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="5958e-112">Methods</span></span>

<span data-ttu-id="5958e-113">Die **iuseridentity** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5958e-113">The **IUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="5958e-114">Methode</span><span class="sxs-lookup"><span data-stu-id="5958e-114">Method</span></span>                                                         | <span data-ttu-id="5958e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5958e-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5958e-116">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="5958e-116">**GetCookie**</span></span>](iuseridentity-getcookie.md)                   | <span data-ttu-id="5958e-117">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5958e-117">Deprecated.</span></span> <span data-ttu-id="5958e-118">Ruft das Cookie ab, mit dem diese Benutzeridentität eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5958e-118">Gets the cookie used to uniquely identify this user identity.</span></span><br/>             |
| [<span data-ttu-id="5958e-119">**Getidentityfolder**</span><span class="sxs-lookup"><span data-stu-id="5958e-119">**GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)   | <span data-ttu-id="5958e-120">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5958e-120">Deprecated.</span></span> <span data-ttu-id="5958e-121">Ruft den Datei Ordner ab, der dieser Identität zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5958e-121">Gets the file folder associated with this identity.</span></span><br/>                       |
| [<span data-ttu-id="5958e-122">**GetName**</span><span class="sxs-lookup"><span data-stu-id="5958e-122">**GetName**</span></span>](iuseridentity-getname.md)                       | <span data-ttu-id="5958e-123">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5958e-123">Deprecated.</span></span> <span data-ttu-id="5958e-124">Ruft den Namen ab, der dieser Benutzeridentität zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5958e-124">Gets the name associated with this user identity.</span></span><br/>                         |
| [<span data-ttu-id="5958e-125">**Openidentityregkey**</span><span class="sxs-lookup"><span data-stu-id="5958e-125">**OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md) | <span data-ttu-id="5958e-126">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5958e-126">Deprecated.</span></span> <span data-ttu-id="5958e-127">Ruft den Schlüssel in der Registrierung ab, der dieser Benutzeridentität entspricht.</span><span class="sxs-lookup"><span data-stu-id="5958e-127">Retrieves the key in the registry that corresponds to this user identity.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5958e-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5958e-128">Remarks</span></span>

<span data-ttu-id="5958e-129">Diese Schnittstelle stellt Informationen bereit, die einer bestimmten Benutzeridentität entsprechen, die auf dem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5958e-129">This interface provides information that corresponds to a specific user identity present on the system.</span></span> <span data-ttu-id="5958e-130">Sie können auf den Identitäts Ordner dieser Benutzeridentität, den zugehörigen Registrierungsschlüssel und das zugehörige Identifikations Cookie zugreifen und den Namen abrufen, der der Benutzeridentität zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5958e-130">You can access this user identity's identity folder, its registry key, and its identification cookie, as well as retrieve the name associated with the user identity.</span></span>

## <a name="requirements"></a><span data-ttu-id="5958e-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5958e-131">Requirements</span></span>



| <span data-ttu-id="5958e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5958e-132">Requirement</span></span> | <span data-ttu-id="5958e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5958e-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5958e-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5958e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5958e-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5958e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5958e-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5958e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5958e-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5958e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5958e-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="5958e-138">End of client support</span></span><br/>    | <span data-ttu-id="5958e-139">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5958e-139">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="5958e-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5958e-140">End of server support</span></span><br/>    | <span data-ttu-id="5958e-141">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5958e-141">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="5958e-142">Header</span><span class="sxs-lookup"><span data-stu-id="5958e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5958e-143"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="5958e-143"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5958e-144">IDL</span><span class="sxs-lookup"><span data-stu-id="5958e-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5958e-145"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5958e-145"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5958e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5958e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5958e-147"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5958e-147"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5958e-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5958e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5958e-149">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="5958e-149">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="5958e-150">**Iuseridentitymanager**</span><span class="sxs-lookup"><span data-stu-id="5958e-150">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="5958e-151">**Iumumuseridentity**</span><span class="sxs-lookup"><span data-stu-id="5958e-151">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> </dl>

 

 
