---
description: Veraltet. Ermöglicht das Benachrichtigen von Änderungen an Benutzer Identitäten im System sowie Benutzer Anforderungen zum Wechseln der aktuellen Benutzeridentität.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Iidentitychangenotify-Schnittstelle (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215931"
---
# <a name="iidentitychangenotify-interface"></a><span data-ttu-id="3f389-104">Iidentitychangenotify-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3f389-104">IIdentityChangeNotify interface</span></span>

<span data-ttu-id="3f389-105">\[Die **iidentitychangenotify** -Schnittstelle ist für die Verwendung in Windows 2000 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f389-105">\[The **IIdentityChangeNotify** interface is available for use in Windows 2000.</span></span> <span data-ttu-id="3f389-106">In Windows XP wurde diese Funktion durch [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md)abgelöst und kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="3f389-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="3f389-107">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3f389-107">Deprecated.</span></span> <span data-ttu-id="3f389-108">Ermöglicht das Benachrichtigen von Änderungen an Benutzer Identitäten im System sowie Benutzer Anforderungen zum Wechseln der aktuellen Benutzeridentität.</span><span class="sxs-lookup"><span data-stu-id="3f389-108">Provides notification of modifications to user identities on the system, as well as user requests to switch the current user identity.</span></span>

## <a name="members"></a><span data-ttu-id="3f389-109">Member</span><span class="sxs-lookup"><span data-stu-id="3f389-109">Members</span></span>

<span data-ttu-id="3f389-110">Die **iidentitychangenotify** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3f389-110">The **IIdentityChangeNotify** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f389-111">**Iidentitychangenotify** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3f389-111">**IIdentityChangeNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="3f389-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="3f389-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f389-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="3f389-113">Methods</span></span>

<span data-ttu-id="3f389-114">Die **iidentitychangenotifisierungsschnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3f389-114">The **IIdentityChangeNotify** interface has these methods.</span></span>



| <span data-ttu-id="3f389-115">Methode</span><span class="sxs-lookup"><span data-stu-id="3f389-115">Method</span></span>                                                                                 | <span data-ttu-id="3f389-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f389-116">Description</span></span>                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f389-117">**Identityinformationchanged**</span><span class="sxs-lookup"><span data-stu-id="3f389-117">**IdentityInformationChanged**</span></span>](iidentitychangenotify-identityinformationchanged.md) | <span data-ttu-id="3f389-118">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3f389-118">Deprecated.</span></span> <span data-ttu-id="3f389-119">Wird aufgerufen, wenn sich die Informationen zu einer Benutzeridentität geändert haben oder wenn eine Benutzeridentität hinzugefügt oder gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="3f389-119">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span><br/>  |
| [<span data-ttu-id="3f389-120">**Queryswitchidentities**</span><span class="sxs-lookup"><span data-stu-id="3f389-120">**QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)           | <span data-ttu-id="3f389-121">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3f389-121">Deprecated.</span></span> <span data-ttu-id="3f389-122">Wird aufgerufen, wenn der aktuelle Benutzer angefordert hat, dass die Benutzeridentität gewechselt wird, jedoch bevor der Switch auftritt.</span><span class="sxs-lookup"><span data-stu-id="3f389-122">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span><br/> |
| [<span data-ttu-id="3f389-123">**Switchidentities**</span><span class="sxs-lookup"><span data-stu-id="3f389-123">**SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)                     | <span data-ttu-id="3f389-124">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3f389-124">Deprecated.</span></span> <span data-ttu-id="3f389-125">Wird aufgerufen, wenn Benutzer Identitäten gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="3f389-125">Called when user identities are switched.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="3f389-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f389-126">Remarks</span></span>

<span data-ttu-id="3f389-127">Um Benachrichtigungen zu implementieren, muss eine abgeleitete Schnittstelle eine Verbindung mit dem [**iuseridentitymanager**](iuseridentitymanager.md) herstellen, indem [**IConnectionPoint:: Rat**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) aufgerufen und ein Zeiger an die-Schnittstelle übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f389-127">To implement notifications, a derived interface must connect to the [**IUserIdentityManager**](iuseridentitymanager.md) by calling [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) and by passing a pointer to the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f389-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3f389-128">Requirements</span></span>



| <span data-ttu-id="3f389-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f389-129">Requirement</span></span> | <span data-ttu-id="3f389-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3f389-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f389-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f389-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3f389-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f389-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3f389-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f389-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3f389-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f389-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3f389-135">Header</span><span class="sxs-lookup"><span data-stu-id="3f389-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f389-136"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f389-136"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f389-137">IDL</span><span class="sxs-lookup"><span data-stu-id="3f389-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f389-138"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f389-138"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="3f389-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3f389-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f389-140"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f389-140"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3f389-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f389-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f389-142">**Iuseridentitymanager**</span><span class="sxs-lookup"><span data-stu-id="3f389-142">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="3f389-143">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="3f389-143">**IConnectionPoint**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
