---
description: Gibt an, welche Audiogeräte der sprach Erfassungs-DSP zum Erfassen und Rendern von Audiodaten verwendet.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: MFPKEY_WMAAECMA_DEVICE_INDEXES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863439"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a><span data-ttu-id="af07d-103">Mfpkey \_ wmaaecma- \_ Geräte \_ Index Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af07d-103">MFPKEY\_WMAAECMA\_DEVICE\_INDEXES Property</span></span>

<span data-ttu-id="af07d-104">Gibt an, welche Audiogeräte der sprach Erfassungs-DSP zum Erfassen und Rendern von Audiodaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="af07d-104">Specifies which audio devices the Voice Capture DSP uses for capturing and rendering audio.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="af07d-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="af07d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="af07d-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af07d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="af07d-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="af07d-107">Data Type</span></span>

<span data-ttu-id="af07d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="af07d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="af07d-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="af07d-109">Default Value</span></span>

<span data-ttu-id="af07d-110">(-1,-1).</span><span class="sxs-lookup"><span data-stu-id="af07d-110">(-1, -1).</span></span>

## <a name="applies-to"></a><span data-ttu-id="af07d-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="af07d-111">Applies To</span></span>

-   [<span data-ttu-id="af07d-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="af07d-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="af07d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af07d-113">Remarks</span></span>

<span data-ttu-id="af07d-114">Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Quell Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="af07d-114">Set this property if you are using the DSP in source mode.</span></span> <span data-ttu-id="af07d-115">Der DSP ignoriert diese Eigenschaft im Filter Modus.</span><span class="sxs-lookup"><span data-stu-id="af07d-115">The DSP ignores this property in filter mode.</span></span>

<span data-ttu-id="af07d-116">Der Wert der-Eigenschaft ist 2 16-Bit- **Wörter**, die in ein **DWORD** gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="af07d-116">The value of the property is two 16-bit **WORD** s packed into a **DWORD**.</span></span> <span data-ttu-id="af07d-117">In den oberen 16 Bits ist das audiorenderinggerät (in der Regel ein Redner) angegeben, und die unteren 16 Bits geben das Erfassungsgerät (in der Regel ein Mikrofon) an.</span><span class="sxs-lookup"><span data-stu-id="af07d-117">The upper 16 bits specify the audio rendering device (typically a speaker), and the lower 16 bits specify the capture device (typically a microphone).</span></span> <span data-ttu-id="af07d-118">Jedes Gerät wird als Index in der audiogeräteauflistung angegeben.</span><span class="sxs-lookup"><span data-stu-id="af07d-118">Each device is specified as an index into the audio device collection.</span></span> <span data-ttu-id="af07d-119">Wenn der Index-1 ist, wird das Standardgerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="af07d-119">If the index is -1, the default device is used.</span></span>

<span data-ttu-id="af07d-120">Der Geräte Index entspricht dem Sammlungs Index, der in der [**immendvicecollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) -Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af07d-120">The device index corresponds to the collection index used in the [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) interface.</span></span> <span data-ttu-id="af07d-121">Die Anwendung muss die ganz gängige Stimme über das ausgewählte renderinggerät abspielen.</span><span class="sxs-lookup"><span data-stu-id="af07d-121">The application must play the far-end voice through the selected rendering device.</span></span> <span data-ttu-id="af07d-122">(Die vielseitige Stimme ist die Stimme der Person am anderen Ende der Telefonleitung, die über den Sprecher auf dem Computer des Benutzers gespielt wird.) Wenn das ausgewählte renderinggerät keinen aktiven Stream hat, kann der DSP keine Ausgabe verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="af07d-122">(The far-end voice is the voice of the person on the other end of the telephone line, which is played through the speaker on the user's computer.) If the selected rendering device does not have an active stream, the DSP cannot process any output.</span></span>

<span data-ttu-id="af07d-123">Der Standardwert dieser Eigenschaft ist (-1,-1).</span><span class="sxs-lookup"><span data-stu-id="af07d-123">The default value of this property is (-1, -1).</span></span>

<span data-ttu-id="af07d-124">Im folgenden Beispiel wird gezeigt, wie die **PROPVARIANT** für diese Eigenschaft initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="af07d-124">The following example shows how to initialize the **PROPVARIANT** for this property.</span></span>


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a><span data-ttu-id="af07d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af07d-125">Requirements</span></span>



| <span data-ttu-id="af07d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af07d-126">Requirement</span></span> | <span data-ttu-id="af07d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="af07d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af07d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af07d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="af07d-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af07d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="af07d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af07d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="af07d-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af07d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af07d-132">Header</span><span class="sxs-lookup"><span data-stu-id="af07d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="af07d-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af07d-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af07d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af07d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af07d-135">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af07d-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="af07d-136">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="af07d-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
