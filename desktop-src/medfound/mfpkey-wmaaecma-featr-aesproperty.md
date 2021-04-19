---
description: Gibt an, wie oft der sprach Erfassungs-DSP für das restliche Signal eine akustische Echo Unterdrückung (AES) ausführt.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: MFPKEY_WMAAECMA_FEATR_AES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353177"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a><span data-ttu-id="d6c5b-103">Mfpkey \_ wmaaecma \_ featr \_ AES-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d6c5b-103">MFPKEY\_WMAAECMA\_FEATR\_AES Property</span></span>

<span data-ttu-id="d6c5b-104">Gibt an, wie oft der sprach Erfassungs-DSP für das restliche Signal eine akustische Echo Unterdrückung (AES) ausführt.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-104">Specifies how many times the Voice Capture DSP performs acoustic echo suppression (AES) on the residual signal.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d6c5b-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d6c5b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d6c5b-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d6c5b-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d6c5b-107">Data Type</span></span>

<span data-ttu-id="d6c5b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d6c5b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d6c5b-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="d6c5b-109">Default Value</span></span>

<span data-ttu-id="d6c5b-110">0</span><span class="sxs-lookup"><span data-stu-id="d6c5b-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="d6c5b-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="d6c5b-111">Applies To</span></span>

-   [<span data-ttu-id="d6c5b-112">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="d6c5b-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="d6c5b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6c5b-113">Remarks</span></span>

<span data-ttu-id="d6c5b-114">Der sprach Erfassungs-DSP kann AES für das restliche Signal nach einem Echo Abbruch ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-114">The Voice Capture DSP can perform AES on the residual signal after echo cancellation.</span></span> <span data-ttu-id="d6c5b-115">Diese Eigenschaft kann den Wert 0, 1 oder 2 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-115">This property can have the value 0, 1, or 2.</span></span> <span data-ttu-id="d6c5b-116">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-116">The default value is 0.</span></span> <span data-ttu-id="d6c5b-117">Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-117">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="d6c5b-118">Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-118">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c5b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6c5b-119">Requirements</span></span>



| <span data-ttu-id="d6c5b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6c5b-120">Requirement</span></span> | <span data-ttu-id="d6c5b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d6c5b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c5b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6c5b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c5b-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6c5b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d6c5b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6c5b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c5b-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6c5b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6c5b-126">Header</span><span class="sxs-lookup"><span data-stu-id="d6c5b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c5b-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c5b-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6c5b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6c5b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c5b-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6c5b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d6c5b-130">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="d6c5b-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
