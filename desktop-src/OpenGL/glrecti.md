---
title: glrecti-Funktion (GL. h)
description: Die glrecti-Funktion zeichnet ein Rechteck.
ms.assetid: 8f618b5e-5406-4342-8f7a-83a65bad8a6f
keywords:
- glrecti-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRecti
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a17512c9720aea1d2b9dcf5c90b0bde4c67b8fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475249"
---
# <a name="glrecti-function"></a><span data-ttu-id="f7093-104">glrecti-Funktion</span><span class="sxs-lookup"><span data-stu-id="f7093-104">glRecti function</span></span>

<span data-ttu-id="f7093-105">Die **glrecti** -Funktion zeichnet ein Rechteck.</span><span class="sxs-lookup"><span data-stu-id="f7093-105">The **glRecti** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7093-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7093-106">Syntax</span></span>


```C++
void WINAPI glRecti(
   GLint x1,
   GLint y1,
   GLint x2,
   GLint y2
);
```



## <a name="parameters"></a><span data-ttu-id="f7093-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7093-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7093-108">*x1*</span><span class="sxs-lookup"><span data-stu-id="f7093-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="f7093-109">Die *x* -Koordinate des Scheitel Punkts eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="f7093-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="f7093-110">*y1*</span><span class="sxs-lookup"><span data-stu-id="f7093-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="f7093-111">Die *y* -Koordinate des Scheitel Punkts eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="f7093-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="f7093-112">*x2*</span><span class="sxs-lookup"><span data-stu-id="f7093-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="f7093-113">Die *x* -Koordinate des umgekehrten Scheitel Punkts des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="f7093-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="f7093-114">*Y2*</span><span class="sxs-lookup"><span data-stu-id="f7093-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="f7093-115">Die *y* -Koordinate des umgekehrten Scheitel Punkts des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="f7093-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7093-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7093-116">Return value</span></span>

<span data-ttu-id="f7093-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f7093-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7093-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f7093-118">Error codes</span></span>

<span data-ttu-id="f7093-119">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f7093-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f7093-120">Name</span><span class="sxs-lookup"><span data-stu-id="f7093-120">Name</span></span>                                                                                                  | <span data-ttu-id="f7093-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f7093-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7093-122"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f7093-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f7093-123">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f7093-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f7093-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7093-124">Remarks</span></span>

<span data-ttu-id="f7093-125">Die **glrecti** -Funktion unterstützt die effiziente Angabe von Rechtecke als zwei Eckpunkte.</span><span class="sxs-lookup"><span data-stu-id="f7093-125">The **glRecti** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="f7093-126">Jeder Rechteck Befehl benötigt vier Argumente, die entweder als zwei aufeinander folgende Paare von (*x*, *y*)-Koordinaten oder als zwei Zeiger auf Arrays angeordnet sind, die jeweils ein (*x*, *y*)-Paar enthalten.</span><span class="sxs-lookup"><span data-stu-id="f7093-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="f7093-127">Das resultierende Rechteck wird in der *z* = 0-Ebene definiert.</span><span class="sxs-lookup"><span data-stu-id="f7093-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="f7093-128">Die Funktion " **glrecti**(*x1,* *Y1,* *x2,* *Y2*)" entspricht genau der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="f7093-128">The **glRecti**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="f7093-129">**glBegin**(GL- \_ Polygon);</span><span class="sxs-lookup"><span data-stu-id="f7093-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="f7093-130">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="f7093-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="f7093-131">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="f7093-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="f7093-132">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="f7093-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="f7093-133">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="f7093-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="f7093-134">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="f7093-134">**glEnd**( );</span></span>

<span data-ttu-id="f7093-135">Beachten Sie Folgendes: Wenn sich der zweite Scheitelpunkt oberhalb und rechts vom ersten Scheitelpunkt befindet, wird das Rechteck mit einem gegen Uhrzeigersinn konstruiert.</span><span class="sxs-lookup"><span data-stu-id="f7093-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7093-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7093-136">Requirements</span></span>



| <span data-ttu-id="f7093-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7093-137">Requirement</span></span> | <span data-ttu-id="f7093-138">Wert</span><span class="sxs-lookup"><span data-stu-id="f7093-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7093-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7093-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f7093-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7093-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f7093-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7093-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f7093-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7093-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7093-143">Header</span><span class="sxs-lookup"><span data-stu-id="f7093-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7093-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7093-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f7093-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7093-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7093-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7093-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7093-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f7093-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7093-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7093-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7093-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7093-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7093-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f7093-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f7093-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f7093-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f7093-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="f7093-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





