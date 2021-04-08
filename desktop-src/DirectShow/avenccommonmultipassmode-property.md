---
description: Gibt die Anzahl von Codierungs Durchläufen an, die der Encoder unterstützt.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Avenccommonmultipassmode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860442"
---
# <a name="avenccommonmultipassmode-property"></a><span data-ttu-id="b7493-103">Avenccommonmultipassmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b7493-103">AVEncCommonMultipassMode property</span></span>

<span data-ttu-id="b7493-104">Gibt die Anzahl von Codierungs Durchläufen an, die der Encoder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7493-104">Specifies the number of encoding passes that the encoder supports.</span></span>

<span data-ttu-id="b7493-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b7493-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7493-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b7493-106">Data type</span></span>

<span data-ttu-id="b7493-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b7493-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b7493-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="b7493-108">Property GUID</span></span>

<span data-ttu-id="b7493-109">**Codecapi \_ avenccommonmultipassmode**</span><span class="sxs-lookup"><span data-stu-id="b7493-109">**CODECAPI\_AVEncCommonMultipassMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="b7493-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b7493-110">Property value</span></span>

<span data-ttu-id="b7493-111">Diese Eigenschaft wird als Wertebereich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7493-111">This property is returned as a range of values.</span></span> <span data-ttu-id="b7493-112">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="b7493-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7493-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7493-113">Remarks</span></span>

<span data-ttu-id="b7493-114">Die Decodierungs Latenz ist definiert als die Menge der Daten, die der Decoder Puffern muss.</span><span class="sxs-lookup"><span data-stu-id="b7493-114">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="b7493-115">Wenn Sie diese Eigenschaft beispielsweise auf **Variant \_ true** für einen MPEG-Video Encoder festlegen, werden die Typen von GOP-Strukturen, die der Encoder verwenden kann, eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="b7493-115">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

<span data-ttu-id="b7493-116">Um den aktuellen Codierungs Durchlauf festzulegen, legen Sie die Eigenschaft " [**avenccommonpassstart**](avenccommonpassstart-property.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="b7493-116">To set the current encoding pass, set the [**AVEncCommonPassStart**](avenccommonpassstart-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7493-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7493-117">Requirements</span></span>



| <span data-ttu-id="b7493-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7493-118">Requirement</span></span> | <span data-ttu-id="b7493-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b7493-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7493-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7493-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b7493-121">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b7493-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b7493-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7493-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b7493-123">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b7493-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b7493-124">Header</span><span class="sxs-lookup"><span data-stu-id="b7493-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7493-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7493-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7493-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7493-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7493-127">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="b7493-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b7493-128">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b7493-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




