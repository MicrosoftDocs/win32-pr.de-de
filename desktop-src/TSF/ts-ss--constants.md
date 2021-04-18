---
title: TS_SS_ Konstanten (textstor. h)
description: Die TS \_ SS \_ \-Konstanten, die vor der Laufzeit in der TS- \_ Status Struktur definiert werden, beschreiben statische Dokument Zustände.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337290"
---
# <a name="ts_ss_-constants"></a><span data-ttu-id="6f231-103">TS- \_ SS- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="6f231-103">TS\_SS\_\* Constants</span></span>

<span data-ttu-id="6f231-104">Die TS- \_ SS- \_ \* Konstanten, die vor der Laufzeit in der [**TS- \_ Status**](/windows/desktop/api/Textstor/ns-textstor-ts_status) Struktur definiert werden, beschreiben statische Dokument Zustände.</span><span class="sxs-lookup"><span data-stu-id="6f231-104">The TS\_SS\_\* constants, defined before run time in the [**TS\_STATUS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure, describe static document states.</span></span>



| <span data-ttu-id="6f231-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="6f231-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="6f231-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f231-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <span data-ttu-id="6f231-107"><dt>**TS \_ SS- \_ disjointsel**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6f231-107"><dt>**TS\_SS\_DISJOINTSEL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                             | <span data-ttu-id="6f231-108">Das Dokument unterstützt mehrere Auswahlmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="6f231-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <span data-ttu-id="6f231-109"><dt>**TS \_ SS- \_ Regionen**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="6f231-109"><dt>**TS\_SS\_REGIONS**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                         | <span data-ttu-id="6f231-110">Das Dokument kann mehrere Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f231-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <span data-ttu-id="6f231-111"><dt>**TS \_ SS \_ Transitory**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="6f231-111"><dt>**TS\_SS\_TRANSITORY**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                | <span data-ttu-id="6f231-112">Es wird erwartet, dass das Dokument einen kurzen Verwendungs Zeitraum hat.</span><span class="sxs-lookup"><span data-stu-id="6f231-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <span data-ttu-id="6f231-113"><dt>**TS \_ SS \_ nohiddentext**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="6f231-113"><dt>**TS\_SS\_NOHIDDENTEXT**</dt> <dt>( 0x8 )</dt></span></span> </dl>                          | <span data-ttu-id="6f231-114">Das Dokument enthält niemals ausgeblendeten Text.</span><span class="sxs-lookup"><span data-stu-id="6f231-114">The document will never contain hidden text.</span></span><br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="6f231-115"><dt>**TS \_ SS \_ tkbautkorrigitenable**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="6f231-115"><dt>**TS\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( 0x10 )</dt></span></span> </dl> | <span data-ttu-id="6f231-116">**Beginnend mit Windows 8:** Das Dokument unterstützt die von der Touchscreen-Tastatur bereitgestellte automatische Korrektur.</span><span class="sxs-lookup"><span data-stu-id="6f231-116">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="6f231-117"><dt>**TS \_ SS \_ tkbvorhertionenable**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="6f231-117"><dt>**TS\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( 0x20 )</dt></span></span> </dl>    | <span data-ttu-id="6f231-118">**Beginnend mit Windows 8:** Das Dokument unterstützt Text Vorschläge von der Touchscreen-Tastatur.</span><span class="sxs-lookup"><span data-stu-id="6f231-118">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6f231-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f231-119">Remarks</span></span>

<span data-ttu-id="6f231-120">Der **dwstaticflags** -Member der **TS- \_ Status** Struktur verwendet diese Konstanten.</span><span class="sxs-lookup"><span data-stu-id="6f231-120">The **dwStaticFlags** member of the **TS\_STATUS** structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f231-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f231-121">Requirements</span></span>



| <span data-ttu-id="6f231-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f231-122">Requirement</span></span> | <span data-ttu-id="6f231-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6f231-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f231-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f231-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f231-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f231-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6f231-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f231-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f231-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f231-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f231-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6f231-128">Redistributable</span></span><br/>          | <span data-ttu-id="6f231-129">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6f231-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="6f231-130">Header</span><span class="sxs-lookup"><span data-stu-id="6f231-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f231-131"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f231-131"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f231-132">IDL</span><span class="sxs-lookup"><span data-stu-id="6f231-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f231-133"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f231-133"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f231-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f231-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f231-135">**TS- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="6f231-135">**TS\_STATUS**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

<span data-ttu-id="6f231-136">[**TF- \_ Status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f231-136">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

