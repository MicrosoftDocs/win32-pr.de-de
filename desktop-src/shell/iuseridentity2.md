---
description: IUserIdentity2 wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: IUserIdentity2-Schnittstelle (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524443"
---
# <a name="iuseridentity2-interface"></a><span data-ttu-id="f658a-104">IUserIdentity2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f658a-104">IUserIdentity2 interface</span></span>

<span data-ttu-id="f658a-105">\[**IUserIdentity2** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f658a-105">\[**IUserIdentity2** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f658a-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="f658a-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="f658a-107">Macht Methoden verfügbar, die die Benennung, das Kennwort und die ordinale Steuerung für eine bestimmte Benutzeridentität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f658a-107">Exposes methods that provide naming, password, and ordinal control for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="f658a-108">Member</span><span class="sxs-lookup"><span data-stu-id="f658a-108">Members</span></span>

<span data-ttu-id="f658a-109">Die **IUserIdentity2** -Schnittstelle erbt von [**iuseridentity**](iuseridentity.md).</span><span class="sxs-lookup"><span data-stu-id="f658a-109">The **IUserIdentity2** interface inherits from [**IUserIdentity**](iuseridentity.md).</span></span> <span data-ttu-id="f658a-110">**IUserIdentity2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f658a-110">**IUserIdentity2** also has these types of members:</span></span>

-   [<span data-ttu-id="f658a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f658a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f658a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f658a-112">Methods</span></span>

<span data-ttu-id="f658a-113">Die **IUserIdentity2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f658a-113">The **IUserIdentity2** interface has these methods.</span></span>



| <span data-ttu-id="f658a-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f658a-114">Method</span></span>                                                  | <span data-ttu-id="f658a-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f658a-115">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="f658a-116">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="f658a-116">**ChangePassword**</span></span>](iuseridentity2-changepassword.md) | <span data-ttu-id="f658a-117">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f658a-117">Deprecated.</span></span> <span data-ttu-id="f658a-118">Legt ein neues Kennwort für die Identität fest.</span><span class="sxs-lookup"><span data-stu-id="f658a-118">Sets a new password for the identity.</span></span><br/>      |
| [<span data-ttu-id="f658a-119">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="f658a-119">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)         | <span data-ttu-id="f658a-120">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f658a-120">Deprecated.</span></span> <span data-ttu-id="f658a-121">Ruft die Ordinalzahl für diese Identität ab.</span><span class="sxs-lookup"><span data-stu-id="f658a-121">Gets the ordinal number for this identity.</span></span><br/> |
| [<span data-ttu-id="f658a-122">**SetName**</span><span class="sxs-lookup"><span data-stu-id="f658a-122">**SetName**</span></span>](iuseridentity2-setname.md)               | <span data-ttu-id="f658a-123">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f658a-123">Deprecated.</span></span> <span data-ttu-id="f658a-124">Legt den anzeigen amen der Identität fest.</span><span class="sxs-lookup"><span data-stu-id="f658a-124">Sets the display name of the identity.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="f658a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f658a-125">Remarks</span></span>

<span data-ttu-id="f658a-126">Diese Schnittstelle stellt auch die Methoden der [**iuseridentity**](iuseridentity.md) -Schnittstelle bereit, von der Sie erbt.</span><span class="sxs-lookup"><span data-stu-id="f658a-126">This interface also provides the methods of the [**IUserIdentity**](iuseridentity.md) interface, from which it inherits.</span></span>

## <a name="requirements"></a><span data-ttu-id="f658a-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f658a-127">Requirements</span></span>



| <span data-ttu-id="f658a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f658a-128">Requirement</span></span> | <span data-ttu-id="f658a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f658a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f658a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f658a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f658a-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f658a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f658a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f658a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f658a-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f658a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f658a-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f658a-134">End of client support</span></span><br/>    | <span data-ttu-id="f658a-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f658a-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="f658a-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f658a-136">End of server support</span></span><br/>    | <span data-ttu-id="f658a-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f658a-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="f658a-138">Header</span><span class="sxs-lookup"><span data-stu-id="f658a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f658a-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="f658a-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="f658a-140">IDL</span><span class="sxs-lookup"><span data-stu-id="f658a-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f658a-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f658a-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="f658a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f658a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f658a-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f658a-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f658a-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f658a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f658a-145">**Iuseridentity**</span><span class="sxs-lookup"><span data-stu-id="f658a-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> </dl>

 

 




