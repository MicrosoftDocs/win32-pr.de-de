---
title: glrectdv-Funktion (GL. h)
description: Die Funktion "glrectdv" zeichnet ein Rechteck.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- glrectdv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRectdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2956a1f658101a384ae69b05ed50418492d264
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391537"
---
# <a name="glrectdv-function"></a><span data-ttu-id="9d3ac-104">glrectdv-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d3ac-104">glRectdv function</span></span>

<span data-ttu-id="9d3ac-105">Die Funktion " **glrectdv** " zeichnet ein Rechteck.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-105">The **glRectdv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3ac-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d3ac-106">Syntax</span></span>


```C++
void WINAPI glRectdv(
   const GLdouble *v1,
   const GLdouble *v2
);
```



## <a name="parameters"></a><span data-ttu-id="9d3ac-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d3ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d3ac-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="9d3ac-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3ac-109">Ein Zeiger auf einen Scheitelpunkt eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="9d3ac-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="9d3ac-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3ac-111">Ein Zeiger auf den umgekehrten Scheitelpunkt des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d3ac-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d3ac-112">Return value</span></span>

<span data-ttu-id="9d3ac-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d3ac-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9d3ac-114">Error codes</span></span>

<span data-ttu-id="9d3ac-115">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9d3ac-116">Name</span><span class="sxs-lookup"><span data-stu-id="9d3ac-116">Name</span></span>                                                                                                  | <span data-ttu-id="9d3ac-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9d3ac-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d3ac-118"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="9d3ac-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9d3ac-119">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9d3ac-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d3ac-120">Remarks</span></span>

<span data-ttu-id="9d3ac-121">Die **glrectd** -Funktion unterstützt die effiziente Angabe von Rechtecke als zwei Eckpunkte.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-121">The **glRectd** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="9d3ac-122">Jeder Rechteck Befehl benötigt vier Argumente, die entweder als zwei aufeinander folgende Paare von (*x*, *y*)-Koordinaten oder als zwei Zeiger auf Arrays angeordnet sind, die jeweils ein (*x*, *y*)-Paar enthalten.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="9d3ac-123">Das resultierende Rechteck wird in der *z* = 0-Ebene definiert.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="9d3ac-124">Die Funktion " **glrectd**(*x1,* *Y1,* *x2,* *Y2*)" entspricht genau der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="9d3ac-124">The **glRectd**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="9d3ac-125">**glBegin**(GL- \_ Polygon);</span><span class="sxs-lookup"><span data-stu-id="9d3ac-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="9d3ac-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="9d3ac-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="9d3ac-127">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="9d3ac-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="9d3ac-128">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="9d3ac-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="9d3ac-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="9d3ac-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="9d3ac-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="9d3ac-130">**glEnd**( );</span></span>

<span data-ttu-id="9d3ac-131">Beachten Sie Folgendes: Wenn sich der zweite Scheitelpunkt oberhalb und rechts vom ersten Scheitelpunkt befindet, wird das Rechteck mit einem gegen Uhrzeigersinn konstruiert.</span><span class="sxs-lookup"><span data-stu-id="9d3ac-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d3ac-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d3ac-132">Requirements</span></span>



| <span data-ttu-id="9d3ac-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d3ac-133">Requirement</span></span> | <span data-ttu-id="9d3ac-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9d3ac-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3ac-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d3ac-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9d3ac-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d3ac-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d3ac-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d3ac-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9d3ac-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d3ac-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d3ac-139">Header</span><span class="sxs-lookup"><span data-stu-id="9d3ac-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d3ac-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d3ac-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9d3ac-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d3ac-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d3ac-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d3ac-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d3ac-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9d3ac-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d3ac-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d3ac-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d3ac-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d3ac-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3ac-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9d3ac-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9d3ac-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9d3ac-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9d3ac-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="9d3ac-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





