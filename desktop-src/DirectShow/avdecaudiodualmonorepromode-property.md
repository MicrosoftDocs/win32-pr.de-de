---
description: Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Avdecaudiodualmonorepromode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747081"
---
# <a name="avdecaudiodualmonorepromode-property"></a><span data-ttu-id="76820-103">Avdecaudiodualmonorepromode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="76820-103">AVDecAudioDualMonoReproMode property</span></span>

<span data-ttu-id="76820-104">Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt.</span><span class="sxs-lookup"><span data-stu-id="76820-104">Specifies how the decoder reproduces dual mono audio.</span></span>

<span data-ttu-id="76820-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="76820-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="76820-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="76820-106">Data type</span></span>

<span data-ttu-id="76820-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="76820-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="76820-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="76820-108">Property GUID</span></span>

<span data-ttu-id="76820-109">**Codecapi \_ avdecaudiodualmonorepromode**</span><span class="sxs-lookup"><span data-stu-id="76820-109">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="76820-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="76820-110">Property value</span></span>

<span data-ttu-id="76820-111">Der Wert dieser Eigenschaft ist ein Member der [**eavdecaudiodualmonorepromode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="76820-111">The value of this property is a member of the [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="76820-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76820-112">Remarks</span></span>

<span data-ttu-id="76820-113">Diese Eigenschaften sind nur anwendbar, wenn der Eingabe Bitstream des Decoders Dual Mono-Audiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="76820-113">This properties applies only when the decoder's input bit stream contains dual mono audio.</span></span> <span data-ttu-id="76820-114">Um diese Bedingung zu testen, müssen Sie den Wert der [avdecaudiodualmono](avdecaudiodualmono-property.md) -Eigenschaft erhalten.</span><span class="sxs-lookup"><span data-stu-id="76820-114">To test this condition, get the value of the [AVDecAudioDualMono](avdecaudiodualmono-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="76820-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76820-115">Requirements</span></span>



| <span data-ttu-id="76820-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76820-116">Requirement</span></span> | <span data-ttu-id="76820-117">Wert</span><span class="sxs-lookup"><span data-stu-id="76820-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76820-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76820-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76820-119">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="76820-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="76820-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76820-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76820-121">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="76820-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="76820-122">Header</span><span class="sxs-lookup"><span data-stu-id="76820-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76820-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="76820-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76820-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76820-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76820-125">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="76820-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="76820-126">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="76820-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




