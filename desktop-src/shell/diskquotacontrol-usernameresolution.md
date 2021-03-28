---
description: Legt einen Wert fest, der steuert, wie die Benutzer Sicherheits-ID (SID) in Benutzernamen aufgelöst wird, oder ruft ihn ab.
title: Diskquotacontrol. usernameresolution (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: fbe079680191937f022bd45a491fad054e1a9033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977505"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="e0434-103">Diskquotacontrol. usernameresolution (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e0434-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="e0434-104">Legt einen Wert fest, der steuert, wie die Benutzer Sicherheits-ID (SID) in Benutzernamen aufgelöst wird, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="e0434-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="e0434-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e0434-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0434-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0434-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="e0434-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e0434-107">Property value</span></span>

<span data-ttu-id="e0434-108">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e0434-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="e0434-109">Lösungstyp</span><span class="sxs-lookup"><span data-stu-id="e0434-109">Resolution Type</span></span> | <span data-ttu-id="e0434-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e0434-110">Value</span></span> | <span data-ttu-id="e0434-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0434-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0434-112">dqresolvenone</span><span class="sxs-lookup"><span data-stu-id="e0434-112">dqResolveNone</span></span>   | <span data-ttu-id="e0434-113">0</span><span class="sxs-lookup"><span data-stu-id="e0434-113">0</span></span>     | <span data-ttu-id="e0434-114">Informationen zu Benutzernamen nicht auflösen.</span><span class="sxs-lookup"><span data-stu-id="e0434-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="e0434-115">dqresolvesync</span><span class="sxs-lookup"><span data-stu-id="e0434-115">dqResolveSync</span></span>   | <span data-ttu-id="e0434-116">1</span><span class="sxs-lookup"><span data-stu-id="e0434-116">1</span></span>     | <span data-ttu-id="e0434-117">Warten Sie, während Sie die Namen Informationen auflösen.</span><span class="sxs-lookup"><span data-stu-id="e0434-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="e0434-118">dqresolveasync</span><span class="sxs-lookup"><span data-stu-id="e0434-118">dqResolveAsync</span></span>  | <span data-ttu-id="e0434-119">2</span><span class="sxs-lookup"><span data-stu-id="e0434-119">2</span></span>     | <span data-ttu-id="e0434-120">Warten Sie nicht, während Sie die Namen Informationen auflösen.</span><span class="sxs-lookup"><span data-stu-id="e0434-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="e0434-121">Das [**onusernamechanged**](diskquotacontrol-onusernamechanged.md) -Ereignis wird ausgelöst, wenn der Name aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="e0434-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e0434-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0434-122">Remarks</span></span>

<span data-ttu-id="e0434-123">Diese Eigenschaft wirkt sich auf die Enumeration von [**didiskquotauser**](didiskquotauser-object.md) -Objekten sowie die Methoden " [**adduser**](diskquotacontrol-adduser.md) " und " [**FINDUSER**](diskquotacontrol-finduser.md) " aus.</span><span class="sxs-lookup"><span data-stu-id="e0434-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0434-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e0434-124">Requirements</span></span>



| <span data-ttu-id="e0434-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0434-125">Requirement</span></span> | <span data-ttu-id="e0434-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e0434-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0434-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0434-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e0434-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0434-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0434-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0434-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e0434-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0434-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e0434-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e0434-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0434-132"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="e0434-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0434-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0434-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0434-134">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="e0434-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




