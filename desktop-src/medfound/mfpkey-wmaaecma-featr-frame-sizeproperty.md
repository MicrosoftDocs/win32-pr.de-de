---
description: Gibt die audioframe-Größe an, die vom sprach Erfassungs-DSP verwendet wird.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: MFPKEY_WMAAECMA_FEATR_FRAME_SIZE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347275"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a><span data-ttu-id="4b2d4-103">Eigenschaft "mfpkey \_ wmaaecma \_ featr \_ Frame \_ size"</span><span class="sxs-lookup"><span data-stu-id="4b2d4-103">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE Property</span></span>

<span data-ttu-id="4b2d4-104">Gibt die audioframe-Größe an, die vom sprach Erfassungs-DSP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-104">Specifies the audio frame size used by the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4b2d4-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4b2d4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4b2d4-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="4b2d4-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4b2d4-107">Data Type</span></span>

<span data-ttu-id="4b2d4-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4b2d4-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4b2d4-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="4b2d4-109">Default Value</span></span>

<span data-ttu-id="4b2d4-110">0</span><span class="sxs-lookup"><span data-stu-id="4b2d4-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="4b2d4-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="4b2d4-111">Applies To</span></span>

-   [<span data-ttu-id="4b2d4-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="4b2d4-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="4b2d4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b2d4-113">Remarks</span></span>

<span data-ttu-id="4b2d4-114">Der Algorithmus für akustische Echo Abbruch (AEC) verarbeitet PCM-Audiobeispiele jeweils einen Frame.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-114">The acoustic echo cancellation (AEC) algorithm processes PCM audio samples one frame at a time.</span></span> <span data-ttu-id="4b2d4-115">Der Wert dieser Eigenschaft ist die Größe des Audioframes in den Beispielen.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-115">The value of this property is the size of the audio frame, in samples.</span></span> <span data-ttu-id="4b2d4-116">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="4b2d4-117">Der sprach Erfassungs-DSP unterstützt die folgenden Frame Größen:</span><span class="sxs-lookup"><span data-stu-id="4b2d4-117">The Voice Capture DSP supports the following frame sizes:</span></span>

-   <span data-ttu-id="4b2d4-118">80</span><span class="sxs-lookup"><span data-stu-id="4b2d4-118">80</span></span>
-   <span data-ttu-id="4b2d4-119">128</span><span class="sxs-lookup"><span data-stu-id="4b2d4-119">128</span></span>
-   <span data-ttu-id="4b2d4-120">160</span><span class="sxs-lookup"><span data-stu-id="4b2d4-120">160</span></span>
-   <span data-ttu-id="4b2d4-121">240</span><span class="sxs-lookup"><span data-stu-id="4b2d4-121">240</span></span>
-   <span data-ttu-id="4b2d4-122">256</span><span class="sxs-lookup"><span data-stu-id="4b2d4-122">256</span></span>
-   <span data-ttu-id="4b2d4-123">320</span><span class="sxs-lookup"><span data-stu-id="4b2d4-123">320</span></span>

<span data-ttu-id="4b2d4-124">Wenn der Wert dieser Eigenschaft NULL ist, wählt der DSP die Frame Größe basierend auf dem System Modus und dem Ausgabeformat aus.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-124">If the value of this property is zero, the DSP selects the frame size based on the system mode and the output format.</span></span>

<span data-ttu-id="4b2d4-125">Für eine optimale Leistung wird jedoch empfohlen, dass Anwendungen den Standardwert verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-125">For the best performance, however, it is recommended that applications use the default value.</span></span> <span data-ttu-id="4b2d4-126">Wenn der Verarbeitungsmodus nur Mikrofon Array ist, ist der Standardwert 320 Samples.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-126">If the processing mode is microphone array only, the default value is 320 samples.</span></span> <span data-ttu-id="4b2d4-127">Der Standardwert für alle anderen Verarbeitungsmodi ist 160 Samples.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-127">For all other processing modes, the default value is 160 samples.</span></span> <span data-ttu-id="4b2d4-128">Weitere Informationen zu den Verarbeitungsmodi des sprach Erfassungs-DSP finden Sie unter [mfpkey \_ wmaaecma \_ System \_ Mode](mfpkey-wmaaecma-system-modeproperty.md).</span><span class="sxs-lookup"><span data-stu-id="4b2d4-128">For more information about the processing modes of the Voice Capture DSP, see [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md).</span></span>

<span data-ttu-id="4b2d4-129">Nach dem ersten Aufrufe von [**imediaobject:: zudepaseestreamingresources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) oder [**imediaobject::P rocess Output**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)können Sie diese Eigenschaft lesen, um die tatsächlich verwendete Frame Größe zu erhalten, auch wenn der [**mfpkey \_ wmaaecma- \_ Funktions \_ Modus**](mfpkey-wmaaecma-feature-modeproperty.md) false ist.</span><span class="sxs-lookup"><span data-stu-id="4b2d4-129">After the first call to [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) or [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), you can read this property to get the actual frame size in use, even when [**MFPKEY\_WMAAECMA\_FEATURE\_MODE**](mfpkey-wmaaecma-feature-modeproperty.md) is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b2d4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b2d4-130">Requirements</span></span>



| <span data-ttu-id="4b2d4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b2d4-131">Requirement</span></span> | <span data-ttu-id="4b2d4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4b2d4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b2d4-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b2d4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4b2d4-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b2d4-134">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4b2d4-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b2d4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4b2d4-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b2d4-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b2d4-137">Header</span><span class="sxs-lookup"><span data-stu-id="4b2d4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b2d4-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b2d4-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b2d4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b2d4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b2d4-140">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b2d4-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4b2d4-141">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="4b2d4-141">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
