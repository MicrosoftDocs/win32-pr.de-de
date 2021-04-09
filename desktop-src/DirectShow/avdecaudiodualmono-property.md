---
description: Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Avdecaudiodualmono-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 107adb00eb68cbb9ec19331b0c0f3f9db916a306
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860421"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="2fa0b-103">Avdecaudiodualmono (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2fa0b-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="2fa0b-104">Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.</span><span class="sxs-lookup"><span data-stu-id="2fa0b-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="2fa0b-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2fa0b-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="2fa0b-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2fa0b-106">Data type</span></span>

<span data-ttu-id="2fa0b-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2fa0b-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2fa0b-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="2fa0b-108">Property GUID</span></span>

<span data-ttu-id="2fa0b-109">**Codecapi \_ avdecaudiodualmono**</span><span class="sxs-lookup"><span data-stu-id="2fa0b-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="2fa0b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2fa0b-110">Property value</span></span>

<span data-ttu-id="2fa0b-111">Der Wert dieser Eigenschaft ist ein Member der [**eavdecaudiodualmono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="2fa0b-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fa0b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fa0b-112">Remarks</span></span>

<span data-ttu-id="2fa0b-113">Diese Eigenschaft wird nur angewendet, wenn der Eingabe-Bit-Stream des Decoders zwei Kanal-Audiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="2fa0b-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="2fa0b-114">Ein Audiodatenstrom mit zwei Kanälen kann als Stereo oder als dualer Mono codiert werden.</span><span class="sxs-lookup"><span data-stu-id="2fa0b-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="2fa0b-115">Wenn das Audio Dual Mono ist, können Sie die [**avdecaudiodualmonorepromode**](avdecaudiodualmonorepromode-property.md) -Eigenschaft festlegen, um zu konfigurieren, wie der Decoder die Audiodatei wiederherstellt.</span><span class="sxs-lookup"><span data-stu-id="2fa0b-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fa0b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fa0b-116">Requirements</span></span>



| <span data-ttu-id="2fa0b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fa0b-117">Requirement</span></span> | <span data-ttu-id="2fa0b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2fa0b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa0b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fa0b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa0b-120">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2fa0b-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2fa0b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fa0b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa0b-122">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2fa0b-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2fa0b-123">Header</span><span class="sxs-lookup"><span data-stu-id="2fa0b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fa0b-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fa0b-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa0b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fa0b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa0b-126">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="2fa0b-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2fa0b-127">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2fa0b-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




