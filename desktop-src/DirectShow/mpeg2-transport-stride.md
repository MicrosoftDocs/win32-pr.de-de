---
description: Die MPEG2 \_ \_ -Transport Stride-Struktur beschreibt das Format von MPEG-2-Transportstream-Paketen (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE-Struktur (bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359250"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="735db-103">MPEG2- \_ Transport- \_ Stride-Struktur</span><span class="sxs-lookup"><span data-stu-id="735db-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="735db-104">Die `MPEG2_TRANSPORT_STRIDE` -Struktur beschreibt das Format von MPEG-2-Transportdaten Strom-Paketen (TS).</span><span class="sxs-lookup"><span data-stu-id="735db-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="735db-105">Diese Struktur ermöglicht Transport Datenströme, bei denen die 188-Byte-Transport Pakete nicht zusammenhängend sind.</span><span class="sxs-lookup"><span data-stu-id="735db-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="735db-106">Im Rahmen dieser Dokumentation werden solche Pakete als *Stride-Pakete* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="735db-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="735db-107">Stride-Pakete werden durch den folgenden Medientyp identifiziert:</span><span class="sxs-lookup"><span data-stu-id="735db-107">Stride packets are identified by the following media type:</span></span>



|             |                                        |
|-------------|----------------------------------------|
| <span data-ttu-id="735db-108">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="735db-108">Major Type</span></span>  | <span data-ttu-id="735db-109">MediaType- \_ Stream</span><span class="sxs-lookup"><span data-stu-id="735db-109">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="735db-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="735db-110">Subtype</span></span>     | <span data-ttu-id="735db-111">Mediasubtype \_ MPEG2- \_ Transport \_ Stride</span><span class="sxs-lookup"><span data-stu-id="735db-111">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="735db-112">Formattyp</span><span class="sxs-lookup"><span data-stu-id="735db-112">Format Type</span></span> | <span data-ttu-id="735db-113">Nicht \_ formatieren</span><span class="sxs-lookup"><span data-stu-id="735db-113">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="735db-114">Der Format Block (**pbformat**) ist optional.</span><span class="sxs-lookup"><span data-stu-id="735db-114">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="735db-115">Wenn der Format Block eingeschlossen ist, muss er mit einer " **MPEG2- \_ Transport \_ Stride** "-Struktur beginnen.</span><span class="sxs-lookup"><span data-stu-id="735db-115">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="735db-116">Diese Struktur definiert das Layout des Transport Pakets innerhalb des STRIDE-Pakets.</span><span class="sxs-lookup"><span data-stu-id="735db-116">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="735db-117">Wenn der Format Block **null** ist, wird davon ausgegangen, dass die Pakete einen Satz von Standardwerten verwenden. Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="735db-117">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="735db-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="735db-118">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="735db-119">Member</span><span class="sxs-lookup"><span data-stu-id="735db-119">Members</span></span>

<dl> <dt>

<span data-ttu-id="735db-120">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="735db-120">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="735db-121">Gibt den Offset (in Bytes) vom Anfang des Pakets bis zum ersten Byte des eingebetteten Transport Pakets an.</span><span class="sxs-lookup"><span data-stu-id="735db-121">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="735db-122">Der Wert muss zwischen 0 (null) und `(dwStride - dwPacketLength)` einschließlich liegen.</span><span class="sxs-lookup"><span data-stu-id="735db-122">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="735db-123">**dwpacketlength**</span><span class="sxs-lookup"><span data-stu-id="735db-123">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="735db-124">Gibt die Länge des eingebetteten Transport Pakets in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="735db-124">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="735db-125">Bei Standard-MPEG-2-Transport Paketen muss der Wert 188 Bytes betragen.</span><span class="sxs-lookup"><span data-stu-id="735db-125">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="735db-126">**dwstride**</span><span class="sxs-lookup"><span data-stu-id="735db-126">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="735db-127">Gibt die Länge des gesamten Stride-Pakets in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="735db-127">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="735db-128">Der Wert muss mindestens lauten `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="735db-128">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="735db-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="735db-129">Remarks</span></span>

<span data-ttu-id="735db-130">Das folgende Diagramm veranschaulicht die Beziehungen zwischen den Strukturmembern.</span><span class="sxs-lookup"><span data-stu-id="735db-130">The following diagram illustrates the relations between the structure members.</span></span>

![MPEG-2-Stride-Paket](images/mpeg2-stride-packet.png)

<span data-ttu-id="735db-132">Eingabepuffer, die Multiplex Stride-Pakete enthalten, weisen einige Einschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="735db-132">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="735db-133">Stride-Pakete müssen zusammenhängend innerhalb des Puffers verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="735db-133">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="735db-134">Es können keine Bytes dem ersten Stride-Paket vorangestellt sein, oder Sie können dem letzten Stride-Paket folgen.</span><span class="sxs-lookup"><span data-stu-id="735db-134">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="735db-135">Eine ganzzahlige Anzahl von Stride-Paketen muss in den Puffer passen. Das heißt, die Pufferlänge% dwstride ist gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="735db-135">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="735db-136">Es gibt keine Einschränkung für die Anzahl von Stride-Paketen pro Puffer.</span><span class="sxs-lookup"><span data-stu-id="735db-136">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="735db-137">Wenn der Medientyp keinen Format Block enthält (**pbformat** ist **null**), werden die folgenden Standardwerte verwendet:</span><span class="sxs-lookup"><span data-stu-id="735db-137">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="735db-138">**dwOffset**: 0</span><span class="sxs-lookup"><span data-stu-id="735db-138">**dwOffset**: 0</span></span>
-   <span data-ttu-id="735db-139">**dwpacketlength**: 188</span><span class="sxs-lookup"><span data-stu-id="735db-139">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="735db-140">**dwstride**: 188</span><span class="sxs-lookup"><span data-stu-id="735db-140">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="735db-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="735db-141">Requirements</span></span>



| <span data-ttu-id="735db-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="735db-142">Requirement</span></span> | <span data-ttu-id="735db-143">Wert</span><span class="sxs-lookup"><span data-stu-id="735db-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="735db-144">Header</span><span class="sxs-lookup"><span data-stu-id="735db-144">Header</span></span><br/> | <dl> <span data-ttu-id="735db-145"><dt>Bdatypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="735db-145"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="735db-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="735db-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735db-147">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="735db-147">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="735db-148">MPEG-2-Medientypen</span><span class="sxs-lookup"><span data-stu-id="735db-148">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




