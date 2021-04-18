---
description: Verpackt die Objekttyp-, Versions-und Größen Informationen, die in vielen NDIS 6,0-Strukturen benötigt werden.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: NDIS_OBJECT_HEADER Struktur (ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347563"
---
# <a name="ndis_object_header-structure"></a><span data-ttu-id="15b2d-103">NDIS- \_ Objekt \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="15b2d-103">NDIS\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="15b2d-104">Die **NDIS- \_ Objekt \_ Header** Struktur verpackt die Objekttyp-, Versions-und Größen Informationen, die in vielen NDIS 6,0-Strukturen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="15b2d-104">The **NDIS\_OBJECT\_HEADER** structure packages the object type, version, and size information that is required in many NDIS 6.0 structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b2d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15b2d-105">Syntax</span></span>


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="15b2d-106">Member</span><span class="sxs-lookup"><span data-stu-id="15b2d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15b2d-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="15b2d-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="15b2d-108">Gibt den Typ des NDIS-Objekts an, das von einer Struktur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="15b2d-108">Specifies the type of NDIS object that a structure describes.</span></span>

</dd> <dt>

<span data-ttu-id="15b2d-109">**Novel**</span><span class="sxs-lookup"><span data-stu-id="15b2d-109">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="15b2d-110">Gibt die Revisionsnummer dieser Struktur an.</span><span class="sxs-lookup"><span data-stu-id="15b2d-110">Specifies the revision number of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="15b2d-111">**Größe**</span><span class="sxs-lookup"><span data-stu-id="15b2d-111">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="15b2d-112">Gibt die Gesamtgröße der NDIS-Struktur (in Bytes) an, die den **NDIS- \_ Objekt \_ Header** enthält.</span><span class="sxs-lookup"><span data-stu-id="15b2d-112">Specifies the total size, in bytes, of the NDIS structure that contains the **NDIS\_OBJECT\_HEADER**.</span></span> <span data-ttu-id="15b2d-113">Diese Größe enthält die Größe des **NDIS- \_ Objekt \_ Header** Members und aller anderen Member der Struktur.</span><span class="sxs-lookup"><span data-stu-id="15b2d-113">This size includes the size of the **NDIS\_OBJECT\_HEADER** member and all other members of the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15b2d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15b2d-114">Requirements</span></span>



| <span data-ttu-id="15b2d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15b2d-115">Requirement</span></span> | <span data-ttu-id="15b2d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="15b2d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b2d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15b2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="15b2d-118">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15b2d-118">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15b2d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15b2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="15b2d-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15b2d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="15b2d-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="15b2d-121">Redistributable</span></span><br/>          | <span data-ttu-id="15b2d-122">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="15b2d-122">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="15b2d-123">Header</span><span class="sxs-lookup"><span data-stu-id="15b2d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="15b2d-124"><dt>Ntddndis. h (Include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15b2d-124"><dt>Ntddndis.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15b2d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15b2d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b2d-126">**\_BSSID- \_ Liste DOT11**</span><span class="sxs-lookup"><span data-stu-id="15b2d-126">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> </dl>

 

 




