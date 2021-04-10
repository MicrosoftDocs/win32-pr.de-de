---
description: Gibt die anfängliche Ebene des Codierungs Puffers in Bits an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Avenccommonbufferinlevel-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125252"
---
# <a name="avenccommonbufferinlevel-property"></a><span data-ttu-id="9324d-104">Avenccommonbufferinlevel (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9324d-104">AVEncCommonBufferInLevel property</span></span>

<span data-ttu-id="9324d-105">Gibt die anfängliche Ebene des Codierungs Puffers in Bits an.</span><span class="sxs-lookup"><span data-stu-id="9324d-105">Specifies the initial level of the encoding buffer, in bits.</span></span> <span data-ttu-id="9324d-106">Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="9324d-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="9324d-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9324d-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9324d-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9324d-108">Data type</span></span>

<span data-ttu-id="9324d-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="9324d-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9324d-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="9324d-110">Property GUID</span></span>

<span data-ttu-id="9324d-111">**Codecapi \_ avenccommonbufferinlevel**</span><span class="sxs-lookup"><span data-stu-id="9324d-111">**CODECAPI\_AVEncCommonBufferInLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="9324d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9324d-112">Property value</span></span>

<span data-ttu-id="9324d-113">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="9324d-113">This property has a linear range of values.</span></span> <span data-ttu-id="9324d-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="9324d-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="9324d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9324d-115">Remarks</span></span>

<span data-ttu-id="9324d-116">Bei MPEG-Videos definiert diese Eigenschaft die anfängliche VBV-Auslastung (Video Buffer Verifier).</span><span class="sxs-lookup"><span data-stu-id="9324d-116">For MPEG video, this property defines the initial video buffer verifier (VBV) fullness.</span></span> <span data-ttu-id="9324d-117">Die Verkettung von Streams während der Codierung wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9324d-117">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="9324d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9324d-118">Requirements</span></span>



| <span data-ttu-id="9324d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9324d-119">Requirement</span></span> | <span data-ttu-id="9324d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9324d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9324d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9324d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9324d-122">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9324d-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9324d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9324d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9324d-124">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9324d-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9324d-125">Header</span><span class="sxs-lookup"><span data-stu-id="9324d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9324d-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9324d-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9324d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9324d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9324d-128">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="9324d-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9324d-129">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9324d-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




