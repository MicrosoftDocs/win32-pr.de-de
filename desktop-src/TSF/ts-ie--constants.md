---
title: TS_IE_ Konstanten (textstor. h)
description: Die TS- \_ IE \_ \-Konstanten beschreiben, wie Text eingefügt wird, der eingebettete Objekte enthalten kann, die von Text Diensten verwendet werden.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103282"
---
# <a name="ts_ie_-constants"></a><span data-ttu-id="aba22-103">TS- \_ IE- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="aba22-103">TS\_IE\_\* Constants</span></span>

<span data-ttu-id="aba22-104">Die TS- \_ IE- \_ \* Konstanten beschreiben, wie Text eingefügt wird, der eingebettete Objekte enthalten kann, die von Text Diensten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aba22-104">The TS\_IE\_\* constants describe how to insert text that can contain embedded objects used by text services.</span></span>



| <span data-ttu-id="aba22-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="aba22-105">Constant/value</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="aba22-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aba22-106">Description</span></span>                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <span data-ttu-id="aba22-107"><dt>**TS \_ IE- \_ Korrektur**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="aba22-107"><dt>**TS\_IE\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>    | <span data-ttu-id="aba22-108">Bei dem Text handelt es sich um eine Transformation (Korrektur) vorhandener Inhalte, und alle speziellen Text Markup Informationen (Metadaten) werden aufbewahrt, wie z. b. WAV-Datei Daten oder eine Sprach-ID.</span><span class="sxs-lookup"><span data-stu-id="aba22-108">The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <span data-ttu-id="aba22-109"><dt>**TS \_ IE- \_ Komposition**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="aba22-109"><dt>**TS\_IE\_COMPOSITION**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="aba22-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aba22-110">Not used.</span></span><br/>                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="aba22-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aba22-111">Remarks</span></span>

<span data-ttu-id="aba22-112">Diese Konstanten werden im *dwFlags* -Parameter von [ITextStoreACP:: insertembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) und [itextstoreanchor:: insertemeingebettet](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)verwendet.</span><span class="sxs-lookup"><span data-stu-id="aba22-112">These constants are used in the *dwFlags* parameter of [ITextStoreACP::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) and [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span></span>

## <a name="requirements"></a><span data-ttu-id="aba22-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aba22-113">Requirements</span></span>



| <span data-ttu-id="aba22-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aba22-114">Requirement</span></span> | <span data-ttu-id="aba22-115">Wert</span><span class="sxs-lookup"><span data-stu-id="aba22-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aba22-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aba22-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aba22-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aba22-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aba22-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aba22-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aba22-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aba22-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aba22-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="aba22-120">Redistributable</span></span><br/>          | <span data-ttu-id="aba22-121">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aba22-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="aba22-122">Header</span><span class="sxs-lookup"><span data-stu-id="aba22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aba22-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="aba22-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="aba22-124">IDL</span><span class="sxs-lookup"><span data-stu-id="aba22-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aba22-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aba22-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba22-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aba22-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba22-127">ITextStoreACP:: insertemeingebettet</span><span class="sxs-lookup"><span data-stu-id="aba22-127">ITextStoreACP::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[<span data-ttu-id="aba22-128">Itextstoreanchor:: insertembedded</span><span class="sxs-lookup"><span data-stu-id="aba22-128">ITextStoreAnchor::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





