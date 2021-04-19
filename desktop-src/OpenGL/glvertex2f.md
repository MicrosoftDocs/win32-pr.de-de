---
title: glVertex2f-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex2f-Funktion (GL. h)
ms.assetid: d351cdc1-efaa-4c06-96d9-c4ef613c64df
keywords:
- glVertex2f-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b2610b4d0498a5a623372ba5f28ee4feea7b40d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106367309"
---
# <a name="glvertex2f-function"></a><span data-ttu-id="a14b9-105">glVertex2f-Funktion</span><span class="sxs-lookup"><span data-stu-id="a14b9-105">glVertex2f function</span></span>

<span data-ttu-id="a14b9-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="a14b9-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a14b9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a14b9-107">Syntax</span></span>


```C++
void WINAPI glVertex2f(
   GLfloat x,
   GLfloat y
);
```



## <a name="parameters"></a><span data-ttu-id="a14b9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a14b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a14b9-109">*x*</span><span class="sxs-lookup"><span data-stu-id="a14b9-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a14b9-110">Gibt die x-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="a14b9-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a14b9-111">*y*</span><span class="sxs-lookup"><span data-stu-id="a14b9-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a14b9-112">Gibt die y-Koordinate eines Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="a14b9-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a14b9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a14b9-113">Return value</span></span>

<span data-ttu-id="a14b9-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a14b9-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a14b9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a14b9-115">Remarks</span></span>

<span data-ttu-id="a14b9-116">Die glVertex-Funktions Befehle werden innerhalb von [**glBegin**](glbegin.md)- / [**glEnd**](glend.md) -Paaren zum Angeben von Punkt-, Linien-und Polygon Scheitel Punkten verwendet.</span><span class="sxs-lookup"><span data-stu-id="a14b9-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="a14b9-117">Die aktuellen Farben, normalen und Texturkoordinaten werden dem Scheitelpunkt zugeordnet, wenn glVertex aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a14b9-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="a14b9-118">Wenn nur *x* und *y* angegeben werden, wird für *z* standardmäßig 0,0 und für *w* der Standardwert 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a14b9-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="a14b9-119">Wenn *x*, *y* und *z* angegeben werden, wird *der Standardwert* 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a14b9-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="a14b9-120">Das Aufrufen von glVertex außerhalb eines **glBegin**- / **glEnd** -Paars führt zu undefiniertem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="a14b9-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14b9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a14b9-121">Requirements</span></span>



| <span data-ttu-id="a14b9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a14b9-122">Requirement</span></span> | <span data-ttu-id="a14b9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a14b9-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a14b9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a14b9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a14b9-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a14b9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a14b9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a14b9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a14b9-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a14b9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a14b9-128">Header</span><span class="sxs-lookup"><span data-stu-id="a14b9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a14b9-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a14b9-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a14b9-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a14b9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a14b9-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a14b9-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a14b9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a14b9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a14b9-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a14b9-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a14b9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a14b9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14b9-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a14b9-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a14b9-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="a14b9-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a14b9-137">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="a14b9-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a14b9-138">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="a14b9-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a14b9-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a14b9-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a14b9-140">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="a14b9-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a14b9-141">**glindex**</span><span class="sxs-lookup"><span data-stu-id="a14b9-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a14b9-142">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="a14b9-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a14b9-143">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="a14b9-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a14b9-144">**glrect**</span><span class="sxs-lookup"><span data-stu-id="a14b9-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="a14b9-145">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="a14b9-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





