---
title: CQPM_INITIALIZE Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, wenn die Seite einem Formular hinzugefügt wird.
ms.assetid: 29cb39d5-9bc4-472e-8a2f-dc6cd505144a
ms.tgt_platform: multiple
keywords:
- CQPM_INITIALIZE Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_INITIALIZE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e95c7087a9cd2d40387c8d7dd07aa93c8f697fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040552"
---
# <a name="cqpm_initialize-message"></a><span data-ttu-id="aea58-104">Cqpm- \_ Initialisierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="aea58-104">CQPM\_INITIALIZE message</span></span>

<span data-ttu-id="aea58-105">Die **cqpm- \_ Initialisierungs** Meldung wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular-Erweiterungs Seite gesendet, wenn die Seite einem Formular hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="aea58-105">The **CQPM\_INITIALIZE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is added to a form.</span></span>

## <a name="parameters"></a><span data-ttu-id="aea58-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aea58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aea58-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aea58-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aea58-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aea58-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="aea58-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aea58-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aea58-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aea58-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aea58-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aea58-111">Return value</span></span>

<span data-ttu-id="aea58-112">Der Rückgabewert für diese Nachricht wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="aea58-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea58-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aea58-113">Requirements</span></span>



| <span data-ttu-id="aea58-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aea58-114">Requirement</span></span> | <span data-ttu-id="aea58-115">Wert</span><span class="sxs-lookup"><span data-stu-id="aea58-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aea58-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aea58-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aea58-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aea58-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="aea58-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aea58-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aea58-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aea58-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="aea58-120">Header</span><span class="sxs-lookup"><span data-stu-id="aea58-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aea58-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="aea58-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea58-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aea58-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea58-123">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="aea58-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





