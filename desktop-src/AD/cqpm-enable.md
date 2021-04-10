---
title: CQPM_ENABLE Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, um die Seite zu aktivieren oder zu deaktivieren.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- CQPM_ENABLE Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040247"
---
# <a name="cqpm_enable-message"></a><span data-ttu-id="f845b-104">Cqpm- \_ Nachricht aktivieren</span><span class="sxs-lookup"><span data-stu-id="f845b-104">CQPM\_ENABLE message</span></span>

<span data-ttu-id="f845b-105">Die **cqpm- \_ Aktivierungs** Nachricht wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, um die Seite zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f845b-105">The **CQPM\_ENABLE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to enable or disable the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="f845b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f845b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f845b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f845b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f845b-108">Enthält 0 (null), um die Seite zu deaktivieren oder um die Seite zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f845b-108">Contains zero to disable the page or nonzero to enable the page.</span></span>

</dd> <dt>

<span data-ttu-id="f845b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f845b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f845b-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f845b-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f845b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f845b-111">Return value</span></span>

<span data-ttu-id="f845b-112">Der Rückgabewert für diese Nachricht wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f845b-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f845b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f845b-113">Requirements</span></span>



| <span data-ttu-id="f845b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f845b-114">Requirement</span></span> | <span data-ttu-id="f845b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f845b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f845b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f845b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f845b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f845b-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="f845b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f845b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f845b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f845b-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="f845b-120">Header</span><span class="sxs-lookup"><span data-stu-id="f845b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f845b-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="f845b-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f845b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f845b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f845b-123">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="f845b-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





