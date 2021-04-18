---
description: Gibt an, ob der sprach Erfassungs-DSP eine automatische Steuerungs Steuerung ausführt.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: MFPKEY_WMAAECMA_FEATR_AGC-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345819"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a><span data-ttu-id="05053-103">Eigenschaft "mfpkey \_ wmaaecma \_ featr \_ AGC"</span><span class="sxs-lookup"><span data-stu-id="05053-103">MFPKEY\_WMAAECMA\_FEATR\_AGC Property</span></span>

<span data-ttu-id="05053-104">Gibt an, ob der sprach Erfassungs-DSP eine automatische Steuerungs Steuerung ausführt.</span><span class="sxs-lookup"><span data-stu-id="05053-104">Specifies whether the Voice Capture DSP performs automatic gain control.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="05053-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="05053-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="05053-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05053-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="05053-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="05053-107">Data Type</span></span>

<span data-ttu-id="05053-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="05053-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="05053-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="05053-109">Default Value</span></span>

<span data-ttu-id="05053-110">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="05053-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="05053-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="05053-111">Applies To</span></span>

-   [<span data-ttu-id="05053-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="05053-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="05053-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05053-113">Remarks</span></span>

<span data-ttu-id="05053-114">Die automatische Gewinn Steuerung ist eine DSP-Komponente (Digital Signal Processing, digitale Signalverarbeitung), die den Zuwachs anpasst, sodass die Ausgabe Ebene des Signals innerhalb desselben ungefähren Bereichs verbleibt.</span><span class="sxs-lookup"><span data-stu-id="05053-114">Automatic gain control is a digital signal processing (DSP) component that adjusts the gain so that the output level of the signal remains within the same approximate range.</span></span>

<span data-ttu-id="05053-115">Diese Eigenschaft kann die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="05053-115">This property can have the following values.</span></span>



| <span data-ttu-id="05053-116">Wert</span><span class="sxs-lookup"><span data-stu-id="05053-116">Value</span></span>          | <span data-ttu-id="05053-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05053-117">Description</span></span>                     |
|----------------|---------------------------------|
| <span data-ttu-id="05053-118">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="05053-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="05053-119">Deaktivieren Sie die automatische Gewinn Steuerung.</span><span class="sxs-lookup"><span data-stu-id="05053-119">Disable automatic gain control.</span></span> |
| <span data-ttu-id="05053-120">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="05053-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="05053-121">Aktivieren Sie die automatische Steuerelement Steuerung.</span><span class="sxs-lookup"><span data-stu-id="05053-121">Enable automatic gain control.</span></span>  |



 

<span data-ttu-id="05053-122">Der Standardwert dieser Eigenschaft ist Variant \_ false (deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="05053-122">The default value of this property is VARIANT\_FALSE (disabled).</span></span> <span data-ttu-id="05053-123">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="05053-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="05053-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05053-124">Requirements</span></span>



| <span data-ttu-id="05053-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05053-125">Requirement</span></span> | <span data-ttu-id="05053-126">Wert</span><span class="sxs-lookup"><span data-stu-id="05053-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05053-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05053-127">Minimum supported client</span></span><br/> | <span data-ttu-id="05053-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05053-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="05053-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05053-129">Minimum supported server</span></span><br/> | <span data-ttu-id="05053-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05053-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05053-131">Header</span><span class="sxs-lookup"><span data-stu-id="05053-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="05053-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="05053-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05053-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05053-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05053-134">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05053-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="05053-135">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="05053-135">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
