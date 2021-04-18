---
title: glEnd-Funktion (GL. h)
description: Die Funktionen "glBegin" und "glEnd" begrenzen die Scheitel Punkte eines primitiven oder einer Gruppe von ähnlichen primitiven. | glEnd-Funktion (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- glEnd-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365253"
---
# <a name="glend-function"></a><span data-ttu-id="afe1b-105">glEnd-Funktion</span><span class="sxs-lookup"><span data-stu-id="afe1b-105">glEnd function</span></span>

<span data-ttu-id="afe1b-106">Die Funktionen " [**glBegin**](glbegin.md) " und " **glEnd** " begrenzen die Scheitel Punkte eines primitiven oder einer Gruppe von ähnlichen primitiven.</span><span class="sxs-lookup"><span data-stu-id="afe1b-106">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe1b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="afe1b-107">Syntax</span></span>


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a><span data-ttu-id="afe1b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="afe1b-108">Parameters</span></span>

<span data-ttu-id="afe1b-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="afe1b-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="afe1b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afe1b-110">Return value</span></span>

<span data-ttu-id="afe1b-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="afe1b-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="afe1b-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="afe1b-112">Error codes</span></span>

<span data-ttu-id="afe1b-113">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="afe1b-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="afe1b-114">Name</span><span class="sxs-lookup"><span data-stu-id="afe1b-114">Name</span></span>                                                                                                  | <span data-ttu-id="afe1b-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="afe1b-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="afe1b-116"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="afe1b-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="afe1b-117">Die Funktion " **glVertex**", " **glcolor**", " **glindex**", " **glnormal**", " **gltexcoord**", " **glevalcoord**", " **glevalpoint**", " **glmaterial**", " **gledgeflag**", " **glCallList**" und " **glcalllists** " wurde zwischen **glBegin** und **dem entsprechenden**</span><span class="sxs-lookup"><span data-stu-id="afe1b-117">A function other than **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList**, or **glCallLists** was called between **glBegin** and the corresponding **glEnd**.</span></span> <span data-ttu-id="afe1b-118">Die Funktion " **glEnd** " wurde aufgerufen, bevor die entsprechende " **glBegin** " aufgerufen wurde, oder " **glBegin** " wurde innerhalb einer **glBegin**- / **glEnd** -Sequenz aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="afe1b-118">The function **glEnd** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glEnd** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="afe1b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afe1b-119">Remarks</span></span>

<span data-ttu-id="afe1b-120">Die Funktionen " [**glBegin**](glbegin.md) " und " **glEnd** " begrenzen die Scheitel Punkte, die eine primitive oder eine Gruppe von ähnlichen primitiven definieren.</span><span class="sxs-lookup"><span data-stu-id="afe1b-120">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="afe1b-121">Die **glBegin** -Funktion akzeptiert ein einzelnes Argument, das angibt, welche von zehn primitiven die Scheitel Punkte bilden.</span><span class="sxs-lookup"><span data-stu-id="afe1b-121">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="afe1b-122">Wenn *n* als ganzzahlige Anzahl beginnend bei eins und *n* als Gesamtzahl der angegebenen Scheitel Punkte übernommen wird, lauten die Interpretationen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="afe1b-122">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="afe1b-123">Sie können nur eine Teilmenge der OpenGL-Funktionen zwischen **glBegin** und **glEnd** verwenden.</span><span class="sxs-lookup"><span data-stu-id="afe1b-123">You can use only a subset of OpenGL functions between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="afe1b-124">Die Funktionen, die Sie verwenden können, sind:</span><span class="sxs-lookup"><span data-stu-id="afe1b-124">The functions you can use are:</span></span>

    -   [<span data-ttu-id="afe1b-125">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="afe1b-125">**glVertex**</span></span>](glvertex-functions.md)
    -   [<span data-ttu-id="afe1b-126">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="afe1b-126">**glColor**</span></span>](glcolor-functions.md)
    -   [<span data-ttu-id="afe1b-127">**glindex**</span><span class="sxs-lookup"><span data-stu-id="afe1b-127">**glIndex**</span></span>](glindex-functions.md)
    -   [<span data-ttu-id="afe1b-128">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="afe1b-128">**glNormal**</span></span>](glnormal-functions.md)
    -   [<span data-ttu-id="afe1b-129">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="afe1b-129">**glTexCoord**</span></span>](gltexcoord-functions.md)
    -   [<span data-ttu-id="afe1b-130">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="afe1b-130">**glEvalCoord**</span></span>](glevalcoord-functions.md)
    -   [<span data-ttu-id="afe1b-131">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="afe1b-131">**glEvalPoint**</span></span>](glevalpoint.md)
    -   [<span data-ttu-id="afe1b-132">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="afe1b-132">**glMaterial**</span></span>](glmaterial-functions.md)
    -   [<span data-ttu-id="afe1b-133">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="afe1b-133">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="afe1b-134">Sie können auch " [**glCallList**](glcalllist.md) " oder " [**glcalllists**](glcalllists.md) " verwenden, um Anzeigelisten auszuführen, die nur die vorangehenden Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="afe1b-134">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="afe1b-135">Wenn eine andere OpenGL-Funktion zwischen **glBegin** und **glEnd** aufgerufen wird, wird das Fehlerflag festgelegt, und die Funktion wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="afe1b-135">If any other OpenGL function is called between **glBegin** and **glEnd**, the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="afe1b-136">Unabhängig von dem Wert, der für den- *Modus* in **glBegin** ausgewählt ist, gibt es keine Beschränkung für die Anzahl der Scheitel Punkte, die Sie zwischen **glBegin** und **glEnd** definieren können.</span><span class="sxs-lookup"><span data-stu-id="afe1b-136">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="afe1b-137">Zeilen, Dreiecke, vier eckale und Polygone, die nicht vollständig angegeben sind, werden nicht gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="afe1b-137">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="afe1b-138">Unvollständige Spezifikations Ergebnisse, wenn zu wenig Scheitel Punkte bereitgestellt werden, um auch einen einzelnen primitiven anzugeben, oder wenn ein falsches Vielfaches von Vertices angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="afe1b-138">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="afe1b-139">Der unvollständige primitive wird ignoriert. die gesamten primitiven werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="afe1b-139">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="afe1b-140">Die minimale Spezifikation der Scheitel Punkte für die einzelnen primitiven ist:</span><span class="sxs-lookup"><span data-stu-id="afe1b-140">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="afe1b-141">Mindestanzahl von Vertices</span><span class="sxs-lookup"><span data-stu-id="afe1b-141">Minimum number of vertices</span></span> | <span data-ttu-id="afe1b-142">Primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="afe1b-142">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="afe1b-143">1</span><span class="sxs-lookup"><span data-stu-id="afe1b-143">1</span></span>                          | <span data-ttu-id="afe1b-144">point</span><span class="sxs-lookup"><span data-stu-id="afe1b-144">point</span></span>             |
    | <span data-ttu-id="afe1b-145">2</span><span class="sxs-lookup"><span data-stu-id="afe1b-145">2</span></span>                          | <span data-ttu-id="afe1b-146">line</span><span class="sxs-lookup"><span data-stu-id="afe1b-146">line</span></span>              |
    | <span data-ttu-id="afe1b-147">3</span><span class="sxs-lookup"><span data-stu-id="afe1b-147">3</span></span>                          | <span data-ttu-id="afe1b-148">Dreieck</span><span class="sxs-lookup"><span data-stu-id="afe1b-148">triangle</span></span>          |
    | <span data-ttu-id="afe1b-149">4</span><span class="sxs-lookup"><span data-stu-id="afe1b-149">4</span></span>                          | <span data-ttu-id="afe1b-150">vierseitigen</span><span class="sxs-lookup"><span data-stu-id="afe1b-150">quadrilateral</span></span>     |
    | <span data-ttu-id="afe1b-151">3</span><span class="sxs-lookup"><span data-stu-id="afe1b-151">3</span></span>                          | <span data-ttu-id="afe1b-152">polygon</span><span class="sxs-lookup"><span data-stu-id="afe1b-152">polygon</span></span>           |

    

     

-   <span data-ttu-id="afe1b-153">Modi, die ein bestimmtes Vielfaches von Vertices erfordern, sind GL- \_ Linien (2), GL \_ -Dreiecke (3), GL \_ -Quad (4) und GL \_ Quad \_ Strip (2).</span><span class="sxs-lookup"><span data-stu-id="afe1b-153">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="afe1b-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afe1b-154">Requirements</span></span>



| <span data-ttu-id="afe1b-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afe1b-155">Requirement</span></span> | <span data-ttu-id="afe1b-156">Wert</span><span class="sxs-lookup"><span data-stu-id="afe1b-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afe1b-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afe1b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="afe1b-158">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afe1b-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="afe1b-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afe1b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="afe1b-160">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afe1b-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="afe1b-161">Header</span><span class="sxs-lookup"><span data-stu-id="afe1b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="afe1b-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="afe1b-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="afe1b-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="afe1b-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="afe1b-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afe1b-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="afe1b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="afe1b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afe1b-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afe1b-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afe1b-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afe1b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe1b-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="afe1b-168">**glBegin**</span></span>](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[<span data-ttu-id="afe1b-169">**glcalllists**</span><span class="sxs-lookup"><span data-stu-id="afe1b-169">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="afe1b-170">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="afe1b-170">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="afe1b-171">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="afe1b-171">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="afe1b-172">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="afe1b-172">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="afe1b-173">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="afe1b-173">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="afe1b-174">**glindex**</span><span class="sxs-lookup"><span data-stu-id="afe1b-174">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="afe1b-175">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="afe1b-175">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="afe1b-176">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="afe1b-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="afe1b-177">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="afe1b-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="afe1b-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="afe1b-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

