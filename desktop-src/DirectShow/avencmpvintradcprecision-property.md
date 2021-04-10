---
description: Gibt die Genauigkeit der DC-Koeffizienten in Bits an. Diese Eigenschaft gilt für MPEG-Video Encoder.
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: Avencmpvintradcprecision-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d4bdd3c08f49586eb2663829271ae4166d917e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860338"
---
# <a name="avencmpvintradcprecision-property"></a><span data-ttu-id="852ee-104">Avencmpvintradcprecision (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="852ee-104">AVEncMPVIntraDCPrecision property</span></span>

<span data-ttu-id="852ee-105">Gibt die Genauigkeit der DC-Koeffizienten in Bits an.</span><span class="sxs-lookup"><span data-stu-id="852ee-105">Specifies the precision of the DC coefficients, in bits.</span></span> <span data-ttu-id="852ee-106">Diese Eigenschaft gilt für MPEG-Video Encoder.</span><span class="sxs-lookup"><span data-stu-id="852ee-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="852ee-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="852ee-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="852ee-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="852ee-108">Data type</span></span>

<span data-ttu-id="852ee-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="852ee-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="852ee-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="852ee-110">Property GUID</span></span>

<span data-ttu-id="852ee-111">**Codecapi \_ avencmpvintradcprecision**</span><span class="sxs-lookup"><span data-stu-id="852ee-111">**CODECAPI\_AVEncMPVIntraDCPrecision**</span></span>

## <a name="property-value"></a><span data-ttu-id="852ee-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="852ee-112">Property value</span></span>

<span data-ttu-id="852ee-113">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="852ee-113">This property has a linear range of values.</span></span> <span data-ttu-id="852ee-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="852ee-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="852ee-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="852ee-115">Remarks</span></span>

<span data-ttu-id="852ee-116">Der übliche Bereich für diese Eigenschaft ist 8 bis 11 Bits.</span><span class="sxs-lookup"><span data-stu-id="852ee-116">The usual range for this property is 8 to 11 bits.</span></span> <span data-ttu-id="852ee-117">Wenn der Wert 0 (null) ist, wählt der Encoder die Genauigkeit aus.</span><span class="sxs-lookup"><span data-stu-id="852ee-117">If the value is zero, the encoder selects the precision.</span></span>

## <a name="requirements"></a><span data-ttu-id="852ee-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="852ee-118">Requirements</span></span>



| <span data-ttu-id="852ee-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="852ee-119">Requirement</span></span> | <span data-ttu-id="852ee-120">Wert</span><span class="sxs-lookup"><span data-stu-id="852ee-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="852ee-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="852ee-121">Minimum supported client</span></span><br/> | <span data-ttu-id="852ee-122">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="852ee-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="852ee-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="852ee-123">Minimum supported server</span></span><br/> | <span data-ttu-id="852ee-124">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="852ee-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="852ee-125">Header</span><span class="sxs-lookup"><span data-stu-id="852ee-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="852ee-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="852ee-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="852ee-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="852ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="852ee-128">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="852ee-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="852ee-129">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="852ee-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




