---
title: glunurbssurface-Funktion (glu. h)
description: Die Funktion "glunurbssurface" definiert die Form einer nicht einheitlichen Oberfläche von rationalem B-Spline (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- glunurbssurface-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949392"
---
# <a name="glunurbssurface-function"></a><span data-ttu-id="6a44c-104">glunurbssurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="6a44c-104">gluNurbsSurface function</span></span>

<span data-ttu-id="6a44c-105">Die Funktion " **glunurbssurface** " definiert die Form einer nicht einheitlichen Oberfläche von rationalem B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="6a44c-105">The **gluNurbsSurface** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a44c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a44c-106">Syntax</span></span>


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="6a44c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a44c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a44c-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="6a44c-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-109">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="6a44c-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-110">*Anzahl von SKUs \_*</span><span class="sxs-lookup"><span data-stu-id="6a44c-110">*sknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-111">Die Anzahl der Knoten in der Richtung der parametrischen *u* .</span><span class="sxs-lookup"><span data-stu-id="6a44c-111">The number of knots in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-112">*sknot*</span><span class="sxs-lookup"><span data-stu-id="6a44c-112">*sknot*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-113">Ein Array von *sknot \_ count* -Werten, die sich in der parametrischen *u* -Richtung nicht verkleinern.</span><span class="sxs-lookup"><span data-stu-id="6a44c-113">An array of *sknot\_count* nondecreasing knot values in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-114">*\_tknotenanzahl*</span><span class="sxs-lookup"><span data-stu-id="6a44c-114">*tknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-115">Die Anzahl der Knoten in der parametrischen *v* -Richtung.</span><span class="sxs-lookup"><span data-stu-id="6a44c-115">The number of knots in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-116">*tknot*</span><span class="sxs-lookup"><span data-stu-id="6a44c-116">*tknot*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-117">Ein Array von *tknot \_* -Werten, die sich in der parametrischen *v* -Richtung nicht verkleinern.</span><span class="sxs-lookup"><span data-stu-id="6a44c-117">An array of *tknot\_count* nondecreasing knot values in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-118">*s \_ Stride*</span><span class="sxs-lookup"><span data-stu-id="6a44c-118">*s\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-119">Der Offset (als eine Reihe einzelner Werte für den Wert für die Genauigkeit) zwischen aufeinander folgenden Steuerungs Punkten in der parametrisierten *u* -Richtung in *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="6a44c-119">The offset (as a number of single precisionfloating-point values) between successive control points in the parametric *u* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-120">*t \_ Stride*</span><span class="sxs-lookup"><span data-stu-id="6a44c-120">*t\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-121">Der Offset (in einzelnen Werten mit Werten für den Gleit Komma Wert) zwischen aufeinander folgenden Kontrollpunkten in der parametrisierten *v* -Richtung in *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="6a44c-121">The offset (in single precisionfloating-point values) between successive control points in the parametric *v* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-122">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="6a44c-122">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-123">Ein Array, das Steuerungs Punkte für die nursb-Oberfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="6a44c-123">An array containing control points for the NURBS surface.</span></span> <span data-ttu-id="6a44c-124">Die Offsets zwischen aufeinander folgenden Kontrollpunkten in den parametrischen *u* -und *v* -Richtungen werden von *s \_ Stride* und *t \_ Stride* angegeben.</span><span class="sxs-lookup"><span data-stu-id="6a44c-124">The offsets between successive control points in the parametric *u* and *v* directions are given by *s\_stride* and *t\_stride*.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-125">*sorder*</span><span class="sxs-lookup"><span data-stu-id="6a44c-125">*sorder*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-126">Die Reihenfolge der nursb-Oberfläche in der Richtung der parametrischen *u* .</span><span class="sxs-lookup"><span data-stu-id="6a44c-126">The order of the NURBS surface in the parametric *u* direction.</span></span> <span data-ttu-id="6a44c-127">Die Reihenfolge ist um eins größer als der Grad. Daher hat eine Oberfläche in *u* eine vier *-Reihenfolge* .</span><span class="sxs-lookup"><span data-stu-id="6a44c-127">The order is one more than the degree, hence a surface that is cubic in *u* has a *u* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-128">*der Tor*</span><span class="sxs-lookup"><span data-stu-id="6a44c-128">*torder*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-129">Die Reihenfolge der nursb-Oberfläche in der parametrischen *v* -Richtung.</span><span class="sxs-lookup"><span data-stu-id="6a44c-129">The order of the NURBS surface in the parametric *v* direction.</span></span> <span data-ttu-id="6a44c-130">Die Reihenfolge ist um eins größer als der Grad. Daher hat eine Oberfläche in *v* die *v* -Reihenfolge 4.</span><span class="sxs-lookup"><span data-stu-id="6a44c-130">The order is one more than the degree, hence a surface that is cubic in *v* has a *v* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="6a44c-131">*type*</span><span class="sxs-lookup"><span data-stu-id="6a44c-131">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="6a44c-132">Der Typ der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="6a44c-132">The type of the surface.</span></span> <span data-ttu-id="6a44c-133">Der *Typparameter* kann einer der gültigen zweidimensionalen auswerterypen sein (z \_ . b. gl map2 \_ Vertex \_ 3 oder GL \_ map2 \_ Color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="6a44c-133">The *type* parameter can be any of the valid two-dimensional evaluator types (such as GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_COLOR\_4).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a44c-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a44c-134">Return value</span></span>

<span data-ttu-id="6a44c-135">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6a44c-135">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a44c-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a44c-136">Remarks</span></span>

<span data-ttu-id="6a44c-137">Verwenden Sie **glunurbssurface** innerhalb einer nurb-Oberflächen Definition, um die Form einer nurb-Oberfläche (vor jeder Kürzung) zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6a44c-137">Use **gluNurbsSurface** within a NURBS surface definition to describe the shape of a NURBS surface (before any trimming).</span></span> <span data-ttu-id="6a44c-138">Verwenden Sie die Funktion " [**glubeginsurface**](glubeginsurface.md) ", um den Anfang einer nurist-Oberflächen Definition zu markieren.</span><span class="sxs-lookup"><span data-stu-id="6a44c-138">To mark the beginning of a NURBS surface definition, use the [**gluBeginSurface**](glubeginsurface.md) function.</span></span> <span data-ttu-id="6a44c-139">Verwenden Sie die Funktion " [**gluendsurface**](gluendsurface.md) ", um das Ende einer nurist-Oberflächen Definition zu markieren.</span><span class="sxs-lookup"><span data-stu-id="6a44c-139">To mark the end of a NURBS surface definition, use the [**gluEndSurface**](gluendsurface.md) function.</span></span> <span data-ttu-id="6a44c-140">Der Befehl " **glunurbssurface** " wird nur innerhalb einer nurb-Oberflächen Definition aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6a44c-140">Call **gluNurbsSurface** within a NURBS surface definition only.</span></span>

<span data-ttu-id="6a44c-141">Sie ordnen positionelle, Textur-und Farbkoordinaten einer Oberfläche zu, indem Sie diese als separate **glunurbssurface** zwischen einem **glubeginsurface**- / **gluendsurface** -paar darstellen.</span><span class="sxs-lookup"><span data-stu-id="6a44c-141">You associate positional, texture, and color coordinates with a surface by presenting each as a separate **gluNurbsSurface** between a **gluBeginSurface**/**gluEndSurface** pair.</span></span> <span data-ttu-id="6a44c-142">Innerhalb eines einzelnen " **glubeginsurface** / **gluendsurface** "-Paars können Sie nur einen Aufrufen von " **glunurbssurface** " für Farbe, Position und Textur Daten erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a44c-142">Within a single **gluBeginSurface**/**gluEndSurface** pair, you can make only one call to **gluNurbsSurface** for color, position, and texture data.</span></span> <span data-ttu-id="6a44c-143">Machen Sie genau einen Aufrufs, um die Position der Oberfläche zu beschreiben (ein *Typ* von GL \_ map2 \_ Vertex \_ 3 oder GL \_ map2 \_ Scheitelpunkt \_ 4).</span><span class="sxs-lookup"><span data-stu-id="6a44c-143">Make exactly one call to describe the position of the surface (a *type* of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4).</span></span>

<span data-ttu-id="6a44c-144">Sie können eine nurb-Oberfläche mit den Funktionen " [**glunurbscurve**](glunurbscurve.md) " und " [**glupwlcurve**](glupwlcurve.md) " zwischen Aufrufen von " [**glubegintrim**](glubegintrim.md) " und " [**gluendtrim**](gluendtrim.md)" kürzen.</span><span class="sxs-lookup"><span data-stu-id="6a44c-144">You can trim a NURBS surface by using the [**gluNurbsCurve**](glunurbscurve.md) and [**gluPwlCurve**](glupwlcurve.md) functions between calls to [**gluBeginTrim**](glubegintrim.md) and [**gluEndTrim**](gluendtrim.md).</span></span>

<span data-ttu-id="6a44c-145">Ein **glunurbssurface** mit *sknot \_ count* -Knoten in der *u* -Richtung und *tknot- \_ Zähler* in der *v* -Richtung mit Orders *sorder* und *torder* müssen (*sknicht \_ count*  - *sorder*) multipied by-Steuerungs Punkte (*tknot \_ count*  - *torder*) enthalten.</span><span class="sxs-lookup"><span data-stu-id="6a44c-145">A **gluNurbsSurface** with *sknot\_count* knots in the *u* direction and *tknot\_count* knots in the *v* direction with orders *sorder* and *torder* must have (*sknot\_count* -*sorder*) multipied by (*tknot\_count* -*torder*) control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a44c-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a44c-146">Requirements</span></span>



| <span data-ttu-id="6a44c-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a44c-147">Requirement</span></span> | <span data-ttu-id="6a44c-148">Wert</span><span class="sxs-lookup"><span data-stu-id="6a44c-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6a44c-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a44c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6a44c-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a44c-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6a44c-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a44c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6a44c-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a44c-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6a44c-153">Header</span><span class="sxs-lookup"><span data-stu-id="6a44c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a44c-154"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a44c-154"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6a44c-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a44c-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a44c-156"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a44c-156"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6a44c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6a44c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a44c-158"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a44c-158"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a44c-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a44c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a44c-160">**glubeginsurface**</span><span class="sxs-lookup"><span data-stu-id="6a44c-160">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="6a44c-161">**glubegintrim**</span><span class="sxs-lookup"><span data-stu-id="6a44c-161">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="6a44c-162">**gluendsurface**</span><span class="sxs-lookup"><span data-stu-id="6a44c-162">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="6a44c-163">**gluendtrim**</span><span class="sxs-lookup"><span data-stu-id="6a44c-163">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="6a44c-164">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="6a44c-164">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="6a44c-165">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="6a44c-165">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="6a44c-166">**glupwlcurve**</span><span class="sxs-lookup"><span data-stu-id="6a44c-166">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





