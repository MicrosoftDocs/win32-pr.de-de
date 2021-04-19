---
title: Glinde XI-Funktion (GL. h)
description: Die Funktion "Glinde XI" legt den aktuellen Farbindex fest.
ms.assetid: c57d2316-4081-40d8-af50-ae0299597803
keywords:
- Glinde XI-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b40d8d0d96aac17c852fb266b23dec23d26c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338129"
---
# <a name="glindexi-function"></a><span data-ttu-id="14c56-104">Glinde XI-Funktion</span><span class="sxs-lookup"><span data-stu-id="14c56-104">glIndexi function</span></span>

<span data-ttu-id="14c56-105">Die Funktion " **Glinde XI** " legt den aktuellen Farbindex fest.</span><span class="sxs-lookup"><span data-stu-id="14c56-105">The **glIndexi** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c56-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="14c56-106">Syntax</span></span>


```C++
void WINAPI glIndexi(
   GLint c
);
```



## <a name="parameters"></a><span data-ttu-id="14c56-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="14c56-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c56-108">*c*</span><span class="sxs-lookup"><span data-stu-id="14c56-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="14c56-109">Der neue Wert für den aktuellen Farb Index.</span><span class="sxs-lookup"><span data-stu-id="14c56-109">The new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c56-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14c56-110">Return value</span></span>

<span data-ttu-id="14c56-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="14c56-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14c56-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14c56-112">Remarks</span></span>

<span data-ttu-id="14c56-113">Die Funktion " **Glinde XI** " aktualisiert den aktuellen Farbindex (mit einem Wert).</span><span class="sxs-lookup"><span data-stu-id="14c56-113">The **glIndexi** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="14c56-114">Es wird ein Argument benötigt: der neue Wert für den aktuellen Farbindex.</span><span class="sxs-lookup"><span data-stu-id="14c56-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="14c56-115">Der aktuelle Index wird als Gleit Komma Wert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14c56-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="14c56-116">Ganzzahlige Werte werden ohne besondere Zuordnung direkt in Gleit Komma Werte konvertiert.</span><span class="sxs-lookup"><span data-stu-id="14c56-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="14c56-117">Index Werte außerhalb des darstellbaren Bereichs des Farb Index Puffers werden nicht gebunden.</span><span class="sxs-lookup"><span data-stu-id="14c56-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="14c56-118">Vor der Deaktivierung eines Indexes (sofern aktiviert) und dem Schreiben in den Framebuffer wird der Index jedoch in ein festes Punkt Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="14c56-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="14c56-119">Alle Bits im ganzzahligen Teil des resultierenden fest Komma Werts, die nicht Bits im Frame Puffer entsprechen, werden maskiert.</span><span class="sxs-lookup"><span data-stu-id="14c56-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="14c56-120">Der aktuelle Index kann jederzeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="14c56-120">The current index can be updated at any time.</span></span> <span data-ttu-id="14c56-121">Insbesondere kann **Glinde** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="14c56-121">In particular, **glIndexi** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="14c56-122">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glindexi** ab:</span><span class="sxs-lookup"><span data-stu-id="14c56-122">The following function retrieves information related to **glIndexi**:</span></span>

<span data-ttu-id="14c56-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Current \_ Index"</span><span class="sxs-lookup"><span data-stu-id="14c56-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="14c56-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14c56-124">Requirements</span></span>



| <span data-ttu-id="14c56-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14c56-125">Requirement</span></span> | <span data-ttu-id="14c56-126">Wert</span><span class="sxs-lookup"><span data-stu-id="14c56-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14c56-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14c56-127">Minimum supported client</span></span><br/> | <span data-ttu-id="14c56-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14c56-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14c56-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14c56-129">Minimum supported server</span></span><br/> | <span data-ttu-id="14c56-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14c56-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14c56-131">Header</span><span class="sxs-lookup"><span data-stu-id="14c56-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="14c56-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c56-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="14c56-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14c56-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="14c56-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14c56-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="14c56-135">DLL</span><span class="sxs-lookup"><span data-stu-id="14c56-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14c56-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14c56-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c56-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14c56-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c56-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="14c56-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="14c56-139">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="14c56-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="14c56-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="14c56-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="14c56-141">**glget**</span><span class="sxs-lookup"><span data-stu-id="14c56-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

