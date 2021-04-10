---
title: TF_SS_ Konstanten (msctf. h)
description: Die TF \_ SS \_ \-Konstanten, die vor der Laufzeit in der TF- \_ Status Struktur definiert werden, beschreiben statische Dokument Zustände.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040712"
---
# <a name="tf_ss_-constants"></a><span data-ttu-id="2db15-103">TF \_ SS- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="2db15-103">TF\_SS\_\* Constants</span></span>

<span data-ttu-id="2db15-104">Die TF \_ SS- \_ \* Konstanten, die vor der Laufzeit in der [**tf- \_ Status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) Struktur definiert werden, beschreiben statische Dokument Zustände.</span><span class="sxs-lookup"><span data-stu-id="2db15-104">The TF\_SS\_\* constants, defined before run time in the [**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure, describe static document states.</span></span>



| <span data-ttu-id="2db15-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="2db15-105">Constant/value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="2db15-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2db15-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <span data-ttu-id="2db15-107"><dt>**Tf \_ SS- \_ disjointsel**</dt> <dt>(TS \_ SS \_ disjointsel)</dt></span><span class="sxs-lookup"><span data-stu-id="2db15-107"><dt>**TF\_SS\_DISJOINTSEL**</dt> <dt>( TS\_SS\_DISJOINTSEL )</dt></span></span> </dl>                                     | <span data-ttu-id="2db15-108">Das Dokument unterstützt mehrere Auswahlmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="2db15-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <span data-ttu-id="2db15-109"><dt>**Tf \_ SS- \_ Regionen**</dt> <dt>(TS \_ SS- \_ Regionen)</dt></span><span class="sxs-lookup"><span data-stu-id="2db15-109"><dt>**TF\_SS\_REGIONS**</dt> <dt>( TS\_SS\_REGIONS )</dt></span></span> </dl>                                                     | <span data-ttu-id="2db15-110">Das Dokument kann mehrere Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2db15-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <span data-ttu-id="2db15-111"><dt>**Tf \_ SS \_ Transitory**</dt> <dt>(TS \_ SS \_ Transitory)</dt></span><span class="sxs-lookup"><span data-stu-id="2db15-111"><dt>**TF\_SS\_TRANSITORY**</dt> <dt>( TS\_SS\_TRANSITORY )</dt></span></span> </dl>                                         | <span data-ttu-id="2db15-112">Es wird erwartet, dass das Dokument einen kurzen Verwendungs Zeitraum hat.</span><span class="sxs-lookup"><span data-stu-id="2db15-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="2db15-113"><dt>**Tf \_ SS \_ tkbautkorrigitenable**</dt> <dt>(TS \_ SS \_ tkbauttable)</dt></span><span class="sxs-lookup"><span data-stu-id="2db15-113"><dt>**TF\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( TS\_SS\_TKBAUTOCORRECTENABLE )</dt></span></span> </dl> | <span data-ttu-id="2db15-114">**Beginnend mit Windows 8:** Das Dokument unterstützt die von der Touchscreen-Tastatur bereitgestellte automatische Korrektur.</span><span class="sxs-lookup"><span data-stu-id="2db15-114">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="2db15-115"><dt>**Tf \_ SS \_ tkbvorhertionenable**</dt> <dt>(TS \_ SS \_ tkbvorhertionenable)</dt></span><span class="sxs-lookup"><span data-stu-id="2db15-115"><dt>**TF\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( TS\_SS\_TKBPREDICTIONENABLE )</dt></span></span> </dl>     | <span data-ttu-id="2db15-116">**Beginnend mit Windows 8:** Das Dokument unterstützt Text Vorschläge von der Touchscreen-Tastatur.</span><span class="sxs-lookup"><span data-stu-id="2db15-116">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2db15-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2db15-117">Remarks</span></span>

<span data-ttu-id="2db15-118">Der **dwstaticflags** -Member der TF- \_ Status Struktur verwendet diese Konstanten.</span><span class="sxs-lookup"><span data-stu-id="2db15-118">The **dwStaticFlags** member of the TF\_STATUS structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="2db15-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2db15-119">Requirements</span></span>



| <span data-ttu-id="2db15-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2db15-120">Requirement</span></span> | <span data-ttu-id="2db15-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2db15-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2db15-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2db15-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2db15-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2db15-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2db15-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2db15-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2db15-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2db15-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2db15-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2db15-126">Redistributable</span></span><br/>          | <span data-ttu-id="2db15-127">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2db15-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="2db15-128">Header</span><span class="sxs-lookup"><span data-stu-id="2db15-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db15-129"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db15-129"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="2db15-130">IDL</span><span class="sxs-lookup"><span data-stu-id="2db15-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2db15-131"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2db15-131"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2db15-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2db15-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="2db15-133">[**TF- \_ Status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2db15-133">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

