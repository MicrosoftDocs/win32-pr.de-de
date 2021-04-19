---
description: Gibt an, ob der sprach Erfassungs-DSP Zeitstempel Statistiken in der Registrierung speichert.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353176"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a><span data-ttu-id="1c30b-103">Mfpkey \_ wmaaecma \_ Abrufen der \_ TS \_ Stats-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1c30b-103">MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS Property</span></span>

<span data-ttu-id="1c30b-104">Gibt an, ob der sprach Erfassungs-DSP Zeitstempel Statistiken in der Registrierung speichert.</span><span class="sxs-lookup"><span data-stu-id="1c30b-104">Specifies whether the Voice Capture DSP stores time stamp statistics in the registry.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1c30b-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1c30b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1c30b-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1c30b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1c30b-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1c30b-107">Data Type</span></span>

<span data-ttu-id="1c30b-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="1c30b-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="1c30b-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="1c30b-109">Default Value</span></span>

<span data-ttu-id="1c30b-110">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="1c30b-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="1c30b-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="1c30b-111">Applies To</span></span>

-   [<span data-ttu-id="1c30b-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="1c30b-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="1c30b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c30b-113">Remarks</span></span>

<span data-ttu-id="1c30b-114">AEC-Algorithmen (Akustik Echo Abbruch) hängen von exakten Zeitstempeln in den Audiostreams ab.</span><span class="sxs-lookup"><span data-stu-id="1c30b-114">Acoustic echo cancellation (AEC) algorithms depend on accurate time stamps on the audio streams.</span></span> <span data-ttu-id="1c30b-115">In der Praxis sind Zeitstempel oft nicht perfekt, und unterschiedliche Audiogeräte können unterschiedliche Raten von Varianz und Abweichung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1c30b-115">In reality, time stamps are often imperfect, and different audio devices can exhibit different rates of variance and drift.</span></span> <span data-ttu-id="1c30b-116">Wenn AEC aktiviert ist, sammelt der DSP Statistiken zu den Zeitstempeln und verwendet diese Informationen, um Ungenauigkeiten zu kompensieren.</span><span class="sxs-lookup"><span data-stu-id="1c30b-116">When AEC is enabled, the DSP collects statistics about the time stamps and uses this information to compensate for inaccuracies.</span></span>

<span data-ttu-id="1c30b-117">Wenn der Wert dieser Eigenschaft Variant true ist \_ , speichert der DSP die in der Registrierung gesammelten Statistiken.</span><span class="sxs-lookup"><span data-stu-id="1c30b-117">If the value of this property is VARIANT\_TRUE, the DSP saves the statistics that it collects in the registry.</span></span> <span data-ttu-id="1c30b-118">Beim nächsten Ausführen von AEC mit dem gleichen Paar von Audiogeräten liest der DSP die statistischen Informationen aus der Registrierung, sodass der DSP effizienter durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1c30b-118">The next time the DSP performs AEC using the same pair of audio devices, it reads the statistical information from the registry, which enables the DSP to perform more efficiently.</span></span>

<span data-ttu-id="1c30b-119">Wenn Sie den Wert dieser Eigenschaft auf Variant true festgelegt \_ haben und Sie den DSP im Filter Modus verwenden, sollten Sie auch die Eigenschaft " [mfpkey \_ wmaaecma \_ devicepair \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="1c30b-119">If you set the value of this property to VARIANT\_TRUE and you are using the DSP in filter mode, you should also set the [MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) property.</span></span> <span data-ttu-id="1c30b-120">Im Quell Modus ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1c30b-120">In source mode, this is not required.</span></span>

<span data-ttu-id="1c30b-121">Der Standardwert dieser Eigenschaft ist Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="1c30b-121">The default value of this property is VARIANT\_FALSE.</span></span> <span data-ttu-id="1c30b-122">Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1c30b-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c30b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c30b-123">Requirements</span></span>



| <span data-ttu-id="1c30b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c30b-124">Requirement</span></span> | <span data-ttu-id="1c30b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1c30b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c30b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c30b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c30b-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c30b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1c30b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c30b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c30b-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c30b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c30b-130">Header</span><span class="sxs-lookup"><span data-stu-id="1c30b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c30b-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c30b-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c30b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c30b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c30b-133">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c30b-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1c30b-134">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="1c30b-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
