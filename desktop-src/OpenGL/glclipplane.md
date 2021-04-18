---
title: glclipplane-Funktion (GL. h)
description: Die glclipplane-Funktion gibt eine Ebene an, auf die die gesamte Geometrie zugeschnitten ist.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glclipplane-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337526"
---
# <a name="glclipplane-function"></a><span data-ttu-id="738a0-104">glclipplane-Funktion</span><span class="sxs-lookup"><span data-stu-id="738a0-104">glClipPlane function</span></span>

<span data-ttu-id="738a0-105">Die **glclipplane** -Funktion gibt eine Ebene an, auf die die gesamte Geometrie zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="738a0-105">The **glClipPlane** function specifies a plane against which all geometry is clipped.</span></span>

## <a name="syntax"></a><span data-ttu-id="738a0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="738a0-106">Syntax</span></span>


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="738a0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="738a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="738a0-108">*Wasser*</span><span class="sxs-lookup"><span data-stu-id="738a0-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="738a0-109">Die Clippingebene, die positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="738a0-109">The clipping plane that is being positioned.</span></span> <span data-ttu-id="738a0-110">Symbolische Namen der Form "GL \_ Clip \_ Plane *i*",  wobei es sich um eine ganze Zahl zwischen 0 und GL \_ Max \_ \_ -Clip-Plane-1 handelt, werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="738a0-110">Symbolic names of the form GL\_CLIP\_PLANE *i*, where *i* is an integer between 0 and GL\_MAX\_CLIP\_PLANES - 1, are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="738a0-111">*Gleichung*</span><span class="sxs-lookup"><span data-stu-id="738a0-111">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="738a0-112">Die Adresse eines Arrays von vier Gleit Komma Werten mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="738a0-112">The address of an array of four double-precision floating-point values.</span></span> <span data-ttu-id="738a0-113">Diese Werte werden als Gleichung der Ebene interpretiert.</span><span class="sxs-lookup"><span data-stu-id="738a0-113">These values are interpreted as a plane equation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="738a0-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="738a0-114">Return value</span></span>

<span data-ttu-id="738a0-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="738a0-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="738a0-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="738a0-116">Error codes</span></span>

<span data-ttu-id="738a0-117">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="738a0-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="738a0-118">Name</span><span class="sxs-lookup"><span data-stu-id="738a0-118">Name</span></span>                                                                                                  | <span data-ttu-id="738a0-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="738a0-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="738a0-120"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="738a0-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="738a0-121">die *Ebene* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="738a0-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="738a0-122"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="738a0-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="738a0-123">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="738a0-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="738a0-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="738a0-124">Remarks</span></span>

<span data-ttu-id="738a0-125">Geometry wird immer an die Grenzen einer sechsstufigen Frustration in *x*, *y* und *z* abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="738a0-125">Geometry is always clipped against the boundaries of a six-plane frustum in *x*, *y*, and *z*.</span></span> <span data-ttu-id="738a0-126">Die **glclipplane** -Funktion ermöglicht die Angabe zusätzlicher Ebenen, nicht notwendigerweise senkrecht zur *x-* Achse, *y-* Achse oder *z*-Achse, auf die die gesamte Geometrie zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="738a0-126">The **glClipPlane** function allows the specification of additional planes, not necessarily perpendicular to the *x-* axis, *y-* axis, or *z*-axis, against which all geometry is clipped.</span></span> <span data-ttu-id="738a0-127">Es können bis zu GL \_ Max \_ cliseplane- \_ Ebenen angegeben werden, wobei \_ Maximale clippinzfelder \_ \_ in allen Implementierungen mindestens sechs ist.</span><span class="sxs-lookup"><span data-stu-id="738a0-127">Up to GL\_MAX\_CLIP\_PLANES planes can be specified, where GL\_MAX\_CLIP\_PLANES is at least six in all implementations.</span></span> <span data-ttu-id="738a0-128">Da der sich ergebende Clippingbereich die Schnittmenge der definierten halbräume ist, wird er immer als "konform" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="738a0-128">Because the resulting clipping region is the intersection of the defined half-spaces, it is always convex.</span></span>

<span data-ttu-id="738a0-129">Die Funktion " **glclipplane** " gibt einen halben Leerraum mithilfe einer Gleichung der Ebene "vier Komponenten" an.</span><span class="sxs-lookup"><span data-stu-id="738a0-129">The **glClipPlane** function specifies a half-space using a four-component plane equation.</span></span> <span data-ttu-id="738a0-130">Wenn Sie " **glclipplane**" aufrufen, wird die *Gleichung* durch die Umkehrung der Modelview-Matrix transformiert und in den resultierenden Augen Koordinaten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="738a0-130">When you call **glClipPlane**,*equation* is transformed by the inverse of the modelview matrix and stored in the resulting eye coordinates.</span></span> <span data-ttu-id="738a0-131">Nachfolgende Änderungen an der Modelview-Matrix haben keine Auswirkungen auf die gespeicherten Ebenen-Gleichung-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="738a0-131">Subsequent changes to the modelview matrix have no effect on the stored plane-equation components.</span></span> <span data-ttu-id="738a0-132">Wenn das Punktprodukt der Augen Koordinaten eines Scheitel Punkts mit den Komponenten der gespeicherten ebenengleichung positiv oder NULL ist, befindet sich der Scheitelpunkt in Bezug auf diese Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="738a0-132">If the dot product of the eye coordinates of a vertex with the stored plane equation components is positive or zero, the vertex is in with respect to that clipping plane.</span></span> <span data-ttu-id="738a0-133">Andernfalls ist Sie Out.</span><span class="sxs-lookup"><span data-stu-id="738a0-133">Otherwise, it is out.</span></span>

<span data-ttu-id="738a0-134">Verwenden Sie die Funktionen [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) , um Clippingebenen zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="738a0-134">Use the [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions to enable and disable clipping planes.</span></span> <span data-ttu-id="738a0-135">Ruft Clippingebenen mit dem Argument GL \_ Clip \_ Plane *i* auf  , wobei die Ebenennummer ist.</span><span class="sxs-lookup"><span data-stu-id="738a0-135">Call clipping planes with the argument GL\_CLIP\_PLANE *i*, where *i* is the plane number.</span></span>

<span data-ttu-id="738a0-136">Standardmäßig werden alle Clippingebenen als (0, 0, 0, 0) in den Augen Koordinaten definiert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="738a0-136">By default, all clipping planes are defined as (0,0,0,0) in eye coordinates and are disabled.</span></span>

<span data-ttu-id="738a0-137">Es ist immer der Fall, dass GL \_ Clip \_ Plane *i* = GL \_ Clip \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="738a0-137">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="738a0-138">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glclipplane** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="738a0-138">The following functions retrieve information related to **glClipPlane**:</span></span>

[<span data-ttu-id="738a0-139">**glgetclipplane**</span><span class="sxs-lookup"><span data-stu-id="738a0-139">**glGetClipPlane**</span></span>](glgetclipplane.md)

<span data-ttu-id="738a0-140">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Clip \_ Plane *i*</span><span class="sxs-lookup"><span data-stu-id="738a0-140">[**glIsEnabled**](glisenabled.md) with argument GL\_CLIP\_PLANE *i*</span></span>

## <a name="requirements"></a><span data-ttu-id="738a0-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="738a0-141">Requirements</span></span>



| <span data-ttu-id="738a0-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="738a0-142">Requirement</span></span> | <span data-ttu-id="738a0-143">Wert</span><span class="sxs-lookup"><span data-stu-id="738a0-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="738a0-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="738a0-144">Minimum supported client</span></span><br/> | <span data-ttu-id="738a0-145">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="738a0-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="738a0-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="738a0-146">Minimum supported server</span></span><br/> | <span data-ttu-id="738a0-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="738a0-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="738a0-148">Header</span><span class="sxs-lookup"><span data-stu-id="738a0-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="738a0-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="738a0-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="738a0-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="738a0-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="738a0-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="738a0-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="738a0-152">DLL</span><span class="sxs-lookup"><span data-stu-id="738a0-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="738a0-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="738a0-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="738a0-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="738a0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738a0-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="738a0-155">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="738a0-156">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="738a0-156">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="738a0-157">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="738a0-157">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="738a0-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="738a0-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="738a0-159">**glgetclipplane**</span><span class="sxs-lookup"><span data-stu-id="738a0-159">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="738a0-160">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="738a0-160">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





