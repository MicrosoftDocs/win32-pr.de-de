---
description: Gibt an, ob der sprach Erfassungs-DSP eine Mikrofon-zuschließung anwendet.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360135"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a><span data-ttu-id="c63d0-103">Mfpkey \_ wmaaecma \_ MIC \_ - \_ bounter-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c63d0-103">MFPKEY\_WMAAECMA\_MIC\_GAIN\_BOUNDER Property</span></span>

<span data-ttu-id="c63d0-104">Gibt an, ob der sprach Erfassungs-DSP eine Mikrofon-zuschließung anwendet.</span><span class="sxs-lookup"><span data-stu-id="c63d0-104">Specifies whether the Voice Capture DSP applies microphone gain bounding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c63d0-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c63d0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c63d0-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c63d0-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c63d0-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c63d0-107">Data Type</span></span>

<span data-ttu-id="c63d0-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="c63d0-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="c63d0-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="c63d0-109">Default Value</span></span>

<span data-ttu-id="c63d0-110">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="c63d0-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="c63d0-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="c63d0-111">Applies To</span></span>

-   [<span data-ttu-id="c63d0-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="c63d0-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="c63d0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c63d0-113">Remarks</span></span>

<span data-ttu-id="c63d0-114">Die Mikrofon-Gewinngrenze stellt sicher, dass das Mikrofon über das richtige Maß an Gewinn verfügt.</span><span class="sxs-lookup"><span data-stu-id="c63d0-114">Microphone gain bounding ensures that the microphone has the correct level of gain.</span></span> <span data-ttu-id="c63d0-115">Wenn der Gewinn zu hoch ist, ist das erfasste Signal möglicherweise erschöpft und wird abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="c63d0-115">If gain is too high, the captured signal might be saturated and will be clipped.</span></span> <span data-ttu-id="c63d0-116">Clipping ist ein nichtlinearer Effekt, der dazu führt, dass der Algorithmus für den akustische Echo Abbruch (AEC) fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c63d0-116">Clipping is a non-linear effect, which will cause the acoustic echo cancellation (AEC) algorithm to fail.</span></span> <span data-ttu-id="c63d0-117">Wenn der Gewinn zu niedrig ist, ist das Signal-zu-Rauschen-Verhältnis gering, was auch bewirken kann, dass der AEC-Algorithmus fehlschlägt oder nicht gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c63d0-117">If the gain is too low, the signal-to-noise ratio is low, which can also cause the AEC algorithm to fail or not perform well.</span></span>

<span data-ttu-id="c63d0-118">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c63d0-118">This property can have the following values.</span></span>



| <span data-ttu-id="c63d0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c63d0-119">Value</span></span>          | <span data-ttu-id="c63d0-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c63d0-120">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="c63d0-121">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="c63d0-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="c63d0-122">Ermöglicht das Begrenzen des Mikrofons.</span><span class="sxs-lookup"><span data-stu-id="c63d0-122">Enable microphone gain bounding.</span></span>  |
| <span data-ttu-id="c63d0-123">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="c63d0-123">VARIANT\_FALSE</span></span> | <span data-ttu-id="c63d0-124">Deaktivieren Sie das Ende des Mikrofons.</span><span class="sxs-lookup"><span data-stu-id="c63d0-124">Disable microphone gain bounding.</span></span> |



 

<span data-ttu-id="c63d0-125">Der Standardwert dieser Eigenschaft ist Variant \_ true (aktiviert).</span><span class="sxs-lookup"><span data-stu-id="c63d0-125">The default value of this property is VARIANT\_TRUE (enabled).</span></span>

<span data-ttu-id="c63d0-126">Das Begrenzen des Mikrofons wird nur angewendet, wenn der DSP im Quell Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c63d0-126">Microphone gain bounding is applies only when the DSP operates in source mode.</span></span> <span data-ttu-id="c63d0-127">Im Filter Modus muss die Anwendung sicherstellen, dass das Mikrofon über die richtige Gewinn Ebene verfügt.</span><span class="sxs-lookup"><span data-stu-id="c63d0-127">In filter mode, the application must ensure that the microphone has the correct gain level.</span></span>

## <a name="requirements"></a><span data-ttu-id="c63d0-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c63d0-128">Requirements</span></span>



| <span data-ttu-id="c63d0-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c63d0-129">Requirement</span></span> | <span data-ttu-id="c63d0-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c63d0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c63d0-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c63d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c63d0-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c63d0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c63d0-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c63d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c63d0-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c63d0-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c63d0-135">Header</span><span class="sxs-lookup"><span data-stu-id="c63d0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c63d0-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c63d0-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c63d0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c63d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c63d0-138">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c63d0-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c63d0-139">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="c63d0-139">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
