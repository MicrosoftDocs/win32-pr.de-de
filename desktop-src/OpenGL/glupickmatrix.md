---
title: glupickmatrix-Funktion (glu. h)
description: Die Funktion "glupickmatrix" definiert einen Auswahlbereich.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- glupickmatrix-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949391"
---
# <a name="glupickmatrix-function"></a><span data-ttu-id="54e39-104">glupickmatrix-Funktion</span><span class="sxs-lookup"><span data-stu-id="54e39-104">gluPickMatrix function</span></span>

<span data-ttu-id="54e39-105">Die Funktion " **glupickmatrix** " definiert einen Auswahlbereich.</span><span class="sxs-lookup"><span data-stu-id="54e39-105">The **gluPickMatrix** function defines a picking region.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e39-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="54e39-106">Syntax</span></span>


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="54e39-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="54e39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54e39-108">*x*</span><span class="sxs-lookup"><span data-stu-id="54e39-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="54e39-109">Die x-Fenster Koordinate eines Auswahl Bereichs.</span><span class="sxs-lookup"><span data-stu-id="54e39-109">The x window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="54e39-110">*y*</span><span class="sxs-lookup"><span data-stu-id="54e39-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="54e39-111">Die y-Fenster Koordinate eines Auswahl Bereichs.</span><span class="sxs-lookup"><span data-stu-id="54e39-111">The y window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="54e39-112">*height*</span><span class="sxs-lookup"><span data-stu-id="54e39-112">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="54e39-113">Die Höhe des Auswahl Bereichs in Fenster Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="54e39-113">The height of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="54e39-114">*width*</span><span class="sxs-lookup"><span data-stu-id="54e39-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="54e39-115">Die Breite des Auswahl Bereichs in Fenster Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="54e39-115">The width of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="54e39-116">*Viewport*</span><span class="sxs-lookup"><span data-stu-id="54e39-116">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="54e39-117">Der aktuelle Viewport (wie bei einem [**glgetintegerv**](glgetintegerv.md) -Befehl).</span><span class="sxs-lookup"><span data-stu-id="54e39-117">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54e39-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54e39-118">Return value</span></span>

<span data-ttu-id="54e39-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="54e39-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e39-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54e39-120">Remarks</span></span>

<span data-ttu-id="54e39-121">Die Funktion " **glupickmatrix** " erstellt eine Projektions Matrix, die Sie verwenden können, um das Zeichnen auf einen kleinen Bereich des Viewports einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="54e39-121">The **gluPickMatrix** function creates a projection matrix you can use to restrict drawing to a small region of the viewport.</span></span>

1.  <span data-ttu-id="54e39-122">Verwenden Sie " **glupickmatrix** ", um das Zeichnen auf einen kleinen Bereich um den Cursor einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="54e39-122">Use **gluPickMatrix** to restrict drawing to a small region around the cursor.</span></span>
2.  <span data-ttu-id="54e39-123">Geben Sie den Auswahlmodus (mit [**glrendermode**](glrendermode.md)) ein, und führen Sie dann die Szene erneut aus.</span><span class="sxs-lookup"><span data-stu-id="54e39-123">Enter selection mode (with [**glRenderMode**](glrendermode.md)), and then rerender the scene.</span></span>

    <span data-ttu-id="54e39-124">Alle primitiven, die in der Nähe des Cursors gezeichnet wurden, werden im Auswahl Puffer identifiziert und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="54e39-124">All primitives that would have been drawn near the cursor are identified and stored in the selection buffer.</span></span>

<span data-ttu-id="54e39-125">Die von " **glupickmatrix** " erstellte Matrix wird mit der aktuellen Matrix so multipliziert, als wäre " [**glmultmatrix**](glmultmatrix.md) " mit der generierten Matrix aufgerufen worden.</span><span class="sxs-lookup"><span data-stu-id="54e39-125">The matrix created by **gluPickMatrix** is multiplied by the current matrix just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span>

1.  <span data-ttu-id="54e39-126">Ruft [**glLoadIdentity**](glloadidentity.md) auf, um eine Identitätsmatrix auf den Perspektiven Matrix Stapel zu laden.</span><span class="sxs-lookup"><span data-stu-id="54e39-126">Call [**glLoadIdentity**](glloadidentity.md) to load an identity matrix onto the perspective matrix stack.</span></span>
2.  <span data-ttu-id="54e39-127">Nennen Sie " **glupickmatrix**".</span><span class="sxs-lookup"><span data-stu-id="54e39-127">Call **gluPickMatrix**.</span></span>
3.  <span data-ttu-id="54e39-128">Ruft eine Funktion (z. b. " [**gluperspective**](gluperspective.md)") auf, um die Perspektiven Matrix anhand der Auswahl Matrix zu multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="54e39-128">Call a function (such as [**gluPerspective**](gluperspective.md)) to multiply the perspective matrix by the pick matrix.</span></span>

<span data-ttu-id="54e39-129">Wenn Sie " **glupickmatrix** " verwenden, um nicht einheitliche rationelle B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) auszuwählen, achten Sie darauf, die NURBS-Eigenschaft zu deaktivieren \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="54e39-129">When using **gluPickMatrix** to pick Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)), be careful to turn off the NURBS property, GLU\_AUTO\_LOAD\_MATRIX.</span></span> <span data-ttu-id="54e39-130">Wenn \_ \_ \_ die Matrix für die automatische Lastenausgleich nicht deaktiviert ist, wird jede gerenderte nursb-Oberfläche anders unterteilt, und die Auswahl Matrix wird ohne die Auswahl Matrix unterteilt.</span><span class="sxs-lookup"><span data-stu-id="54e39-130">If GLU\_AUTO\_LOAD\_MATRIX is not turned off, any NURBS surface rendered is subdivided differently with the pick matrix from how it was subdivided without the pick matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="54e39-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54e39-131">Examples</span></span>

<span data-ttu-id="54e39-132">Beim Rendern einer Szene wie folgt:</span><span class="sxs-lookup"><span data-stu-id="54e39-132">When rendering a scene as follows:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



<span data-ttu-id="54e39-133">mit dem folgenden Code wird ein Teil des Viewports ausgewählt:</span><span class="sxs-lookup"><span data-stu-id="54e39-133">the following code selects a portion of the viewport:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a><span data-ttu-id="54e39-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54e39-134">Requirements</span></span>



| <span data-ttu-id="54e39-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54e39-135">Requirement</span></span> | <span data-ttu-id="54e39-136">Wert</span><span class="sxs-lookup"><span data-stu-id="54e39-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54e39-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54e39-137">Minimum supported client</span></span><br/> | <span data-ttu-id="54e39-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54e39-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="54e39-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54e39-139">Minimum supported server</span></span><br/> | <span data-ttu-id="54e39-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54e39-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="54e39-141">Header</span><span class="sxs-lookup"><span data-stu-id="54e39-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="54e39-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="54e39-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="54e39-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54e39-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="54e39-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54e39-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="54e39-145">DLL</span><span class="sxs-lookup"><span data-stu-id="54e39-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54e39-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54e39-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54e39-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54e39-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e39-148">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="54e39-148">**glGetIntegerv**</span></span>](glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="54e39-149">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="54e39-149">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="54e39-150">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="54e39-150">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="54e39-151">**glrendermode**</span><span class="sxs-lookup"><span data-stu-id="54e39-151">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="54e39-152">**gluperspective**</span><span class="sxs-lookup"><span data-stu-id="54e39-152">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





