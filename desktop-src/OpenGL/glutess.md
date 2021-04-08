---
title: glutesscallback-Funktion (glu. h)
description: Die Funktion "glutesscallback" definiert einen Rückruf für ein Mosaik Objekt.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- glutesscallback-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957076"
---
# <a name="glutesscallback-function"></a><span data-ttu-id="cf343-104">glutesscallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf343-104">gluTessCallback function</span></span>

<span data-ttu-id="cf343-105">Die Funktion " **glutesscallback** " definiert einen Rückruf für ein Mosaik Objekt.</span><span class="sxs-lookup"><span data-stu-id="cf343-105">The **gluTessCallback** function defines a callback for a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf343-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf343-106">Syntax</span></span>


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="cf343-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf343-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf343-108">*ATI*</span><span class="sxs-lookup"><span data-stu-id="cf343-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="cf343-109">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="cf343-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cf343-110">*,*</span><span class="sxs-lookup"><span data-stu-id="cf343-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="cf343-111">Der Rückruf, der definiert wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-111">The callback being defined.</span></span> <span data-ttu-id="cf343-112">Die folgenden Werte sind gültig: glu \_ Tess \_ Begin, Glu \_ Tess \_ Begin \_ Data, Glu \_ Tess \_ Edge \_ Flag, Glu \_ Tess \_ Edge \_ \_ flagdaten, Glu \_ Tess \_ Vertex, Glu \_ Tess \_ Vertex \_ Data, Glu \_ Tess \_ End, Glu \_ Tess \_ End \_ Data, Glu \_ Tess \_ Combine, Glu \_ Tess \_ Combine \_ Data, Glu \_ Tess \_ Error und glu \_ Tess- \_ Fehler \_ Daten.</span><span class="sxs-lookup"><span data-stu-id="cf343-112">The following values are valid: GLU\_TESS\_BEGIN, GLU\_TESS\_BEGIN\_DATA, GLU\_TESS\_EDGE\_FLAG, GLU\_TESS\_EDGE\_FLAG\_DATA, GLU\_TESS\_VERTEX, GLU\_TESS\_VERTEX\_DATA, GLU\_TESS\_END, GLU\_TESS\_END\_DATA, GLU\_TESS\_COMBINE, GLU\_TESS\_COMBINE\_DATA, GLU\_TESS\_ERROR, and GLU\_TESS\_ERROR\_DATA.</span></span>

<span data-ttu-id="cf343-113">Weitere Informationen zu diesen Rückrufen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="cf343-113">For more information on these callbacks, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="cf343-114">*fn*</span><span class="sxs-lookup"><span data-stu-id="cf343-114">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="cf343-115">Die aufzurufende Funktion.</span><span class="sxs-lookup"><span data-stu-id="cf343-115">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf343-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf343-116">Return value</span></span>

<span data-ttu-id="cf343-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cf343-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf343-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf343-118">Remarks</span></span>

<span data-ttu-id="cf343-119">Verwenden Sie " **glutesscallback** ", um einen Rückruf anzugeben, der von einem Mosaik Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf343-119">Use **gluTessCallback** to specify a callback to be used by a tessellation object.</span></span> <span data-ttu-id="cf343-120">Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cf343-120">If the specified callback is already defined, then it is replaced.</span></span> <span data-ttu-id="cf343-121">Wenn *FN* **null** ist, wird der vorhandene Rückruf nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cf343-121">If *fn* is **NULL**, then the existing callback becomes undefined.</span></span>

<span data-ttu-id="cf343-122">Das Mosaik Objekt verwendet diese Rückrufe, um zu beschreiben, wie ein Polygon, das Sie angeben, in Dreiecke unterteilt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-122">The tessellation object uses these callbacks to describe how a polygon that you specify is broken into triangles.</span></span>

<span data-ttu-id="cf343-123">Es gibt zwei Versionen der einzelnen Rückruf, eine mit Polygon Daten, die Sie definieren können, und eine, ohne.</span><span class="sxs-lookup"><span data-stu-id="cf343-123">There are two versions of each callback, one with polygon data that you can define and one without.</span></span> <span data-ttu-id="cf343-124">Wenn beide Versionen eines bestimmten Rückrufs angegeben werden, wird der Rückruf mit den von Ihnen angegebenen Polygon Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf343-124">If both versions of a particular callback are specified, the callback with the polygon data you specify will be used.</span></span> <span data-ttu-id="cf343-125">Der *Polygon- \_ Daten* Parameter von " [**glutess beginpolygon**](glutessbeginpolygon.md) " ist eine Kopie des Zeigers, der beim Aufruf von " **glutess beginpolygon** " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cf343-125">The *polygon\_data* parameter of [**gluTessBeginPolygon**](glutessbeginpolygon.md) is a copy of the pointer that was specified when **gluTessBeginPolygon** was called.</span></span>

<span data-ttu-id="cf343-126">Im folgenden finden Sie gültige Rückrufe:</span><span class="sxs-lookup"><span data-stu-id="cf343-126">The following are valid callbacks:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf343-127">Rückruf</span><span class="sxs-lookup"><span data-stu-id="cf343-127">Callback</span></span></th>
<th><span data-ttu-id="cf343-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf343-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf343-129">GLU_TESS_BEGIN</span><span class="sxs-lookup"><span data-stu-id="cf343-129">GLU_TESS_BEGIN</span></span></td>
<td><span data-ttu-id="cf343-130">Der GLU_TESS_BEGIN Rückruf wird wie " <a href="glbegin.md"><strong>glBegin</strong></a> " aufgerufen, um den Anfang eines primitiven (Dreiecks) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cf343-130">The GLU_TESS_BEGIN callback is invoked like <a href="glbegin.md"><strong>glBegin</strong></a> to indicate the start of a (triangle) primitive.</span></span> <span data-ttu-id="cf343-131">Die Funktion nimmt ein einzelnes Argument des Typs " <strong>GLenum</strong>" an.</span><span class="sxs-lookup"><span data-stu-id="cf343-131">The function takes a single argument of type <strong>GLenum</strong>.</span></span> <span data-ttu-id="cf343-132">Wenn Sie die GLU_TESS_BOUNDARY_ONLY-Eigenschaft auf GL_FALSE festlegen, wird das-Argument entweder auf GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP oder GL_TRIANGLES festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf343-132">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_FALSE, the argument is set to either GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, or GL_TRIANGLES.</span></span> <span data-ttu-id="cf343-133">Wenn Sie die GLU_TESS_BOUNDARY_ONLY-Eigenschaft auf GL_TRUE festlegen, wird das-Argument auf GL_LINE_LOOP festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf343-133">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_TRUE, the argument is set to GL_LINE_LOOP.</span></span> <span data-ttu-id="cf343-134">Der Funktionsprototyp für diesen Rückruf lautet wie folgt: <strong>void</strong> <strong>Begin</strong> (<strong>GLenum</strong> <em>Type</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-134">The function prototype for this callback is as follows: <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>type</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf343-135">GLU_TESS_BEGIN_DATA</span><span class="sxs-lookup"><span data-stu-id="cf343-135">GLU_TESS_BEGIN_DATA</span></span></td>
<td><span data-ttu-id="cf343-136">GLU_TESS_BEGIN_DATA ist mit dem GLU_TESS_BEGIN Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt.</span><span class="sxs-lookup"><span data-stu-id="cf343-136">GLU_TESS_BEGIN_DATA is the same as the GLU_TESS_BEGIN callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="cf343-137">Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-137">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="cf343-138">Der Funktionsprototyp für diesen Rückruf ist: <strong>void</strong> <strong>begindata</strong> (<strong>GLenum</strong> <em>Type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-138">The function prototype for this callback is: <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf343-139">GLU_TESS_EDGE_FLAG</span><span class="sxs-lookup"><span data-stu-id="cf343-139">GLU_TESS_EDGE_FLAG</span></span></td>
<td><span data-ttu-id="cf343-140">Der GLU_TESS_EDGE_FLAG Rückruf ähnelt dem <a href="gledgeflag-functions.md"><strong>gledgeflag</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf343-140">The GLU_TESS_EDGE_FLAG callback is similar to <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span></span> <span data-ttu-id="cf343-141">Die Funktion nimmt ein einzelnes boolesches Flag an, das angibt, welche Ränder auf der Polygon Grenze liegen.</span><span class="sxs-lookup"><span data-stu-id="cf343-141">The function takes a single Boolean flag that indicates which edges lie on the polygon boundary.</span></span> <span data-ttu-id="cf343-142">Wenn das Flag GL_TRUE ist, beginnt jeder nachfolgende Scheitelpunkt mit einem Rand, der sich auf der Polygon Grenze befindet. Das heißt, ein Rand, der einen inneren Bereich von einem äußeren Bereich trennt.</span><span class="sxs-lookup"><span data-stu-id="cf343-142">If the flag is GL_TRUE, then each vertex that follows begins an edge that lies on the polygon boundary; that is, an edge which separates an interior region from an exterior one.</span></span> <span data-ttu-id="cf343-143">Wenn das Flag GL_FALSE ist, beginnt jeder nachfolgende Scheitelpunkt mit einem Rand im Polygon Inneren.</span><span class="sxs-lookup"><span data-stu-id="cf343-143">If the flag is GL_FALSE, then each vertex that follows begins an edge that lies in the polygon interior.</span></span> <span data-ttu-id="cf343-144">Der GLU_TESS_EDGE_FLAG Rückruf (falls definiert) wird aufgerufen, bevor der erste Vertex-Rückruf erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cf343-144">The GLU_TESS_EDGE_FLAG callback (if defined) is invoked before the first vertex callback is made.</span></span> <span data-ttu-id="cf343-145">Da Dreiecks Lüfter und Dreieck Striche keine Edge-Flags unterstützen, wird der BEGIN-Rückruf nicht mit GL_TRIANGLE_FAN oder GL_TRIANGLE_STRIP aufgerufen, wenn ein Edge-Flag-Rückruf bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-145">Because triangle fans and triangle strips do not support edge flags, the begin callback is not called with GL_TRIANGLE_FAN or GL_TRIANGLE_STRIP if an edge flag callback is provided.</span></span> <span data-ttu-id="cf343-146">Stattdessen werden die Lüfter und die Striche in unabhängige Dreiecke konvertiert.</span><span class="sxs-lookup"><span data-stu-id="cf343-146">Instead, the fans and strips are converted to independent triangles.</span></span> <span data-ttu-id="cf343-147">Der Funktionsprototyp für diesen Rückruf ist:</span><span class="sxs-lookup"><span data-stu-id="cf343-147">The function prototype for this callback is:</span></span><br/> <span data-ttu-id="cf343-148"><strong>void</strong> <strong>edgeflag</strong> (<strong>glboolean</strong> - <em>Flag</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>flag</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf343-149">GLU_TESS_EDGE_FLAG_DATA</span><span class="sxs-lookup"><span data-stu-id="cf343-149">GLU_TESS_EDGE_FLAG_DATA</span></span></td>
<td><span data-ttu-id="cf343-150">Der GLU_TESS_EDGE_FLAG_DATA Rückruf ist mit dem GLU_TESS_EDGE_FLAG Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt.</span><span class="sxs-lookup"><span data-stu-id="cf343-150">The GLU_TESS_EDGE_FLAG_DATA callback is the same as the GLU_TESS_EDGE_FLAG callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="cf343-151">Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-151">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="cf343-152">Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong> <strong>edgeflagdata</strong> (<strong>glboolean</strong> - <em>Flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-152">The function prototype for this callback is: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf343-153">GLU_TESS_VERTEX</span><span class="sxs-lookup"><span data-stu-id="cf343-153">GLU_TESS_VERTEX</span></span></td>
<td><span data-ttu-id="cf343-154">Der GLU_TESS_VERTEX Rückruf wird zwischen den Anfang-und endrückrufen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cf343-154">The GLU_TESS_VERTEX callback is invoked between the begin and end callbacks.</span></span> <span data-ttu-id="cf343-155">Sie ähnelt glVertex und definiert die vertexen der Dreiecke, die vom Mosaik Prozess erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cf343-155">It is similar to glVertex , and it defines the vertexes of the triangles created by the tessellation process.</span></span> <span data-ttu-id="cf343-156">Die Funktion nimmt einen Zeiger als einziges Argument an.</span><span class="sxs-lookup"><span data-stu-id="cf343-156">The function takes a pointer as its only argument.</span></span> <span data-ttu-id="cf343-157">Dieser Zeiger ist mit dem nicht transparenten Zeiger identisch, den Sie beim Definieren des Scheitel Punkts angegeben haben (siehe " <a href="glutessvertex.md"><strong>glutess Scheitel</strong></a>Punkt").</span><span class="sxs-lookup"><span data-stu-id="cf343-157">This pointer is identical to the opaque pointer that you provided when you defined the vertex (see <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span></span> <span data-ttu-id="cf343-158">Der Funktionsprototyp für diesen Rückruf ist: <strong>void</strong> <strong>Scheitel</strong> Punkt (<strong>void</strong> \* <em>vertex_data</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-158">The function prototype for this callback is: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf343-159">GLU_TESS_VERTEX_DATA</span><span class="sxs-lookup"><span data-stu-id="cf343-159">GLU_TESS_VERTEX_DATA</span></span></td>
<td><span data-ttu-id="cf343-160">Der GLU_TESS_VERTEX_DATA ist mit dem GLU_TESS_VERTEX Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt.</span><span class="sxs-lookup"><span data-stu-id="cf343-160">The GLU_TESS_VERTEX_DATA is the same as the GLU_TESS_VERTEX callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="cf343-161">Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-161">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="cf343-162">Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong>  <strong>vertexdata</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-162">The function prototype for this callback is: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf343-163">GLU_TESS_END</span><span class="sxs-lookup"><span data-stu-id="cf343-163">GLU_TESS_END</span></span></td>
<td><span data-ttu-id="cf343-164">Der GLU_TESS_END Rückruf erfüllt den gleichen Zweck wie <a href="glend.md"><strong>glEnd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf343-164">The GLU_TESS_END callback serves the same purpose as <a href="glend.md"><strong>glEnd</strong></a>.</span></span> <span data-ttu-id="cf343-165">Er gibt das Ende eines primitiven an und übernimmt keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="cf343-165">It indicates the end of a primitive, and it takes no arguments.</span></span> <span data-ttu-id="cf343-166">Der Funktionsprototyp für diesen Rückruf ist: <strong>void</strong> <strong>End</strong> (<strong>void</strong>);</span><span class="sxs-lookup"><span data-stu-id="cf343-166">The function prototype for this callback is: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf343-167">GLU_TESS_END_DATA</span><span class="sxs-lookup"><span data-stu-id="cf343-167">GLU_TESS_END_DATA</span></span></td>
<td><span data-ttu-id="cf343-168">Der GLU_TESS_END_DATA Rückruf ist mit dem GLU_TESS_END Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt.</span><span class="sxs-lookup"><span data-stu-id="cf343-168">The GLU_TESS_END_DATA callback is the same as the GLU_TESS_END callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="cf343-169">Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-169">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="cf343-170">Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-170">The function prototype for this callback is: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf343-171">GLU_TESS_COMBINE</span><span class="sxs-lookup"><span data-stu-id="cf343-171">GLU_TESS_COMBINE</span></span></td>
<td><span data-ttu-id="cf343-172">Rufen Sie den GLU_TESS_COMBINE Rückruf auf, um einen neuen Scheitelpunkt zu erstellen, wenn das Mosaik eine Schnittmenge erkennt, oder um die Funktionen zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="cf343-172">Call the GLU_TESS_COMBINE callback to create a new vertex when the tessellation detects an intersection, or to merge features.</span></span> <span data-ttu-id="cf343-173">Die Funktion nimmt vier Argumente an: ein Array mit drei Elementen, jeweils vom Typ gldouble.</span><span class="sxs-lookup"><span data-stu-id="cf343-173">The function takes four arguments: An array of three elements, each of type Gldouble.</span></span><br/> <span data-ttu-id="cf343-174">Ein Array von vier Zeigern.</span><span class="sxs-lookup"><span data-stu-id="cf343-174">An array of four pointers.</span></span><br/> <span data-ttu-id="cf343-175">Ein Array von vier Elementen, jeweils vom Typ "glfloat".</span><span class="sxs-lookup"><span data-stu-id="cf343-175">An array of four elements, each of type GLfloat.</span></span><br/> <span data-ttu-id="cf343-176">Ein Zeiger auf einen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="cf343-176">A pointer to a pointer.</span></span><br/> <span data-ttu-id="cf343-177">Der Funktionsprototyp für diesen Rückruf ist:</span><span class="sxs-lookup"><span data-stu-id="cf343-177">The function prototype for this callback is:</span></span> <br/> <span data-ttu-id="cf343-178"><strong>void</strong> <strong>Combine</strong>(<strong>gldouble</strong> <em>CoOrds</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>glfloat</strong> <em>Weight</em>[4], <strong>void</strong>  \*\* <em>OutData</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>);</span></span><br/> <span data-ttu-id="cf343-179">Der Scheitelpunkt ist eine lineare Kombination aus bis zu vier vorhandenen vertexen, die in vertex_data gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cf343-179">The vertex is defined as a linear combination of up to four existing vertexes, stored in vertex_data.</span></span> <span data-ttu-id="cf343-180">Die Koeffizienten der linearen Kombination werden durch Gewichtung angegeben. Diese Gewichtungen summieren immer auf 1,0.</span><span class="sxs-lookup"><span data-stu-id="cf343-180">The coefficients of the linear combination are given by weight; these weights always sum to 1.0.</span></span> <span data-ttu-id="cf343-181">Alle Scheitelpunkt Zeiger sind gültig, auch wenn einige der Gewichtungen NULL sind.</span><span class="sxs-lookup"><span data-stu-id="cf343-181">All vertex pointers are valid even when some of the weights are zero.</span></span> <span data-ttu-id="cf343-182">Der CoOrds-Parameter gibt den Speicherort des neuen Scheitel Punkts an.</span><span class="sxs-lookup"><span data-stu-id="cf343-182">The coords parameter gives the location of the new vertex.</span></span><br/> <span data-ttu-id="cf343-183">Weisen Sie einen anderen Scheitelpunkt zu, interpolieren Sie Parameter mit vertex_data und Gewichtung, und geben Sie den neuen Scheitelpunkt Zeiger in OutData zurück.</span><span class="sxs-lookup"><span data-stu-id="cf343-183">Allocate another vertex, interpolate parameters using vertex_data and weight, and return the new vertex pointer in outData.</span></span> <span data-ttu-id="cf343-184">Dieses Handle wird während der Rendering-Rückrufe bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cf343-184">This handle is supplied during rendering callbacks.</span></span> <span data-ttu-id="cf343-185">Freigeben von Arbeitsspeicher nach dem Aufrufen von " <a href="glutessendpolygon.md"><strong>glutessendpolygon</strong></a>".</span><span class="sxs-lookup"><span data-stu-id="cf343-185">Free the memory sometime after calling <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span></span><br/> <span data-ttu-id="cf343-186">Wenn das Polygon z. b. in einer beliebigen Ebene im dreidimensionalen Raum liegt und Sie jedem Scheitelpunkt eine Farbe zuordnen, könnte der GLU_TESS_COMBINE Rückruf wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="cf343-186">For example, if the polygon lies in an arbitrary plane in three-dimensional space, and you associate a color with each vertex, the GLU_TESS_COMBINE callback might look like the following:</span></span><br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
<span data-ttu-id="cf343-187">Wenn das Mosaik eine Schnittmenge erkennt, muss die GLU_TESS_COMBINE oder GLU_TESS_COMBINE_DATA Rückrufs (siehe unten) definiert sein, und es muss ein nicht-<strong>null</strong> -Zeiger in dataout geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cf343-187">When the tessellation detects an intersection, the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback (see below) must be defined, and must write a non-<strong>NULL</strong> pointer into dataOut.</span></span> <span data-ttu-id="cf343-188">Andernfalls tritt der GLU_TESS_NEED_COMBINE_CALLBACK Fehler auf, und es wird keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="cf343-188">Otherwise the GLU_TESS_NEED_COMBINE_CALLBACK error occurs, and no output is generated.</span></span> <span data-ttu-id="cf343-189">(Dies ist der einzige Fehler, der während des Mosaik-und Renderings auftreten kann.)</span><span class="sxs-lookup"><span data-stu-id="cf343-189">(This is the only error that can occur during tessellation and rendering.)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf343-190">GLU_TESS_COMBINE_DATA</span><span class="sxs-lookup"><span data-stu-id="cf343-190">GLU_TESS_COMBINE_DATA</span></span></td>
<td><span data-ttu-id="cf343-191">Der GLU_TESS_COMBINE_DATA Rückruf ist mit dem GLU_TESS_COMBINE Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt.</span><span class="sxs-lookup"><span data-stu-id="cf343-191">The GLU_TESS_COMBINE_DATA callback is the same as the GLU_TESS_COMBINE callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="cf343-192">Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-192">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="cf343-193">Der Funktionsprototyp für diesen Rückruf ist " <strong>void</strong> <strong>combinedata</strong> (<strong>gldouble</strong> <em>CoOrds</em>[3]", " <strong>void</strong> \*<em>vertex_data</em>[4]", " <strong>glfloat</strong> <em>Weight</em>[4]", " <strong>void</strong>  \*\* <em>OutData</em>", " <strong>void</strong> \* <em>polygon_data</em>");</span><span class="sxs-lookup"><span data-stu-id="cf343-193">The function prototype for this callback is: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf343-194">GLU_TESS_ERROR</span><span class="sxs-lookup"><span data-stu-id="cf343-194">GLU_TESS_ERROR</span></span></td>
<td><span data-ttu-id="cf343-195">Der GLU_TESS_ERROR Rückruf wird aufgerufen, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="cf343-195">The GLU_TESS_ERROR callback is called when an error is encountered.</span></span> <span data-ttu-id="cf343-196">Das einzige Argument ist vom Typ " <strong>GLenum</strong>". Gibt den spezifischen Fehler an, der aufgetreten ist, und wird auf einen der folgenden festgelegt: GLU_TESS_MISSING_BEGIN_POLYGON</span><span class="sxs-lookup"><span data-stu-id="cf343-196">The one argument is of type <strong>GLenum</strong>; it indicates the specific error that occurred and is set to one of the following: GLU_TESS_MISSING_BEGIN_POLYGON</span></span><br/> <span data-ttu-id="cf343-197">GLU_TESS_MISSING_END_POLYGON</span><span class="sxs-lookup"><span data-stu-id="cf343-197">GLU_TESS_MISSING_END_POLYGON</span></span><br/> <span data-ttu-id="cf343-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="cf343-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span></span><br/> <span data-ttu-id="cf343-199">GLU_TESS_MISSING_END_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="cf343-199">GLU_TESS_MISSING_END_CONTOUR</span></span><br/> <span data-ttu-id="cf343-200">GLU_TESS_COORD_TOO_LARGE</span><span class="sxs-lookup"><span data-stu-id="cf343-200">GLU_TESS_COORD_TOO_LARGE</span></span><br/> <span data-ttu-id="cf343-201">GLU_TESS_NEED_COMBINE_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="cf343-201">GLU_TESS_NEED_COMBINE_CALLBACK</span></span><br/> <span data-ttu-id="cf343-202">Rufen Sie zum Abrufen von Zeichen folgen, die diese Fehler beschreiben, die Zeichen folgen auf.</span><span class="sxs-lookup"><span data-stu-id="cf343-202">Call gluErrorString to retrieve character strings describing these errors.</span></span> <span data-ttu-id="cf343-203">Der Funktionsprototyp für diesen Rückruf lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cf343-203">The function prototype for this callback is as follows:</span></span><br/> <span data-ttu-id="cf343-204"><strong>void</strong> - <strong>Fehler</strong> (<strong>GLenum</strong> <em>errno</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-204"><strong>void</strong> <strong>error</strong> (<strong>GLenum</strong> <em>errno</em>);</span></span><br/> <span data-ttu-id="cf343-205">Die glu-Bibliothek stellt die ersten vier Fehler wieder her, indem Sie den fehlenden Aufruf oder die fehlenden Aufrufe einfügt.</span><span class="sxs-lookup"><span data-stu-id="cf343-205">The GLU library recovers from the first four errors by inserting the missing call or calls.</span></span> <span data-ttu-id="cf343-206">GLU_TESS_COORD_TOO_LARGE gibt an, dass die Vertex-Koordinate die vordefinierte Konstante GLU_TESS_MAX_COORD in absoluten Wert überschritten hat und dass der Wert gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="cf343-206">GLU_TESS_COORD_TOO_LARGE indicates that some vertex coordinate exceeded the predefined constant GLU_TESS_MAX_COORD in absolute value, and that the value has been clamped.</span></span> <span data-ttu-id="cf343-207">(Koordinaten Werte müssen klein genug sein, damit zwei ohne Überlauf multipliziert werden können.) GLU_TESS_NEED_COMBINE_CALLBACK gibt an, dass das Mosaik eine Überschneidung zwischen zwei Kanten in den Eingabedaten erkannt hat und der GLU_TESS_COMBINE oder GLU_TESS_COMBINE_DATA Rückruf nicht bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cf343-207">(Coordinate values must be small enough that two can be multiplied together without overflow.) GLU_TESS_NEED_COMBINE_CALLBACK indicates that the tessellation detected an intersection between two edges in the input data, and the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback was not provided.</span></span> <span data-ttu-id="cf343-208">Es wird keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="cf343-208">No output will be generated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf343-209">GLU_TESS_ERROR_DATA</span><span class="sxs-lookup"><span data-stu-id="cf343-209">GLU_TESS_ERROR_DATA</span></span></td>
<td><span data-ttu-id="cf343-210">Der GLU_TESS_ERROR_DATA Rückruf ist mit dem GLU_TESS_ERROR Rückruf identisch, mit dem Unterschied, dass er ein zusätzliches Zeigerargument annimmt.</span><span class="sxs-lookup"><span data-stu-id="cf343-210">The GLU_TESS_ERROR_DATA callback is the same as the GLU_TESS_ERROR callback, except that it takes an additional pointer argument.</span></span> <span data-ttu-id="cf343-211">Dieser Zeiger ist mit dem opaken Zeiger identisch, der beim Aufrufen von " <a href="glutessbeginpolygon.md"><strong>glutess beginpolygon</strong></a>" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-211">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="cf343-212">Der Funktionsprototyp für diesen Rückruf lautet: <strong>void</strong> <strong>ErrorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="cf343-212">The function prototype for this callback is: <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="cf343-213">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf343-213">Requirements</span></span>



| <span data-ttu-id="cf343-214">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf343-214">Requirement</span></span> | <span data-ttu-id="cf343-215">Wert</span><span class="sxs-lookup"><span data-stu-id="cf343-215">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf343-216">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf343-216">Minimum supported client</span></span><br/> | <span data-ttu-id="cf343-217">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf343-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cf343-218">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf343-218">Minimum supported server</span></span><br/> | <span data-ttu-id="cf343-219">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf343-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cf343-220">Header</span><span class="sxs-lookup"><span data-stu-id="cf343-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf343-221"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf343-221"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cf343-222">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf343-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf343-223"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf343-223"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf343-224">DLL</span><span class="sxs-lookup"><span data-stu-id="cf343-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf343-225"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf343-225"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf343-226">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf343-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf343-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cf343-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cf343-228">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="cf343-228">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="cf343-229">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cf343-229">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cf343-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="cf343-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> <dt>

[<span data-ttu-id="cf343-231">**gludeletetess**</span><span class="sxs-lookup"><span data-stu-id="cf343-231">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="cf343-232">**gluerrorstring**</span><span class="sxs-lookup"><span data-stu-id="cf343-232">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="cf343-233">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="cf343-233">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="cf343-234">**glutess beginpolygon**</span><span class="sxs-lookup"><span data-stu-id="cf343-234">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="cf343-235">**glutessendpolygon**</span><span class="sxs-lookup"><span data-stu-id="cf343-235">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="cf343-236">**glutess Vertex**</span><span class="sxs-lookup"><span data-stu-id="cf343-236">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





