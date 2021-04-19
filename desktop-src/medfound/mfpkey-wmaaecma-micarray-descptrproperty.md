---
description: Gibt die Mikrofon Array Geometrie für den sprach Erfassungs-DSP an.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: MFPKEY_WMAAECMA_MICARRAY_DESCPTR-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355571"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a><span data-ttu-id="6ca6a-103">Mfpkey \_ wmaaecma \_ micarray \_ descptr (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6ca6a-103">MFPKEY\_WMAAECMA\_MICARRAY\_DESCPTR Property</span></span>

<span data-ttu-id="6ca6a-104">Gibt die Mikrofon Array Geometrie für den sprach Erfassungs-DSP an.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-104">Specifies the microphone array geometry for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="6ca6a-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="6ca6a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="6ca6a-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="6ca6a-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6ca6a-107">Data Type</span></span>

<span data-ttu-id="6ca6a-108">VT- \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="6ca6a-108">VT\_BLOB</span></span>

## <a name="applies-to"></a><span data-ttu-id="6ca6a-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="6ca6a-109">Applies To</span></span>

-   [<span data-ttu-id="6ca6a-110">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="6ca6a-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="6ca6a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ca6a-111">Remarks</span></span>

<span data-ttu-id="6ca6a-112">Der Wert dieser Eigenschaft ist eine [**kston- \_ MIC- \_ array \_ Geometrie**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) Struktur.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-112">The value of this property is a [**KSAUDIO\_MIC\_ARRAY\_GEOMETRY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) structure.</span></span> <span data-ttu-id="6ca6a-113">Diese Struktur wird in der Header Datei "ksmedia. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-113">This structure is defined in the header file KsMedia.h.</span></span> <span data-ttu-id="6ca6a-114">Um die Geometrie des mikrofonarrays abzurufen, Fragen Sie das Audiogerät nach der Geometry-Eigenschaft des ksproperty \_ - \_ audiomic-Arrays ab, \_ indem Sie \_ die Methode " **ikscontrol:: ksproperty** " auf dem Gerät aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-114">To get the microphone array geometry, query the audio device for the KSPROPERTY\_AUDIO\_MIC\_ARRAY\_GEOMETRY property by calling the **IKsControl::KSProperty** method on the device.</span></span> <span data-ttu-id="6ca6a-115">Weitere Informationen zu mikrofonarrays finden Sie im Whitepaper [Erstellen und Verwenden von mikrofonarrays für Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span><span class="sxs-lookup"><span data-stu-id="6ca6a-115">For more information on microphone arrays, download the white paper [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span></span>

<span data-ttu-id="6ca6a-116">Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Filter Modus verwenden und die Verarbeitung von mikrofonarrays aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-116">Set this property if you are using the DSP in filter mode and microphone array processing is enabled.</span></span> <span data-ttu-id="6ca6a-117">Wenn Sie den DSP im Quell Modus verwenden, fragt der DSP das Gerät automatisch nach den Geometry-Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-117">If you are using the DSP in source mode, the DSP automatically queries the device for the geometry information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca6a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ca6a-118">Requirements</span></span>



| <span data-ttu-id="6ca6a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ca6a-119">Requirement</span></span> | <span data-ttu-id="6ca6a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6ca6a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca6a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ca6a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca6a-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ca6a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6ca6a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ca6a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca6a-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ca6a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ca6a-125">Header</span><span class="sxs-lookup"><span data-stu-id="6ca6a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca6a-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca6a-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca6a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ca6a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca6a-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ca6a-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6ca6a-129">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="6ca6a-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
