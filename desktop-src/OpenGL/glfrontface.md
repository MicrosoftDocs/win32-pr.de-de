---
title: glfrontface-Funktion (GL. h)
description: Die Funktion "glfrontface" definiert Front-und rückwärts gerichtete Polygone.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glfrontface-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957159"
---
# <a name="glfrontface-function"></a><span data-ttu-id="3be8d-104">glfrontface-Funktion</span><span class="sxs-lookup"><span data-stu-id="3be8d-104">glFrontFace function</span></span>

<span data-ttu-id="3be8d-105">Die Funktion " **glfrontface** " definiert Front-und rückwärts gerichtete Polygone.</span><span class="sxs-lookup"><span data-stu-id="3be8d-105">The **glFrontFace** function defines front-facing and back-facing polygons.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be8d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3be8d-106">Syntax</span></span>


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="3be8d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3be8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be8d-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="3be8d-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="3be8d-109">Die Ausrichtung von nach vorne gerichteten Polygonen.</span><span class="sxs-lookup"><span data-stu-id="3be8d-109">The orientation of front-facing polygons.</span></span> <span data-ttu-id="3be8d-110">GL \_ CW und GL \_ CCW werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3be8d-110">GL\_CW and GL\_CCW are accepted.</span></span> <span data-ttu-id="3be8d-111">Der Standardwert ist GL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="3be8d-111">The default value is GL\_CCW.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be8d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3be8d-112">Return value</span></span>

<span data-ttu-id="3be8d-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3be8d-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3be8d-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3be8d-114">Error codes</span></span>

<span data-ttu-id="3be8d-115">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3be8d-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3be8d-116">Name</span><span class="sxs-lookup"><span data-stu-id="3be8d-116">Name</span></span>                                                                                                  | <span data-ttu-id="3be8d-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3be8d-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3be8d-118"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3be8d-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3be8d-119">der *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="3be8d-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="3be8d-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="3be8d-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3be8d-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3be8d-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3be8d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3be8d-122">Remarks</span></span>

<span data-ttu-id="3be8d-123">In einer Szene, die vollständig aus nicht transparenten geschlossenen Oberflächen besteht, werden die rückwärts gerichteten Polygone nie sichtbar.</span><span class="sxs-lookup"><span data-stu-id="3be8d-123">In a scene composed entirely of opaque closed surfaces, back-facing polygons are never visible.</span></span> <span data-ttu-id="3be8d-124">Die Beseitigung dieser unsichtbaren Polygone hat den offensichtlichen Vorteil, dass das Rendering des Bilds beschleunigt wird.</span><span class="sxs-lookup"><span data-stu-id="3be8d-124">Eliminating these invisible polygons has the obvious benefit of speeding up the rendering of the image.</span></span> <span data-ttu-id="3be8d-125">Sie aktivieren und deaktivieren die Beseitigung von mit der Rückseite verknüpfte Polygone mit [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) mithilfe des "Argument GL \_ cull \_ Face".</span><span class="sxs-lookup"><span data-stu-id="3be8d-125">You enable and disable elimination of back-facing polygons with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) using argument GL\_CULL\_FACE.</span></span>

<span data-ttu-id="3be8d-126">Die Projektion einer Polygon-zu-Fenster-Koordinate wird als "im Uhrzeigersinn" bezeichnet, wenn ein imaginäres Objekt, das auf den Pfad vom ersten Scheitelpunkt, seinen zweiten Scheitelpunkt usw., bis zum letzten Scheitelpunkt folgt, und schließlich zurück zum ersten Scheitelpunkt in einer Richtung im Uhrzeigersinn zum Inneren des Polygons bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="3be8d-126">The projection of a polygon to window coordinates is said to have clockwise winding if an imaginary object following the path from its first vertex, its second vertex, and so on, to its last vertex, and finally back to its first vertex, moves in a clockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="3be8d-127">Das Vieleck des Polygons wird gegen den Uhrzeigersinn gesetzt, wenn das imaginäre Objekt, das denselben Pfad folgt, gegen den Uhrzeigersinn zum Inneren des Polygons bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="3be8d-127">The polygon's winding is said to be counterclockwise if the imaginary object following the same path moves in a counterclockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="3be8d-128">Die **glfrontface** -Funktion gibt an, ob Polygone mit dem Uhrzeigersinn im Uhrzeigersinn in Fenster Koordinaten oder gegen den Uhrzeigersinn im Uhrzeigersinn in Fenster Koordinaten übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="3be8d-128">The **glFrontFace** function specifies whether polygons with clockwise winding in window coordinates, or counterclockwise winding in window coordinates, are taken to be front-facing.</span></span> <span data-ttu-id="3be8d-129">Durch \_ die Übergabe von GL CCW an *Mode* werden Polygone gegen den Uhrzeigersinn als Front-on ausgewählt; GL \_ CW wählt Polygone im Uhrzeigersinn als Front-on aus.</span><span class="sxs-lookup"><span data-stu-id="3be8d-129">Passing GL\_CCW to *mode* selects counterclockwise polygons as front-facing; GL\_CW selects clockwise polygons as front-facing.</span></span> <span data-ttu-id="3be8d-130">Standardmäßig werden Polygone gegen den Uhrzeigersinn als Front-on verwendet.</span><span class="sxs-lookup"><span data-stu-id="3be8d-130">By default, counterclockwise polygons are taken to be front-facing.</span></span>

<span data-ttu-id="3be8d-131">Mit der folgenden Funktion werden Informationen zu **glfrontface** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="3be8d-131">The following function retrieves information about **glFrontface**:</span></span>

<span data-ttu-id="3be8d-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Front- \_ Face</span><span class="sxs-lookup"><span data-stu-id="3be8d-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FRONT\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="3be8d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3be8d-133">Requirements</span></span>



| <span data-ttu-id="3be8d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3be8d-134">Requirement</span></span> | <span data-ttu-id="3be8d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3be8d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3be8d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3be8d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3be8d-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3be8d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3be8d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3be8d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3be8d-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3be8d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3be8d-140">Header</span><span class="sxs-lookup"><span data-stu-id="3be8d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3be8d-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3be8d-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3be8d-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3be8d-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="3be8d-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3be8d-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3be8d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3be8d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3be8d-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3be8d-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be8d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3be8d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be8d-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3be8d-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3be8d-148">**glcullface**</span><span class="sxs-lookup"><span data-stu-id="3be8d-148">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="3be8d-149">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="3be8d-149">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="3be8d-150">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="3be8d-150">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="3be8d-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3be8d-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3be8d-152">**glget**</span><span class="sxs-lookup"><span data-stu-id="3be8d-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3be8d-153">**gllightmodel**</span><span class="sxs-lookup"><span data-stu-id="3be8d-153">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





