---
title: CQPM_RELEASE Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, wenn die Seite entladen wird.
ms.assetid: b935ae8d-a07f-4f0d-b379-5512e96a25a5
ms.tgt_platform: multiple
keywords:
- CQPM_RELEASE Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_RELEASE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4957f02b57f499d80f7802b4fe9bd2639485b8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040550"
---
# <a name="cqpm_release-message"></a><span data-ttu-id="6e416-104">Cqpm- \_ releasenachricht</span><span class="sxs-lookup"><span data-stu-id="6e416-104">CQPM\_RELEASE message</span></span>

<span data-ttu-id="6e416-105">Die **cqpm- \_ releasenachricht** wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular-Erweiterungs Seite gesendet, wenn die Seite gerade entladen wird.</span><span class="sxs-lookup"><span data-stu-id="6e416-105">The **CQPM\_RELEASE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is about to be unloaded.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e416-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e416-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e416-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e416-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e416-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e416-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e416-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e416-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e416-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e416-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e416-111">Return value</span></span>

<span data-ttu-id="6e416-112">Der Rückgabewert für diese Nachricht wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6e416-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e416-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e416-113">Requirements</span></span>



| <span data-ttu-id="6e416-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e416-114">Requirement</span></span> | <span data-ttu-id="6e416-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6e416-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e416-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e416-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e416-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e416-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="6e416-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e416-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e416-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e416-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="6e416-120">Header</span><span class="sxs-lookup"><span data-stu-id="6e416-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e416-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e416-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e416-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e416-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e416-123">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="6e416-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





