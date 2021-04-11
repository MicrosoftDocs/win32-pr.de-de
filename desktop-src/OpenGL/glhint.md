---
title: glhint-Funktion (GL. h)
description: Die Funktion "glhint" gibt Implementierungs spezifische Hinweise an.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glhint-Funktion OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103198"
---
# <a name="glhint-function"></a><span data-ttu-id="5521d-104">glhint-Funktion</span><span class="sxs-lookup"><span data-stu-id="5521d-104">glHint function</span></span>

<span data-ttu-id="5521d-105">Die Funktion " **glhint** " gibt Implementierungs spezifische Hinweise an.</span><span class="sxs-lookup"><span data-stu-id="5521d-105">The **glHint** function specifies implementation-specific hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="5521d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5521d-106">Syntax</span></span>


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="5521d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5521d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5521d-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="5521d-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="5521d-109">Eine symbolische Konstante, die das zu kontrollier Ende Verhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="5521d-109">A symbolic constant indicating the behavior to be controlled.</span></span> <span data-ttu-id="5521d-110">Die folgenden symbolischen Konstanten, zusammen mit der vorgeschlagenen Semantik, werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5521d-110">The following symbolic constants, along with suggested semantics, are accepted.</span></span>



| <span data-ttu-id="5521d-111">Wert</span><span class="sxs-lookup"><span data-stu-id="5521d-111">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="5521d-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5521d-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <span data-ttu-id="5521d-113"><dt>**GL- \_ Nebel \_ Hinweis**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-113"><dt>**GL\_FOG\_HINT**</dt></span></span> </dl>                                                           | <span data-ttu-id="5521d-114">Gibt die Genauigkeit der Nebel Berechnung an.</span><span class="sxs-lookup"><span data-stu-id="5521d-114">Indicates the accuracy of fog calculation.</span></span> <span data-ttu-id="5521d-115">Wenn die Berechnung pro Pixel-Nebel von der OpenGL-Implementierung nicht effizient unterstützt wird, kann das Hinweise von GL nicht \_ \_ Care oder GL \_ schnellste zu einer pro-Vertex-Berechnung von Nebeleffekten führen.</span><span class="sxs-lookup"><span data-stu-id="5521d-115">If per-pixel fog calculation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in per-vertex calculation of fog effects.</span></span><br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <span data-ttu-id="5521d-116"><dt>**GL- \_ Linien- \_ Smooth- \_ Hinweis**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-116"><dt>**GL\_LINE\_SMOOTH\_HINT**</dt></span></span> </dl>                                  | <span data-ttu-id="5521d-117">Gibt die Stichproben Qualität von Zeilen mit Antialiasing an.</span><span class="sxs-lookup"><span data-stu-id="5521d-117">Indicates the sampling quality of antialiased lines.</span></span> <span data-ttu-id="5521d-118">Hinting GL \_ schönste kann dazu führen, dass während der rasterisierung mehr Pixel Fragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5521d-118">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <span data-ttu-id="5521d-119"><dt>**GL \_ Perspective- \_ Korrektur \_ Hinweis**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-119"><dt>**GL\_PERSPECTIVE\_CORRECTION\_HINT**</dt></span></span> </dl> | <span data-ttu-id="5521d-120">Gibt die Qualität der Farb-und Texturkoordinaten Interpolations an.</span><span class="sxs-lookup"><span data-stu-id="5521d-120">Indicates the quality of color and texture coordinate interpolation.</span></span> <span data-ttu-id="5521d-121">Wenn die parameterinterpolung von Perspektiven korrigiert nicht effizient von der OpenGL-Implementierung unterstützt wird, kann das Hinweise von GL nicht \_ \_ Care oder GL \_ schnellste zu einer einfachen linearen interpolung von Farben und/oder Texturkoordinaten führen.</span><span class="sxs-lookup"><span data-stu-id="5521d-121">If perspective-corrected parameter interpolation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in simple linear interpolation of colors and/or texture coordinates.</span></span><br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <span data-ttu-id="5521d-122"><dt>**GL \_ Point \_ Smooth- \_ Hinweis**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-122"><dt>**GL\_POINT\_SMOOTH\_HINT**</dt></span></span> </dl>                               | <span data-ttu-id="5521d-123">Gibt die Stichproben Qualität von Antialiasing Punkten an.</span><span class="sxs-lookup"><span data-stu-id="5521d-123">Indicates the sampling quality of antialiased points.</span></span> <span data-ttu-id="5521d-124">Hinting GL \_ schönste kann dazu führen, dass während der rasterisierung mehr Pixel Fragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5521d-124">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <span data-ttu-id="5521d-125"><dt>**GL- \_ Polygon- \_ Smooth- \_ Hinweis**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-125"><dt>**GL\_POLYGON\_SMOOTH\_HINT**</dt></span></span> </dl>                         | <span data-ttu-id="5521d-126">Gibt die Stichproben Qualität von Polygonen mit antialigwerten an.</span><span class="sxs-lookup"><span data-stu-id="5521d-126">Indicates the sampling quality of antialiased polygons.</span></span> <span data-ttu-id="5521d-127">Hinting GL \_ schönste kann dazu führen, dass während der rasterisierung mehr Pixel Fragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5521d-127">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="5521d-128">*mode*</span><span class="sxs-lookup"><span data-stu-id="5521d-128">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="5521d-129">Eine symbolische Konstante, die das gewünschte Verhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="5521d-129">A symbolic constant indicating the desired behavior.</span></span> <span data-ttu-id="5521d-130">Die folgenden symbolischen Konstanten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5521d-130">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="5521d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5521d-131">Value</span></span>                                                                                                                                                       | <span data-ttu-id="5521d-132">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5521d-132">Meaning</span></span>                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <span data-ttu-id="5521d-133"><dt>**GL \_ schnellste**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-133"><dt>**GL\_FASTEST**</dt></span></span> </dl>        | <span data-ttu-id="5521d-134">Die effizienteste Option sollte ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="5521d-134">The most efficient option should be chosen.</span></span><br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <span data-ttu-id="5521d-135"><dt>**GL am \_ schönsten**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-135"><dt>**GL\_NICEST**</dt></span></span> </dl>           | <span data-ttu-id="5521d-136">Die am besten geeignete Option oder höchste Qualität sollte ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="5521d-136">The most correct, or highest quality, option should be chosen.</span></span><br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <span data-ttu-id="5521d-137"><dt>**GL ist nicht \_ \_ wichtig**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-137"><dt>**GL\_DONT\_CARE**</dt></span></span> </dl> | <span data-ttu-id="5521d-138">Der Client hat keine bevorzugte Einstellung.</span><span class="sxs-lookup"><span data-stu-id="5521d-138">The client doesn't have a preference.</span></span><br/>                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5521d-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5521d-139">Return value</span></span>

<span data-ttu-id="5521d-140">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5521d-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5521d-141">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="5521d-141">Error codes</span></span>

<span data-ttu-id="5521d-142">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5521d-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5521d-143">Name</span><span class="sxs-lookup"><span data-stu-id="5521d-143">Name</span></span>                                                                                                  | <span data-ttu-id="5521d-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5521d-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5521d-145"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5521d-146">der *Ziel* -oder *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="5521d-146">*target* or *mode* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="5521d-147"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5521d-148">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5521d-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5521d-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5521d-149">Remarks</span></span>

<span data-ttu-id="5521d-150">Wenn es Raum für die Interpretation gibt, können Sie bestimmte Aspekte des OpenGL-Verhaltens mit Hinweisen steuern.</span><span class="sxs-lookup"><span data-stu-id="5521d-150">When there is room for interpretation, you can control certain aspects of OpenGL behavior with hints.</span></span> <span data-ttu-id="5521d-151">Sie geben einen Hinweis mit zwei Argumenten an.</span><span class="sxs-lookup"><span data-stu-id="5521d-151">You specify a hint with two arguments.</span></span> <span data-ttu-id="5521d-152">Der *Ziel* Parameter ist eine symbolische Konstante, die das Verhalten angibt, das gesteuert werden soll, und der *Modus* ist eine weitere symbolische Konstante, die das gewünschte Verhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="5521d-152">The *target* parameter is a symbolic constant indicating the behavior to be controlled, and *mode* is another symbolic constant indicating the desired behavior.</span></span>

<span data-ttu-id="5521d-153">Obwohl die Implementierungsaspekte, die angegeben werden können, wohl definiert sind, hängt die Interpretation der Hinweise von der Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="5521d-153">Though the implementation aspects that can be hinted are well defined, the interpretation of the hints depends on the implementation.</span></span>

<span data-ttu-id="5521d-154">Die **glhint** -Funktion kann ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="5521d-154">The **glHint** function can be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5521d-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5521d-155">Requirements</span></span>



| <span data-ttu-id="5521d-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5521d-156">Requirement</span></span> | <span data-ttu-id="5521d-157">Wert</span><span class="sxs-lookup"><span data-stu-id="5521d-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5521d-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5521d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="5521d-159">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5521d-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5521d-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5521d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="5521d-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5521d-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5521d-162">Header</span><span class="sxs-lookup"><span data-stu-id="5521d-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="5521d-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5521d-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5521d-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="5521d-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5521d-166">DLL</span><span class="sxs-lookup"><span data-stu-id="5521d-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5521d-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5521d-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5521d-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5521d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5521d-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5521d-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5521d-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5521d-170">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





