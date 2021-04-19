---
description: Die PID \_ -Karten Struktur enthält den Inhalt einer MPEG-2-Transportdaten Strom-Paket-ID.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: PID_MAP-Struktur (bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361679"
---
# <a name="pid_map-structure"></a><span data-ttu-id="03720-103">PID- \_ Karten Struktur</span><span class="sxs-lookup"><span data-stu-id="03720-103">PID\_MAP structure</span></span>

<span data-ttu-id="03720-104">Die- `PID_MAP` Struktur enthält den Inhalt einer MPEG-2-Transportdaten Strom-Paket-ID.</span><span class="sxs-lookup"><span data-stu-id="03720-104">The `PID_MAP` structure contains identifies the contents of an MPEG-2 transport stream packet ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="03720-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03720-105">Syntax</span></span>


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a><span data-ttu-id="03720-106">Member</span><span class="sxs-lookup"><span data-stu-id="03720-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="03720-107">**ulpid**</span><span class="sxs-lookup"><span data-stu-id="03720-107">**ulPID**</span></span>
</dt> <dd>

<span data-ttu-id="03720-108">Gibt die Paket-ID (PID) an.</span><span class="sxs-lookup"><span data-stu-id="03720-108">Specifies the packet ID (PID)</span></span>

</dd> <dt>

<span data-ttu-id="03720-109">**Mediasamplecontent**</span><span class="sxs-lookup"><span data-stu-id="03720-109">**MediaSampleContent**</span></span>
</dt> <dd>

<span data-ttu-id="03720-110">Gibt den Inhalt der Paket Nutzlast als den Enumerationstyp " [**Media \_ Sample \_ Content**](media-sample-content.md) " an.</span><span class="sxs-lookup"><span data-stu-id="03720-110">Specifies the contents of the packet payload, as a [**MEDIA\_SAMPLE\_CONTENT**](media-sample-content.md) enumeration type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03720-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03720-111">Requirements</span></span>



| <span data-ttu-id="03720-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03720-112">Requirement</span></span> | <span data-ttu-id="03720-113">Wert</span><span class="sxs-lookup"><span data-stu-id="03720-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03720-114">Header</span><span class="sxs-lookup"><span data-stu-id="03720-114">Header</span></span><br/> | <dl> <span data-ttu-id="03720-115"><dt>Bdatypes. h (Include bmolface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03720-115"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03720-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03720-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03720-117">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="03720-117">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="03720-118">**Ienumpidmap-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="03720-118">**IEnumPIDMap Interface**</span></span>](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




