---
title: glindexdv-Funktion (GL. h)
description: Die Funktion "glindexdv" legt den aktuellen Farbindex fest.
ms.assetid: e718e8c5-66e4-472c-9138-177c5ee697d3
keywords:
- glindexdv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2512e9100c4b3f68f644eb51c3d5d460787f49b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740656"
---
# <a name="glindexdv-function"></a><span data-ttu-id="86c66-104">glindexdv-Funktion</span><span class="sxs-lookup"><span data-stu-id="86c66-104">glIndexdv function</span></span>

<span data-ttu-id="86c66-105">Die Funktion " **glindexdv** " legt den aktuellen Farbindex fest.</span><span class="sxs-lookup"><span data-stu-id="86c66-105">The **glIndexdv** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c66-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="86c66-106">Syntax</span></span>


```C++
void WINAPI glIndexdv(
   const GLdouble *c
);
```



## <a name="parameters"></a><span data-ttu-id="86c66-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="86c66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c66-108">*c*</span><span class="sxs-lookup"><span data-stu-id="86c66-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="86c66-109">Ein Zeiger auf ein Array mit einem Element, das den neuen Wert für den aktuellen Farb Index enthält.</span><span class="sxs-lookup"><span data-stu-id="86c66-109">A pointer to a one-element array that contains the new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c66-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86c66-110">Return value</span></span>

<span data-ttu-id="86c66-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="86c66-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86c66-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86c66-112">Remarks</span></span>

<span data-ttu-id="86c66-113">Die Funktion " **glindexdv** " aktualisiert den aktuellen Farbindex (mit einem Wert).</span><span class="sxs-lookup"><span data-stu-id="86c66-113">The **glIndexdv** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="86c66-114">Es wird ein Argument benötigt: der neue Wert für den aktuellen Farbindex.</span><span class="sxs-lookup"><span data-stu-id="86c66-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="86c66-115">Der aktuelle Index wird als Gleit Komma Wert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="86c66-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="86c66-116">Ganzzahlige Werte werden ohne besondere Zuordnung direkt in Gleit Komma Werte konvertiert.</span><span class="sxs-lookup"><span data-stu-id="86c66-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="86c66-117">Index Werte außerhalb des darstellbaren Bereichs des Farb Index Puffers werden nicht gebunden.</span><span class="sxs-lookup"><span data-stu-id="86c66-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="86c66-118">Vor der Deaktivierung eines Indexes (sofern aktiviert) und dem Schreiben in den Framebuffer wird der Index jedoch in ein festes Punkt Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="86c66-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="86c66-119">Alle Bits im ganzzahligen Teil des resultierenden fest Komma Werts, die nicht Bits im Frame Puffer entsprechen, werden maskiert.</span><span class="sxs-lookup"><span data-stu-id="86c66-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="86c66-120">Der aktuelle Index kann jederzeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="86c66-120">The current index can be updated at any time.</span></span> <span data-ttu-id="86c66-121">Insbesondere kann **glindexdv** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="86c66-121">In particular, **glIndexdv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="86c66-122">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glindexdv** ab:</span><span class="sxs-lookup"><span data-stu-id="86c66-122">The following function retrieves information related to **glIndexdv**:</span></span>

<span data-ttu-id="86c66-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Current \_ Index"</span><span class="sxs-lookup"><span data-stu-id="86c66-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="86c66-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86c66-124">Requirements</span></span>



| <span data-ttu-id="86c66-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86c66-125">Requirement</span></span> | <span data-ttu-id="86c66-126">Wert</span><span class="sxs-lookup"><span data-stu-id="86c66-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86c66-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86c66-127">Minimum supported client</span></span><br/> | <span data-ttu-id="86c66-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86c66-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="86c66-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86c66-129">Minimum supported server</span></span><br/> | <span data-ttu-id="86c66-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86c66-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86c66-131">Header</span><span class="sxs-lookup"><span data-stu-id="86c66-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c66-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="86c66-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="86c66-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86c66-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="86c66-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86c66-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="86c66-135">DLL</span><span class="sxs-lookup"><span data-stu-id="86c66-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86c66-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c66-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c66-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86c66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c66-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="86c66-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="86c66-139">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="86c66-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="86c66-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="86c66-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="86c66-141">**glget**</span><span class="sxs-lookup"><span data-stu-id="86c66-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

