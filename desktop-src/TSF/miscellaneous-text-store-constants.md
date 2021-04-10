---
title: Sonstige Text Speicher Konstanten (textstor. h)
description: Die verschiedenen Text Speicher Konstanten legen bestimmte Eigenschaften für Text Speicher fest.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105399"
---
# <a name="miscellaneous-text-store-constants"></a><span data-ttu-id="ef7d3-103">Sonstige Text Speicher Konstanten</span><span class="sxs-lookup"><span data-stu-id="ef7d3-103">Miscellaneous Text Store Constants</span></span>

<span data-ttu-id="ef7d3-104">Die verschiedenen Text Speicher Konstanten legen bestimmte Eigenschaften für Text Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-104">The miscellaneous text store constants set certain properties for text stores.</span></span>



| <span data-ttu-id="ef7d3-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="ef7d3-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="ef7d3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef7d3-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <span data-ttu-id="ef7d3-107"><dt>**TS \_ Standard \_ Auswahl**</dt> <dt>((ULONG)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="ef7d3-107"><dt>**TS\_DEFAULT\_SELECTION**</dt> <dt>( ( ULONG )-1 )</dt></span></span> </dl> | <span data-ttu-id="ef7d3-108">Wenn der *ulindex* -Parameter von [ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) auf diesen Wert festgelegt ist, wird die Standardauswahl abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-108">If the *ulIndex* parameter of [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) is set to this value, the default selection is obtained.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <span data-ttu-id="ef7d3-109"><dt>**TS \_ GEA \_ ausgeblendet**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ef7d3-109"><dt>**TS\_GEA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="ef7d3-110">Wenn der *dwFlags* -Parameter von [itextstoreanchor:: getemembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) auf diesen Wert festgelegt ist, kann ein eingebettetes Objekt in ausgeblendetem Text gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-110">If *dwFlags* parameter of [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) is set to this value, an embedded object can be located within hidden text.</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <span data-ttu-id="ef7d3-111"><dt>**TS \_ GTA \_ ausgeblendet**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ef7d3-111"><dt>**TS\_GTA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="ef7d3-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-112">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <span data-ttu-id="ef7d3-113"><dt>**TS \_ St- \_ Korrektur**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ef7d3-113"><dt>**TS\_ST\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="ef7d3-114">Wenn der *dwFlags* -Parameter von [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [itextstoreanchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)oder [ITextStoreACPSink:: ontextchange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) auf diesen Wert festgelegt ist, ist der Text eine Transformation (Korrektur) vorhandener Inhalte, und alle speziellen Text Markup Informationen (Metadaten) werden aufbewahrt, wie z. b</span><span class="sxs-lookup"><span data-stu-id="ef7d3-114">If *dwFlags* parameter of [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext), or [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <span data-ttu-id="ef7d3-115"><dt>**TS \_ TC- \_ Korrektur**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ef7d3-115"><dt>**TS\_TC\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="ef7d3-116">Wenn der *dwFlags* -Parameter von [itextstoreanchorsink:: ontextchange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) auf diesen Wert festgelegt ist, ist der Text eine Transformation (Korrektur) vorhandener Inhalte, und alle speziellen Text Markup Informationen (Metadaten) werden beibehalten, wie z. b. WAV-Datei Daten oder ein sprach Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-116">If *dwFlags* parameter of [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <span data-ttu-id="ef7d3-117"><dt>**TS \_ VCookie- \_ NUL**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="ef7d3-117"><dt>**TS\_VCOOKIE\_NUL**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                    | <span data-ttu-id="ef7d3-118">Wird intern von TSF verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-118">Used internally by TSF.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="ef7d3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef7d3-119">Requirements</span></span>



| <span data-ttu-id="ef7d3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef7d3-120">Requirement</span></span> | <span data-ttu-id="ef7d3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ef7d3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7d3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef7d3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef7d3-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef7d3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ef7d3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef7d3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef7d3-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef7d3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef7d3-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ef7d3-126">Redistributable</span></span><br/>          | <span data-ttu-id="ef7d3-127">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ef7d3-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="ef7d3-128">Header</span><span class="sxs-lookup"><span data-stu-id="ef7d3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef7d3-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef7d3-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef7d3-130">IDL</span><span class="sxs-lookup"><span data-stu-id="ef7d3-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef7d3-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef7d3-131"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef7d3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef7d3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef7d3-133">ITF context:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="ef7d3-133">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="ef7d3-134">ITextStoreACP:: SetText</span><span class="sxs-lookup"><span data-stu-id="ef7d3-134">ITextStoreACP::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[<span data-ttu-id="ef7d3-135">Itextstoreanchor:: SetText</span><span class="sxs-lookup"><span data-stu-id="ef7d3-135">ITextStoreAnchor::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[<span data-ttu-id="ef7d3-136">Itextstoreanchor:: getembedded</span><span class="sxs-lookup"><span data-stu-id="ef7d3-136">ITextStoreAnchor::GetEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[<span data-ttu-id="ef7d3-137">ITextStoreACPSink:: ontextchange</span><span class="sxs-lookup"><span data-stu-id="ef7d3-137">ITextStoreACPSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="ef7d3-138">Itextstoreanchorsink:: ontextchange</span><span class="sxs-lookup"><span data-stu-id="ef7d3-138">ITextStoreAnchorSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="ef7d3-139">Sonstige frameworkkonstanten</span><span class="sxs-lookup"><span data-stu-id="ef7d3-139">Miscellaneous Framework Constants</span></span>](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





