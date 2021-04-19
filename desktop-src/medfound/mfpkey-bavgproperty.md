---
description: Gibt das Puffer Fenster (in Millisekunden) eines eingeschränkten VBR-Streams (Variable-Bitrate) mit der durchschnittlichen Bitrate an (angegeben durch mfpkey \_ Ravg).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: MFPKEY_BAVG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349390"
---
# <a name="mfpkey_bavg-property"></a><span data-ttu-id="03525-103">Mfpkey- \_ bavg (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="03525-103">MFPKEY\_BAVG Property</span></span>

<span data-ttu-id="03525-104">Gibt das Puffer Fenster (in Millisekunden) eines eingeschränkten VBR-Streams (Variable-Bitrate) mit der durchschnittlichen Bitrate an (angegeben durch [mfpkey \_ Ravg](mfpkey-ravgproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="03525-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by [MFPKEY\_RAVG](mfpkey-ravgproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="03525-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="03525-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="03525-106">g \_ wszwmvcbavg</span><span class="sxs-lookup"><span data-stu-id="03525-106">g\_wszWMVCBAvg</span></span>

## <a name="data-type"></a><span data-ttu-id="03525-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="03525-107">Data Type</span></span>

<span data-ttu-id="03525-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="03525-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="03525-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="03525-109">Default Value</span></span>

<span data-ttu-id="03525-110">Kein Standardwert, aber der Codec berechnet einen entsprechenden Wert auf der Grundlage der anderen eingeschränkten VBR-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="03525-110">No default value, but the codec will compute an appropriate value based on the other constrained VBR settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="03525-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03525-111">Remarks</span></span>

<span data-ttu-id="03525-112">Dieser Wert wird nach dem letzten Codierungs Durchlauf durch den Codec berechnet.</span><span class="sxs-lookup"><span data-stu-id="03525-112">This value is computed by the codec after the final encoding pass.</span></span> <span data-ttu-id="03525-113">Sie sollten diesen Wert erst Abfragen, wenn die Codierung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="03525-113">You should not query for this value until after encoding is complete.</span></span> <span data-ttu-id="03525-114">Der Codec interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungs Sitzung übersteigt. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="03525-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="03525-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03525-115">Requirements</span></span>



| <span data-ttu-id="03525-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03525-116">Requirement</span></span> | <span data-ttu-id="03525-117">Wert</span><span class="sxs-lookup"><span data-stu-id="03525-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03525-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03525-118">Minimum supported client</span></span><br/> | <span data-ttu-id="03525-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03525-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="03525-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03525-120">Minimum supported server</span></span><br/> | <span data-ttu-id="03525-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03525-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03525-122">Header</span><span class="sxs-lookup"><span data-stu-id="03525-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="03525-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03525-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03525-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03525-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03525-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03525-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




