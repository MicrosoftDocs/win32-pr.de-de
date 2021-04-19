---
description: Gibt den Typ der sprach Aktivitäts Erkennung an, den der sprach Erfassungs-DSP ausführt.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: MFPKEY_WMAAECMA_FEATR_VAD-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348489"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a><span data-ttu-id="c0b27-103">Mfpkey \_ wmaaecma \_ featr \_ VAD (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c0b27-103">MFPKEY\_WMAAECMA\_FEATR\_VAD Property</span></span>

<span data-ttu-id="c0b27-104">Gibt den Typ der sprach Aktivitäts Erkennung an, den der sprach Erfassungs-DSP ausführt.</span><span class="sxs-lookup"><span data-stu-id="c0b27-104">Specifies the type of voice activity detection that the Voice Capture DSP performs.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c0b27-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c0b27-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c0b27-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0b27-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c0b27-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c0b27-107">Data Type</span></span>

<span data-ttu-id="c0b27-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c0b27-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c0b27-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="c0b27-109">Default Value</span></span>

<span data-ttu-id="c0b27-110">0</span><span class="sxs-lookup"><span data-stu-id="c0b27-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="c0b27-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="c0b27-111">Applies To</span></span>

-   [<span data-ttu-id="c0b27-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="c0b27-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="c0b27-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0b27-113">Remarks</span></span>

<span data-ttu-id="c0b27-114">Der Wert dieser Eigenschaft ist ein Member der [AEC \_ VAD- \_ Modus](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="c0b27-114">The value of this property is a member of the [AEC\_VAD\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) enumeration.</span></span> <span data-ttu-id="c0b27-115">Die Ausgabe der sprach Aktivitäts Erkennung ist eine Zahl zwischen 0 und 3, die für jeden audioframe berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c0b27-115">The output from voice activity detection is a number from 0 to 3, calculated for each audio frame.</span></span> <span data-ttu-id="c0b27-116">Der DSP codiert das Ergebnis auf das niedrigste Bit der ersten beiden Audiobeispiele in jedem audioframe.</span><span class="sxs-lookup"><span data-stu-id="c0b27-116">The DSP encodes the result in the lowest bit of the first two audio samples in each audio frame.</span></span> <span data-ttu-id="c0b27-117">Die Bedeutung des Werts hängt vom angegebenen Modus ab.</span><span class="sxs-lookup"><span data-stu-id="c0b27-117">The meaning of the value depends on the specified mode.</span></span>

<span data-ttu-id="c0b27-118">Der folgende Code zeigt, wie die Ergebnisse aus den Audiodaten extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="c0b27-118">The following code shows how to extract the results from the audio data.</span></span> <span data-ttu-id="c0b27-119">In diesem Beispiel ist *poutput* ein Zeiger auf den Anfang eines Audioframes in den Ausgabedaten.</span><span class="sxs-lookup"><span data-stu-id="c0b27-119">In this example, *pOutput* is a pointer to the start of an audio frame in the output data.</span></span>


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



<span data-ttu-id="c0b27-120">Der Standardwert dieser Eigenschaft ist 0 (deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="c0b27-120">The default value of this property is 0 (disabled).</span></span> <span data-ttu-id="c0b27-121">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="c0b27-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b27-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0b27-122">Requirements</span></span>



| <span data-ttu-id="c0b27-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0b27-123">Requirement</span></span> | <span data-ttu-id="c0b27-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c0b27-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b27-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0b27-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b27-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0b27-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c0b27-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0b27-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b27-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0b27-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0b27-129">Header</span><span class="sxs-lookup"><span data-stu-id="c0b27-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b27-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b27-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b27-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0b27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b27-132">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0b27-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
