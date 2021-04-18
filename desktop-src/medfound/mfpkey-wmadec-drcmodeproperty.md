---
description: Gibt den dynamischen Bereichs Steuerungs Modus an, den der Audiodecoder verwendet.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: MFPKEY_WMADEC_DRCMODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215045"
---
# <a name="mfpkey_wmadec_drcmode-property"></a><span data-ttu-id="a7683-103">Mfpkey \_ wmadec \_ drcmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a7683-103">MFPKEY\_WMADEC\_DRCMODE Property</span></span>

<span data-ttu-id="a7683-104">Gibt den dynamischen Bereichs Steuerungs Modus an, den der Audiodecoder verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7683-104">Specifies the dynamic range control mode that the audio decoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a7683-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a7683-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a7683-106">g \_ wszwmacdrcsetting</span><span class="sxs-lookup"><span data-stu-id="a7683-106">g\_wszWMACDRCSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="a7683-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a7683-107">Data Type</span></span>

<span data-ttu-id="a7683-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a7683-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a7683-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="a7683-109">Default Value</span></span>

<span data-ttu-id="a7683-110">0</span><span class="sxs-lookup"><span data-stu-id="a7683-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="a7683-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7683-111">Remarks</span></span>

<span data-ttu-id="a7683-112">Dieser ganzzahlige Wert liegt zwischen 0 und 2.</span><span class="sxs-lookup"><span data-stu-id="a7683-112">This integer value ranges from 0 to 2.</span></span> <span data-ttu-id="a7683-113">Umso größer der Wert, desto kleiner der dynamische Bereich der nicht komprimierten Audioausgabe.</span><span class="sxs-lookup"><span data-stu-id="a7683-113">The greater the value, the smaller the dynamic range of the uncompressed audio output.</span></span> <span data-ttu-id="a7683-114">Der Wert 0 signalisiert dem Codec, dass kein dynamisches Bereichs Steuerelement durchgeführt werden soll, d. h., der Codec ändert nicht den inhärenten dynamischen Bereich des codierten Inhalts.</span><span class="sxs-lookup"><span data-stu-id="a7683-114">A value of 0 signals the codec to perform no dynamic range control, that is, the codec will not alter the inherent dynamic range of the encoded content.</span></span>

<span data-ttu-id="a7683-115">Wenn dieser Wert auf 1 oder 2 festgelegt ist, verwendet der Codec die folgenden Eigenschaften, um das erforderliche dynamische Bereichs Steuerelement zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="a7683-115">If this value is set to 1 or 2, the codec will use the following properties to determine the needed dynamic range control:</span></span>

-   [<span data-ttu-id="a7683-116">mfpkey \_ wmadrc \_ avgref</span><span class="sxs-lookup"><span data-stu-id="a7683-116">MFPKEY\_WMADRC\_AVGREF</span></span>](mfpkey-wmadrc-avgrefproperty.md)
-   [<span data-ttu-id="a7683-117">mfpkey \_ wmadrc- \_ Peer-Ref</span><span class="sxs-lookup"><span data-stu-id="a7683-117">MFPKEY\_WMADRC\_PEAKREF</span></span>](mfpkey-wmadrc-peakrefproperty.md)
-   [<span data-ttu-id="a7683-118">mfpkey \_ wmademokratische \_ avgtarget</span><span class="sxs-lookup"><span data-stu-id="a7683-118">MFPKEY\_WMADRC\_AVGTARGET</span></span>](mfpkey-wmadrc-avgtargetproperty.md)
-   [<span data-ttu-id="a7683-119">mfpkey \_ wmadrc- \_ Peer Ziel</span><span class="sxs-lookup"><span data-stu-id="a7683-119">MFPKEY\_WMADRC\_PEAKTARGET</span></span>](mfpkey-wmadrc-peaktargetproperty.md)

<span data-ttu-id="a7683-120">Wenn Sie keine Zielwerte angeben, stellt der Codec seinen eigenen bereit.</span><span class="sxs-lookup"><span data-stu-id="a7683-120">If you do not provide target values, the codec will provide its own.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7683-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7683-121">Requirements</span></span>



| <span data-ttu-id="a7683-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7683-122">Requirement</span></span> | <span data-ttu-id="a7683-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a7683-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7683-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7683-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a7683-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7683-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a7683-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7683-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a7683-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7683-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7683-128">Header</span><span class="sxs-lookup"><span data-stu-id="a7683-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7683-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7683-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7683-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7683-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7683-131">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7683-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




