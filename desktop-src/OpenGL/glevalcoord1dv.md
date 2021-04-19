---
title: glEvalCoord1dv-Funktion (GL. h)
description: Die glEvalCoord1dv-Funktion wertet aktivierte eindimensionale Zuordnungen aus.
ms.assetid: 6f966141-d4e6-4b54-b465-3ced33b57caf
keywords:
- glEvalCoord1dv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018c984c74ed6fa0d7224e7e0520c023e8b6bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344680"
---
# <a name="glevalcoord1dv-function"></a><span data-ttu-id="9d9b1-104">glEvalCoord1dv-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d9b1-104">glEvalCoord1dv function</span></span>

<span data-ttu-id="9d9b1-105">Die [**glEvalCoord1dv**](glevalcoord1d.md) -Funktion wertet aktivierte eindimensionale Zuordnungen aus.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-105">The [**glEvalCoord1dv**](glevalcoord1d.md) function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d9b1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d9b1-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1dv(
   const GLdouble *u
);
```



## <a name="parameters"></a><span data-ttu-id="9d9b1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d9b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d9b1-108">*n*</span><span class="sxs-lookup"><span data-stu-id="9d9b1-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="9d9b1-109">Ein Zeiger auf ein Array, das die Domänen Koordinate *u* enthält.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d9b1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d9b1-110">Return value</span></span>

<span data-ttu-id="9d9b1-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d9b1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d9b1-112">Remarks</span></span>

<span data-ttu-id="9d9b1-113">Die **glEvalCoord1dv** -Funktion wertet aktivierte eindimensionale Zuordnungen bei Argument *u* aus.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-113">The **glEvalCoord1dv** function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="9d9b1-114">Definieren von Maps mit [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="9d9b1-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="9d9b1-115">Aktivieren oder deaktivieren Sie Sie mit [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="9d9b1-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="9d9b1-116">Wenn eine der Funktionen von **glevalcoord** ausgegeben wird, werden alle derzeit aktivierten Zuordnungen der aufgeführten Dimension ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="9d9b1-117">Dann ist es für jede aktivierte Zuordnung so, als ob die entsprechende OpenGL-Funktion mit dem berechneten Wert ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="9d9b1-118">Das heißt, wenn der GL \_ zuordnung1 \_ Index oder der GL \_ map2- \_ Index aktiviert ist, wird eine [**glindex**](glindex-functions.md) -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="9d9b1-119">Wenn gl \_ zuordnung1 \_ Color \_ 4 oder GL \_ map2 \_ Color \_ 4 aktiviert ist, wird eine **glcolor** -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="9d9b1-120">Wenn gl \_ zuordnung1 \_ Normal oder GL \_ map2 \_ Normal aktiviert ist, wird ein normaler Vektor erzeugt. und wenn eine von GL zuordnung1 Textur coord \_ \_ \_ \_ 1, GL \_ zuordnung1 \_ Texture \_ coord \_ 2, GL \_ zuordnung1 \_ Texture \_ coord \_ 3, GL \_ zuordnung1 \_ Texture \_ coord \_ 4, GL \_ map2 \_ Texture \_ coord \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL \_ map2 \_ Texture \_ coord \_ 3 und GL \_ map2 \_ Texture \_ coord \_ 4 aktiviert ist, wird eine entsprechende [**gltexcoord**](gltexcoord-functions.md) -Funktion simuliert.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="9d9b1-121">OpenGL verwendet ausgewertete Werte anstelle der aktuellen Werte für die aktivierten Auswertungen und die aktuellen Werte für Farbe, Farbindex, normale und Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="9d9b1-122">Die ausgewerteten Werte aktualisieren jedoch nicht die aktuellen Werte.</span><span class="sxs-lookup"><span data-stu-id="9d9b1-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="9d9b1-123">Wenn daher die [**glVertex**](glvertex-functions.md) -Funktionen mit **glevalcoord** -Funktionen vermischt werden, werden die den **glVertex** -Funktionen zugeordneten Farb-, normal-und Texturkoordinaten nicht von den Werten beeinflusst, die von den Funktionen von **glevalcoord** generiert werden, sondern nur durch die neuesten Funktionen von [**glcolor**](glcolor-functions.md), [**glindex**](glindex-functions.md), [**glnormal**](glnormal-functions.md)und [**gltexcoord**](gltexcoord-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="9d9b1-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="9d9b1-124">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **glEvalCoord1dv** -Funktion ab:</span><span class="sxs-lookup"><span data-stu-id="9d9b1-124">The following functions retrieve information related to the **glEvalCoord1dv** function:</span></span>

<span data-ttu-id="9d9b1-125">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="9d9b1-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="9d9b1-126">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="9d9b1-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="9d9b1-127">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Index</span><span class="sxs-lookup"><span data-stu-id="9d9b1-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="9d9b1-128">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Farbe \_ 4</span><span class="sxs-lookup"><span data-stu-id="9d9b1-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="9d9b1-129">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="9d9b1-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="9d9b1-130">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 1</span><span class="sxs-lookup"><span data-stu-id="9d9b1-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="9d9b1-131">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 2</span><span class="sxs-lookup"><span data-stu-id="9d9b1-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="9d9b1-132">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 3</span><span class="sxs-lookup"><span data-stu-id="9d9b1-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="9d9b1-133">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ zuordnung1 \_ Textur \_ Koord \_ 4</span><span class="sxs-lookup"><span data-stu-id="9d9b1-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="9d9b1-134">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="9d9b1-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="9d9b1-135">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="9d9b1-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="9d9b1-136">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Index</span><span class="sxs-lookup"><span data-stu-id="9d9b1-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="9d9b1-137">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Farbe \_ 4</span><span class="sxs-lookup"><span data-stu-id="9d9b1-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="9d9b1-138">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="9d9b1-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="9d9b1-139">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 1</span><span class="sxs-lookup"><span data-stu-id="9d9b1-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="9d9b1-140">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 2</span><span class="sxs-lookup"><span data-stu-id="9d9b1-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="9d9b1-141">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 3</span><span class="sxs-lookup"><span data-stu-id="9d9b1-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="9d9b1-142">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ map2 \_ Textur \_ Koord \_ 4</span><span class="sxs-lookup"><span data-stu-id="9d9b1-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="9d9b1-143">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Auto \_ Normal</span><span class="sxs-lookup"><span data-stu-id="9d9b1-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9b1-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d9b1-144">Requirements</span></span>



| <span data-ttu-id="9d9b1-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d9b1-145">Requirement</span></span> | <span data-ttu-id="9d9b1-146">Wert</span><span class="sxs-lookup"><span data-stu-id="9d9b1-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9b1-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d9b1-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9b1-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d9b1-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d9b1-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d9b1-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9b1-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d9b1-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d9b1-151">Header</span><span class="sxs-lookup"><span data-stu-id="9d9b1-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d9b1-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b1-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9d9b1-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d9b1-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d9b1-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b1-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d9b1-155">DLL</span><span class="sxs-lookup"><span data-stu-id="9d9b1-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d9b1-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b1-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d9b1-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d9b1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d9b1-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-159">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-160">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-163">**glevalmesh**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-164">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-165">**glgetmap**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-166">**glindex**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-167">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-170">**glmapgrid**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-171">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-172">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="9d9b1-173">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="9d9b1-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





