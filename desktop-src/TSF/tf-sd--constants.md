---
title: TF_SD_ Konstanten (msctf. h)
description: Die TF \_ SD \_ \-Konstanten beschreiben den Dokument Status.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103014"
---
# <a name="tf_sd_-constants"></a><span data-ttu-id="fb469-103">TF \_ SD- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="fb469-103">TF\_SD\_\* Constants</span></span>

<span data-ttu-id="fb469-104">Die TF \_ SD- \_ \* Konstanten beschreiben den Dokument Status.</span><span class="sxs-lookup"><span data-stu-id="fb469-104">The TF\_SD\_\* constants describe the document status.</span></span>



| <span data-ttu-id="fb469-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="fb469-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="fb469-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb469-106">Description</span></span>                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <span data-ttu-id="fb469-107"><dt>**Tf \_ SD \_**</dt> schreibgeschützt <dt>(TS \_ SD \_</dt> schreibgeschützt)</span><span class="sxs-lookup"><span data-stu-id="fb469-107"><dt>**TF\_SD\_READONLY**</dt> <dt>( TS\_SD\_READONLY )</dt></span></span> </dl> | <span data-ttu-id="fb469-108">Das Dokument ist schreibgeschützt und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fb469-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <span data-ttu-id="fb469-109"><dt>**Tf \_ SD- \_ Lade**</dt> Vorgänge <dt>(TS \_ SD- \_ Laden)</dt></span><span class="sxs-lookup"><span data-stu-id="fb469-109"><dt>**TF\_SD\_LOADING**</dt> <dt>( TS\_SD\_LOADING )</dt></span></span> </dl>     | <span data-ttu-id="fb469-110">Das Dokument wird geladen und kann unvollständig sein.</span><span class="sxs-lookup"><span data-stu-id="fb469-110">The document is loading and can be incomplete.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="fb469-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb469-111">Remarks</span></span>

<span data-ttu-id="fb469-112">Der **dwdynamicflags** -Member der [tf- \_ Status](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) Struktur verwendet diese Konstanten.</span><span class="sxs-lookup"><span data-stu-id="fb469-112">The **dwDynamicFlags** member of the [TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb469-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb469-113">Requirements</span></span>



| <span data-ttu-id="fb469-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb469-114">Requirement</span></span> | <span data-ttu-id="fb469-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fb469-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb469-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb469-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fb469-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb469-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fb469-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb469-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fb469-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb469-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fb469-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="fb469-120">Redistributable</span></span><br/>          | <span data-ttu-id="fb469-121">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fb469-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="fb469-122">Header</span><span class="sxs-lookup"><span data-stu-id="fb469-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb469-123"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb469-123"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb469-124">IDL</span><span class="sxs-lookup"><span data-stu-id="fb469-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb469-125"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb469-125"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb469-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb469-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb469-127">[TF- \_ Status](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fb469-127">[TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fb469-128">TS \_ SD- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="fb469-128">TS\_SD\_\* Constants</span></span>](ts-sd--constants.md)
</dt> <dt>

[<span data-ttu-id="fb469-129">Itfcontextowner:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="fb469-129">ITfContextOwner::GetStatus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[<span data-ttu-id="fb469-130">ITF contextownerservices:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="fb469-130">ITfContextOwnerServices::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[<span data-ttu-id="fb469-131">ITextStoreACP:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="fb469-131">ITextStoreACP::GetStatus</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[<span data-ttu-id="fb469-132">ITF statussunk:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="fb469-132">ITfStatusSunk::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

