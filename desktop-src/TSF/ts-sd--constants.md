---
title: TS_SD_ Konstanten (textstor. h)
description: Die TS \_ SD \_ \-Konstanten beschreiben dynamische Dokument Zustände, die von einer Anwendung zur Laufzeit verwendet werden.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337918"
---
# <a name="ts_sd_-constants"></a><span data-ttu-id="cccc2-103">TS \_ SD- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="cccc2-103">TS\_SD\_\* Constants</span></span>

<span data-ttu-id="cccc2-104">Die TS \_ SD- \_ \* Konstanten beschreiben dynamische Dokument Zustände, die von einer Anwendung zur Laufzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cccc2-104">The TS\_SD\_\* constants describe dynamic document states used by an application at runtime.</span></span>



| <span data-ttu-id="cccc2-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="cccc2-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="cccc2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cccc2-106">Description</span></span>                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <span data-ttu-id="cccc2-107"><dt>**TS \_ SD \_**</dt> schreibgeschützt <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="cccc2-107"><dt>**TS\_SD\_READONLY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="cccc2-108">Das Dokument ist schreibgeschützt und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cccc2-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <span data-ttu-id="cccc2-109"><dt>**TS \_ SD- \_ Lade**</dt> Vorgänge <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="cccc2-109"><dt>**TS\_SD\_LOADING**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                 | <span data-ttu-id="cccc2-110">Das Dokument wird geladen und ist möglicherweise unvollständig.</span><span class="sxs-lookup"><span data-stu-id="cccc2-110">The document is loading and might be incomplete.</span></span><br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <span data-ttu-id="cccc2-111"><dt>**TS \_ SD \_ maskall**</dt> <dt>(TS \_ SD Schreib geschützter \_ \| TS \_ SD- \_ Ladevorgang)</dt></span><span class="sxs-lookup"><span data-stu-id="cccc2-111"><dt>**TS\_SD\_MASKALL**</dt> <dt>( TS\_SD\_READONLY \| TS\_SD\_LOADING )</dt></span></span> </dl> | <span data-ttu-id="cccc2-112">Das Dokument ist schreibgeschützt und wird geladen.</span><span class="sxs-lookup"><span data-stu-id="cccc2-112">The document is both read-only and loading.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="cccc2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cccc2-113">Remarks</span></span>

<span data-ttu-id="cccc2-114">Der **dwdynamicflags** -Member der [TS- \_ Status](/windows/desktop/api/Textstor/ns-textstor-ts_status) Struktur verwendet diese Konstanten.</span><span class="sxs-lookup"><span data-stu-id="cccc2-114">The **dwDynamicFlags** member of the [TS\_STATUS](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="cccc2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cccc2-115">Requirements</span></span>



| <span data-ttu-id="cccc2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cccc2-116">Requirement</span></span> | <span data-ttu-id="cccc2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cccc2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cccc2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cccc2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cccc2-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cccc2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cccc2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cccc2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cccc2-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cccc2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cccc2-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cccc2-122">Redistributable</span></span><br/>          | <span data-ttu-id="cccc2-123">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cccc2-123">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="cccc2-124">Header</span><span class="sxs-lookup"><span data-stu-id="cccc2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cccc2-125"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="cccc2-125"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="cccc2-126">IDL</span><span class="sxs-lookup"><span data-stu-id="cccc2-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cccc2-127"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cccc2-127"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cccc2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cccc2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cccc2-129">TS- \_ Status</span><span class="sxs-lookup"><span data-stu-id="cccc2-129">TS\_STATUS</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[<span data-ttu-id="cccc2-130">TF \_ SD- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="cccc2-130">TF\_SD\_\* Constants</span></span>](tf-sd--constants.md)
</dt> </dl>

 

 





