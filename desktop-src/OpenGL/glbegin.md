---
title: glBegin-Funktion (GL. h)
description: Die Funktionen "glBegin" und "glEnd" begrenzen die Scheitel Punkte eines primitiven oder einer Gruppe von ähnlichen primitiven. | glBegin-Funktion (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- glBegin-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961424"
---
# <a name="glbegin-function"></a><span data-ttu-id="ba75b-105">glBegin-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba75b-105">glBegin function</span></span>

<span data-ttu-id="ba75b-106">Die Funktionen " **glBegin** " und " [**glEnd**](glend.md) " begrenzen die Scheitel Punkte eines primitiven oder einer Gruppe von ähnlichen primitiven.</span><span class="sxs-lookup"><span data-stu-id="ba75b-106">The **glBegin** and [**glend**](glend.md) functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba75b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba75b-107">Syntax</span></span>


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="ba75b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba75b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba75b-109">*mode*</span><span class="sxs-lookup"><span data-stu-id="ba75b-109">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="ba75b-110">Die primitiven oder primitiven, die aus Scheitel Punkten erstellt werden, die zwischen **glBegin** und dem nachfolgenden [**glEnd**](glend.md)dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ba75b-110">The primitive or primitives that will be created from vertices presented between **glBegin** and the subsequent [**glend**](glend.md).</span></span> <span data-ttu-id="ba75b-111">Die folgenden symbolischen Konstanten und ihre Bedeutung sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="ba75b-111">The following are accepted symbolic constants and their meanings:</span></span>



| <span data-ttu-id="ba75b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ba75b-112">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="ba75b-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ba75b-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <span data-ttu-id="ba75b-114"><dt>**GL- \_ Punkte**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-114"><dt>**GL\_POINTS**</dt></span></span> </dl>                          | <span data-ttu-id="ba75b-115">Behandelt jeden Scheitelpunkt als einen einzelnen Punkt.</span><span class="sxs-lookup"><span data-stu-id="ba75b-115">Treats each vertex as a single point.</span></span> <span data-ttu-id="ba75b-116">Scheitel *Punkt n definiert* Punkt *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-116">Vertex *n* defines point *n*.</span></span> <span data-ttu-id="ba75b-117">*N* Punkte werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-117">*N* points are drawn.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <span data-ttu-id="ba75b-118"><dt>**GL- \_ Zeilen**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-118"><dt>**GL\_LINES**</dt></span></span> </dl>                             | <span data-ttu-id="ba75b-119">Behandelt jedes Paar von Scheitel Punkten als unabhängiges Liniensegment.</span><span class="sxs-lookup"><span data-stu-id="ba75b-119">Treats each pair of vertices as an independent line segment.</span></span> <span data-ttu-id="ba75b-120">Die Scheitel Punkte *2n-1* und *2N* definieren Zeile *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-120">Vertices *2n - 1* and *2n* define line *n*.</span></span> <span data-ttu-id="ba75b-121">*N/2* Zeilen werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-121">*N/2* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <span data-ttu-id="ba75b-122"><dt>**GL- \_ Zeilen \_ Streifen**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-122"><dt>**GL\_LINE\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="ba75b-123">Zeichnet eine verbundene Gruppe von Liniensegmenten vom ersten Scheitelpunkt bis zum letzten.</span><span class="sxs-lookup"><span data-stu-id="ba75b-123">Draws a connected group of line segments from the first vertex to the last.</span></span> <span data-ttu-id="ba75b-124">Die Scheitel Punkte *n* und *n + 1* definieren Zeile *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-124">Vertices *n* and *n+1* define line *n*.</span></span> <span data-ttu-id="ba75b-125">*N-1* Zeilen werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-125">*N - 1* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <span data-ttu-id="ba75b-126"><dt>**GL- \_ Zeilen \_ Schleife**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-126"><dt>**GL\_LINE\_LOOP**</dt></span></span> </dl>                | <span data-ttu-id="ba75b-127">Zeichnet eine verbundene Gruppe von Liniensegmenten vom ersten Vertex bis zum letzten und dann zurück zum ersten.</span><span class="sxs-lookup"><span data-stu-id="ba75b-127">Draws a connected group of line segments from the first vertex to the last, then back to the first.</span></span> <span data-ttu-id="ba75b-128">Die Scheitel Punkte *n* und *n + 1* definieren Zeile *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-128">Vertices *n* and *n + 1* define line *n*.</span></span> <span data-ttu-id="ba75b-129">Die letzte Zeile wird jedoch durch Vertices *N* und *1* definiert.</span><span class="sxs-lookup"><span data-stu-id="ba75b-129">The last line, however, is defined by vertices *N* and *1*.</span></span> <span data-ttu-id="ba75b-130">*N* Zeilen werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-130">*N* lines are drawn.</span></span><br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <span data-ttu-id="ba75b-131"><dt>**GL- \_ Dreiecke**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-131"><dt>**GL\_TRIANGLES**</dt></span></span> </dl>                 | <span data-ttu-id="ba75b-132">Behandelt jedes tripleder Scheitel Punkte als unabhängiges Dreieck.</span><span class="sxs-lookup"><span data-stu-id="ba75b-132">Treats each triplet of vertices as an independent triangle.</span></span> <span data-ttu-id="ba75b-133">Die Scheitel Punkte *3N-2*, *3N-1* und *3N* definieren das Dreieck *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-133">Vertices *3n - 2*, *3n - 1*, and *3n* define triangle *n*.</span></span> <span data-ttu-id="ba75b-134">*N/3-* Dreiecke werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-134">*N/3* triangles are drawn.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <span data-ttu-id="ba75b-135"><dt>**GL- \_ Dreiecks \_ Streifen**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-135"><dt>**GL\_TRIANGLE\_STRIP**</dt></span></span> </dl> | <span data-ttu-id="ba75b-136">Zeichnet eine verbundene Gruppe von Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="ba75b-136">Draws a connected group of triangles.</span></span> <span data-ttu-id="ba75b-137">Für jeden Scheitelpunkt, der nach den ersten beiden Scheitel Punkten dargestellt wird, wird ein Dreieck definiert.</span><span class="sxs-lookup"><span data-stu-id="ba75b-137">One triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="ba75b-138">Für ungerade *n*, Vertices *n*, *n + 1* und *n + 2* definieren Sie das Dreieck *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-138">For odd *n*, vertices *n*, *n + 1*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="ba75b-139">Für gerade *n* werden die Scheitel Punkte *n + 1*, *n* und *n + 2* das Dreieck *n* definieren.</span><span class="sxs-lookup"><span data-stu-id="ba75b-139">For even *n*, vertices *n + 1*, *n*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="ba75b-140">*N-2* Dreiecke werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-140">*N - 2* triangles are drawn.</span></span><br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <span data-ttu-id="ba75b-141"><dt>**GL- \_ Dreiecks \_ Lüfter**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-141"><dt>**GL\_TRIANGLE\_FAN**</dt></span></span> </dl>       | <span data-ttu-id="ba75b-142">Zeichnet eine verbundene Gruppe von Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="ba75b-142">Draws a connected group of triangles.</span></span> <span data-ttu-id="ba75b-143">für jeden Scheitelpunkt, der nach den ersten beiden Scheitel Punkten dargestellt wird, wird ein Dreieck definiert.</span><span class="sxs-lookup"><span data-stu-id="ba75b-143">one triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="ba75b-144">Die Scheitel Punkte *1*, *n + 1*, *n + 2* definieren das Dreieck *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-144">Vertices *1*, *n + 1*, *n + 2* define triangle *n*.</span></span> <span data-ttu-id="ba75b-145">*N-2* Dreiecke werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-145">*N - 2* triangles are drawn.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <span data-ttu-id="ba75b-146"><dt>**GL \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-146"><dt>**GL\_QUADS**</dt></span></span> </dl>                             | <span data-ttu-id="ba75b-147">Behandelt jede Gruppe von vier Scheitel Punkten als unabhängige vier Vertices.</span><span class="sxs-lookup"><span data-stu-id="ba75b-147">Treats each group of four vertices as an independent quadrilateral.</span></span> <span data-ttu-id="ba75b-148">Vertices *4N-3*, *4N-2*, *4N-1* und *4N* definieren vierseitiges *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-148">Vertices *4n - 3*, *4n - 2*, *4n - 1*, and *4n* define quadrilateral *n*.</span></span> <span data-ttu-id="ba75b-149">*N/4* viereckale werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-149">*N/4* quadrilaterals are drawn.</span></span><br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <span data-ttu-id="ba75b-150"><dt>**GL \_ Quad \_ Strip**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-150"><dt>**GL\_QUAD\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="ba75b-151">Zeichnet eine verbundene Gruppe von viereckalen.</span><span class="sxs-lookup"><span data-stu-id="ba75b-151">Draws a connected group of quadrilaterals.</span></span> <span data-ttu-id="ba75b-152">Für jedes Paar von Vertices, die nach dem ersten paar dargestellt werden, ist ein Viereck definiert.</span><span class="sxs-lookup"><span data-stu-id="ba75b-152">One quadrilateral is defined for each pair of vertices presented after the first pair.</span></span> <span data-ttu-id="ba75b-153">Die Scheitel Punkte *2n-1*, *2N*, *2N + 2* und *2n + 1* definieren vierseitige *n*.</span><span class="sxs-lookup"><span data-stu-id="ba75b-153">Vertices *2n - 1*, *2n*, *2n + 2*, and *2n + 1* define quadrilateral *n*.</span></span> <span data-ttu-id="ba75b-154">*N/2-1* viereckale werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-154">*N/2 - 1* quadrilaterals are drawn.</span></span> <span data-ttu-id="ba75b-155">Beachten Sie, dass die Reihenfolge, in der die Scheitel Punkte verwendet werden, um ein vierseitiges aus den Bereichs Daten zu erstellen, von dem mit unabhängigen Daten verwendeten abweicht</span><span class="sxs-lookup"><span data-stu-id="ba75b-155">Note that the order in which vertices are used to construct a quadrilateral from strip data is different from that used with independent data.</span></span><br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <span data-ttu-id="ba75b-156"><dt>**GL- \_ Polygon**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-156"><dt>**GL\_POLYGON**</dt></span></span> </dl>                       | <span data-ttu-id="ba75b-157">Zeichnet ein einzelnes, zusammen gemitteles Polygon.</span><span class="sxs-lookup"><span data-stu-id="ba75b-157">Draws a single, convex polygon.</span></span> <span data-ttu-id="ba75b-158">In den Scheitel Punkten *1* bis *N* wird dieses Polygon definiert.</span><span class="sxs-lookup"><span data-stu-id="ba75b-158">Vertices *1* through *N* define this polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba75b-159">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba75b-159">Return value</span></span>

<span data-ttu-id="ba75b-160">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ba75b-160">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba75b-161">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ba75b-161">Error codes</span></span>

<span data-ttu-id="ba75b-162">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ba75b-162">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ba75b-163">Name</span><span class="sxs-lookup"><span data-stu-id="ba75b-163">Name</span></span>                                                                                                  | <span data-ttu-id="ba75b-164">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ba75b-164">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba75b-165"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-165"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ba75b-166">der *Modus* wurde auf einen nicht akzeptierten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba75b-166">*mode* was set to an unaccepted value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="ba75b-167"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-167"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ba75b-168">Die Funktion " [glVertex](glvertex-functions.md)", " [glcolor](glcolor-functions.md)", " [glindex](glindex-functions.md)", " [glnormal](glnormal-functions.md)", " [gltexcoord](gltexcoord-functions.md)", " [glevalcoord](glevalcoord-functions.md)", " [glevalpoint](glevalpoint.md)", " [glmaterial](glmaterial-functions.md)", " [gledgeflag](gledgeflag-functions.md)", " [**glCallList**](glcalllist.md)" und " [**glcalllists**](glcalllists.md) " wurde zwischen **glBegin** und [**dem entsprechenden**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="ba75b-168">A function other than [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md), or [**glCallLists**](glcalllists.md) was called between **glBegin** and the corresponding [**glend**](glend.md).</span></span> <span data-ttu-id="ba75b-169">Die Funktion " **glEnd** " wurde aufgerufen, bevor die entsprechende " **glBegin** " aufgerufen wurde, oder " **glBegin** " wurde innerhalb einer **glBegin**- / **glEnd** -Sequenz aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ba75b-169">The function **glend** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glend** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ba75b-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba75b-170">Remarks</span></span>

<span data-ttu-id="ba75b-171">Die Funktionen " **glBegin** " und " [**glEnd**](glend.md) " begrenzen die Scheitel Punkte, die eine primitive oder eine Gruppe von ähnlichen primitiven definieren.</span><span class="sxs-lookup"><span data-stu-id="ba75b-171">The **glBegin** and [**glend**](glend.md) functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="ba75b-172">Die **glBegin** -Funktion akzeptiert ein einzelnes Argument, das angibt, welche von zehn primitiven die Scheitel Punkte bilden.</span><span class="sxs-lookup"><span data-stu-id="ba75b-172">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="ba75b-173">Wenn *n* als ganzzahlige Anzahl beginnend bei eins und *n* als Gesamtzahl der angegebenen Scheitel Punkte übernommen wird, lauten die Interpretationen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba75b-173">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="ba75b-174">Sie können nur eine Teilmenge der OpenGL-Funktionen zwischen **glBegin** und [**glEnd**](glend.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="ba75b-174">You can use only a subset of OpenGL functions between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="ba75b-175">Die Funktionen, die Sie verwenden können, sind:</span><span class="sxs-lookup"><span data-stu-id="ba75b-175">The functions you can use are:</span></span>

    [<span data-ttu-id="ba75b-176">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ba75b-176">**glVertex**</span></span>](glvertex-functions.md)

     

    [<span data-ttu-id="ba75b-177">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="ba75b-177">**glColor**</span></span>](glcolor-functions.md)

     

    [<span data-ttu-id="ba75b-178">**glindex**</span><span class="sxs-lookup"><span data-stu-id="ba75b-178">**glIndex**</span></span>](glindex-functions.md)

     

    [<span data-ttu-id="ba75b-179">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="ba75b-179">**glNormal**</span></span>](glnormal-functions.md)

     

    [<span data-ttu-id="ba75b-180">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="ba75b-180">**glTexCoord**</span></span>](gltexcoord-functions.md)

     

    [<span data-ttu-id="ba75b-181">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="ba75b-181">**glEvalCoord**</span></span>](glevalcoord-functions.md)

     

    [<span data-ttu-id="ba75b-182">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="ba75b-182">**glEvalPoint**</span></span>](glevalpoint.md)

     

    [<span data-ttu-id="ba75b-183">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="ba75b-183">**glMaterial**</span></span>](glmaterial-functions.md)

     

    [<span data-ttu-id="ba75b-184">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="ba75b-184">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="ba75b-185">Sie können auch " [**glCallList**](glcalllist.md) " oder " [**glcalllists**](glcalllists.md) " verwenden, um Anzeigelisten auszuführen, die nur die vorangehenden Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba75b-185">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="ba75b-186">Wenn eine andere OpenGL-Funktion zwischen **glBegin** und [**glEnd**](glend.md)aufgerufen wird, wird das Fehlerflag festgelegt, und die Funktion wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ba75b-186">If any other OpenGL function is called between **glBegin** and [**glend**](glend.md), the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="ba75b-187">Unabhängig von dem Wert, der für den- *Modus* in **glBegin** ausgewählt ist, gibt es keine Beschränkung für die Anzahl der Scheitel Punkte, die Sie zwischen **glBegin** und [**glEnd**](glend.md)definieren können.</span><span class="sxs-lookup"><span data-stu-id="ba75b-187">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="ba75b-188">Zeilen, Dreiecke, vier eckale und Polygone, die nicht vollständig angegeben sind, werden nicht gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-188">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="ba75b-189">Unvollständige Spezifikations Ergebnisse, wenn zu wenig Scheitel Punkte bereitgestellt werden, um auch einen einzelnen primitiven anzugeben, oder wenn ein falsches Vielfaches von Vertices angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba75b-189">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="ba75b-190">Der unvollständige primitive wird ignoriert. die gesamten primitiven werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba75b-190">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="ba75b-191">Die minimale Spezifikation der Scheitel Punkte für die einzelnen primitiven ist:</span><span class="sxs-lookup"><span data-stu-id="ba75b-191">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="ba75b-192">Mindestanzahl von Vertices</span><span class="sxs-lookup"><span data-stu-id="ba75b-192">Minimum number of vertices</span></span> | <span data-ttu-id="ba75b-193">Primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="ba75b-193">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="ba75b-194">1</span><span class="sxs-lookup"><span data-stu-id="ba75b-194">1</span></span>                          | <span data-ttu-id="ba75b-195">point</span><span class="sxs-lookup"><span data-stu-id="ba75b-195">point</span></span>             |
    | <span data-ttu-id="ba75b-196">2</span><span class="sxs-lookup"><span data-stu-id="ba75b-196">2</span></span>                          | <span data-ttu-id="ba75b-197">line</span><span class="sxs-lookup"><span data-stu-id="ba75b-197">line</span></span>              |
    | <span data-ttu-id="ba75b-198">3</span><span class="sxs-lookup"><span data-stu-id="ba75b-198">3</span></span>                          | <span data-ttu-id="ba75b-199">Dreieck</span><span class="sxs-lookup"><span data-stu-id="ba75b-199">triangle</span></span>          |
    | <span data-ttu-id="ba75b-200">4</span><span class="sxs-lookup"><span data-stu-id="ba75b-200">4</span></span>                          | <span data-ttu-id="ba75b-201">vierseitigen</span><span class="sxs-lookup"><span data-stu-id="ba75b-201">quadrilateral</span></span>     |
    | <span data-ttu-id="ba75b-202">3</span><span class="sxs-lookup"><span data-stu-id="ba75b-202">3</span></span>                          | <span data-ttu-id="ba75b-203">polygon</span><span class="sxs-lookup"><span data-stu-id="ba75b-203">polygon</span></span>           |

    

     

-   <span data-ttu-id="ba75b-204">Modi, die ein bestimmtes Vielfaches von Vertices erfordern, sind GL- \_ Linien (2), GL \_ -Dreiecke (3), GL \_ -Quad (4) und GL \_ Quad \_ Strip (2).</span><span class="sxs-lookup"><span data-stu-id="ba75b-204">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba75b-205">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba75b-205">Requirements</span></span>



| <span data-ttu-id="ba75b-206">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba75b-206">Requirement</span></span> | <span data-ttu-id="ba75b-207">Wert</span><span class="sxs-lookup"><span data-stu-id="ba75b-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba75b-208">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba75b-208">Minimum supported client</span></span><br/> | <span data-ttu-id="ba75b-209">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba75b-209">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ba75b-210">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba75b-210">Minimum supported server</span></span><br/> | <span data-ttu-id="ba75b-211">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba75b-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba75b-212">Header</span><span class="sxs-lookup"><span data-stu-id="ba75b-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba75b-213"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-213"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ba75b-214">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba75b-214">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba75b-215"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-215"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba75b-216">DLL</span><span class="sxs-lookup"><span data-stu-id="ba75b-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba75b-217"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba75b-217"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba75b-218">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba75b-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba75b-219">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="ba75b-219">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="ba75b-220">**glcalllists**</span><span class="sxs-lookup"><span data-stu-id="ba75b-220">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="ba75b-221">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="ba75b-221">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ba75b-222">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="ba75b-222">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="ba75b-223">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ba75b-223">**glEnd**</span></span>](/windows/desktop/OpenGL/glend)
</dt> <dt>

[<span data-ttu-id="ba75b-224">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="ba75b-224">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ba75b-225">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="ba75b-225">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="ba75b-226">**glindex**</span><span class="sxs-lookup"><span data-stu-id="ba75b-226">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ba75b-227">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="ba75b-227">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="ba75b-228">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="ba75b-228">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="ba75b-229">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="ba75b-229">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ba75b-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ba75b-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

