---
description: Gibt an, ob der sprach Erfassungs-DSP die Vorverarbeitung eines mikrofonarrays ausführt.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347863"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a><span data-ttu-id="cc4d9-103">Mfpkey \_ wmaaecma \_ featr \_ micarr \_ Preproc-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cc4d9-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC Property</span></span>

<span data-ttu-id="cc4d9-104">Gibt an, ob der sprach Erfassungs-DSP die Vorverarbeitung eines mikrofonarrays ausführt.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-104">Specifies whether the Voice Capture DSP performs microphone array preprocessing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cc4d9-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cc4d9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cc4d9-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="cc4d9-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cc4d9-107">Data Type</span></span>

<span data-ttu-id="cc4d9-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="cc4d9-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="cc4d9-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="cc4d9-109">Default Value</span></span>

<span data-ttu-id="cc4d9-110">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="cc4d9-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="cc4d9-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="cc4d9-111">Applies To</span></span>

-   [<span data-ttu-id="cc4d9-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="cc4d9-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="cc4d9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc4d9-113">Remarks</span></span>

<span data-ttu-id="cc4d9-114">Bei der Vorverarbeitung können Sie stationäre Töne entfernen, die die Verarbeitung beeinträchtigen, z. b. ein Ton mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-114">Preprocessing can remove stationary tones that interfere with processing, such as a tone with a fixed pitch.</span></span>

<span data-ttu-id="cc4d9-115">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-115">This property can have the following values.</span></span>



| <span data-ttu-id="cc4d9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cc4d9-116">Value</span></span>          | <span data-ttu-id="cc4d9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc4d9-117">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="cc4d9-118">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="cc4d9-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="cc4d9-119">Deaktivieren Sie die Vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-119">Disable preprocessing.</span></span> |
| <span data-ttu-id="cc4d9-120">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="cc4d9-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="cc4d9-121">Aktivieren der Vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-121">Enable preprocessing.</span></span>  |



 

<span data-ttu-id="cc4d9-122">Der Standardwert dieser Eigenschaft ist Variant \_ true (aktiviert).</span><span class="sxs-lookup"><span data-stu-id="cc4d9-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="cc4d9-123">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="cc4d9-124">Der DSP verwendet diese Eigenschaft nur, wenn die Verarbeitung von mikrofonarrays aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-124">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc4d9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc4d9-125">Requirements</span></span>



| <span data-ttu-id="cc4d9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc4d9-126">Requirement</span></span> | <span data-ttu-id="cc4d9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cc4d9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4d9-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc4d9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cc4d9-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc4d9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cc4d9-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc4d9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cc4d9-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc4d9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc4d9-132">Header</span><span class="sxs-lookup"><span data-stu-id="cc4d9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc4d9-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc4d9-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4d9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc4d9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4d9-135">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc4d9-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="cc4d9-136">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="cc4d9-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
