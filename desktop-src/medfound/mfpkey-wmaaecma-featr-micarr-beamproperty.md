---
description: Gibt an, welcher Strahl der sprach Erfassungs-DSP für die Verarbeitung von mikrofonarrays verwendet.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: MFPKEY_WMAAECMA_FEATR_MICARR_BEAM-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360136"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a><span data-ttu-id="208d5-103">Mfpkey \_ wmaaecma \_ featr \_ micarr- \_ Eigenschaft (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="208d5-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_BEAM Property</span></span>

<span data-ttu-id="208d5-104">Gibt an, welcher Strahl der sprach Erfassungs-DSP für die Verarbeitung von mikrofonarrays verwendet.</span><span class="sxs-lookup"><span data-stu-id="208d5-104">Specifies which beam the Voice Capture DSP uses for microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="208d5-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="208d5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="208d5-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="208d5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="208d5-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="208d5-107">Data Type</span></span>

<span data-ttu-id="208d5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="208d5-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="208d5-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="208d5-109">Applies To</span></span>

-   [<span data-ttu-id="208d5-110">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="208d5-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="208d5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="208d5-111">Remarks</span></span>

<span data-ttu-id="208d5-112">Legen Sie diese Eigenschaft fest, wenn der Wert der Eigenschaft " [mfpkey \_ wmaaecma \_ featr \_ micarr \_ Mode](mfpkey-wmaaecma-featr-micarr-modeproperty.md) " micarray \_ extern \_ Beam ist.</span><span class="sxs-lookup"><span data-stu-id="208d5-112">Set this property if the value of the [MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) property is MICARRAY\_EXTERN\_BEAM.</span></span>

<span data-ttu-id="208d5-113">Wenn der Wert von " [**mfpkey \_ wmaaecma \_ featr \_ micarr \_ Mode**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) " micarray \_ Single \_ Beam ist, können Sie diese Eigenschaft lesen, um abzufragen, welcher Strahl vom DSP ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="208d5-113">If the value of [**MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) is MICARRAY\_SINGLE\_BEAM, you can read this property to query which beam was selected by the DSP.</span></span>

<span data-ttu-id="208d5-114">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="208d5-114">This property can have the following values.</span></span> <span data-ttu-id="208d5-115">Werte sind horizontal in Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-115">Values are in degrees horizontal.</span></span>



| <span data-ttu-id="208d5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="208d5-116">Value</span></span> | <span data-ttu-id="208d5-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="208d5-117">Description</span></span>              |
|-------|--------------------------|
| <span data-ttu-id="208d5-118">0</span><span class="sxs-lookup"><span data-stu-id="208d5-118">0</span></span>     | <span data-ttu-id="208d5-119">-50 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-119">-50 degrees.</span></span>             |
| <span data-ttu-id="208d5-120">1</span><span class="sxs-lookup"><span data-stu-id="208d5-120">1</span></span>     | <span data-ttu-id="208d5-121">-40 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-121">-40 degrees.</span></span>             |
| <span data-ttu-id="208d5-122">2</span><span class="sxs-lookup"><span data-stu-id="208d5-122">2</span></span>     | <span data-ttu-id="208d5-123">-30 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-123">-30 degrees.</span></span>             |
| <span data-ttu-id="208d5-124">3</span><span class="sxs-lookup"><span data-stu-id="208d5-124">3</span></span>     | <span data-ttu-id="208d5-125">-20 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-125">-20 degrees.</span></span>             |
| <span data-ttu-id="208d5-126">4</span><span class="sxs-lookup"><span data-stu-id="208d5-126">4</span></span>     | <span data-ttu-id="208d5-127">-10 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-127">-10 degrees.</span></span>             |
| <span data-ttu-id="208d5-128">5</span><span class="sxs-lookup"><span data-stu-id="208d5-128">5</span></span>     | <span data-ttu-id="208d5-129">0 Grad (Mittelstrahl).</span><span class="sxs-lookup"><span data-stu-id="208d5-129">0 degrees (center beam).</span></span> |
| <span data-ttu-id="208d5-130">6</span><span class="sxs-lookup"><span data-stu-id="208d5-130">6</span></span>     | <span data-ttu-id="208d5-131">10 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-131">10 degrees.</span></span>              |
| <span data-ttu-id="208d5-132">7</span><span class="sxs-lookup"><span data-stu-id="208d5-132">7</span></span>     | <span data-ttu-id="208d5-133">20 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-133">20 degrees.</span></span>              |
| <span data-ttu-id="208d5-134">8</span><span class="sxs-lookup"><span data-stu-id="208d5-134">8</span></span>     | <span data-ttu-id="208d5-135">30 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-135">30 degrees.</span></span>              |
| <span data-ttu-id="208d5-136">9</span><span class="sxs-lookup"><span data-stu-id="208d5-136">9</span></span>     | <span data-ttu-id="208d5-137">40 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-137">40 degrees.</span></span>              |
| <span data-ttu-id="208d5-138">10</span><span class="sxs-lookup"><span data-stu-id="208d5-138">10</span></span>    | <span data-ttu-id="208d5-139">50 Grad.</span><span class="sxs-lookup"><span data-stu-id="208d5-139">50 degrees.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="208d5-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="208d5-140">Requirements</span></span>



| <span data-ttu-id="208d5-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="208d5-141">Requirement</span></span> | <span data-ttu-id="208d5-142">Wert</span><span class="sxs-lookup"><span data-stu-id="208d5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="208d5-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="208d5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="208d5-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="208d5-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="208d5-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="208d5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="208d5-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="208d5-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="208d5-147">Header</span><span class="sxs-lookup"><span data-stu-id="208d5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="208d5-148"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="208d5-148"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="208d5-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="208d5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="208d5-150">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="208d5-150">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="208d5-151">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="208d5-151">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
