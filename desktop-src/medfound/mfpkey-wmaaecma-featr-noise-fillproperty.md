---
description: Gibt an, ob der sprach Erfassungs-DSP Füllvorgänge durchführt.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: MFPKEY_WMAAECMA_FEATR_NOISE_FILL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349091"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a><span data-ttu-id="5d421-103">Mfpkey \_ wmaaecma \_ featr- \_ Rausch \_ Füll Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5d421-103">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL Property</span></span>

<span data-ttu-id="5d421-104">Gibt an, ob der sprach Erfassungs-DSP Füllvorgänge durchführt.</span><span class="sxs-lookup"><span data-stu-id="5d421-104">Specifies whether the Voice Capture DSP performs noise filling.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5d421-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5d421-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5d421-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d421-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5d421-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5d421-107">Data Type</span></span>

<span data-ttu-id="5d421-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5d421-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="5d421-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="5d421-109">Default Value</span></span>

<span data-ttu-id="5d421-110">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="5d421-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="5d421-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="5d421-111">Applies To</span></span>

-   [<span data-ttu-id="5d421-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="5d421-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="5d421-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d421-113">Remarks</span></span>

<span data-ttu-id="5d421-114">Das Füll Füllungs Zeichen fügt eine kleine Menge an Geräuschen zu den Teilen des Signals hinzu, bei denen das Mittel Clipping die restlichen Echo Punkte entfernt hat.</span><span class="sxs-lookup"><span data-stu-id="5d421-114">Noise filling adds a small amount of noise to portions of the signal where center clipping has removed the residual echoes.</span></span> <span data-ttu-id="5d421-115">Dies führt zu einer besseren Benutzererfahrung als bei der Verwendung von stillen Lücken im Signal.</span><span class="sxs-lookup"><span data-stu-id="5d421-115">This results in a better experience for the user than leaving silent gaps in the signal.</span></span>

<span data-ttu-id="5d421-116">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5d421-116">This property can have the following values.</span></span>



| <span data-ttu-id="5d421-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5d421-117">Value</span></span>          | <span data-ttu-id="5d421-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d421-118">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="5d421-119">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="5d421-119">VARIANT\_TRUE</span></span>  | <span data-ttu-id="5d421-120">Aktivieren Sie Füll Füllung.</span><span class="sxs-lookup"><span data-stu-id="5d421-120">Enable noise filling.</span></span>  |
| <span data-ttu-id="5d421-121">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="5d421-121">VARIANT\_FALSE</span></span> | <span data-ttu-id="5d421-122">Deaktivieren Sie die Füll Füllung.</span><span class="sxs-lookup"><span data-stu-id="5d421-122">Disable noise filling.</span></span> |



 

<span data-ttu-id="5d421-123">Der Standardwert dieser Eigenschaft ist Variant \_ true (aktiviert).</span><span class="sxs-lookup"><span data-stu-id="5d421-123">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="5d421-124">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="5d421-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="5d421-125">Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5d421-125">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d421-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d421-126">Requirements</span></span>



| <span data-ttu-id="5d421-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d421-127">Requirement</span></span> | <span data-ttu-id="5d421-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5d421-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d421-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d421-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5d421-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d421-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5d421-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d421-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5d421-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d421-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d421-133">Header</span><span class="sxs-lookup"><span data-stu-id="5d421-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d421-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d421-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d421-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d421-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d421-136">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5d421-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5d421-137">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="5d421-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
