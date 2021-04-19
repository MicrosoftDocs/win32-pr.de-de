---
title: glVertex3d-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex3d-Funktion (GL. h)
ms.assetid: 531a552d-7979-4994-ad28-73c2d3987bae
keywords:
- glVertex3d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608ab02bf2cd41b7f2ffcc8fa3fe8cb2dea0ca89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366606"
---
# <a name="glvertex3d-function"></a><span data-ttu-id="56d86-105">glVertex3d-Funktion</span><span class="sxs-lookup"><span data-stu-id="56d86-105">glVertex3d function</span></span>

<span data-ttu-id="56d86-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="56d86-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d86-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56d86-107">Syntax</span></span>


```C++
void WINAPI glVertex3d(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="56d86-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56d86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56d86-109">*x*</span><span class="sxs-lookup"><span data-stu-id="56d86-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="56d86-110">Gibt die x-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="56d86-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="56d86-111">*y*</span><span class="sxs-lookup"><span data-stu-id="56d86-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="56d86-112">Gibt die y-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="56d86-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="56d86-113">*z*</span><span class="sxs-lookup"><span data-stu-id="56d86-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="56d86-114">Gibt die z-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="56d86-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56d86-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56d86-115">Return value</span></span>

<span data-ttu-id="56d86-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="56d86-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56d86-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56d86-117">Remarks</span></span>

<span data-ttu-id="56d86-118">Die glVertex-Funktions Befehle werden innerhalb von [**glBegin**](glbegin.md)- / [**glEnd**](glend.md) -Paaren zum Angeben von Punkt-, Linien-und Polygon Scheitel Punkten verwendet.</span><span class="sxs-lookup"><span data-stu-id="56d86-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="56d86-119">Die aktuellen Farben, normalen und Texturkoordinaten werden dem Scheitelpunkt zugeordnet, wenn glVertex aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56d86-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="56d86-120">Wenn nur *x* und *y* angegeben werden, wird für *z* standardmäßig 0,0 und für *w* der Standardwert 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="56d86-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="56d86-121">Wenn *x*, *y* und *z* angegeben werden, wird *der Standardwert* 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="56d86-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="56d86-122">Das Aufrufen von glVertex außerhalb eines **glBegin**- / **glEnd** -Paars führt zu undefiniertem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="56d86-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="56d86-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56d86-123">Requirements</span></span>



| <span data-ttu-id="56d86-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56d86-124">Requirement</span></span> | <span data-ttu-id="56d86-125">Wert</span><span class="sxs-lookup"><span data-stu-id="56d86-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56d86-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56d86-126">Minimum supported client</span></span><br/> | <span data-ttu-id="56d86-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56d86-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="56d86-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56d86-128">Minimum supported server</span></span><br/> | <span data-ttu-id="56d86-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56d86-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56d86-130">Header</span><span class="sxs-lookup"><span data-stu-id="56d86-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="56d86-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="56d86-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="56d86-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56d86-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="56d86-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56d86-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="56d86-134">DLL</span><span class="sxs-lookup"><span data-stu-id="56d86-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56d86-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56d86-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56d86-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56d86-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d86-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="56d86-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="56d86-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="56d86-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="56d86-139">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="56d86-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="56d86-140">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="56d86-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="56d86-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="56d86-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="56d86-142">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="56d86-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="56d86-143">**glindex**</span><span class="sxs-lookup"><span data-stu-id="56d86-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="56d86-144">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="56d86-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="56d86-145">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="56d86-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="56d86-146">**glrect**</span><span class="sxs-lookup"><span data-stu-id="56d86-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="56d86-147">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="56d86-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





