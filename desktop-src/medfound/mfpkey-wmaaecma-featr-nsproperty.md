---
description: Gibt an, ob der sprach Erfassungs-DSP eine Rauschunterdrückung ausführt.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: MFPKEY_WMAAECMA_FEATR_NS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368179"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a><span data-ttu-id="3859a-103">Mfpkey \_ wmaaecma \_ featr \_ NS-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3859a-103">MFPKEY\_WMAAECMA\_FEATR\_NS Property</span></span>

<span data-ttu-id="3859a-104">Gibt an, ob der sprach Erfassungs-DSP eine Rauschunterdrückung ausführt.</span><span class="sxs-lookup"><span data-stu-id="3859a-104">Specifies whether the Voice Capture DSP performs noise suppression.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3859a-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3859a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3859a-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3859a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3859a-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3859a-107">Data Type</span></span>

<span data-ttu-id="3859a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3859a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="3859a-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="3859a-109">Default Value</span></span>

<span data-ttu-id="3859a-110">1</span><span class="sxs-lookup"><span data-stu-id="3859a-110">1</span></span>

## <a name="applies-to"></a><span data-ttu-id="3859a-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="3859a-111">Applies To</span></span>

-   [<span data-ttu-id="3859a-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="3859a-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="3859a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3859a-113">Remarks</span></span>

<span data-ttu-id="3859a-114">Bei der Rauschunterdrückung handelt es sich um eine DSP-Komponente (Digital Signal Processing, digitale Signalverarbeitung), mit der das Füll Zeichen im Audiosignal unterdrückt wird</span><span class="sxs-lookup"><span data-stu-id="3859a-114">Noise suppression is a digital signal processing (DSP) component that suppresses or reduces stationary background noise in the audio signal.</span></span> <span data-ttu-id="3859a-115">Die Rauschunterdrückung wird nach der Verarbeitung des akustischen Echo Abbruchs (AEC) und der Mikrofon Array Verarbeitung angewendet.</span><span class="sxs-lookup"><span data-stu-id="3859a-115">Noise suppression is applied after the acoustic echo cancellation (AEC) and microphone array processing.</span></span>

<span data-ttu-id="3859a-116">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3859a-116">This property can have the following values.</span></span>



| <span data-ttu-id="3859a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3859a-117">Value</span></span> | <span data-ttu-id="3859a-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3859a-118">Description</span></span>                |
|-------|----------------------------|
| <span data-ttu-id="3859a-119">0</span><span class="sxs-lookup"><span data-stu-id="3859a-119">0</span></span>     | <span data-ttu-id="3859a-120">Deaktivieren Sie die Rauschunterdrückung.</span><span class="sxs-lookup"><span data-stu-id="3859a-120">Disable noise suppression.</span></span> |
| <span data-ttu-id="3859a-121">1</span><span class="sxs-lookup"><span data-stu-id="3859a-121">1</span></span>     | <span data-ttu-id="3859a-122">Aktivieren Sie die Rauschunterdrückung.</span><span class="sxs-lookup"><span data-stu-id="3859a-122">Enable noise suppression.</span></span>  |



 

<span data-ttu-id="3859a-123">Der Standardwert dieser Eigenschaft ist 1 (aktiviert).</span><span class="sxs-lookup"><span data-stu-id="3859a-123">The default value of this property is 1 (enabled).</span></span> <span data-ttu-id="3859a-124">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="3859a-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="3859a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3859a-125">Requirements</span></span>



| <span data-ttu-id="3859a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3859a-126">Requirement</span></span> | <span data-ttu-id="3859a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3859a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3859a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3859a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3859a-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3859a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3859a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3859a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3859a-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3859a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3859a-132">Header</span><span class="sxs-lookup"><span data-stu-id="3859a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3859a-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3859a-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3859a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3859a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3859a-135">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3859a-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3859a-136">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="3859a-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
