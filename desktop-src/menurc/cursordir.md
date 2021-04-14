---
title: Cursor dir-Struktur
description: Enthält die Dimensionen eines einzelnen Cursor Bilds in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Cursor-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392146"
---
# <a name="cursordir-structure"></a><span data-ttu-id="2262e-105">Cursor dir-Struktur</span><span class="sxs-lookup"><span data-stu-id="2262e-105">CURSORDIR structure</span></span>

<span data-ttu-id="2262e-106">Enthält die Dimensionen eines einzelnen Cursor Bilds in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2262e-106">Contains the dimensions of an individual cursor image in a resource group.</span></span> <span data-ttu-id="2262e-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2262e-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2262e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2262e-108">Syntax</span></span>


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a><span data-ttu-id="2262e-109">Member</span><span class="sxs-lookup"><span data-stu-id="2262e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2262e-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="2262e-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="2262e-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="2262e-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2262e-112">Die Breite des Cursors in Pixel.</span><span class="sxs-lookup"><span data-stu-id="2262e-112">The width of the cursor, in pixels.</span></span> <span data-ttu-id="2262e-113">Zulässige Werte sind 16, 32 und 64.</span><span class="sxs-lookup"><span data-stu-id="2262e-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="2262e-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="2262e-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="2262e-115">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="2262e-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2262e-116">Die Höhe des Cursors in Pixel.</span><span class="sxs-lookup"><span data-stu-id="2262e-116">The height of the cursor, in pixels.</span></span> <span data-ttu-id="2262e-117">Zulässige Werte sind 16, 32 und 64.</span><span class="sxs-lookup"><span data-stu-id="2262e-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2262e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2262e-118">Remarks</span></span>

<span data-ttu-id="2262e-119">Die **cursordir** -Struktur wird in der [**resdir**](resdir.md) -Struktur übermittelt, wenn die **resdir** -Struktur einen Cursor beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2262e-119">The **CURSORDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="2262e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2262e-120">Requirements</span></span>



| <span data-ttu-id="2262e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2262e-121">Requirement</span></span> | <span data-ttu-id="2262e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2262e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2262e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2262e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2262e-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2262e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2262e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2262e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2262e-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2262e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2262e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2262e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="2262e-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2262e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2262e-129">**Resdir**</span><span class="sxs-lookup"><span data-stu-id="2262e-129">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="2262e-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2262e-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2262e-131">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2262e-131">Resources</span></span>](resources.md)
</dt> </dl>

 

 





