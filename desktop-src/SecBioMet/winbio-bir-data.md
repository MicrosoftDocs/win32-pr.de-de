---
title: WINBIO_BIR_DATA Struktur (winbio \_ types. h)
description: Gibt die Größe (in Bytes) und den Offset eines Blocks biometrischer Informationen an.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- WINBIO_BIR_DATA Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391881"
---
# <a name="winbio_bir_data-structure"></a><span data-ttu-id="00a01-104">Winbio \_ Bir- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="00a01-104">WINBIO\_BIR\_DATA structure</span></span>

<span data-ttu-id="00a01-105">Die **\_ \_ Datenstruktur "winbio Bir** " gibt die Größe, in Bytes und den Offset eines Blocks biometrischer Informationen an.</span><span class="sxs-lookup"><span data-stu-id="00a01-105">The **WINBIO\_BIR\_DATA** structure specifies the size, in bytes, and the offset of a block of biometric information.</span></span> <span data-ttu-id="00a01-106">Diese Struktur wird von der [**winbio \_ Bir**](winbio-bir.md) -Struktur verwendet, um anzugeben, wo sich die verschiedenen Teile eines biometrischen Informations Satzes befinden.</span><span class="sxs-lookup"><span data-stu-id="00a01-106">This structure is used by the [**WINBIO\_BIR**](winbio-bir.md) structure to specify where the various parts of a biometric information record are located.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="00a01-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a><span data-ttu-id="00a01-108">Member</span><span class="sxs-lookup"><span data-stu-id="00a01-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="00a01-109">**Größe**</span><span class="sxs-lookup"><span data-stu-id="00a01-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="00a01-110">Größe (in Bytes) der biometrischen Informationen.</span><span class="sxs-lookup"><span data-stu-id="00a01-110">Size, in bytes, of the biometric information.</span></span>

</dd> <dt>

<span data-ttu-id="00a01-111">**Offset**</span><span class="sxs-lookup"><span data-stu-id="00a01-111">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="00a01-112">Der Offset der biometrischen Informationen in Bytes vom Anfang der [**winbio \_**](winbio-bir.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="00a01-112">Offset, in bytes from the beginning of the [**WINBIO\_BIR**](winbio-bir.md) structure, of the biometric information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00a01-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00a01-113">Remarks</span></span>

<span data-ttu-id="00a01-114">Die Verwendung von Offsets anstelle von Zeigern ermöglicht die einfache Serialisierung von Bir und für eine weniger komplizierte Übersetzung zwischen 32-und 64-Bit-Umgebungen oder zwischen Benutzer-und Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="00a01-114">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="00a01-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00a01-115">Requirements</span></span>



| <span data-ttu-id="00a01-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00a01-116">Requirement</span></span> | <span data-ttu-id="00a01-117">Wert</span><span class="sxs-lookup"><span data-stu-id="00a01-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a01-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00a01-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00a01-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00a01-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="00a01-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00a01-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00a01-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00a01-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="00a01-122">Header</span><span class="sxs-lookup"><span data-stu-id="00a01-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a01-123"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00a01-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a01-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00a01-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a01-125">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="00a01-125">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="00a01-126">**winbio \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="00a01-126">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="00a01-127">**winbio- \_ Bir- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="00a01-127">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





