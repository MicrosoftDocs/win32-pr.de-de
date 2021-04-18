---
description: Gibt die gewünschte maximale Volumeebene der Ausgabe Audioinhalte an.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: MFPKEY_WMADRC_PEAKTARGET-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345267"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a><span data-ttu-id="e3852-103">Mfpkey \_ wmadrc- \_ Eigenschaft "Peer Ziel"</span><span class="sxs-lookup"><span data-stu-id="e3852-103">MFPKEY\_WMADRC\_PEAKTARGET Property</span></span>

<span data-ttu-id="e3852-104">Gibt die gewünschte maximale Volumeebene der Ausgabe Audioinhalte an.</span><span class="sxs-lookup"><span data-stu-id="e3852-104">Specifies the desired maximum volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e3852-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e3852-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e3852-106">g \_ wszwmadrcpeer Target</span><span class="sxs-lookup"><span data-stu-id="e3852-106">g\_wszWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="e3852-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e3852-107">Data Type</span></span>

<span data-ttu-id="e3852-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e3852-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e3852-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="e3852-109">Default Value</span></span>

<span data-ttu-id="e3852-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e3852-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3852-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3852-111">Remarks</span></span>

<span data-ttu-id="e3852-112">Sie können diesen Wert für den Decoder für das dynamische Bereichs Steuerelement festlegen, aber er wirkt sich nur dann aus, wenn die Eigenschaft [mfpkey \_ wmadec \_ drcmode](mfpkey-wmadec-drcmodeproperty.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e3852-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="e3852-113">Wenn Sie das dynamische Bereichs Steuerelement vom Decoder anfordern, wenn diese Eigenschaft nicht festgelegt ist, berechnet der Codec einen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="e3852-113">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="e3852-114">Verwenden Sie die Eigenschaften [mfpkey \_ wmadrc \_ avgref](mfpkey-wmadrc-avgrefproperty.md) und [mfpkey \_ wmadrc \_ ](mfpkey-wmadrc-peakrefproperty.md) -Eigenschaft, um die entsprechenden Werte für diese Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e3852-114">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

<span data-ttu-id="e3852-115">Weitere Informationen zur Steuerung des dynamischen Bereichs finden Sie im Webartikel [Windows Media Audio Professional-Codec-Features](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="e3852-115">For more information on dynamic range control, see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3852-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3852-116">Requirements</span></span>



| <span data-ttu-id="e3852-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3852-117">Requirement</span></span> | <span data-ttu-id="e3852-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e3852-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3852-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3852-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3852-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3852-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e3852-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3852-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3852-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3852-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3852-123">Header</span><span class="sxs-lookup"><span data-stu-id="e3852-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3852-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3852-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3852-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3852-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3852-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3852-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
