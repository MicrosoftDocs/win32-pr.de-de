---
description: Gibt an, ob der sprach Erfassungs-DSP den Quell Modus oder Filter Modus verwendet.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: MFPKEY_WMAAECMA_DMO_SOURCE_MODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215050"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a><span data-ttu-id="baa27-103">Eigenschaft "mfpkey \_ wmaaecma \_ DMO \_ Source \_ Mode"</span><span class="sxs-lookup"><span data-stu-id="baa27-103">MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE Property</span></span>

<span data-ttu-id="baa27-104">Gibt an, ob der sprach Erfassungs-DSP den Quell Modus oder Filter Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="baa27-104">Specifies whether the Voice Capture DSP uses source mode or filter mode.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="baa27-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="baa27-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="baa27-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="baa27-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="baa27-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="baa27-107">Data Type</span></span>

<span data-ttu-id="baa27-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="baa27-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="baa27-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="baa27-109">Default Value</span></span>

<span data-ttu-id="baa27-110">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="baa27-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="baa27-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="baa27-111">Applies To</span></span>

-   [<span data-ttu-id="baa27-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="baa27-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="baa27-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="baa27-113">Remarks</span></span>

<span data-ttu-id="baa27-114">Im Quell Modus muss die Anwendung keine Eingabedaten an den DSP senden, da der DSP automatisch Daten von den Audiogeräten abruft.</span><span class="sxs-lookup"><span data-stu-id="baa27-114">In source mode, the application does not need to send input data to the DSP, because the DSP automatically pulls data from the audio devices.</span></span> <span data-ttu-id="baa27-115">Im Filter Modus muss die Anwendung die Eingabedaten an den DSP senden.</span><span class="sxs-lookup"><span data-stu-id="baa27-115">In filter mode, the application must send the input data to the DSP.</span></span>

<span data-ttu-id="baa27-116">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="baa27-116">This property can have the following values.</span></span>



| <span data-ttu-id="baa27-117">Wert</span><span class="sxs-lookup"><span data-stu-id="baa27-117">Value</span></span>          | <span data-ttu-id="baa27-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="baa27-118">Description</span></span>  |
|----------------|--------------|
| <span data-ttu-id="baa27-119">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="baa27-119">VARIANT\_FALSE</span></span> | <span data-ttu-id="baa27-120">Filter Modus.</span><span class="sxs-lookup"><span data-stu-id="baa27-120">Filter mode.</span></span> |
| <span data-ttu-id="baa27-121">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="baa27-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="baa27-122">Der Quell Modus.</span><span class="sxs-lookup"><span data-stu-id="baa27-122">Source mode.</span></span> |



 

> [!Note]  
> <span data-ttu-id="baa27-123">Wenn sich der DMO im Quell Modus befindet, sollten Sie nur [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) aufrufen, um das Ausgabedatenstrom Format festzulegen, und [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) nicht aufrufen, um Eingabedaten Strom Formate festzulegen.</span><span class="sxs-lookup"><span data-stu-id="baa27-123">When the DMO is in source mode, you should only call [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) to set output stream format, and do not call [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) to set input stream formats.</span></span> <span data-ttu-id="baa27-124">Andernfalls schlägt die DMO-Initialisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="baa27-124">Otherwise DMO initialization will fail.</span></span>

 

<span data-ttu-id="baa27-125">Wenn der Wert dieser Eigenschaft Variant true ist \_ , weist der DSP keine Eingaben auf.</span><span class="sxs-lookup"><span data-stu-id="baa27-125">If the value of this property is VARIANT\_TRUE, the DSP has zero inputs.</span></span> <span data-ttu-id="baa27-126">Wenn der Wert Variant \_ false ist, verfügt der DSP abhängig vom Wert der Eigenschaft [mfpkey \_ wmaaecma \_ System \_ Mode](mfpkey-wmaaecma-system-modeproperty.md) , wie in der folgenden Tabelle gezeigt, über eine oder zwei Eingaben.</span><span class="sxs-lookup"><span data-stu-id="baa27-126">If the value is VARIANT\_FALSE, the DSP has one or two inputs, depending on the value of the [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md) property, as shown in the following table.</span></span>



| <span data-ttu-id="baa27-127">Wert</span><span class="sxs-lookup"><span data-stu-id="baa27-127">Value</span></span>                     | <span data-ttu-id="baa27-128">Anzahl von Eingaben</span><span class="sxs-lookup"><span data-stu-id="baa27-128">Number of inputs</span></span> |
|---------------------------|------------------|
| <span data-ttu-id="baa27-129">Optibeam \_ \_ -Array und \_ AEC</span><span class="sxs-lookup"><span data-stu-id="baa27-129">OPTIBEAM\_ARRAY\_AND\_AEC</span></span> | <span data-ttu-id="baa27-130">2</span><span class="sxs-lookup"><span data-stu-id="baa27-130">2</span></span>                |
| <span data-ttu-id="baa27-131">nur Optibeam- \_ array \_</span><span class="sxs-lookup"><span data-stu-id="baa27-131">OPTIBEAM\_ARRAY\_ONLY</span></span>     | <span data-ttu-id="baa27-132">1</span><span class="sxs-lookup"><span data-stu-id="baa27-132">1</span></span>                |
| <span data-ttu-id="baa27-133">einzelner \_ Channel- \_ AEC</span><span class="sxs-lookup"><span data-stu-id="baa27-133">SINGLE\_CHANNEL\_AEC</span></span>      | <span data-ttu-id="baa27-134">2</span><span class="sxs-lookup"><span data-stu-id="baa27-134">2</span></span>                |
| <span data-ttu-id="baa27-135">\_ \_ nsagc eines einzelnen Kanals</span><span class="sxs-lookup"><span data-stu-id="baa27-135">SINGLE\_CHANNEL\_NSAGC</span></span>    | <span data-ttu-id="baa27-136">1</span><span class="sxs-lookup"><span data-stu-id="baa27-136">1</span></span>                |



 

> [!Note]  
> <span data-ttu-id="baa27-137">Nur Modi mit einer einzelnen Eingabe können mit dem Wrapper Filter DMO aus der DirectShow 9,0-API verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="baa27-137">Only modes with a single input will work with the wrapper filter DMO from the DirectShow 9.0 API.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="baa27-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baa27-138">Requirements</span></span>



| <span data-ttu-id="baa27-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baa27-139">Requirement</span></span> | <span data-ttu-id="baa27-140">Wert</span><span class="sxs-lookup"><span data-stu-id="baa27-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="baa27-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="baa27-141">Minimum supported client</span></span><br/> | <span data-ttu-id="baa27-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baa27-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="baa27-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="baa27-143">Minimum supported server</span></span><br/> | <span data-ttu-id="baa27-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baa27-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="baa27-145">Header</span><span class="sxs-lookup"><span data-stu-id="baa27-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="baa27-146"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="baa27-146"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baa27-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baa27-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa27-148">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="baa27-148">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="baa27-149">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="baa27-149">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
