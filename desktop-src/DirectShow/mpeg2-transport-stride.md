---
description: Die MPEG2 \_ TRANSPORT \_ STRIDE-Struktur beschreibt das Format von MPEG-2-Transportstreampaketen (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE -Struktur (Bdatypes.h)
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
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908488"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="eeac9-103">\_ \_ MPEG2-TRANSPORT-STRIDE-Struktur</span><span class="sxs-lookup"><span data-stu-id="eeac9-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="eeac9-104">Die `MPEG2_TRANSPORT_STRIDE` -Struktur beschreibt das Format von MPEG-2-Transportstreampaketen (TS).</span><span class="sxs-lookup"><span data-stu-id="eeac9-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="eeac9-105">Diese Struktur ermöglicht Transportstreams, bei denen die 188-Byte-Transportpakete nicht zusammenhängend sind.</span><span class="sxs-lookup"><span data-stu-id="eeac9-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="eeac9-106">Im Sinne dieser Dokumentation werden solche Pakete als *Stride-Pakete bezeichnet.*</span><span class="sxs-lookup"><span data-stu-id="eeac9-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="eeac9-107">Stride-Pakete werden durch den folgenden Medientyp identifiziert:</span><span class="sxs-lookup"><span data-stu-id="eeac9-107">Stride packets are identified by the following media type:</span></span>



| <span data-ttu-id="eeac9-108">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="eeac9-108">Label</span></span> | <span data-ttu-id="eeac9-109">Wert</span><span class="sxs-lookup"><span data-stu-id="eeac9-109">Value</span></span> |
|-------------|----------------------------------------|
| <span data-ttu-id="eeac9-110">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="eeac9-110">Major Type</span></span>  | <span data-ttu-id="eeac9-111">\_MEDIATYPE-Stream</span><span class="sxs-lookup"><span data-stu-id="eeac9-111">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="eeac9-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="eeac9-112">Subtype</span></span>     | <span data-ttu-id="eeac9-113">MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT-STRIDE \_</span><span class="sxs-lookup"><span data-stu-id="eeac9-113">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="eeac9-114">Formattyp</span><span class="sxs-lookup"><span data-stu-id="eeac9-114">Format Type</span></span> | <span data-ttu-id="eeac9-115">FORMAT \_ None</span><span class="sxs-lookup"><span data-stu-id="eeac9-115">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="eeac9-116">Der Formatblock (**pbFormat**) ist optional.</span><span class="sxs-lookup"><span data-stu-id="eeac9-116">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="eeac9-117">Wenn der Formatblock enthalten ist, muss er mit einer **MPEG2 \_ \_ TRANSPORT-STRIDE-Struktur** beginnen.</span><span class="sxs-lookup"><span data-stu-id="eeac9-117">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="eeac9-118">Diese Struktur definiert das Layout des Transportpakets innerhalb des Stride-Pakets.</span><span class="sxs-lookup"><span data-stu-id="eeac9-118">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="eeac9-119">Wenn der Formatblock NULL **ist,** wird davon ausgegangen, dass die Pakete einen Satz von Standardwerten verwenden. Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="eeac9-119">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeac9-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeac9-120">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="eeac9-121">Member</span><span class="sxs-lookup"><span data-stu-id="eeac9-121">Members</span></span>

<dl> <dt>

<span data-ttu-id="eeac9-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="eeac9-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="eeac9-123">Gibt den Offset vom Anfang des Pakets bis zum ersten Byte des eingebetteten Transportpakets in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="eeac9-123">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="eeac9-124">Der Wert muss von 0 (null) bis `(dwStride - dwPacketLength)` einschließlich liegen.</span><span class="sxs-lookup"><span data-stu-id="eeac9-124">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="eeac9-125">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="eeac9-125">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="eeac9-126">Gibt die Länge des eingebetteten Transportpakets in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="eeac9-126">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="eeac9-127">Für MPEG-2-Standardtransportpakete muss der Wert 188 Bytes betragen.</span><span class="sxs-lookup"><span data-stu-id="eeac9-127">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="eeac9-128">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="eeac9-128">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="eeac9-129">Gibt die Länge des gesamten Schrittpakets in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="eeac9-129">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="eeac9-130">Der Wert muss mindestens `(dwOffset + dwPacketLength)` sein.</span><span class="sxs-lookup"><span data-stu-id="eeac9-130">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eeac9-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eeac9-131">Remarks</span></span>

<span data-ttu-id="eeac9-132">Das folgende Diagramm veranschaulicht die Beziehungen zwischen den Strukturmembern.</span><span class="sxs-lookup"><span data-stu-id="eeac9-132">The following diagram illustrates the relations between the structure members.</span></span>

![mpeg-2 stride packet](images/mpeg2-stride-packet.png)

<span data-ttu-id="eeac9-134">Für Eingabepuffer, die Multiplexpakete enthalten, gelten einige Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="eeac9-134">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="eeac9-135">Schrittpakete müssen zusammenhängend innerhalb des Puffers gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="eeac9-135">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="eeac9-136">Dem ersten Schrittpaket dürfen keine Bytes vorangestellt oder dem letzten Schrittpaket folgen.</span><span class="sxs-lookup"><span data-stu-id="eeac9-136">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="eeac9-137">Eine ganzzahligen Anzahl von Schrittpaketen muss in den Puffer passen. Das bedeutet, dass die Pufferlänge % dwStride gleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="eeac9-137">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="eeac9-138">Es gibt keine Einschränkung hinsichtlich der Anzahl von Schrittpaketen pro Puffer.</span><span class="sxs-lookup"><span data-stu-id="eeac9-138">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="eeac9-139">Wenn der Medientyp keinen Formatblock enthält (**pbFormat** ist **NULL),** werden die folgenden Standardwerte verwendet:</span><span class="sxs-lookup"><span data-stu-id="eeac9-139">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="eeac9-140">**dwOffset:** 0</span><span class="sxs-lookup"><span data-stu-id="eeac9-140">**dwOffset**: 0</span></span>
-   <span data-ttu-id="eeac9-141">**dwPacketLength**: 188</span><span class="sxs-lookup"><span data-stu-id="eeac9-141">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="eeac9-142">**dwStride**: 188</span><span class="sxs-lookup"><span data-stu-id="eeac9-142">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="eeac9-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eeac9-143">Requirements</span></span>



| <span data-ttu-id="eeac9-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eeac9-144">Requirement</span></span> | <span data-ttu-id="eeac9-145">Wert</span><span class="sxs-lookup"><span data-stu-id="eeac9-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eeac9-146">Header</span><span class="sxs-lookup"><span data-stu-id="eeac9-146">Header</span></span><br/> | <dl> <span data-ttu-id="eeac9-147"><dt>Bdatypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="eeac9-147"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeac9-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eeac9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeac9-149">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="eeac9-149">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="eeac9-150">MPEG-2-Medientypen</span><span class="sxs-lookup"><span data-stu-id="eeac9-150">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




