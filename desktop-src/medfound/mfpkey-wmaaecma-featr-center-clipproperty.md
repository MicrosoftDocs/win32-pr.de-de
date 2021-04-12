---
description: Gibt an, ob der sprach Erfassungs-DSP das zentrale Abschneiden durchführt.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: MFPKEY_WMAAECMA_FEATR_CENTER_CLIP-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215049"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a><span data-ttu-id="1d68c-103">Mfpkey \_ wmaaecma \_ featr \_ Center- \_ Clip (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1d68c-103">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP Property</span></span>

<span data-ttu-id="1d68c-104">Gibt an, ob der sprach Erfassungs-DSP das zentrale Abschneiden durchführt.</span><span class="sxs-lookup"><span data-stu-id="1d68c-104">Specifies whether the Voice Capture DSP performs center clipping.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1d68c-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1d68c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1d68c-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1d68c-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1d68c-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1d68c-107">Data Type</span></span>

<span data-ttu-id="1d68c-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="1d68c-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="1d68c-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="1d68c-109">Default Value</span></span>

<span data-ttu-id="1d68c-110">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="1d68c-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="1d68c-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="1d68c-111">Applies To</span></span>

-   [<span data-ttu-id="1d68c-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="1d68c-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="1d68c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d68c-113">Remarks</span></span>

<span data-ttu-id="1d68c-114">Das zentrale Clipping ist ein Prozess, bei dem kleine Echo Restwerte entfernt werden, die nach der AEC-Verarbeitung in Single-Talk-Situationen verbleiben (wenn die Sprache nur an einem Ende der Zeile auftritt).</span><span class="sxs-lookup"><span data-stu-id="1d68c-114">Center clipping is a process that removes small echo residuals that remain after AEC processing, in single-talk situations (when speech occurs only on one end of the line).</span></span>

<span data-ttu-id="1d68c-115">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1d68c-115">This property can have the following values.</span></span>



| <span data-ttu-id="1d68c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1d68c-116">Value</span></span>          | <span data-ttu-id="1d68c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d68c-117">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="1d68c-118">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="1d68c-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="1d68c-119">Deaktivieren Sie das zentrale Clipping.</span><span class="sxs-lookup"><span data-stu-id="1d68c-119">Disable center clipping.</span></span> |
| <span data-ttu-id="1d68c-120">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="1d68c-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="1d68c-121">Aktivieren Sie das zentrale Clipping.</span><span class="sxs-lookup"><span data-stu-id="1d68c-121">Enable center clipping.</span></span>  |



 

<span data-ttu-id="1d68c-122">Der Standardwert dieser Eigenschaft ist Variant \_ true (aktiviert).</span><span class="sxs-lookup"><span data-stu-id="1d68c-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="1d68c-123">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="1d68c-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="1d68c-124">Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1d68c-124">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d68c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d68c-125">Requirements</span></span>



| <span data-ttu-id="1d68c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d68c-126">Requirement</span></span> | <span data-ttu-id="1d68c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1d68c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d68c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d68c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d68c-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d68c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1d68c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d68c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d68c-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d68c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1d68c-132">Header</span><span class="sxs-lookup"><span data-stu-id="1d68c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d68c-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d68c-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d68c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d68c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d68c-135">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d68c-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1d68c-136">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="1d68c-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
