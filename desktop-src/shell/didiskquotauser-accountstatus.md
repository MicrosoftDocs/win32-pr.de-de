---
description: Ruft den Status des Benutzerkontos ab.
title: DIDiskQuotaUser.AccountStatus-Eigenschaft
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
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841651"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="f9622-103">DIDiskQuotaUser.AccountStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f9622-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="f9622-104">Ruft den Status des Benutzerkontos ab.</span><span class="sxs-lookup"><span data-stu-id="f9622-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="f9622-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f9622-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9622-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9622-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="f9622-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f9622-107">Property value</span></span>

<span data-ttu-id="f9622-108">Diese Eigenschaft kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="f9622-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="f9622-109">Status</span><span class="sxs-lookup"><span data-stu-id="f9622-109">Status</span></span>            | <span data-ttu-id="f9622-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f9622-110">Value</span></span> | <span data-ttu-id="f9622-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9622-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="f9622-112">dqAcctResolved</span><span class="sxs-lookup"><span data-stu-id="f9622-112">dqAcctResolved</span></span>    | <span data-ttu-id="f9622-113">0</span><span class="sxs-lookup"><span data-stu-id="f9622-113">0</span></span>     | <span data-ttu-id="f9622-114">Kontoinformationen werden aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f9622-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="f9622-115">dqAcctUnavailable</span><span class="sxs-lookup"><span data-stu-id="f9622-115">dqAcctUnavailable</span></span> | <span data-ttu-id="f9622-116">1</span><span class="sxs-lookup"><span data-stu-id="f9622-116">1</span></span>     | <span data-ttu-id="f9622-117">Kontoinformationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9622-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="f9622-118">dqAcctDeleted</span><span class="sxs-lookup"><span data-stu-id="f9622-118">dqAcctDeleted</span></span>     | <span data-ttu-id="f9622-119">2</span><span class="sxs-lookup"><span data-stu-id="f9622-119">2</span></span>     | <span data-ttu-id="f9622-120">Das Konto wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f9622-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="f9622-121">dqAcctInvalid</span><span class="sxs-lookup"><span data-stu-id="f9622-121">dqAcctInvalid</span></span>     | <span data-ttu-id="f9622-122">3</span><span class="sxs-lookup"><span data-stu-id="f9622-122">3</span></span>     | <span data-ttu-id="f9622-123">Das Konto ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f9622-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="f9622-124">dqAcctUnknown</span><span class="sxs-lookup"><span data-stu-id="f9622-124">dqAcctUnknown</span></span>     | <span data-ttu-id="f9622-125">4</span><span class="sxs-lookup"><span data-stu-id="f9622-125">4</span></span>     | <span data-ttu-id="f9622-126">Das Konto wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f9622-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="f9622-127">dqAcctUnresolved</span><span class="sxs-lookup"><span data-stu-id="f9622-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="f9622-128">5</span><span class="sxs-lookup"><span data-stu-id="f9622-128">5</span></span>     | <span data-ttu-id="f9622-129">Kontoinformationen sind nicht aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f9622-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="f9622-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9622-130">Requirements</span></span>



| <span data-ttu-id="f9622-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9622-131">Requirement</span></span> | <span data-ttu-id="f9622-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f9622-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9622-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9622-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f9622-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9622-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9622-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9622-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f9622-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9622-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f9622-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f9622-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9622-138"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="f9622-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9622-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9622-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9622-140">**DIDiskQuotaUser-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f9622-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




