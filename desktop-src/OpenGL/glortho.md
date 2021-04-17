---
title: glortho-Funktion (GL. h)
description: Die glortho-Funktion multipliziert die aktuelle Matrix mit einer orthografischen Matrix.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glortho-Funktion OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104560255"
---
# <a name="glortho-function"></a><span data-ttu-id="71161-104">glortho-Funktion</span><span class="sxs-lookup"><span data-stu-id="71161-104">glOrtho function</span></span>

<span data-ttu-id="71161-105">Die **glortho** -Funktion multipliziert die aktuelle Matrix mit einer orthografischen Matrix.</span><span class="sxs-lookup"><span data-stu-id="71161-105">The **glOrtho** function multiplies the current matrix by an orthographic matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="71161-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="71161-106">Syntax</span></span>


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="71161-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="71161-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71161-108">*linken*</span><span class="sxs-lookup"><span data-stu-id="71161-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="71161-109">Die Koordinaten für die linke vertikale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="71161-109">The coordinates for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="71161-110">*Richting*</span><span class="sxs-lookup"><span data-stu-id="71161-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="71161-111">Die Koordinaten für die vertikale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="71161-111">The coordinates for theright vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="71161-112">*unten*</span><span class="sxs-lookup"><span data-stu-id="71161-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="71161-113">Die Koordinaten für die untere horizontale Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="71161-113">The coordinates for the bottom horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="71161-114">*top*</span><span class="sxs-lookup"><span data-stu-id="71161-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="71161-115">Die Koordinaten für die oberen horizontalen clippingpläne.</span><span class="sxs-lookup"><span data-stu-id="71161-115">The coordinates for the top horizontal clipping plans.</span></span>

</dd> <dt>

<span data-ttu-id="71161-116">*znear*</span><span class="sxs-lookup"><span data-stu-id="71161-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="71161-117">Die Abstände zur näheren Ausschneide Ebene.</span><span class="sxs-lookup"><span data-stu-id="71161-117">The distances to the nearer depth clipping plane.</span></span> <span data-ttu-id="71161-118">Diese Distanz ist negativ, wenn sich die Ebene hinter dem Viewer befinden soll.</span><span class="sxs-lookup"><span data-stu-id="71161-118">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> <dt>

<span data-ttu-id="71161-119">*zfar*</span><span class="sxs-lookup"><span data-stu-id="71161-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="71161-120">Die Abstände zur weiteren tiefen Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="71161-120">The distances to the farther depth clipping plane.</span></span> <span data-ttu-id="71161-121">Diese Distanz ist negativ, wenn sich die Ebene hinter dem Viewer befinden soll.</span><span class="sxs-lookup"><span data-stu-id="71161-121">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71161-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71161-122">Return value</span></span>

<span data-ttu-id="71161-123">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71161-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71161-124">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="71161-124">Error codes</span></span>

<span data-ttu-id="71161-125">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71161-125">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71161-126">Name</span><span class="sxs-lookup"><span data-stu-id="71161-126">Name</span></span>                                                                                                  | <span data-ttu-id="71161-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71161-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71161-128"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="71161-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71161-129">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="71161-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71161-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71161-130">Remarks</span></span>

<span data-ttu-id="71161-131">Die **glortho** -Funktion beschreibt eine perspektivische Matrix, die eine parallele Projektion erzeugt.</span><span class="sxs-lookup"><span data-stu-id="71161-131">The **glOrtho** function describes a perspective matrix that produces a parallel projection.</span></span> <span data-ttu-id="71161-132">Mit den Parametern (*left*, *Bottom*, *near*) und (*right*, *Top*, *near*) werden die Punkte auf der Near Clipping-Ebene angegeben, die der unteren linken und oberen rechten Ecke des Fensters zugeordnet sind, vorausgesetzt, das Auge befindet sich bei (0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="71161-132">The (*left*, *bottom*, *near*) and (*right*, *top*, *near*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0, 0, 0).</span></span> <span data-ttu-id="71161-133">Der *Far* -Parameter gibt den Speicherort der weit entfernten Clippingebene an.</span><span class="sxs-lookup"><span data-stu-id="71161-133">The *far* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="71161-134">*Znear* und *zfar* können entweder positiv oder negativ sein.</span><span class="sxs-lookup"><span data-stu-id="71161-134">Both *zNear* and *zFar* can be either positive or negative.</span></span> <span data-ttu-id="71161-135">Die entsprechende Matrix ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="71161-135">The corresponding matrix is shown in the following image.</span></span>

![Diagramm mit der Perspektiven Matrix, die von der Funktion "glortho" beschrieben wird.](images/ortho1.png)

<span data-ttu-id="71161-137">where</span><span class="sxs-lookup"><span data-stu-id="71161-137">where</span></span>

![Gleichungen, die die Perspektiven Matrix beschreiben.](images/ortho2.png)

<span data-ttu-id="71161-139">Die aktuelle Matrix wird mit dieser Matrix multipliziert, wobei die aktuelle Matrix durch das Ergebnis ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="71161-139">The current matrix is multiplied by this matrix with the result replacing the current matrix.</span></span> <span data-ttu-id="71161-140">Das heißt, wenn m die aktuelle Matrix und O die Ortho-Matrix ist, wird m durch m o ersetzt.</span><span class="sxs-lookup"><span data-stu-id="71161-140">That is, if M is the current matrix and O is the ortho matrix, then M is replaced with M   O.</span></span>

<span data-ttu-id="71161-141">Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix** , um den aktuellen Matrix Stapel zu speichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="71161-141">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the current matrix stack.</span></span> <span data-ttu-id="71161-142">Verwenden Sie [**glMatrixMode**](glmatrixmode.md) , um die aktuelle Matrix festzulegen.</span><span class="sxs-lookup"><span data-stu-id="71161-142">Use [**glMatrixMode**](glmatrixmode.md) to set the current matrix.</span></span>

<span data-ttu-id="71161-143">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glortho** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="71161-143">The following functions retrieve information related to **glOrtho**:</span></span>

<span data-ttu-id="71161-144">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="71161-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="71161-145">**glget** mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="71161-145">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="71161-146">**glget** mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="71161-146">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="71161-147">**glget** mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="71161-147">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="71161-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71161-148">Requirements</span></span>



| <span data-ttu-id="71161-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71161-149">Requirement</span></span> | <span data-ttu-id="71161-150">Wert</span><span class="sxs-lookup"><span data-stu-id="71161-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71161-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71161-151">Minimum supported client</span></span><br/> | <span data-ttu-id="71161-152">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71161-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71161-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71161-153">Minimum supported server</span></span><br/> | <span data-ttu-id="71161-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71161-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71161-155">Header</span><span class="sxs-lookup"><span data-stu-id="71161-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="71161-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71161-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71161-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71161-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="71161-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71161-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71161-159">DLL</span><span class="sxs-lookup"><span data-stu-id="71161-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71161-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71161-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71161-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71161-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71161-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71161-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71161-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71161-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71161-164">**glfrustum**</span><span class="sxs-lookup"><span data-stu-id="71161-164">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="71161-165">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="71161-165">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="71161-166">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="71161-166">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="71161-167">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="71161-167">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="71161-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="71161-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





