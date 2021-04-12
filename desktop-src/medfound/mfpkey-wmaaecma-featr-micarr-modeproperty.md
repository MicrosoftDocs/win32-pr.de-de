---
description: Gibt an, wie der sprach Aufzeichnungs-DSP die Verarbeitung von mikrofonarrays ausführt.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: MFPKEY_WMAAECMA_FEATR_MICARR_MODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215047"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a><span data-ttu-id="ce600-103">Eigenschaft "mfpkey \_ wmaaecma \_ featr \_ micarr \_ Mode"</span><span class="sxs-lookup"><span data-stu-id="ce600-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property</span></span>

<span data-ttu-id="ce600-104">Gibt an, wie der sprach Aufzeichnungs-DSP die Verarbeitung von mikrofonarrays ausführt.</span><span class="sxs-lookup"><span data-stu-id="ce600-104">Specifies how the Voice Capture DSP performs microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ce600-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ce600-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ce600-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce600-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ce600-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ce600-107">Data Type</span></span>

<span data-ttu-id="ce600-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ce600-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ce600-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="ce600-109">Default Value</span></span>

<span data-ttu-id="ce600-110">micarray- \_ einzelner \_ Strahl</span><span class="sxs-lookup"><span data-stu-id="ce600-110">MICARRAY\_SINGLE\_BEAM</span></span>

## <a name="applies-to"></a><span data-ttu-id="ce600-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="ce600-111">Applies To</span></span>

-   [<span data-ttu-id="ce600-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="ce600-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="ce600-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce600-113">Remarks</span></span>

<span data-ttu-id="ce600-114">Der Wert dieser Eigenschaft ist ein Member der [MIC \_ array \_ Mode](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="ce600-114">The value of this property is a member of the [MIC\_ARRAY\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) enumeration.</span></span> <span data-ttu-id="ce600-115">Der Standardwert ist micarray \_ Single \_ Beam.</span><span class="sxs-lookup"><span data-stu-id="ce600-115">The default value is MICARRAY\_SINGLE\_BEAM.</span></span> <span data-ttu-id="ce600-116">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce600-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="ce600-117">Der DSP verwendet diese Eigenschaft nur, wenn die Verarbeitung von mikrofonarrays aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ce600-117">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce600-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce600-118">Requirements</span></span>



| <span data-ttu-id="ce600-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce600-119">Requirement</span></span> | <span data-ttu-id="ce600-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ce600-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce600-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce600-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce600-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce600-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ce600-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce600-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce600-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce600-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce600-125">Header</span><span class="sxs-lookup"><span data-stu-id="ce600-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce600-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce600-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce600-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce600-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce600-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce600-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ce600-129">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="ce600-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
