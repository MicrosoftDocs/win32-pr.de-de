---
title: glindexfv-Funktion (GL. h)
description: Die Funktion "glindexfv" legt den aktuellen Farbindex fest.
ms.assetid: 355d1896-ea9d-4a80-9dee-285f3bf638e5
keywords:
- glindexfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a649f15dd6fad637d9e742a97235fdcd99d82794
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040342"
---
# <a name="glindexfv-function"></a><span data-ttu-id="20a16-104">glindexfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="20a16-104">glIndexfv function</span></span>

<span data-ttu-id="20a16-105">Die Funktion " **glindexfv** " legt den aktuellen Farbindex fest.</span><span class="sxs-lookup"><span data-stu-id="20a16-105">The **glIndexfv** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="20a16-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="20a16-106">Syntax</span></span>


```C++
void WINAPI glIndexfv(
   const GLfloat *c
);
```



## <a name="parameters"></a><span data-ttu-id="20a16-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="20a16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20a16-108">*c*</span><span class="sxs-lookup"><span data-stu-id="20a16-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="20a16-109">Ein Zeiger auf ein Array mit einem Element, das den neuen Wert für den aktuellen Farb Index enthält.</span><span class="sxs-lookup"><span data-stu-id="20a16-109">A pointer to a one-element array that contains the new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20a16-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20a16-110">Return value</span></span>

<span data-ttu-id="20a16-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="20a16-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20a16-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20a16-112">Remarks</span></span>

<span data-ttu-id="20a16-113">Die Funktion " **glindexfv** " aktualisiert den aktuellen Farbindex (mit einem Wert).</span><span class="sxs-lookup"><span data-stu-id="20a16-113">The **glIndexfv** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="20a16-114">Es wird ein Argument benötigt: der neue Wert für den aktuellen Farbindex.</span><span class="sxs-lookup"><span data-stu-id="20a16-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="20a16-115">Der aktuelle Index wird als Gleit Komma Wert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="20a16-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="20a16-116">Ganzzahlige Werte werden ohne besondere Zuordnung direkt in Gleit Komma Werte konvertiert.</span><span class="sxs-lookup"><span data-stu-id="20a16-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="20a16-117">Index Werte außerhalb des darstellbaren Bereichs des Farb Index Puffers werden nicht gebunden.</span><span class="sxs-lookup"><span data-stu-id="20a16-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="20a16-118">Vor der Deaktivierung eines Indexes (sofern aktiviert) und dem Schreiben in den Framebuffer wird der Index jedoch in ein festes Punkt Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="20a16-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="20a16-119">Alle Bits im ganzzahligen Teil des resultierenden fest Komma Werts, die nicht Bits im Frame Puffer entsprechen, werden maskiert.</span><span class="sxs-lookup"><span data-stu-id="20a16-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="20a16-120">Der aktuelle Index kann jederzeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="20a16-120">The current index can be updated at any time.</span></span> <span data-ttu-id="20a16-121">Insbesondere kann **glindexfv** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="20a16-121">In particular, **glIndexfv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="20a16-122">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glindexfv** ab:</span><span class="sxs-lookup"><span data-stu-id="20a16-122">The following function retrieves information related to **glIndexfv**:</span></span>

<span data-ttu-id="20a16-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Current \_ Index"</span><span class="sxs-lookup"><span data-stu-id="20a16-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="20a16-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20a16-124">Requirements</span></span>



| <span data-ttu-id="20a16-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20a16-125">Requirement</span></span> | <span data-ttu-id="20a16-126">Wert</span><span class="sxs-lookup"><span data-stu-id="20a16-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20a16-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20a16-127">Minimum supported client</span></span><br/> | <span data-ttu-id="20a16-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20a16-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="20a16-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20a16-129">Minimum supported server</span></span><br/> | <span data-ttu-id="20a16-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20a16-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20a16-131">Header</span><span class="sxs-lookup"><span data-stu-id="20a16-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="20a16-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="20a16-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="20a16-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="20a16-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="20a16-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20a16-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="20a16-135">DLL</span><span class="sxs-lookup"><span data-stu-id="20a16-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20a16-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20a16-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20a16-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20a16-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a16-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="20a16-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="20a16-139">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="20a16-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="20a16-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="20a16-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="20a16-141">**glget**</span><span class="sxs-lookup"><span data-stu-id="20a16-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

