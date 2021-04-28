---
description: 'AVDecAudioDualMono-Eigenschaft: Gibt an, ob 2-Kanal-Audio als Stereo oder duales Mono codiert wird.'
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: AVDecAudioDualMono-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096568"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="b3149-103">AVDecAudioDualMono (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b3149-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="b3149-104">Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.</span><span class="sxs-lookup"><span data-stu-id="b3149-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="b3149-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b3149-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3149-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b3149-106">Data type</span></span>

<span data-ttu-id="b3149-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b3149-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b3149-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="b3149-108">Property GUID</span></span>

<span data-ttu-id="b3149-109">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="b3149-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="b3149-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b3149-110">Property value</span></span>

<span data-ttu-id="b3149-111">Der Wert dieser Eigenschaft ist ein Member der [**eAVDecAudioDualMono-Enumeration.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)</span><span class="sxs-lookup"><span data-stu-id="b3149-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3149-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3149-112">Remarks</span></span>

<span data-ttu-id="b3149-113">Diese Eigenschaft gilt nur, wenn der Eingabebitstream des Decoders Zweikanalaudiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="b3149-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="b3149-114">Ein Zweikanal-Audiostream kann als Stereo oder duales Mono codiert werden.</span><span class="sxs-lookup"><span data-stu-id="b3149-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="b3149-115">Wenn die Audiodaten dual mono sind, können Sie die [**AVDecAudioDualMonoReproMode-Eigenschaft**](avdecaudiodualmonorepromode-property.md) festlegen, um zu konfigurieren, wie der Decoder die Audiodaten reproduziert.</span><span class="sxs-lookup"><span data-stu-id="b3149-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3149-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3149-116">Requirements</span></span>



| <span data-ttu-id="b3149-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3149-117">Requirement</span></span> | <span data-ttu-id="b3149-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b3149-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3149-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3149-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3149-120">UWP-Apps für Windows 2000 \[ \| Professional-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3149-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b3149-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3149-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b3149-122">Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3149-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b3149-123">Header</span><span class="sxs-lookup"><span data-stu-id="b3149-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3149-124"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="b3149-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3149-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3149-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3149-126">Codec-API-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3149-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b3149-127">**ICodecAPI-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b3149-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




