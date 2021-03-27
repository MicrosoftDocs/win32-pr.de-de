---
description: Iuseridentitymanager wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Iuseridentitymanager-Schnittstelle (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861783"
---
# <a name="iuseridentitymanager-interface"></a><span data-ttu-id="67df7-104">Iuseridentitymanager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="67df7-104">IUserIdentityManager interface</span></span>

<span data-ttu-id="67df7-105">\[**Iuseridentitymanager** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="67df7-105">\[**IUserIdentityManager** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="67df7-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="67df7-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="67df7-107">Macht Methoden verfügbar, mit denen Benutzer Identitäten im System identifiziert, aufgelistet und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="67df7-107">Exposes methods that identify, enumerate, and manage user identities on the system.</span></span>

## <a name="members"></a><span data-ttu-id="67df7-108">Member</span><span class="sxs-lookup"><span data-stu-id="67df7-108">Members</span></span>

<span data-ttu-id="67df7-109">Die **iuseridentitymanager** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="67df7-109">The **IUserIdentityManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67df7-110">**Iuseridentitymanager** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="67df7-110">**IUserIdentityManager** also has these types of members:</span></span>

-   [<span data-ttu-id="67df7-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="67df7-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67df7-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="67df7-112">Methods</span></span>

<span data-ttu-id="67df7-113">Die **iuseridentitymanager** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="67df7-113">The **IUserIdentityManager** interface has these methods.</span></span>



| <span data-ttu-id="67df7-114">Methode</span><span class="sxs-lookup"><span data-stu-id="67df7-114">Method</span></span>                                                                  | <span data-ttu-id="67df7-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67df7-115">Description</span></span>                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67df7-116">**-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="67df7-116">**EnumIdentities**</span></span>](iuseridentitymanager-enumidentities.md)           | <span data-ttu-id="67df7-117">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="67df7-117">Deprecated.</span></span> <span data-ttu-id="67df7-118">Ruft ein [**ienumuseridentity**](ienumuseridentity.md) -Objekt ab, das verwendet werden kann, um die Benutzer Identitäten aufzulisten, die auf dem System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="67df7-118">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span><br/> |
| [<span data-ttu-id="67df7-119">**Getidentitybycookie**</span><span class="sxs-lookup"><span data-stu-id="67df7-119">**GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md) | <span data-ttu-id="67df7-120">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="67df7-120">Deprecated.</span></span> <span data-ttu-id="67df7-121">Ruft eine bestimmte Benutzeridentität durch das Cookie ab, das zur eindeutigen Identifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="67df7-121">Gets a specific user identity by the cookie used to uniquely identify it.</span></span><br/>                                                                        |
| [<span data-ttu-id="67df7-122">**Abmeldung**</span><span class="sxs-lookup"><span data-stu-id="67df7-122">**Logoff**</span></span>](iuseridentitymanager-logoff.md)                           | <span data-ttu-id="67df7-123">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="67df7-123">Deprecated.</span></span> <span data-ttu-id="67df7-124">Melden Sie sich von der aktuellen Identität ab.</span><span class="sxs-lookup"><span data-stu-id="67df7-124">Log off the current identity.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="67df7-125">**Anmelden**</span><span class="sxs-lookup"><span data-stu-id="67df7-125">**Logon**</span></span>](iuseridentitymanager-logon.md)                             | <span data-ttu-id="67df7-126">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="67df7-126">Deprecated.</span></span> <span data-ttu-id="67df7-127">Zeigt dem Benutzer eine Benutzeroberfläche an und ermöglicht dem Benutzer die Auswahl einer Benutzeridentität.</span><span class="sxs-lookup"><span data-stu-id="67df7-127">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="67df7-128">Bei erfolgreicher Ausführung wird die Benutzeridentität angemeldet und abgerufen.</span><span class="sxs-lookup"><span data-stu-id="67df7-128">If successful, the user identity will be logged on and retrieved.</span></span><br/>        |
| [<span data-ttu-id="67df7-129">**Manageidentities**</span><span class="sxs-lookup"><span data-stu-id="67df7-129">**ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)       | <span data-ttu-id="67df7-130">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="67df7-130">Deprecated.</span></span> <span data-ttu-id="67df7-131">Zeigt dem Benutzer eine Benutzeroberfläche an und ermöglicht dem Benutzer die Verwaltung von Benutzer Identitäten.</span><span class="sxs-lookup"><span data-stu-id="67df7-131">Displays a UI to the user, allowing the user to manage user identities.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="67df7-132">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="67df7-132">Requirements</span></span>



| <span data-ttu-id="67df7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67df7-133">Requirement</span></span> | <span data-ttu-id="67df7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="67df7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67df7-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67df7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="67df7-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67df7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="67df7-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67df7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="67df7-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67df7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="67df7-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="67df7-139">End of client support</span></span><br/>    | <span data-ttu-id="67df7-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="67df7-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="67df7-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="67df7-141">End of server support</span></span><br/>    | <span data-ttu-id="67df7-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67df7-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="67df7-143">Header</span><span class="sxs-lookup"><span data-stu-id="67df7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="67df7-144"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="67df7-144"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="67df7-145">IDL</span><span class="sxs-lookup"><span data-stu-id="67df7-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67df7-146"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67df7-146"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="67df7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="67df7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67df7-148"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67df7-148"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67df7-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="67df7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67df7-150">**Iuseridentity**</span><span class="sxs-lookup"><span data-stu-id="67df7-150">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="67df7-151">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="67df7-151">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="67df7-152">**Iumumuseridentity**</span><span class="sxs-lookup"><span data-stu-id="67df7-152">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="67df7-153">**Iidentitychangenotify**</span><span class="sxs-lookup"><span data-stu-id="67df7-153">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> </dl>

 

 
