---
title: Iconresdir-Struktur
description: Enthält die Dimensionen und das Farb Format eines einzelnen Symbol Bilds in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Iconresdir-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338343"
---
# <a name="iconresdir-structure"></a><span data-ttu-id="7ee67-105">Iconresdir-Struktur</span><span class="sxs-lookup"><span data-stu-id="7ee67-105">ICONRESDIR structure</span></span>

<span data-ttu-id="7ee67-106">Enthält die Dimensionen und das Farb Format eines einzelnen Symbol Bilds in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ee67-106">Contains the dimensions and color format of an individual icon image in a resource group.</span></span> <span data-ttu-id="7ee67-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7ee67-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee67-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ee67-108">Syntax</span></span>


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a><span data-ttu-id="7ee67-109">Member</span><span class="sxs-lookup"><span data-stu-id="7ee67-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ee67-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="7ee67-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="7ee67-111">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="7ee67-111">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="7ee67-112">Die Breite des Symbols in Pixel.</span><span class="sxs-lookup"><span data-stu-id="7ee67-112">The width of the icon, in pixels.</span></span> <span data-ttu-id="7ee67-113">Zulässige Werte sind 16, 32 und 64.</span><span class="sxs-lookup"><span data-stu-id="7ee67-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="7ee67-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="7ee67-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="7ee67-115">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="7ee67-115">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="7ee67-116">Die Höhe des Symbols in Pixel.</span><span class="sxs-lookup"><span data-stu-id="7ee67-116">The height of the icon, in pixels.</span></span> <span data-ttu-id="7ee67-117">Zulässige Werte sind 16, 32 und 64.</span><span class="sxs-lookup"><span data-stu-id="7ee67-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="7ee67-118">**Colorcount**</span><span class="sxs-lookup"><span data-stu-id="7ee67-118">**ColorCount**</span></span>
</dt> <dd>

<span data-ttu-id="7ee67-119">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="7ee67-119">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="7ee67-120">Die Anzahl der Farben im Symbol.</span><span class="sxs-lookup"><span data-stu-id="7ee67-120">The number of colors in the icon.</span></span> <span data-ttu-id="7ee67-121">Zulässige Werte sind 2, 8 und 16.</span><span class="sxs-lookup"><span data-stu-id="7ee67-121">Acceptable values are 2, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="7ee67-122">**bleiben**</span><span class="sxs-lookup"><span data-stu-id="7ee67-122">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7ee67-123">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="7ee67-123">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="7ee67-124">Bleiben muss auf denselben Wert festgelegt werden wie der des reservierten Felds im Header der Symbol Datei.</span><span class="sxs-lookup"><span data-stu-id="7ee67-124">Reserved; must be set to the same value as that of the reserved field in the icon file header.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ee67-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ee67-125">Remarks</span></span>

<span data-ttu-id="7ee67-126">Die **iconresdir** -Struktur wird in der [**resdir**](resdir.md) -Struktur übermittelt, wenn die **resdir** -Struktur ein Symbol beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ee67-126">The **ICONRESDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes an icon.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee67-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ee67-127">Requirements</span></span>



| <span data-ttu-id="7ee67-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ee67-128">Requirement</span></span> | <span data-ttu-id="7ee67-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7ee67-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7ee67-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ee67-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7ee67-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ee67-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7ee67-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ee67-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7ee67-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ee67-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7ee67-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ee67-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ee67-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7ee67-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7ee67-136">**Resdir**</span><span class="sxs-lookup"><span data-stu-id="7ee67-136">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="7ee67-137">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7ee67-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7ee67-138">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7ee67-138">Resources</span></span>](resources.md)
</dt> </dl>

 

 





