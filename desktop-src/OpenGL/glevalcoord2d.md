---
title: glEvalCoord2d-Funktion (GL. h)
description: Die glEvalCoord2d-Funktion wertet aktivierte zweidimensionale Zuordnungen aus.
ms.assetid: 95963abc-841a-4154-92d5-5ae3e6de0f97
keywords:
- glEvalCoord2d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036e2ee10d1ceac6df6a68a35c1da881d1d478b5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104569078"
---
# <a name="glevalcoord2d-function"></a><span data-ttu-id="9bcc6-104">glEvalCoord2d-Funktion</span><span class="sxs-lookup"><span data-stu-id="9bcc6-104">glEvalCoord2d function</span></span>

<span data-ttu-id="9bcc6-105">Die **glEvalCoord2d** -Funktion wertet aktivierte zweidimensionale Zuordnungen aus.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-105">The **glEvalCoord2d** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcc6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bcc6-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2d(
   GLdouble u,
   GLdouble v
);
```



## <a name="parameters"></a><span data-ttu-id="9bcc6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bcc6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcc6-108">*n*</span><span class="sxs-lookup"><span data-stu-id="9bcc6-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcc6-109">Ein-Wert *, bei dem* es sich um die Domänen Koordinate der in einer vorherigen [**glMap2**](glmap2.md) -Funktion definierten Basis Funktion handelt.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9bcc6-110">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="9bcc6-110">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcc6-111">Ein-Wert *, bei dem* es sich um die Domänen Koordinate für die in einer vorherigen [**glMap2**](glmap2.md) -Funktion definierte Basis Funktion handelt.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-111">A value that is the domain coordinate *v* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bcc6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bcc6-112">Return value</span></span>

<span data-ttu-id="9bcc6-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bcc6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bcc6-114">Remarks</span></span>

<span data-ttu-id="9bcc6-115">Die **glEvalCoord2d** -Funktion wertet aktivierte zweidimensionale Karten mit zwei Domänen Werten aus: *u* und *v*.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-115">The **glEvalCoord2d** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="9bcc6-116">Definieren von Zuordnungen mit [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="9bcc6-116">Define maps with [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="9bcc6-117">Aktivieren oder deaktivieren Sie Sie mit [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="9bcc6-117">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="9bcc6-118">Wenn eine der Funktionen von **glevalcoord** ausgegeben wird, werden alle derzeit aktivierten Zuordnungen der aufgeführten Dimension ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-118">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="9bcc6-119">Dann ist es für jede aktivierte Zuordnung so, als ob die entsprechende OpenGL-Funktion mit dem berechneten Wert ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-119">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="9bcc6-120">Das heißt, wenn der GL \_ zuordnung1 \_ Index oder der GL \_ map2- \_ Index aktiviert ist, wird eine [**glindex**](glindex-functions.md) -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-120">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="9bcc6-121">Wenn gl \_ zuordnung1 \_ Color \_ 4 oder GL \_ map2 \_ Color \_ 4 aktiviert ist, wird eine **glcolor** -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-121">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="9bcc6-122">Wenn gl \_ zuordnung1 \_ Normal oder GL \_ map2 \_ Normal aktiviert ist, wird ein normaler Vektor erzeugt. und wenn eine von GL zuordnung1 Textur coord \_ \_ \_ \_ 1, GL \_ zuordnung1 \_ Texture \_ coord \_ 2, GL \_ zuordnung1 \_ Texture \_ coord \_ 3, GL \_ zuordnung1 \_ Texture \_ coord \_ 4, GL \_ map2 \_ Texture \_ coord \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL \_ map2 \_ Texture \_ coord \_ 3 und GL \_ map2 \_ Texture \_ coord \_ 4 aktiviert ist, wird eine entsprechende [**gltexcoord**](gltexcoord-functions.md) -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-122">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="9bcc6-123">OpenGL verwendet ausgewertete Werte anstelle der aktuellen Werte für die aktivierten Auswertungen und die aktuellen Werte für Farbe, Farbindex, normale und Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-123">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="9bcc6-124">Die ausgewerteten Werte aktualisieren jedoch nicht die aktuellen Werte.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-124">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="9bcc6-125">Wenn daher die [**glVertex**](glvertex-functions.md) -Funktionen mit **glevalcoord** -Funktionen vermischt werden, werden die den **glVertex** -Funktionen zugeordneten Farb-, normal-und Texturkoordinaten nicht von den Werten beeinflusst, die von den Funktionen von **glevalcoord** generiert werden, sondern nur durch die neuesten Funktionen von [**glcolor**](glcolor-functions.md), [**glindex**](glindex-functions.md), [**glnormal**](glnormal-functions.md)und [**gltexcoord**](gltexcoord-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="9bcc6-125">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="9bcc6-126">Wenn die automatische normale Generierung aktiviert ist, ruft **glEvalCoord2d** [**glEnable**](glenable.md) mit dem Argument GL \_ Auto \_ Normal auf, um Oberflächen normale zu generieren, unabhängig vom Inhalt oder der Aktivierung der GL \_ map2 \_ Normal Karte.</span><span class="sxs-lookup"><span data-stu-id="9bcc6-126">If automatic normal generation is enabled, **glEvalCoord2d** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="9bcc6-127">Let</span><span class="sxs-lookup"><span data-stu-id="9bcc6-127">Let</span></span>

![Gleichung, die einen produktübergreifenden Wert für eine Karte m anzeigt.](images/evlcrd01.png)

<span data-ttu-id="9bcc6-129">Die generierte normale **n** ist</span><span class="sxs-lookup"><span data-stu-id="9bcc6-129">The generated normal **n** is</span></span>

![Gleichung mit dem generierten normalen n für die Karte.](images/evlcrd02.png)

<span data-ttu-id="9bcc6-131">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glEvalCoord2d** -Funktion ab:</span><span class="sxs-lookup"><span data-stu-id="9bcc6-131">The following functions retrieve information related to the **glEvalCoord2d** function:</span></span>

<span data-ttu-id="9bcc6-132">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="9bcc6-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="9bcc6-133">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="9bcc6-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="9bcc6-134">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Index</span><span class="sxs-lookup"><span data-stu-id="9bcc6-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="9bcc6-135">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Farbe \_ 4</span><span class="sxs-lookup"><span data-stu-id="9bcc6-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="9bcc6-136">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="9bcc6-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="9bcc6-137">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 1</span><span class="sxs-lookup"><span data-stu-id="9bcc6-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="9bcc6-138">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 2</span><span class="sxs-lookup"><span data-stu-id="9bcc6-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="9bcc6-139">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 3</span><span class="sxs-lookup"><span data-stu-id="9bcc6-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="9bcc6-140">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 4</span><span class="sxs-lookup"><span data-stu-id="9bcc6-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="9bcc6-141">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="9bcc6-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="9bcc6-142">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="9bcc6-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="9bcc6-143">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Index</span><span class="sxs-lookup"><span data-stu-id="9bcc6-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="9bcc6-144">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Farbe \_ 4</span><span class="sxs-lookup"><span data-stu-id="9bcc6-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="9bcc6-145">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="9bcc6-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="9bcc6-146">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 1</span><span class="sxs-lookup"><span data-stu-id="9bcc6-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="9bcc6-147">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 2</span><span class="sxs-lookup"><span data-stu-id="9bcc6-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="9bcc6-148">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 3</span><span class="sxs-lookup"><span data-stu-id="9bcc6-148">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="9bcc6-149">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 4</span><span class="sxs-lookup"><span data-stu-id="9bcc6-149">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="9bcc6-150">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Auto \_ Normal</span><span class="sxs-lookup"><span data-stu-id="9bcc6-150">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcc6-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bcc6-151">Requirements</span></span>



| <span data-ttu-id="9bcc6-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bcc6-152">Requirement</span></span> | <span data-ttu-id="9bcc6-153">Wert</span><span class="sxs-lookup"><span data-stu-id="9bcc6-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcc6-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bcc6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="9bcc6-155">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bcc6-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9bcc6-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bcc6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="9bcc6-157">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bcc6-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9bcc6-158">Header</span><span class="sxs-lookup"><span data-stu-id="9bcc6-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bcc6-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bcc6-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9bcc6-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9bcc6-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="9bcc6-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bcc6-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9bcc6-162">DLL</span><span class="sxs-lookup"><span data-stu-id="9bcc6-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bcc6-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bcc6-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcc6-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bcc6-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcc6-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-166">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-166">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-167">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-167">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-168">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-168">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-170">**glevalmesh**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-170">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-171">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-171">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-172">**glgetmap**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-172">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-173">**glindex**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-173">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-174">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-174">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-175">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-175">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-176">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-176">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-177">**glmapgrid**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-177">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-178">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-178">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-179">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-179">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="9bcc6-180">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="9bcc6-180">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





