---
title: Localheader-Struktur
description: Enthält die x-und y-Koordinaten eines Hotspots, der mit dem durch eine resdir-Struktur identifizierten Cursor verknüpft ist. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Localheader-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392007"
---
# <a name="localheader-structure"></a><span data-ttu-id="67473-105">Localheader-Struktur</span><span class="sxs-lookup"><span data-stu-id="67473-105">LOCALHEADER structure</span></span>

<span data-ttu-id="67473-106">Enthält die x-und y-Koordinaten eines Hotspots, der mit dem durch eine [**resdir**](resdir.md) -Struktur identifizierten Cursor verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="67473-106">Contains the x- and y-coordinates of a hotspot associated with the cursor identified by a [**RESDIR**](resdir.md) structure.</span></span> <span data-ttu-id="67473-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="67473-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="67473-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="67473-108">Syntax</span></span>


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a><span data-ttu-id="67473-109">Member</span><span class="sxs-lookup"><span data-stu-id="67473-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="67473-110">**xhotspot**</span><span class="sxs-lookup"><span data-stu-id="67473-110">**xHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="67473-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="67473-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="67473-112">Die x-Koordinate der Cursorposition in Pixel.</span><span class="sxs-lookup"><span data-stu-id="67473-112">The x-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="67473-113">**yhotspot**</span><span class="sxs-lookup"><span data-stu-id="67473-113">**yHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="67473-114">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="67473-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="67473-115">Die y-Koordinate der Cursorposition in Pixel.</span><span class="sxs-lookup"><span data-stu-id="67473-115">The y-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67473-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67473-116">Remarks</span></span>

<span data-ttu-id="67473-117">Die **localheader** -Struktur ist die erste Daten, die in die [RT- \_ Cursor](/windows/desktop/menurc/resource-types) Ressource geschrieben werden, wenn eine [**resdir**](resdir.md) -Strukturinformationen über einen Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="67473-117">The **LOCALHEADER** structure is the first data written to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource if a [**RESDIR**](resdir.md) structure contains information about a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="67473-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67473-118">Requirements</span></span>



| <span data-ttu-id="67473-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67473-119">Requirement</span></span> | <span data-ttu-id="67473-120">Wert</span><span class="sxs-lookup"><span data-stu-id="67473-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="67473-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67473-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67473-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67473-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="67473-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67473-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67473-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67473-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="67473-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67473-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="67473-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="67473-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="67473-127">**Cursor Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="67473-127">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="67473-128">**Resdir**</span><span class="sxs-lookup"><span data-stu-id="67473-128">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="67473-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="67473-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67473-130">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="67473-130">Resources</span></span>](resources.md)
</dt> </dl>

 

