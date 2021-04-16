---
title: glEvalCoord2dv-Funktion (GL. h)
description: Die glEvalCoord2dv-Funktion wertet aktivierte zweidimensionale Zuordnungen aus.
ms.assetid: 726a0c0c-d69e-46dc-b78e-a0d1e9ad97cd
keywords:
- glEvalCoord2dv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a685606fb1445c6841efdf506a1f2d4747da838
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104558691"
---
# <a name="glevalcoord2dv-function"></a><span data-ttu-id="bdb29-104">glEvalCoord2dv-Funktion</span><span class="sxs-lookup"><span data-stu-id="bdb29-104">glEvalCoord2dv function</span></span>

<span data-ttu-id="bdb29-105">Die **glEvalCoord2dv** -Funktion wertet aktivierte zweidimensionale Zuordnungen aus.</span><span class="sxs-lookup"><span data-stu-id="bdb29-105">The **glEvalCoord2dv** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb29-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdb29-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2dv(
   const GLdouble *u
);
```



## <a name="parameters"></a><span data-ttu-id="bdb29-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdb29-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb29-108">*n*</span><span class="sxs-lookup"><span data-stu-id="bdb29-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="bdb29-109">Ein Zeiger auf ein Array, das die Domänen Koordinate *u* enthält.</span><span class="sxs-lookup"><span data-stu-id="bdb29-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb29-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdb29-110">Return value</span></span>

<span data-ttu-id="bdb29-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bdb29-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb29-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdb29-112">Remarks</span></span>

<span data-ttu-id="bdb29-113">Die **glEvalCoord2dv** -Funktion wertet aktivierte zweidimensionale Karten mit zwei Domänen Werten aus: *u* und *v*.</span><span class="sxs-lookup"><span data-stu-id="bdb29-113">The **glEvalCoord2dv** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="bdb29-114">Definieren von Maps mit [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="bdb29-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="bdb29-115">Aktivieren oder deaktivieren Sie Sie mit [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="bdb29-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="bdb29-116">Wenn eine der Funktionen von **glevalcoord** ausgegeben wird, werden alle derzeit aktivierten Zuordnungen der aufgeführten Dimension ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="bdb29-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="bdb29-117">Dann ist es für jede aktivierte Zuordnung so, als ob die entsprechende OpenGL-Funktion mit dem berechneten Wert ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="bdb29-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="bdb29-118">Das heißt, wenn der GL \_ zuordnung1 \_ Index oder der GL \_ map2- \_ Index aktiviert ist, wird eine [**glindex**](glindex-functions.md) -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="bdb29-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="bdb29-119">Wenn gl \_ zuordnung1 \_ Color \_ 4 oder GL \_ map2 \_ Color \_ 4 aktiviert ist, wird eine **glcolor** -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="bdb29-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="bdb29-120">Wenn gl \_ zuordnung1 \_ Normal oder GL \_ map2 \_ Normal aktiviert ist, wird ein normaler Vektor erzeugt. und wenn eine von GL zuordnung1 Textur coord \_ \_ \_ \_ 1, GL \_ zuordnung1 \_ Texture \_ coord \_ 2, GL \_ zuordnung1 \_ Texture \_ coord \_ 3, GL \_ zuordnung1 \_ Texture \_ coord \_ 4, GL \_ map2 \_ Texture \_ coord \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL \_ map2 \_ Texture \_ coord \_ 3 und GL \_ map2 \_ Texture \_ coord \_ 4 aktiviert ist, wird eine entsprechende [**gltexcoord**](gltexcoord-functions.md) -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="bdb29-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="bdb29-121">OpenGL verwendet ausgewertete Werte anstelle der aktuellen Werte für die aktivierten Auswertungen und die aktuellen Werte für Farbe, Farbindex, normale und Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="bdb29-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="bdb29-122">Die ausgewerteten Werte aktualisieren jedoch nicht die aktuellen Werte.</span><span class="sxs-lookup"><span data-stu-id="bdb29-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="bdb29-123">Wenn daher die [**glVertex**](glvertex-functions.md) -Funktionen mit **glevalcoord** -Funktionen vermischt werden, werden die den **glVertex** -Funktionen zugeordneten Farb-, normal-und Texturkoordinaten nicht von den Werten beeinflusst, die von den Funktionen von **glevalcoord** generiert werden, sondern nur durch die neuesten Funktionen von [**glcolor**](glcolor-functions.md), [**glindex**](glindex-functions.md), [**glnormal**](glnormal-functions.md)und [**gltexcoord**](gltexcoord-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="bdb29-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="bdb29-124">Wenn die automatische normale Generierung aktiviert ist, ruft **glEvalCoord2dv** [**glEnable**](glenable.md) mit dem Argument GL \_ Auto \_ Normal auf, um Oberflächen normale zu generieren, unabhängig vom Inhalt oder der Aktivierung der GL \_ map2 \_ Normal Karte.</span><span class="sxs-lookup"><span data-stu-id="bdb29-124">If automatic normal generation is enabled, **glEvalCoord2dv** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="bdb29-125">Let</span><span class="sxs-lookup"><span data-stu-id="bdb29-125">Let</span></span>

![Gleichung, die einen produktübergreifenden Wert für eine Karte m anzeigt.](images/evlcrd01.png)

<span data-ttu-id="bdb29-127">Die generierte normale **n** ist</span><span class="sxs-lookup"><span data-stu-id="bdb29-127">The generated normal **n** is</span></span>

![Gleichung mit dem generierten normalen n für die Karte.](images/evlcrd02.png)

<span data-ttu-id="bdb29-129">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glEvalCoord2dv** -Funktion ab:</span><span class="sxs-lookup"><span data-stu-id="bdb29-129">The following functions retrieve information related to the **glEvalCoord2dv** function:</span></span>

<span data-ttu-id="bdb29-130">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="bdb29-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="bdb29-131">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="bdb29-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="bdb29-132">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Index</span><span class="sxs-lookup"><span data-stu-id="bdb29-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="bdb29-133">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Farbe \_ 4</span><span class="sxs-lookup"><span data-stu-id="bdb29-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="bdb29-134">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="bdb29-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="bdb29-135">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 1</span><span class="sxs-lookup"><span data-stu-id="bdb29-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="bdb29-136">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 2</span><span class="sxs-lookup"><span data-stu-id="bdb29-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="bdb29-137">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 3</span><span class="sxs-lookup"><span data-stu-id="bdb29-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="bdb29-138">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 4</span><span class="sxs-lookup"><span data-stu-id="bdb29-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="bdb29-139">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="bdb29-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="bdb29-140">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="bdb29-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="bdb29-141">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Index</span><span class="sxs-lookup"><span data-stu-id="bdb29-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="bdb29-142">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Farbe \_ 4</span><span class="sxs-lookup"><span data-stu-id="bdb29-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="bdb29-143">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="bdb29-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="bdb29-144">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 1</span><span class="sxs-lookup"><span data-stu-id="bdb29-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="bdb29-145">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 2</span><span class="sxs-lookup"><span data-stu-id="bdb29-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="bdb29-146">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 3</span><span class="sxs-lookup"><span data-stu-id="bdb29-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="bdb29-147">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 4</span><span class="sxs-lookup"><span data-stu-id="bdb29-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="bdb29-148">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Auto \_ Normal</span><span class="sxs-lookup"><span data-stu-id="bdb29-148">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb29-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdb29-149">Requirements</span></span>



| <span data-ttu-id="bdb29-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdb29-150">Requirement</span></span> | <span data-ttu-id="bdb29-151">Wert</span><span class="sxs-lookup"><span data-stu-id="bdb29-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb29-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdb29-152">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb29-153">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdb29-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bdb29-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdb29-154">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb29-155">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdb29-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bdb29-156">Header</span><span class="sxs-lookup"><span data-stu-id="bdb29-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb29-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb29-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bdb29-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bdb29-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdb29-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdb29-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bdb29-160">DLL</span><span class="sxs-lookup"><span data-stu-id="bdb29-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdb29-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdb29-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb29-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdb29-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb29-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bdb29-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bdb29-164">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="bdb29-164">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="bdb29-165">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="bdb29-165">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="bdb29-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="bdb29-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="bdb29-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bdb29-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bdb29-168">**glevalmesh**</span><span class="sxs-lookup"><span data-stu-id="bdb29-168">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="bdb29-169">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="bdb29-169">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="bdb29-170">**glgetmap**</span><span class="sxs-lookup"><span data-stu-id="bdb29-170">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="bdb29-171">**glindex**</span><span class="sxs-lookup"><span data-stu-id="bdb29-171">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="bdb29-172">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="bdb29-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="bdb29-173">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="bdb29-173">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="bdb29-174">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="bdb29-174">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="bdb29-175">**glmapgrid**</span><span class="sxs-lookup"><span data-stu-id="bdb29-175">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="bdb29-176">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="bdb29-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="bdb29-177">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="bdb29-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="bdb29-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="bdb29-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





