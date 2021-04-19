---
description: Legt den Verarbeitungsmodus für den sprach Erfassungs-DSP fest.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348910"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a><span data-ttu-id="2f55d-103">Mfpkey- \_ wmaaecma- \_ System \_ Modus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2f55d-103">MFPKEY\_WMAAECMA\_SYSTEM\_MODE Property</span></span>

<span data-ttu-id="2f55d-104">Legt den Verarbeitungsmodus für den sprach Erfassungs-DSP fest.</span><span class="sxs-lookup"><span data-stu-id="2f55d-104">Sets the processing mode for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2f55d-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2f55d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2f55d-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2f55d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2f55d-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2f55d-107">Data Type</span></span>

<span data-ttu-id="2f55d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2f55d-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="2f55d-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="2f55d-109">Applies To</span></span>

-   [<span data-ttu-id="2f55d-110">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="2f55d-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="2f55d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f55d-111">Remarks</span></span>

<span data-ttu-id="2f55d-112">Der Wert dieser Eigenschaft ist ein Member der [AEC systemmodusenumeration \_ \_ ](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .</span><span class="sxs-lookup"><span data-stu-id="2f55d-112">The value of this property is a member of the [AEC\_SYSTEM\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) enumeration.</span></span>

<span data-ttu-id="2f55d-113">Die-Eigenschaft muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2f55d-113">The property must be one of the following values.</span></span>



| <span data-ttu-id="2f55d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2f55d-114">Value</span></span> | <span data-ttu-id="2f55d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f55d-115">Description</span></span>                                 |
|-------|---------------------------------------------|
| <span data-ttu-id="2f55d-116">0</span><span class="sxs-lookup"><span data-stu-id="2f55d-116">0</span></span>     | <span data-ttu-id="2f55d-117">Nur der Modus für audioecho-Abbruch (AEC)</span><span class="sxs-lookup"><span data-stu-id="2f55d-117">Audio echo cancellation (AEC) only mode</span></span>     |
| <span data-ttu-id="2f55d-118">2</span><span class="sxs-lookup"><span data-stu-id="2f55d-118">2</span></span>     | <span data-ttu-id="2f55d-119">Modus für die Verarbeitung von mikrofonarrays (nur Map)</span><span class="sxs-lookup"><span data-stu-id="2f55d-119">Microphone array processing (MAP) only mode</span></span> |
| <span data-ttu-id="2f55d-120">4</span><span class="sxs-lookup"><span data-stu-id="2f55d-120">4</span></span>     | <span data-ttu-id="2f55d-121">AEC-und Zuordnungs Modus</span><span class="sxs-lookup"><span data-stu-id="2f55d-121">AEC and MAP mode</span></span>                            |
| <span data-ttu-id="2f55d-122">5</span><span class="sxs-lookup"><span data-stu-id="2f55d-122">5</span></span>     | <span data-ttu-id="2f55d-123">Weder AEC noch Kartenmodus</span><span class="sxs-lookup"><span data-stu-id="2f55d-123">Neither AEC nor MAP mode</span></span>                    |



 

<span data-ttu-id="2f55d-124">Sie müssen diese Eigenschaft festlegen, bevor Sie den sprach Erfassungs-DSP verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f55d-124">You must set this property before using the Voice Capture DSP.</span></span> <span data-ttu-id="2f55d-125">Nachdem Sie diese Eigenschaft festgelegt haben, können Sie den DSP mit seinen Standardeinstellungen verwenden oder zusätzliche Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="2f55d-125">After you set this property, you can use the DSP with its default settings, or set additional properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f55d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f55d-126">Requirements</span></span>



| <span data-ttu-id="2f55d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f55d-127">Requirement</span></span> | <span data-ttu-id="2f55d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2f55d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f55d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f55d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f55d-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f55d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2f55d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f55d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f55d-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f55d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f55d-133">Header</span><span class="sxs-lookup"><span data-stu-id="2f55d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f55d-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f55d-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f55d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f55d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f55d-136">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f55d-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2f55d-137">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="2f55d-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
