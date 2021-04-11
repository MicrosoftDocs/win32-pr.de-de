---
description: Gibt Slice-Steuerungsdaten an.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: DXVA_Slice_HEVC_Short-Struktur (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041551"
---
# <a name="dxva_slice_hevc_short-structure"></a><span data-ttu-id="41c62-103">DXVA- \_ Slice- \_ hevc- \_ kurzstruktur</span><span class="sxs-lookup"><span data-stu-id="41c62-103">DXVA\_Slice\_HEVC\_Short structure</span></span>

<span data-ttu-id="41c62-104">Gibt Slice-Steuerungsdaten an.</span><span class="sxs-lookup"><span data-stu-id="41c62-104">Specifies slice control data.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c62-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41c62-105">Syntax</span></span>


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a><span data-ttu-id="41c62-106">Member</span><span class="sxs-lookup"><span data-stu-id="41c62-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41c62-107">**Bsnalunitdataloation**</span><span class="sxs-lookup"><span data-stu-id="41c62-107">**BSNALunitDataLocation**</span></span>
</dt> <dd>

<span data-ttu-id="41c62-108">Gibt den Speicherort der NAL-Einheit an.</span><span class="sxs-lookup"><span data-stu-id="41c62-108">Specifies the location of the NAL unit.</span></span>

</dd> <dt>

<span data-ttu-id="41c62-109">**Slicebytesinbuffer**</span><span class="sxs-lookup"><span data-stu-id="41c62-109">**SliceBytesInBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="41c62-110">Die Anzahl der Bytes im Bitstrom-Datenpuffer, die dieser Slice-Steuerelement Datenstruktur zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="41c62-110">The number of bytes in the bitstream data buffer that are associated with this slice control data structure.</span></span>

</dd> <dt>

<span data-ttu-id="41c62-111">**wbadslicechopping**</span><span class="sxs-lookup"><span data-stu-id="41c62-111">**wBadSliceChopping**</span></span>
</dt> <dd>

<span data-ttu-id="41c62-112">Wenn eine Off-Host-Bitstrom-Verarbeitung verwendet wird, gibt dieser Wert das ungültige Slice-Segment an und enthält einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="41c62-112">If off-host bitstream parsing is used, this value indicates the bad slice chopping and contains one of the following values:</span></span>



| <span data-ttu-id="41c62-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41c62-113">Requirement</span></span> | <span data-ttu-id="41c62-114">Wert</span><span class="sxs-lookup"><span data-stu-id="41c62-114">Value</span></span> |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c62-115">Wert</span><span class="sxs-lookup"><span data-stu-id="41c62-115">Value</span></span> | <span data-ttu-id="41c62-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41c62-116">Description</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="41c62-117">0</span><span class="sxs-lookup"><span data-stu-id="41c62-117">0</span></span>     | <span data-ttu-id="41c62-118">Alle Bits für den Slice befinden sich innerhalb des entsprechenden Bitstrom-Daten Puffers.</span><span class="sxs-lookup"><span data-stu-id="41c62-118">All bits for the slice are located within the corresponding bitstream data buffer.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="41c62-119">1</span><span class="sxs-lookup"><span data-stu-id="41c62-119">1</span></span>     | <span data-ttu-id="41c62-120">Der Bitstrom-Datenpuffer enthält den Anfang des Slice, jedoch nicht den gesamten Slice, da der Puffer voll ist.</span><span class="sxs-lookup"><span data-stu-id="41c62-120">The bitstream data buffer contains the start of the slice, but not the entire slice, because the buffer is full.</span></span>                                                                                                                                        |
| <span data-ttu-id="41c62-121">2</span><span class="sxs-lookup"><span data-stu-id="41c62-121">2</span></span>     | <span data-ttu-id="41c62-122">Der Bitstrom-Datenpuffer enthält das Ende des Slice.</span><span class="sxs-lookup"><span data-stu-id="41c62-122">The bitstream data buffer contains the end of the slice.</span></span> <span data-ttu-id="41c62-123">Der Start des Slice ist nicht enthalten, da sich der Start des Slice im vorherigen Bitstrom-Datenpuffer befand.</span><span class="sxs-lookup"><span data-stu-id="41c62-123">It does not contain the start of the slice, because the start of the slice was located in the previous bitstream data buffer.</span></span>                                                                  |
| <span data-ttu-id="41c62-124">3</span><span class="sxs-lookup"><span data-stu-id="41c62-124">3</span></span>     | <span data-ttu-id="41c62-125">Der Bitstrom-Datenpuffer enthält den Anfang des Slice nicht, da sich der Start des Slice im vorherigen Bitstrom-Datenpuffer befunden hat und das Ende des Slice nicht enthält, da der aktuelle Bitstrom-Datenpuffer ebenfalls voll ist.</span><span class="sxs-lookup"><span data-stu-id="41c62-125">The bitstream data buffer does not contain the start of the slice because the start of the slice was located in the previous bitstream data buffer and it does not contain the end of the slice becuase the current bitstream data buffer is also full.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41c62-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41c62-126">Remarks</span></span>

<span data-ttu-id="41c62-127">**DXVA \_ Slice \_ hevc \_ Short** enthält Slice-Steuerungsdaten, die vom Host Software Decoder an den Hardwarebeschleuniger übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="41c62-127">**DXVA\_Slice\_HEVC\_Short** contains slice control data which is passed to the hardware accelerator from the host software decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c62-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41c62-128">Requirements</span></span>



| <span data-ttu-id="41c62-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41c62-129">Requirement</span></span> | <span data-ttu-id="41c62-130">Wert</span><span class="sxs-lookup"><span data-stu-id="41c62-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="41c62-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41c62-131">Minimum supported client</span></span><br/> | <span data-ttu-id="41c62-132">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="41c62-132">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="41c62-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41c62-133">Minimum supported server</span></span><br/> | <span data-ttu-id="41c62-134">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41c62-134">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="41c62-135">Header</span><span class="sxs-lookup"><span data-stu-id="41c62-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c62-136"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c62-136"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c62-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41c62-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c62-138">Media Foundation Strukturen</span><span class="sxs-lookup"><span data-stu-id="41c62-138">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




