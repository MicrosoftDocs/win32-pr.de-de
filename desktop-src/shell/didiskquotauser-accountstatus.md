---
description: Ruft den Status des Benutzerkontos ab.
title: Didiskquotauser. accountStatus (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977257"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="3b8d4-103">Didiskquotauser. accountStatus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3b8d4-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="3b8d4-104">Ruft den Status des Benutzerkontos ab.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="3b8d4-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8d4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b8d4-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="3b8d4-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3b8d4-107">Property value</span></span>

<span data-ttu-id="3b8d4-108">Diese Eigenschaft kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="3b8d4-109">Status</span><span class="sxs-lookup"><span data-stu-id="3b8d4-109">Status</span></span>            | <span data-ttu-id="3b8d4-110">Wert</span><span class="sxs-lookup"><span data-stu-id="3b8d4-110">Value</span></span> | <span data-ttu-id="3b8d4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b8d4-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="3b8d4-112">dqacctregelöst</span><span class="sxs-lookup"><span data-stu-id="3b8d4-112">dqAcctResolved</span></span>    | <span data-ttu-id="3b8d4-113">0</span><span class="sxs-lookup"><span data-stu-id="3b8d4-113">0</span></span>     | <span data-ttu-id="3b8d4-114">Die Kontoinformationen wurden aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="3b8d4-115">dqacctunavailable</span><span class="sxs-lookup"><span data-stu-id="3b8d4-115">dqAcctUnavailable</span></span> | <span data-ttu-id="3b8d4-116">1</span><span class="sxs-lookup"><span data-stu-id="3b8d4-116">1</span></span>     | <span data-ttu-id="3b8d4-117">Kontoinformationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="3b8d4-118">dqacctdeleted</span><span class="sxs-lookup"><span data-stu-id="3b8d4-118">dqAcctDeleted</span></span>     | <span data-ttu-id="3b8d4-119">2</span><span class="sxs-lookup"><span data-stu-id="3b8d4-119">2</span></span>     | <span data-ttu-id="3b8d4-120">Das Konto wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="3b8d4-121">dqacctinvalid</span><span class="sxs-lookup"><span data-stu-id="3b8d4-121">dqAcctInvalid</span></span>     | <span data-ttu-id="3b8d4-122">3</span><span class="sxs-lookup"><span data-stu-id="3b8d4-122">3</span></span>     | <span data-ttu-id="3b8d4-123">Das Konto ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="3b8d4-124">dqacctunknown</span><span class="sxs-lookup"><span data-stu-id="3b8d4-124">dqAcctUnknown</span></span>     | <span data-ttu-id="3b8d4-125">4</span><span class="sxs-lookup"><span data-stu-id="3b8d4-125">4</span></span>     | <span data-ttu-id="3b8d4-126">Das Konto wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="3b8d4-127">dqacctunaufgelöst</span><span class="sxs-lookup"><span data-stu-id="3b8d4-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="3b8d4-128">5</span><span class="sxs-lookup"><span data-stu-id="3b8d4-128">5</span></span>     | <span data-ttu-id="3b8d4-129">Die Kontoinformationen sind nicht aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="3b8d4-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="3b8d4-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3b8d4-130">Requirements</span></span>



| <span data-ttu-id="3b8d4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b8d4-131">Requirement</span></span> | <span data-ttu-id="3b8d4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3b8d4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8d4-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b8d4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8d4-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b8d4-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b8d4-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b8d4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8d4-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b8d4-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3b8d4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3b8d4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b8d4-138"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3b8d4-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8d4-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3b8d4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8d4-140">**Didiskquotauser-Objekt**</span><span class="sxs-lookup"><span data-stu-id="3b8d4-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




