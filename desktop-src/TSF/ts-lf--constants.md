---
title: TS_LF_ Konstanten (textstor. h)
description: Die TS \_ LF \_ \-Konstanten geben den Typ der Dokument Sperre an.
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341352"
---
# <a name="ts_lf_-constants"></a><span data-ttu-id="bc797-103">TS \_ LF- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="bc797-103">TS\_LF\_\* Constants</span></span>

<span data-ttu-id="bc797-104">Die TS- \_ LF- \_ \* Konstanten geben den Typ der Dokument Sperre an.</span><span class="sxs-lookup"><span data-stu-id="bc797-104">The TS\_LF\_\* constants specify the type of document lock.</span></span>



| <span data-ttu-id="bc797-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="bc797-105">Constant/value</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="bc797-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc797-106">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <span data-ttu-id="bc797-107"><dt>**TS \_ LF \_ Synchronisieren**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bc797-107"><dt>**TS\_LF\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                | <span data-ttu-id="bc797-108">Das Dokument hat eine synchrone Sperre, wenn dieses Flag mit anderen Flags kombiniert wird.</span><span class="sxs-lookup"><span data-stu-id="bc797-108">The document has a synchronous-lock if this flag is combined with other flags.</span></span><br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <span data-ttu-id="bc797-109"><dt>**TS \_ LF- \_ Lese**</dt> Vorgang <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="bc797-109"><dt>**TS\_LF\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                | <span data-ttu-id="bc797-110">Das Dokument weist eine schreibgeschützte Sperre auf und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bc797-110">The document has a read-only lock and cannot be modified.</span></span><br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <span data-ttu-id="bc797-111"><dt>**TS \_ LF- \_ Lesevorgang**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="bc797-111"><dt>**TS\_LF\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl> | <span data-ttu-id="bc797-112">Das Dokument hat eine Lese-/Schreibsperre und kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bc797-112">The document has a read/write lock and can be modified.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="bc797-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc797-113">Requirements</span></span>



| <span data-ttu-id="bc797-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc797-114">Requirement</span></span> | <span data-ttu-id="bc797-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bc797-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc797-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc797-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc797-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc797-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bc797-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc797-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc797-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc797-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc797-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="bc797-120">Redistributable</span></span><br/>          | <span data-ttu-id="bc797-121">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc797-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="bc797-122">Header</span><span class="sxs-lookup"><span data-stu-id="bc797-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc797-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc797-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc797-124">IDL</span><span class="sxs-lookup"><span data-stu-id="bc797-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc797-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc797-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc797-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc797-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc797-127">Dokument Sperren</span><span class="sxs-lookup"><span data-stu-id="bc797-127">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="bc797-128">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="bc797-128">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="bc797-129">ITextStoreACPSink:: onlockgewährten</span><span class="sxs-lookup"><span data-stu-id="bc797-129">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="bc797-130">Itextstoreanchor:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="bc797-130">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="bc797-131">Itextstoreanchorsink:: onlockgewährten</span><span class="sxs-lookup"><span data-stu-id="bc797-131">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





