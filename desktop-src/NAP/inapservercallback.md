---
title: Inapservercallback-Schnittstelle (napsystemhealthvalidator. h)
description: SHVs verwenden, um den Abschluss einer asynchronen Anforderung zu signalisieren.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- Inapservercallback-Schnittstelle NAP
- Inapservercallback-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475267"
---
# <a name="inapservercallback-interface"></a><span data-ttu-id="f0712-105">Inapservercallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f0712-105">INapServerCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="f0712-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0712-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f0712-107">Der **inapservercallback** stellt eine Methode bereit, die SHVs verwendet, um den Abschluss einer asynchronen Anforderung zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="f0712-107">The **INapServerCallback** provides a method that SHVs use to signal asynchronous request completion.</span></span>

## <a name="members"></a><span data-ttu-id="f0712-108">Member</span><span class="sxs-lookup"><span data-stu-id="f0712-108">Members</span></span>

<span data-ttu-id="f0712-109">Die **inapservercallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f0712-109">The **INapServerCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f0712-110">**Inapservercallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f0712-110">**INapServerCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f0712-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f0712-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f0712-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f0712-112">Methods</span></span>

<span data-ttu-id="f0712-113">Die **inapservercallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f0712-113">The **INapServerCallback** interface has these methods.</span></span>



| <span data-ttu-id="f0712-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f0712-114">Method</span></span>                                                                         | <span data-ttu-id="f0712-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0712-115">Description</span></span>                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="f0712-116">**Inapservercallback:: OnComplete**</span><span class="sxs-lookup"><span data-stu-id="f0712-116">**INapServerCallback::OnComplete**</span></span>](inapservercallback-oncomplete-method.md) | <span data-ttu-id="f0712-117">Wird von SHVs verwendet, um den Abschluss einer asynchronen Anforderung zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="f0712-117">Used by SHVs to signal asynchronous request completion.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f0712-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0712-118">Requirements</span></span>



| <span data-ttu-id="f0712-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0712-119">Requirement</span></span> | <span data-ttu-id="f0712-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f0712-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0712-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0712-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0712-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0712-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="f0712-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0712-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0712-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0712-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0712-125">Header</span><span class="sxs-lookup"><span data-stu-id="f0712-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0712-126"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0712-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0712-127">IDL</span><span class="sxs-lookup"><span data-stu-id="f0712-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0712-128"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0712-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="f0712-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f0712-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0712-130"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0712-130"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="f0712-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0712-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0712-132">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f0712-132">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f0712-133">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="f0712-133">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

