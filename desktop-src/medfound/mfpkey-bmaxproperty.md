---
description: Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch mfpkey Rmax) in Millisekunden an \_ .
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: MFPKEY_BMAX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351549"
---
# <a name="mfpkey_bmax-property"></a><span data-ttu-id="ef765-103">Mfpkey ( \_ bmax-Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ef765-103">MFPKEY\_BMAX Property</span></span>

<span data-ttu-id="ef765-104">Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch [mfpkey \_ Rmax](mfpkey-rmaxproperty.md)) in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="ef765-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by [MFPKEY\_RMAX](mfpkey-rmaxproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ef765-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ef765-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ef765-106">g \_ wszwmvcbmax</span><span class="sxs-lookup"><span data-stu-id="ef765-106">g\_wszWMVCBMax</span></span>

## <a name="data-type"></a><span data-ttu-id="ef765-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ef765-107">Data Type</span></span>

<span data-ttu-id="ef765-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ef765-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ef765-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="ef765-109">Default Value</span></span>

<span data-ttu-id="ef765-110">Keine Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="ef765-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef765-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef765-111">Remarks</span></span>

<span data-ttu-id="ef765-112">Sie müssen diesen Wert für die VBR-Codierung mit hoher Einschränkung festlegen.</span><span class="sxs-lookup"><span data-stu-id="ef765-112">You must set this value for peak-constrained VBR encoding.</span></span> <span data-ttu-id="ef765-113">Nachdem Sie mit dem Verarbeiten von Beispielen begonnen haben, müssen Sie diesen Wert erst Abfragen, wenn Sie mit dem Codieren des Streams fertig sind.</span><span class="sxs-lookup"><span data-stu-id="ef765-113">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="ef765-114">Der Codec interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungs Sitzung übersteigt. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="ef765-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef765-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef765-115">Requirements</span></span>



| <span data-ttu-id="ef765-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef765-116">Requirement</span></span> | <span data-ttu-id="ef765-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ef765-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef765-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef765-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ef765-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef765-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ef765-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef765-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ef765-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef765-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef765-122">Header</span><span class="sxs-lookup"><span data-stu-id="ef765-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef765-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef765-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef765-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef765-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef765-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ef765-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




