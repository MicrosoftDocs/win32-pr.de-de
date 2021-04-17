---
title: glsskalierte Funktion (GL. h)
description: Die Funktionen "glScalef" und "glScalef" multiplizieren die aktuelle Matrix mit einer allgemeinen Skalierungs Matrix. | glsskalierte Funktion (GL. h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- glskalierte Funktion OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2655924f5716e142832882441066d4772d0e63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104558956"
---
# <a name="glscaled-function"></a><span data-ttu-id="c2cf2-105">glsskalierte Funktion</span><span class="sxs-lookup"><span data-stu-id="c2cf2-105">glScaled function</span></span>

<span data-ttu-id="c2cf2-106">Die Funktionen " **glScalef** " und " [**glScalef**](glscalef.md) " multiplizieren die aktuelle Matrix mit einer allgemeinen Skalierungs Matrix.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-106">The **glScaled** and [**glScalef**](glscalef.md) functions multiply the current matrix by a general scaling matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cf2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2cf2-107">Syntax</span></span>


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="c2cf2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2cf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cf2-109">*x*</span><span class="sxs-lookup"><span data-stu-id="c2cf2-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cf2-110">Skalierungsfaktoren entlang der *x* -Achse.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-110">Scale factors along the *x* axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2cf2-111">*y*</span><span class="sxs-lookup"><span data-stu-id="c2cf2-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cf2-112">Skalierungsfaktoren entlang der *y* -Achse.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-112">Scale factors along the *y* axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2cf2-113">*z*</span><span class="sxs-lookup"><span data-stu-id="c2cf2-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cf2-114">Skalierungsfaktoren entlang der *z* -Achse.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-114">Scale factors along the *z* axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cf2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2cf2-115">Return value</span></span>

<span data-ttu-id="c2cf2-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2cf2-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c2cf2-117">Error codes</span></span>

<span data-ttu-id="c2cf2-118">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c2cf2-119">Name</span><span class="sxs-lookup"><span data-stu-id="c2cf2-119">Name</span></span>                                                                                                  | <span data-ttu-id="c2cf2-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2cf2-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2cf2-121"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cf2-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c2cf2-122">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c2cf2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2cf2-123">Remarks</span></span>

<span data-ttu-id="c2cf2-124">Die Funktion " **glscaling** " erzeugt eine allgemeine Skalierung entlang der *x*-, *y*-und *z* -Achse.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-124">The **glScaled** function produces a general scaling along the *x*, *y*, and *z* axes.</span></span> <span data-ttu-id="c2cf2-125">Die drei Argumente geben die gewünschten Skalierungsfaktoren entlang der drei Achsen an.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-125">The three arguments indicate the desired scale factors along each of the three axes.</span></span> <span data-ttu-id="c2cf2-126">Die resultierende Matrix ist</span><span class="sxs-lookup"><span data-stu-id="c2cf2-126">The resulting matrix is</span></span>

![Das Diagramm zeigt die Matrix der Skalierungsfaktoren entlang der x-, y-und z-Achse an.](images/scale01.png)

<span data-ttu-id="c2cf2-128">Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Skalierungs Matrix multipliziert, und das Produkt ersetzt die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-128">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this scale matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="c2cf2-129">Das heißt, wenn m die aktuelle Matrix und S die Skalierungs Matrix ist, wird m durch m S ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-129">That is, if M is the current matrix and S is the scale matrix, then M is replaced with M   S.</span></span>

<span data-ttu-id="c2cf2-130">Wenn der Matrix Modus "GL \_ Modelview" oder "GL" ist \_ , werden alle Objekte skaliert, die nach dem Aufruf von " **glbricks** " gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-130">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glScaled** is called are scaled.</span></span> <span data-ttu-id="c2cf2-131">Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix**](glpopmatrix.md) , um das nicht skalierte Koordinatensystem zu speichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c2cf2-131">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unscaled coordinate system.</span></span>

<span data-ttu-id="c2cf2-132">Wenn für die Modelview-Matrix andere Skalierungsfaktoren als 1,0 übernommen werden und Beleuchtung aktiviert ist, sollte die automatische Normalisierung von normalen wahrscheinlich auch aktiviert werden ([**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) mit dem Argument GL \_ normalize).</span><span class="sxs-lookup"><span data-stu-id="c2cf2-132">If scale factors other than 1.0 are applied to the modelview matrix and lighting is enabled, automatic normalization of normals should probably also be enabled ([**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_NORMALIZE).</span></span>

<span data-ttu-id="c2cf2-133">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glskaliert** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="c2cf2-133">The following functions retrieve information related to **glScaled**:</span></span>

<span data-ttu-id="c2cf2-134">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="c2cf2-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="c2cf2-135">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="c2cf2-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="c2cf2-136">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="c2cf2-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="c2cf2-137">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="c2cf2-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="c2cf2-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2cf2-138">Requirements</span></span>



| <span data-ttu-id="c2cf2-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2cf2-139">Requirement</span></span> | <span data-ttu-id="c2cf2-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c2cf2-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cf2-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2cf2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c2cf2-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2cf2-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2cf2-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2cf2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c2cf2-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2cf2-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2cf2-145">Header</span><span class="sxs-lookup"><span data-stu-id="c2cf2-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2cf2-146"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2cf2-146"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c2cf2-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2cf2-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2cf2-148"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2cf2-148"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2cf2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c2cf2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2cf2-150"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2cf2-150"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2cf2-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2cf2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cf2-152">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-152">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c2cf2-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c2cf2-154">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-154">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="c2cf2-155">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-155">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="c2cf2-156">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-156">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="c2cf2-157">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-157">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="c2cf2-158">**glrotiert**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-158">**glRotated**</span></span>](glrotated.md)
</dt> <dt>

[<span data-ttu-id="c2cf2-159">**glrotatef**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-159">**glRotatef**</span></span>](glrotatef.md)
</dt> <dt>

[<span data-ttu-id="c2cf2-160">**gltranslate**</span><span class="sxs-lookup"><span data-stu-id="c2cf2-160">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





