---
title: glcullface-Funktion (GL. h)
description: Mit der Funktion "glcullface" wird angegeben, ob Front-of-und Back-of-factorins gefiltert werden können.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glcullface-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949529"
---
# <a name="glcullface-function"></a><span data-ttu-id="dbf71-104">glcullface-Funktion</span><span class="sxs-lookup"><span data-stu-id="dbf71-104">glCullFace function</span></span>

<span data-ttu-id="dbf71-105">Mit der Funktion " **glcullface** " wird angegeben, ob Front-of-und Back-of-factorins gefiltert werden können.</span><span class="sxs-lookup"><span data-stu-id="dbf71-105">The **glCullFace** function specifies whether front-facing or back-facing facets can be culled.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf71-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbf71-106">Syntax</span></span>


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="dbf71-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbf71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf71-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="dbf71-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="dbf71-109">Gibt an, ob Vordergrund-oder Hintergrund Facetten als Kandidaten für die Berechnung dienen.</span><span class="sxs-lookup"><span data-stu-id="dbf71-109">Specifies whether front-facing or back-facing facets are candidates for culling.</span></span> <span data-ttu-id="dbf71-110">Die symbolischen Konstanten GL \_ Front, GL \_ Back und GL \_ Front \_ und \_ Back werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="dbf71-110">The symbolic constants GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK are accepted.</span></span> <span data-ttu-id="dbf71-111">Der Standardwert ist "GL \_ Back".</span><span class="sxs-lookup"><span data-stu-id="dbf71-111">The default value is GL\_BACK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf71-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbf71-112">Return value</span></span>

<span data-ttu-id="dbf71-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dbf71-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dbf71-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="dbf71-114">Error codes</span></span>

<span data-ttu-id="dbf71-115">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dbf71-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="dbf71-116">Name</span><span class="sxs-lookup"><span data-stu-id="dbf71-116">Name</span></span>                                                                                                  | <span data-ttu-id="dbf71-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dbf71-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbf71-118"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dbf71-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="dbf71-119">der *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="dbf71-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="dbf71-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="dbf71-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="dbf71-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dbf71-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dbf71-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbf71-122">Remarks</span></span>

<span data-ttu-id="dbf71-123">Die Funktion " **glcullface** " gibt an, ob Front-und Hintergrund Facetten (wie im Modus festgelegt) durch ein-und facetentergebnissen (im *Modus* festgelegt) gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="dbf71-123">The **glCullFace** function specifies whether front-facing or back-facing facets are culled (as specified by *mode*) when facet culling is enabled.</span></span> <span data-ttu-id="dbf71-124">Sie aktivieren und deaktivieren die faceterelung mithilfe von [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md) mit dem Argument GL \_ cull \_ Face.</span><span class="sxs-lookup"><span data-stu-id="dbf71-124">You enable and disable facet culling using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_CULL\_FACE.</span></span> <span data-ttu-id="dbf71-125">Facetten sind Dreiecke, Vierecke, Polygone und Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="dbf71-125">Facets include triangles, quadrilaterals, polygons, and rectangles.</span></span>

<span data-ttu-id="dbf71-126">Die [**glfrontface**](glfrontface.md) -Funktion gibt an, welcher der Uhrzeigersinn-und gegen Uhrzeigersinn-Facetten Front-und rückwärts-ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="dbf71-126">The [**glFrontFace**](glfrontface.md) function specifies which of the clockwise and counterclockwise facets are front-facing and back-facing.</span></span>

<span data-ttu-id="dbf71-127">Wenn der *Modus* "GL" \_ vor \_ und hinten ist \_ , werden keine Facetten gezeichnet, aber andere primitive, z. b. Punkte und Linien, werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dbf71-127">If *mode* is GL\_FRONT\_AND\_BACK, no facets are drawn, but other primitives, such as points and lines, are drawn.</span></span>

<span data-ttu-id="dbf71-128">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glcullface** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="dbf71-128">The following functions retrieve information related to **glCullFace**:</span></span>

<span data-ttu-id="dbf71-129">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ cull \_ Face \_ Mode"</span><span class="sxs-lookup"><span data-stu-id="dbf71-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CULL\_FACE\_MODE</span></span>

<span data-ttu-id="dbf71-130">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ cull \_ Face</span><span class="sxs-lookup"><span data-stu-id="dbf71-130">[**glIsEnabled**](glisenabled.md) with argument GL\_CULL\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf71-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbf71-131">Requirements</span></span>



| <span data-ttu-id="dbf71-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbf71-132">Requirement</span></span> | <span data-ttu-id="dbf71-133">Wert</span><span class="sxs-lookup"><span data-stu-id="dbf71-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf71-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbf71-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf71-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbf71-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dbf71-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbf71-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf71-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbf71-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dbf71-138">Header</span><span class="sxs-lookup"><span data-stu-id="dbf71-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf71-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf71-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dbf71-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dbf71-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbf71-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbf71-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dbf71-142">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf71-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbf71-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf71-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf71-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbf71-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf71-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="dbf71-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dbf71-146">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="dbf71-146">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="dbf71-147">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="dbf71-147">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="dbf71-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="dbf71-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dbf71-149">**glfrontface**</span><span class="sxs-lookup"><span data-stu-id="dbf71-149">**glFrontFace**</span></span>](glfrontface.md)
</dt> <dt>

[<span data-ttu-id="dbf71-150">**glget**</span><span class="sxs-lookup"><span data-stu-id="dbf71-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="dbf71-151">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="dbf71-151">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





