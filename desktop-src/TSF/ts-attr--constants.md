---
title: TS_ATTR_ Konstanten (textstor. h)
description: Die TS \_ attr \_ \-Konstanten werden verwendet, um die Werte von Dokument Attributen abzurufen und zu ändern. Diese Konstanten bilden mögliche Werte von Bitfeld-Flags in ITextStoreACP-und itextstoreanchor-Methoden.
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477997"
---
# <a name="ts_attr_-constants"></a><span data-ttu-id="dba25-104">TS \_ attr- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="dba25-104">TS\_ATTR\_\* Constants</span></span>

<span data-ttu-id="dba25-105">Die TS \_ attr \_ \* -Konstanten werden verwendet, um die Werte von Dokument Attributen abzurufen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="dba25-105">The TS\_ATTR\_\* constants are used to obtain and change the values of document attributes.</span></span> <span data-ttu-id="dba25-106">Diese Konstanten bilden mögliche Werte von Bitfeld-Flags in [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) und [itextstoreanchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="dba25-106">These constants form possible values of bitfield flags in [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>



| <span data-ttu-id="dba25-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="dba25-107">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="dba25-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dba25-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <span data-ttu-id="dba25-109"><dt>**TS \_ Attr \_ \_ rückwärts suchen**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="dba25-109"><dt>**TS\_ATTR\_FIND\_BACKWARDS**</dt> <dt>( 0x1 )</dt></span></span> </dl>        | <span data-ttu-id="dba25-110">Suchen Sie rückwärts von der Start-oder Ankerposition an der Position, an der ein Übergang in einem Dokument Attribut Wert auftritt.</span><span class="sxs-lookup"><span data-stu-id="dba25-110">Search backward from the start character or anchor position for the position where a transition occurs in a document attribute value.</span></span> <span data-ttu-id="dba25-111">Der Standardwert ist Search Forward.</span><span class="sxs-lookup"><span data-stu-id="dba25-111">The default is search forward.</span></span><br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <span data-ttu-id="dba25-112"><dt>**TS \_ Attr- \_ Suche nach \_ gewünschten \_ Offset**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="dba25-112"><dt>**TS\_ATTR\_FIND\_WANT\_OFFSET**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="dba25-113">Gibt die Anzahl der Zeichen zwischen dem Startzeichen oder der Ankerposition (**acpstart** in [ITextStoreACP:: findnextattrtransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) oder **pastart** in [itextstoreanchor:: findnextattrtransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) und der Position an, an der ein Attribut Übergang auftritt.</span><span class="sxs-lookup"><span data-stu-id="dba25-113">Return the number of characters between the start character or anchor position (**acpStart** in [ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) or **paStart** in [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) and the position at which an attribute transition occurs.</span></span><br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <span data-ttu-id="dba25-114"><dt>**TS \_ Attr \_ Find \_ Updatestart**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="dba25-114"><dt>**TS\_ATTR\_FIND\_UPDATESTART**</dt> <dt>( 0x4 )</dt></span></span> </dl>  | <span data-ttu-id="dba25-115">Wird von [itextstoreanchor:: findnextattrtransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) verwendet, um den Eingabe Anker beim nächsten Attribut Übergang (sofern gefunden) zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="dba25-115">Used by [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) to position the input anchor at the next attribute transition, if one is found.</span></span> <span data-ttu-id="dba25-116">Andernfalls wird der Eingabe Anker nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="dba25-116">Otherwise the input anchor is not modified.</span></span><br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <span data-ttu-id="dba25-117"><dt>**TS \_ Attr \_ \_ \_ Suchwert suchen**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="dba25-117"><dt>**TS\_ATTR\_FIND\_WANT\_VALUE**</dt> <dt>( 0x8 )</dt></span></span> </dl>    | <span data-ttu-id="dba25-118">Laden unterstützter Dokument Attributwerte in die [TS \_ attrval](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="dba25-118">Load supported document attribute values into the [TS\_ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) structure.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <span data-ttu-id="dba25-119"><dt>**TS \_ Attr \_ Find \_ will \_ End**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="dba25-119"><dt>**TS\_ATTR\_FIND\_WANT\_END**</dt> <dt>( 0x10 )</dt></span></span> </dl>         | <span data-ttu-id="dba25-120">Wird von [ITextStoreACP:: requestatus trstransitioningatposition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) und [itextstoreanchor:: requestatus trstransitioningatposition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) verwendet, um die Dokument Attributwerte abzurufen, die an der angegebenen Zeichenposition oder Ankerposition enden.</span><span class="sxs-lookup"><span data-stu-id="dba25-120">Used by [ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) and [ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) to obtain the document attribute values that end at the specified character or anchor position.</span></span><br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <span data-ttu-id="dba25-121"><dt>**TS \_ Attr- \_ Suche \_ ausgeblendet**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="dba25-121"><dt>**TS\_ATTR\_FIND\_HIDDEN**</dt> <dt>( 0x20 )</dt></span></span> </dl>                | <span data-ttu-id="dba25-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="dba25-122">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="dba25-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dba25-123">Requirements</span></span>



| <span data-ttu-id="dba25-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dba25-124">Requirement</span></span> | <span data-ttu-id="dba25-125">Wert</span><span class="sxs-lookup"><span data-stu-id="dba25-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dba25-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dba25-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dba25-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dba25-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dba25-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dba25-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dba25-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dba25-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dba25-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="dba25-130">Redistributable</span></span><br/>          | <span data-ttu-id="dba25-131">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dba25-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="dba25-132">Header</span><span class="sxs-lookup"><span data-stu-id="dba25-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="dba25-133"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="dba25-133"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="dba25-134">IDL</span><span class="sxs-lookup"><span data-stu-id="dba25-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dba25-135"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dba25-135"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dba25-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dba25-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba25-137">TS \_ -attrd</span><span class="sxs-lookup"><span data-stu-id="dba25-137">TS\_ATTRID</span></span>](ts-attrid.md)
</dt> <dt>

[<span data-ttu-id="dba25-138">TS- \_ attrval</span><span class="sxs-lookup"><span data-stu-id="dba25-138">TS\_ATTRVAL</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[<span data-ttu-id="dba25-139">ITextStoreACP:: findnextattrtransition</span><span class="sxs-lookup"><span data-stu-id="dba25-139">ITextStoreACP::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="dba25-140">ITextStoreACP:: requestatus-stransitioningatposition</span><span class="sxs-lookup"><span data-stu-id="dba25-140">ITextStoreACP::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="dba25-141">Itextstoreanchor:: findnextattrtransition</span><span class="sxs-lookup"><span data-stu-id="dba25-141">ITextStoreAnchor::FindNextAttrTransition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="dba25-142">Itextstoreanchor:: requestatus-stransitioningatposition</span><span class="sxs-lookup"><span data-stu-id="dba25-142">ITextStoreAnchor::RequestAttrsTransitioningAtPosition</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





