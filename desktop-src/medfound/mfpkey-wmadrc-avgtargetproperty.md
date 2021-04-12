---
description: Gibt die gewünschte durchschnittliche Volumeebene der Ausgabe Audioinhalte an.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: MFPKEY_WMADRC_AVGTARGET-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215422"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a><span data-ttu-id="6a486-103">Avgtarget-Eigenschaft für mfpkey \_ wmadrc \_</span><span class="sxs-lookup"><span data-stu-id="6a486-103">MFPKEY\_WMADRC\_AVGTARGET Property</span></span>

<span data-ttu-id="6a486-104">Gibt die gewünschte durchschnittliche Volumeebene der Ausgabe Audioinhalte an.</span><span class="sxs-lookup"><span data-stu-id="6a486-104">Specifies the desired average volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="6a486-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="6a486-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="6a486-106">g \_ wszwmadrcaveragetarget</span><span class="sxs-lookup"><span data-stu-id="6a486-106">g\_wszWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="6a486-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6a486-107">Data Type</span></span>

<span data-ttu-id="6a486-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6a486-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="6a486-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="6a486-109">Default Value</span></span>

<span data-ttu-id="6a486-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6a486-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a486-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a486-111">Remarks</span></span>

<span data-ttu-id="6a486-112">Sie können diesen Wert für den Decoder für das dynamische Bereichs Steuerelement festlegen, aber er wirkt sich nur dann aus, wenn die Eigenschaft [mfpkey \_ wmadec \_ drcmode](mfpkey-wmadec-drcmodeproperty.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6a486-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

> [!Note]  
> <span data-ttu-id="6a486-113">Es wird nicht empfohlen, den durchschnittlichen Zielwert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6a486-113">Setting the average target value is not recommended.</span></span> <span data-ttu-id="6a486-114">Die Anpassung des durchschnittlichen Werts wirkt sich nicht auf den Unterschied zwischen lautstarkem und weichem Sound aus.</span><span class="sxs-lookup"><span data-stu-id="6a486-114">Adjusting the average value does not affect the difference between loud and soft sounds.</span></span> <span data-ttu-id="6a486-115">Stattdessen wird das gesamte durchschnittliche Volume, das während der Wiedergabe unerwünschte Verzerrung verursachen kann, reduziert oder erhöht.</span><span class="sxs-lookup"><span data-stu-id="6a486-115">Instead, it cuts or boosts the overall average volume which may cause undesirable distortion during playback.</span></span>

 

<span data-ttu-id="6a486-116">Wenn Sie das dynamische Bereichs Steuerelement vom Decoder anfordern, wenn diese Eigenschaft nicht festgelegt ist, berechnet der Codec einen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="6a486-116">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="6a486-117">Verwenden Sie die Eigenschaften [mfpkey \_ wmadrc \_ avgref](mfpkey-wmadrc-avgrefproperty.md) und [mfpkey \_ wmadrc \_ ](mfpkey-wmadrc-peakrefproperty.md) -Eigenschaft, um die entsprechenden Werte für diese Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6a486-117">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a486-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a486-118">Requirements</span></span>



| <span data-ttu-id="6a486-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a486-119">Requirement</span></span> | <span data-ttu-id="6a486-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6a486-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a486-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a486-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a486-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a486-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6a486-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a486-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a486-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a486-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a486-125">Header</span><span class="sxs-lookup"><span data-stu-id="6a486-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a486-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a486-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a486-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a486-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a486-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a486-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




