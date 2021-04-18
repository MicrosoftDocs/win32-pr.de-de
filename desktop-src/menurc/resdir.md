---
title: Resdir-Struktur
description: Enthält Informationen zu einem einzelnen Symbol oder einer Cursor Komponente in einer Ressourcengruppe. Es gibt eine resdir-Struktur für jede Gruppen Komponente. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Resdir-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337303"
---
# <a name="resdir-structure"></a><span data-ttu-id="bba00-106">Resdir-Struktur</span><span class="sxs-lookup"><span data-stu-id="bba00-106">RESDIR structure</span></span>

<span data-ttu-id="bba00-107">Enthält Informationen zu einem einzelnen Symbol oder einer Cursor Komponente in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bba00-107">Contains information about an individual icon or cursor component in a resource group.</span></span> <span data-ttu-id="bba00-108">Es gibt eine **resdir** -Struktur für jede Gruppen Komponente.</span><span class="sxs-lookup"><span data-stu-id="bba00-108">There is one **RESDIR** structure for each group component.</span></span> <span data-ttu-id="bba00-109">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bba00-109">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba00-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bba00-110">Syntax</span></span>


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a><span data-ttu-id="bba00-111">Member</span><span class="sxs-lookup"><span data-stu-id="bba00-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="bba00-112">**Symbol:**</span><span class="sxs-lookup"><span data-stu-id="bba00-112">**Icon**</span></span>
</dt> <dd>

<span data-ttu-id="bba00-113">Typ: **[ **iconresdir**](iconresdir.md)**</span><span class="sxs-lookup"><span data-stu-id="bba00-113">Type: **[**ICONRESDIR**](iconresdir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba00-114">Die Breite, Höhe und Farbzahl des Symbols.</span><span class="sxs-lookup"><span data-stu-id="bba00-114">The width, height, and color count of the indicated icon.</span></span>

</dd> <dt>

<span data-ttu-id="bba00-115">**Cursor**</span><span class="sxs-lookup"><span data-stu-id="bba00-115">**Cursor**</span></span>
</dt> <dd>

<span data-ttu-id="bba00-116">Typ: **[ **Cursor dir**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="bba00-116">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba00-117">Die Breite und Höhe des Mauszeigers.</span><span class="sxs-lookup"><span data-stu-id="bba00-117">The width and height of the indicated cursor.</span></span>

</dd> <dt>

<span data-ttu-id="bba00-118">**Back**</span><span class="sxs-lookup"><span data-stu-id="bba00-118">**Planes**</span></span>
</dt> <dd>

<span data-ttu-id="bba00-119">Typ: **[ **Cursor dir**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="bba00-119">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba00-120">Die Anzahl von Farbebenen in der Symbol-oder Cursor Bitmap.</span><span class="sxs-lookup"><span data-stu-id="bba00-120">The number of color planes in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bba00-121">**BitCount**</span><span class="sxs-lookup"><span data-stu-id="bba00-121">**BitCount**</span></span>
</dt> <dd>

<span data-ttu-id="bba00-122">Typ: **[ **Cursor dir**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="bba00-122">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba00-123">Die Anzahl der Bits pro Pixel in der Symbol-oder Cursor Bitmap.</span><span class="sxs-lookup"><span data-stu-id="bba00-123">The number of bits per pixel in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bba00-124">**Bytesinres**</span><span class="sxs-lookup"><span data-stu-id="bba00-124">**BytesInRes**</span></span>
</dt> <dd>

<span data-ttu-id="bba00-125">Typ: **[ **Cursor dir**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="bba00-125">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba00-126">Die Größe der Ressource in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bba00-126">The size of the resource, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bba00-127">**Iconcurrd**</span><span class="sxs-lookup"><span data-stu-id="bba00-127">**IconCursorId**</span></span>
</dt> <dd>

<span data-ttu-id="bba00-128">Typ: **[ **Cursor dir**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="bba00-128">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bba00-129">Das Symbol oder der Cursor mit einem eindeutigen ordinalbezeichner.</span><span class="sxs-lookup"><span data-stu-id="bba00-129">The icon or cursor with a unique ordinal identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bba00-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bba00-130">Remarks</span></span>

<span data-ttu-id="bba00-131">Eine oder mehrere **resdir** -Strukturen folgen direkt der Struktur " [**netwheader**](newheader.md) " in der RES-Datei.</span><span class="sxs-lookup"><span data-stu-id="bba00-131">One or more **RESDIR** structures immediately follow the [**NEWHEADER**](newheader.md) structure in the .res file.</span></span> <span data-ttu-id="bba00-132">Der **rescount** -Member der Struktur " **netwheader** " gibt die Anzahl der **resdir** -Strukturen an.</span><span class="sxs-lookup"><span data-stu-id="bba00-132">The **ResCount** member of the **NEWHEADER** structure specifies the number of **RESDIR** structures.</span></span> <span data-ttu-id="bba00-133">Beachten Sie, dass die **resdir** -Struktur entweder aus einer [**iconresdir**](iconresdir.md) -Struktur oder aus einer [**Cursor dir**](cursordir.md) -Struktur besteht, gefolgt **von den** Membern, **bitCount**, **bytesinres** und **iconcurrsorid** .</span><span class="sxs-lookup"><span data-stu-id="bba00-133">Note that the **RESDIR** structure consists of either an [**ICONRESDIR**](iconresdir.md) structure or a [**CURSORDIR**](cursordir.md) structure followed by the **Planes**, **BitCount**, **BytesInRes**, and **IconCursorId** members.</span></span> <span data-ttu-id="bba00-134">Wenn die **resdir** -Strukturinformationen über einen Cursor enthält, sind die ersten beiden **Wörter**, die der Ressourcen Compiler in die [RT- \_ Cursor](/windows/desktop/menurc/resource-types) Ressource schreibt, die **xhotspot** -und **yhotspot** -Elemente der [**localheader**](localheader.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bba00-134">If the **RESDIR** structure contains information about a cursor, the first two **WORD** s the resource compiler writes to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource are the **xHotSpot** and **yHotSpot** members of the [**LOCALHEADER**](localheader.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba00-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bba00-135">Requirements</span></span>



| <span data-ttu-id="bba00-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bba00-136">Requirement</span></span> | <span data-ttu-id="bba00-137">Wert</span><span class="sxs-lookup"><span data-stu-id="bba00-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bba00-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bba00-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bba00-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bba00-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bba00-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bba00-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bba00-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bba00-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bba00-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bba00-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="bba00-143">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="bba00-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bba00-144">**Cursor Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="bba00-144">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="bba00-145">**Iconresdir**</span><span class="sxs-lookup"><span data-stu-id="bba00-145">**ICONRESDIR**</span></span>](iconresdir.md)
</dt> <dt>

[<span data-ttu-id="bba00-146">**Localheader**</span><span class="sxs-lookup"><span data-stu-id="bba00-146">**LOCALHEADER**</span></span>](localheader.md)
</dt> <dt>

[<span data-ttu-id="bba00-147">**"Nwheader"**</span><span class="sxs-lookup"><span data-stu-id="bba00-147">**NEWHEADER**</span></span>](newheader.md)
</dt> <dt>

<span data-ttu-id="bba00-148">**Licher**</span><span class="sxs-lookup"><span data-stu-id="bba00-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bba00-149">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bba00-149">Resources</span></span>](resources.md)
</dt> </dl>

 

