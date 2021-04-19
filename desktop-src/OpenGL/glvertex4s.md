---
title: glVertex4s-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex4s-Funktion (GL. h)
ms.assetid: 5030e0dd-9a81-482d-8d87-bfc9355a3c92
keywords:
- glVertex4s-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex4s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efcf64b6864d27e8df77056db14e9132cfbaaf5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106364341"
---
# <a name="glvertex4s-function"></a><span data-ttu-id="9a1e3-105">glVertex4s-Funktion</span><span class="sxs-lookup"><span data-stu-id="9a1e3-105">glVertex4s function</span></span>

<span data-ttu-id="9a1e3-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a1e3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a1e3-107">Syntax</span></span>


```C++
void WINAPI glVertex4s(
   GLshort x,
   GLshort y,
   GLshort z,
   GLshort w
);
```



## <a name="parameters"></a><span data-ttu-id="9a1e3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a1e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a1e3-109">*x*</span><span class="sxs-lookup"><span data-stu-id="9a1e3-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1e3-110">Gibt die x-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="9a1e3-111">*y*</span><span class="sxs-lookup"><span data-stu-id="9a1e3-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1e3-112">Gibt die y-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="9a1e3-113">*z*</span><span class="sxs-lookup"><span data-stu-id="9a1e3-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1e3-114">Gibt die z-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="9a1e3-115">*w*</span><span class="sxs-lookup"><span data-stu-id="9a1e3-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1e3-116">Gibt die w-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a1e3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a1e3-117">Return value</span></span>

<span data-ttu-id="9a1e3-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a1e3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a1e3-119">Remarks</span></span>

<span data-ttu-id="9a1e3-120">Die glVertex-Funktions Befehle werden innerhalb von [**glBegin**](glbegin.md)- / [**glEnd**](glend.md) -Paaren zum Angeben von Punkt-, Linien-und Polygon Scheitel Punkten verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="9a1e3-121">Die aktuellen Farben, normalen und Texturkoordinaten werden dem Scheitelpunkt zugeordnet, wenn glVertex aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="9a1e3-122">Wenn nur *x* und *y* angegeben werden, wird für *z* standardmäßig 0,0 und für *w* der Standardwert 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="9a1e3-123">Wenn *x*, *y* und *z* angegeben werden, wird *der Standardwert* 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="9a1e3-124">Das Aufrufen von glVertex außerhalb eines **glBegin**- / **glEnd** -Paars führt zu undefiniertem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="9a1e3-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a1e3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a1e3-125">Requirements</span></span>



| <span data-ttu-id="9a1e3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a1e3-126">Requirement</span></span> | <span data-ttu-id="9a1e3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9a1e3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a1e3-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a1e3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9a1e3-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a1e3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9a1e3-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a1e3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9a1e3-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a1e3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a1e3-132">Header</span><span class="sxs-lookup"><span data-stu-id="9a1e3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a1e3-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a1e3-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9a1e3-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a1e3-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a1e3-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a1e3-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9a1e3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9a1e3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a1e3-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a1e3-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a1e3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a1e3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1e3-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-141">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-142">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-144">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-145">**glindex**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-146">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-147">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-148">**glrect**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="9a1e3-149">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="9a1e3-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





