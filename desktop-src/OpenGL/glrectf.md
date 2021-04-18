---
title: glrectf-Funktion (GL. h)
description: Die Funktion "glrectf" zeichnet ein Rechteck.
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
keywords:
- glrectf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRectf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0c7036ae7395dce66d88f52c30631be801c4af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475252"
---
# <a name="glrectf-function"></a><span data-ttu-id="8bc77-104">glrectf-Funktion</span><span class="sxs-lookup"><span data-stu-id="8bc77-104">glRectf function</span></span>

<span data-ttu-id="8bc77-105">Die Funktion " [**glrectf**](glrectd.md) " zeichnet ein Rechteck.</span><span class="sxs-lookup"><span data-stu-id="8bc77-105">The [**glRectf**](glrectd.md) function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc77-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bc77-106">Syntax</span></span>


```C++
void WINAPI glRectf(
   GLfloat x1,
   GLfloat y1,
   GLfloat x2,
   GLfloat y2
);
```



## <a name="parameters"></a><span data-ttu-id="8bc77-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bc77-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bc77-108">*x1*</span><span class="sxs-lookup"><span data-stu-id="8bc77-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="8bc77-109">Die *x* -Koordinate des Scheitel Punkts eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8bc77-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="8bc77-110">*y1*</span><span class="sxs-lookup"><span data-stu-id="8bc77-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="8bc77-111">Die *y* -Koordinate des Scheitel Punkts eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8bc77-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="8bc77-112">*x2*</span><span class="sxs-lookup"><span data-stu-id="8bc77-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="8bc77-113">Die *x* -Koordinate des umgekehrten Scheitel Punkts des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8bc77-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="8bc77-114">*Y2*</span><span class="sxs-lookup"><span data-stu-id="8bc77-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="8bc77-115">Die *y* -Koordinate des umgekehrten Scheitel Punkts des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8bc77-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bc77-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8bc77-116">Return value</span></span>

<span data-ttu-id="8bc77-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8bc77-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8bc77-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8bc77-118">Error codes</span></span>

<span data-ttu-id="8bc77-119">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8bc77-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8bc77-120">Name</span><span class="sxs-lookup"><span data-stu-id="8bc77-120">Name</span></span>                                                                                                  | <span data-ttu-id="8bc77-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8bc77-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8bc77-122"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="8bc77-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8bc77-123">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8bc77-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8bc77-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bc77-124">Remarks</span></span>

<span data-ttu-id="8bc77-125">Die **glrectf** -Funktion unterstützt die effiziente Angabe von Rechtecke als zwei Eckpunkte.</span><span class="sxs-lookup"><span data-stu-id="8bc77-125">The **glRectf** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="8bc77-126">Jeder Rechteck Befehl benötigt vier Argumente, die entweder als zwei aufeinander folgende Paare von (*x*, *y*)-Koordinaten oder als zwei Zeiger auf Arrays angeordnet sind, die jeweils ein (*x*, *y*)-Paar enthalten.</span><span class="sxs-lookup"><span data-stu-id="8bc77-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="8bc77-127">Das resultierende Rechteck wird in der *z* = 0-Ebene definiert.</span><span class="sxs-lookup"><span data-stu-id="8bc77-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="8bc77-128">Die Funktion " **glrectf**(*x1,* *Y1,* *x2,* *Y2*)" entspricht genau der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="8bc77-128">The **glRectf**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="8bc77-129">**glBegin**(GL- \_ Polygon);</span><span class="sxs-lookup"><span data-stu-id="8bc77-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="8bc77-130">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="8bc77-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="8bc77-131">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="8bc77-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="8bc77-132">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="8bc77-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="8bc77-133">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="8bc77-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="8bc77-134">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="8bc77-134">**glEnd**( );</span></span>

<span data-ttu-id="8bc77-135">Beachten Sie Folgendes: Wenn sich der zweite Scheitelpunkt oberhalb und rechts vom ersten Scheitelpunkt befindet, wird das Rechteck mit einem gegen Uhrzeigersinn konstruiert.</span><span class="sxs-lookup"><span data-stu-id="8bc77-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bc77-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bc77-136">Requirements</span></span>



| <span data-ttu-id="8bc77-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bc77-137">Requirement</span></span> | <span data-ttu-id="8bc77-138">Wert</span><span class="sxs-lookup"><span data-stu-id="8bc77-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bc77-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bc77-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8bc77-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bc77-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8bc77-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bc77-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8bc77-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bc77-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8bc77-143">Header</span><span class="sxs-lookup"><span data-stu-id="8bc77-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bc77-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bc77-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8bc77-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8bc77-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bc77-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bc77-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8bc77-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8bc77-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bc77-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bc77-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bc77-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bc77-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc77-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8bc77-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8bc77-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8bc77-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8bc77-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="8bc77-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





