---
title: CQPM_HANDLERSPECIFIC Meldung (cmnquery. h)
description: Basiswert, der für Nachrichten verwendet wird, die für den Abfrage Handler privat sind.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- CQPM_HANDLERSPECIFIC Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475585"
---
# <a name="cqpm_handlerspecific-message"></a><span data-ttu-id="d82bf-104">Cqpm- \_ handlerspecific-Meldung</span><span class="sxs-lookup"><span data-stu-id="d82bf-104">CQPM\_HANDLERSPECIFIC message</span></span>

<span data-ttu-id="d82bf-105">Die **cqpm \_ handlerspecific** -Meldung ist der Basiswert, der für Nachrichten verwendet wird, die für den Abfrage Handler privat sind.</span><span class="sxs-lookup"><span data-stu-id="d82bf-105">The **CQPM\_HANDLERSPECIFIC** message is the base value used for messages that are private to the query handler.</span></span> <span data-ttu-id="d82bf-106">Der Abfrage Handler sollte diesen Wert privaten Nachrichten hinzufügen, um sicherzustellen, dass keine Nachrichten Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="d82bf-106">The query handler should add this value to private messages to ensure that message collisions do not occur.</span></span>

## <a name="parameters"></a><span data-ttu-id="d82bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d82bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d82bf-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d82bf-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d82bf-109">Enthält zusätzliche Nachrichten Daten.</span><span class="sxs-lookup"><span data-stu-id="d82bf-109">Contains additional message data.</span></span> <span data-ttu-id="d82bf-110">Der Inhalt dieses Parameters wird vom Abfrage Handler definiert.</span><span class="sxs-lookup"><span data-stu-id="d82bf-110">The content of this parameter is defined by the query handler.</span></span>

</dd> <dt>

<span data-ttu-id="d82bf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d82bf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d82bf-112">Enthält zusätzliche Nachrichten Daten.</span><span class="sxs-lookup"><span data-stu-id="d82bf-112">Contains additional message data.</span></span> <span data-ttu-id="d82bf-113">Der Inhalt dieses Parameters wird vom Abfrage Handler definiert.</span><span class="sxs-lookup"><span data-stu-id="d82bf-113">The content of this parameter is defined by the query handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d82bf-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d82bf-114">Return value</span></span>

<span data-ttu-id="d82bf-115">Die Bedeutung des Rückgabewerts wird durch den Abfrage Handler definiert.</span><span class="sxs-lookup"><span data-stu-id="d82bf-115">The meaning of the return value is defined by the query handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="d82bf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d82bf-116">Requirements</span></span>



| <span data-ttu-id="d82bf-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d82bf-117">Requirement</span></span> | <span data-ttu-id="d82bf-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d82bf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d82bf-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d82bf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d82bf-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d82bf-120">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="d82bf-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d82bf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d82bf-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d82bf-122">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="d82bf-123">Header</span><span class="sxs-lookup"><span data-stu-id="d82bf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d82bf-124"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="d82bf-124"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d82bf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d82bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82bf-126">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="d82bf-126">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





