---
description: Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-, Variable-Bit-Rate (VBR)-Codierung verwendet wird.
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: MFPKEY_RAVG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367867"
---
# <a name="mfpkey_ravg-property"></a><span data-ttu-id="e8569-103">Mfpkey \_ Ravg (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e8569-103">MFPKEY\_RAVG Property</span></span>

<span data-ttu-id="e8569-104">Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-, Variable-Bit-Rate (VBR)-Codierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8569-104">Specifies the average bit rate, in bits per second, used for 2-pass, variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e8569-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e8569-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e8569-106">g \_ wszwmvcavgbitrate</span><span class="sxs-lookup"><span data-stu-id="e8569-106">g\_wszWMVCAvgBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="e8569-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e8569-107">Data Type</span></span>

<span data-ttu-id="e8569-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e8569-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="e8569-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8569-109">Remarks</span></span>

<span data-ttu-id="e8569-110">In eingeschränkter und uneingeschränkter VBR ist dieser Wert die durchschnittliche Bitrate während der gesamten Dauer des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="e8569-110">In both constrained and unconstrained VBR, this value is the average bit rate across the duration of the content.</span></span>

<span data-ttu-id="e8569-111">Sie müssen diesen Wert für beide Modi der zweistufigen VBR-Codierung festlegen.</span><span class="sxs-lookup"><span data-stu-id="e8569-111">You must set this value for both modes of two-pass VBR encoding.</span></span> <span data-ttu-id="e8569-112">Nachdem Sie mit dem Verarbeiten von Beispielen begonnen haben, müssen Sie diesen Wert erst Abfragen, wenn Sie mit dem Codieren des Streams fertig sind.</span><span class="sxs-lookup"><span data-stu-id="e8569-112">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="e8569-113">Der Encoder interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungs Sitzung übersteigt. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="e8569-113">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="e8569-114">Diese Eigenschaft kann auch am Ende einer 1-Pass-VBR-Codierungs Sitzung gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="e8569-114">This property can also be read at the end of a 1-pass VBR encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8569-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8569-115">Requirements</span></span>



| <span data-ttu-id="e8569-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8569-116">Requirement</span></span> | <span data-ttu-id="e8569-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e8569-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8569-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8569-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e8569-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8569-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e8569-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8569-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e8569-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8569-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8569-122">Header</span><span class="sxs-lookup"><span data-stu-id="e8569-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8569-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8569-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8569-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8569-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8569-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8569-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




