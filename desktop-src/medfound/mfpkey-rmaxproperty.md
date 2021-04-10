---
description: Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Wiedergabe verwendet wird.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215483"
---
# <a name="mfpkey_rmax-property"></a><span data-ttu-id="5174d-103">Mfpkey- \_ Rmax-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5174d-103">MFPKEY\_RMAX Property</span></span>

<span data-ttu-id="5174d-104">Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Wiedergabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5174d-104">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) playback.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5174d-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5174d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5174d-106">g \_ wszwmvcmaxbitrate</span><span class="sxs-lookup"><span data-stu-id="5174d-106">g\_wszWMVCMaxBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="5174d-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5174d-107">Data Type</span></span>

<span data-ttu-id="5174d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5174d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5174d-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="5174d-109">Default Value</span></span>

<span data-ttu-id="5174d-110">Keine Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="5174d-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="5174d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5174d-111">Remarks</span></span>

<span data-ttu-id="5174d-112">Dieser Wert stellt die Spitzen Bitrate für die Wiedergabe dar.</span><span class="sxs-lookup"><span data-stu-id="5174d-112">This value represents the peak bit rate for playback.</span></span> <span data-ttu-id="5174d-113">Der Wert von [mfpkey \_ bmax](mfpkey-bmaxproperty.md) wird verwendet, um den Puffer in Bezug auf diese Bitrate zu beschreiben. der eingeschränkte VBR ähnelt der konstanten Bitrate (CBR) und verwendet diesen Wert als Bitrate.</span><span class="sxs-lookup"><span data-stu-id="5174d-113">The value of [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is used to describe the buffer in terms of this bit rate; in effect, constrained VBR is similar to constant bit rate (CBR) using this value as the bit rate.</span></span> <span data-ttu-id="5174d-114">Ein eingeschränkter VBR-Datenstrom kann jedoch mit einer niedrigeren Bitrate wiedergegeben werden, solange der Puffer erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="5174d-114">However, a constrained VBR stream can be played back at a lower bit rate, as long as the buffer is increased.</span></span>

<span data-ttu-id="5174d-115">Sie müssen diesen Wert für die mit hoher Last beschränkte VBR-Codierung mit zwei bestanden festlegen.</span><span class="sxs-lookup"><span data-stu-id="5174d-115">You must set this value for peak-constrained two-pass VBR encoding.</span></span> <span data-ttu-id="5174d-116">Nachdem Sie mit dem Verarbeiten von Beispielen begonnen haben, müssen Sie diesen Wert erst Abfragen, wenn Sie mit dem Codieren des Streams fertig sind.</span><span class="sxs-lookup"><span data-stu-id="5174d-116">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="5174d-117">Der Encoder interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungs Sitzung übersteigt. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="5174d-117">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="5174d-118">In der Regel ist dieser Wert zwei bis dreimal größer als der Wert von [mfpkey \_ Ravg](mfpkey-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="5174d-118">Typically, this value is two to three times greater than the value of [MFPKEY\_RAVG](mfpkey-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5174d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5174d-119">Requirements</span></span>



| <span data-ttu-id="5174d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5174d-120">Requirement</span></span> | <span data-ttu-id="5174d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5174d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5174d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5174d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5174d-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5174d-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5174d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5174d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5174d-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5174d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5174d-126">Header</span><span class="sxs-lookup"><span data-stu-id="5174d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5174d-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5174d-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5174d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5174d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5174d-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5174d-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




