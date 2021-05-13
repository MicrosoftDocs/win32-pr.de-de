---
description: Legt einen Wert fest, der steuert, wie die Benutzersicherheits-ID (SID) in Benutzernamen aufgelöst wird, oder ruft diesen ab.
title: DiskQuotaControl.UserNameResolution-Eigenschaft
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
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841461"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="2e370-103">DiskQuotaControl.UserNameResolution-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2e370-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="2e370-104">Legt einen Wert fest oder ruft einen Wert ab, der steuert, wie Benutzersicherheits-IDs (SID) in Benutzernamen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2e370-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="2e370-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2e370-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e370-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e370-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="2e370-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2e370-107">Property value</span></span>

<span data-ttu-id="2e370-108">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2e370-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="2e370-109">Auflösungstyp</span><span class="sxs-lookup"><span data-stu-id="2e370-109">Resolution Type</span></span> | <span data-ttu-id="2e370-110">Wert</span><span class="sxs-lookup"><span data-stu-id="2e370-110">Value</span></span> | <span data-ttu-id="2e370-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e370-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e370-112">dqResolveNone</span><span class="sxs-lookup"><span data-stu-id="2e370-112">dqResolveNone</span></span>   | <span data-ttu-id="2e370-113">0</span><span class="sxs-lookup"><span data-stu-id="2e370-113">0</span></span>     | <span data-ttu-id="2e370-114">Lösen Sie keine Benutzernameninformationen auf.</span><span class="sxs-lookup"><span data-stu-id="2e370-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="2e370-115">dqResolveSync</span><span class="sxs-lookup"><span data-stu-id="2e370-115">dqResolveSync</span></span>   | <span data-ttu-id="2e370-116">1</span><span class="sxs-lookup"><span data-stu-id="2e370-116">1</span></span>     | <span data-ttu-id="2e370-117">Warten Sie, während Die Namensinformationen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2e370-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="2e370-118">dqResolveAsync</span><span class="sxs-lookup"><span data-stu-id="2e370-118">dqResolveAsync</span></span>  | <span data-ttu-id="2e370-119">2</span><span class="sxs-lookup"><span data-stu-id="2e370-119">2</span></span>     | <span data-ttu-id="2e370-120">Warten Sie nicht, während Sie Namensinformationen auflösen.</span><span class="sxs-lookup"><span data-stu-id="2e370-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="2e370-121">Das [**OnUserNameChanged-Ereignis**](diskquotacontrol-onusernamechanged.md) wird ausgelöst, wenn der Name aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="2e370-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2e370-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e370-122">Remarks</span></span>

<span data-ttu-id="2e370-123">Diese Eigenschaft wirkt sich auf die Enumeration von [**DIDiskQuotaUser-Objekten**](didiskquotauser-object.md) sowie auf die [**AddUser-**](diskquotacontrol-adduser.md) und [**FindUser-Methoden**](diskquotacontrol-finduser.md) aus.</span><span class="sxs-lookup"><span data-stu-id="2e370-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e370-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e370-124">Requirements</span></span>



| <span data-ttu-id="2e370-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e370-125">Requirement</span></span> | <span data-ttu-id="2e370-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2e370-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e370-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e370-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e370-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e370-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e370-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e370-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e370-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e370-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2e370-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2e370-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e370-132"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2e370-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e370-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e370-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e370-134">**DiskQuotaControl-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2e370-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




