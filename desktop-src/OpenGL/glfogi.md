---
title: glFogi-Funktion (Gl.h)
description: Die Funktion "glfogi" gibt Nebel Parameter an.
ms.assetid: c2ffb41d-3d97-4b72-b16d-cfbffa1179d1
keywords:
- glfogi-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFogi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc718a007035204f6e984eea87f1e21ba09ac8f0
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "103869343"
---
# <a name="glfogi-function"></a><span data-ttu-id="4fba1-104">glfogi-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fba1-104">glFogi function</span></span>

<span data-ttu-id="4fba1-105">Die Funktion " **glfogi** " gibt Nebel Parameter an.</span><span class="sxs-lookup"><span data-stu-id="4fba1-105">The **glFogi** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fba1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fba1-106">Syntax</span></span>


```C++
void WINAPI glFogi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="4fba1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fba1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fba1-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="4fba1-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="4fba1-109">Gibt einen einwertigen Nebel Parameter an.</span><span class="sxs-lookup"><span data-stu-id="4fba1-109">Specifies a single-valued fog parameter.</span></span>

<span data-ttu-id="4fba1-110">Akzeptiert einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="4fba1-110">Accepts one of the following values.</span></span>



| <span data-ttu-id="4fba1-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4fba1-111">Value</span></span>                                                                                                                                                             | <span data-ttu-id="4fba1-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4fba1-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="4fba1-113"><dt>**GL- \_ Nebel \_ Modus**</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-113"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="4fba1-114">Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der die Gleichung angibt, die zum Berechnen des Nebel Blend Faktors *f* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fba1-114">The *params* parameter is a single integer value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="4fba1-115">Drei symbolische Konstanten werden akzeptiert: GL \_ linear, GL \_ exp und GL \_ exp2.</span><span class="sxs-lookup"><span data-stu-id="4fba1-115">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="4fba1-116">Die Gleichungen, die diesen symbolischen Konstanten entsprechen, werden im folgenden Abschnitt mit Hinweisen definiert.</span><span class="sxs-lookup"><span data-stu-id="4fba1-116">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="4fba1-117">Der standardnebelmodus ist GL \_ Exp.</span><span class="sxs-lookup"><span data-stu-id="4fba1-117">The default fog mode is GL\_EXP.</span></span><br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="4fba1-118"><dt>**GL- \_ Nebel \_ Dichte**</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-118"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="4fba1-119">Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der die *Dichte* angibt, die in beiden exponentiellen Nebel Gleichungen verwendete Nebeldichte.</span><span class="sxs-lookup"><span data-stu-id="4fba1-119">The *params* parameter is a single integer value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="4fba1-120">Nur nicht negative dichten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4fba1-120">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="4fba1-121">Die standardmäßige Nebeldichte ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="4fba1-121">The default fog density is 1.0.</span></span><br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="4fba1-122"><dt>**GL. \_ Nebel \_ Anfang**</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-122"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="4fba1-123">Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der den *Start* angibt, wobei der Near Distance in der linearen Nebel Gleichung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fba1-123">The *params* parameter is a single integer value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="4fba1-124">Der Standardwert für fast Distance ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="4fba1-124">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="4fba1-125"><dt>**GL- \_ Nebel \_ Ende**</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-125"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="4fba1-126">Der Parameter " *para* meters" ist ein einzelner ganzzahliger Wert, der " *End*" angibt, d. h. der Abstand in der linearen Nebel Gleichung.</span><span class="sxs-lookup"><span data-stu-id="4fba1-126">The *params* parameter is a single integer value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="4fba1-127">Der Standardabstand ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="4fba1-127">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="4fba1-128"><dt>**GL- \_ Nebel \_ Index**</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-128"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="4fba1-129">Der Parameter " *para* meters" ist ein einzelner ganzzahliger Wert, der *i*<sub>f</sub> angibt, dem Nebel Farbindex.</span><span class="sxs-lookup"><span data-stu-id="4fba1-129">The *params* parameter is a single integer value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="4fba1-130">Der standardmäßige Nebel Index ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="4fba1-130">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="4fba1-131">*param*</span><span class="sxs-lookup"><span data-stu-id="4fba1-131">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="4fba1-132">Gibt den Wert an, auf den *PName* festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4fba1-132">Specifies the value that *pname* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fba1-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fba1-133">Return value</span></span>

<span data-ttu-id="4fba1-134">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4fba1-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4fba1-135">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4fba1-135">Error codes</span></span>

<span data-ttu-id="4fba1-136">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4fba1-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4fba1-137">Name</span><span class="sxs-lookup"><span data-stu-id="4fba1-137">Name</span></span>                                                                                                  | <span data-ttu-id="4fba1-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4fba1-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fba1-139"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4fba1-140">*PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="4fba1-140">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="4fba1-141"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4fba1-142">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4fba1-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4fba1-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fba1-143">Remarks</span></span>

<span data-ttu-id="4fba1-144">Sie aktivieren und deaktivieren den Nebel mit [**glEnable**](glenable.md) und [**glEnable**](gldisable.md)mithilfe des Arguments GL \_ Fog.</span><span class="sxs-lookup"><span data-stu-id="4fba1-144">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="4fba1-145">Wenn Sie aktiviert ist, wirkt sich der Nebel auf rasterisierte Geometrie, Bitmaps und Pixelblöcke aus, aber nicht auf Puffer Löschvorgänge.</span><span class="sxs-lookup"><span data-stu-id="4fba1-145">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="4fba1-146">Die Funktion " **glfogi** " weist den Wert oder die Werte in den *para* Metern dem durch " *PName*" angegebenen Nebel Parameter zu.</span><span class="sxs-lookup"><span data-stu-id="4fba1-146">The **glFogi** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="4fba1-147">Der Nebel kombiniert eine arrayfarbe mit der Post texturturfarbe jedes rasterisierten Pixel Fragments mithilfe eines Mischungs Faktors *f*.</span><span class="sxs-lookup"><span data-stu-id="4fba1-147">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="4fba1-148">Der Faktor *f* wird auf eine von drei Arten berechnet, abhängig vom Nebel Modus.</span><span class="sxs-lookup"><span data-stu-id="4fba1-148">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="4fba1-149">Lassen Sie *z* den Abstand in den Augen Koordinaten vom Ursprung zum Fragment, das gefockt wird, angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fba1-149">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="4fba1-150">Die Gleichung für den \_ linearen GL-Nebel lautet:</span><span class="sxs-lookup"><span data-stu-id="4fba1-150">The equation for GL\_LINEAR fog is:</span></span>

![Gleichung, die den Wert GL_LINEAR Nebel anzeigt.](images/fog01.png)

<span data-ttu-id="4fba1-152">Die Gleichung für GL \_ Exp Nebel lautet:</span><span class="sxs-lookup"><span data-stu-id="4fba1-152">The equation for GL\_EXP fog is:</span></span>

![Gleichung, die den Wert des Mischungs Faktors in GL_EXP Nebel Modus anzeigt.](images/fog02.png)

<span data-ttu-id="4fba1-154">Die Gleichung für GL \_ exp2 Nebel lautet:</span><span class="sxs-lookup"><span data-stu-id="4fba1-154">The equation for GL\_EXP2 fog is:</span></span>

![Gleichung, die den Wert des Mischungs Faktors in GL_EXP2 Nebel Modus anzeigt.](images/fog03.png)

<span data-ttu-id="4fba1-156">Unabhängig vom Nebel Modus wird *f* an den Bereich \[ 0, 1, \] nach der Berechnung gebunden.</span><span class="sxs-lookup"><span data-stu-id="4fba1-156">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="4fba1-157">Wenn sich OpenGL im RGBA-Farbmodus befindet, wird die Farbe *C*<sub>r</sub> des Fragments durch ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4fba1-157">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Gleichung, die die Farbe des Foto Fragments als Funktion der Mischungs Faktor-und Nebelfarbe anzeigt.](images/fog04.png)

<span data-ttu-id="4fba1-159">Im Farb Index Modus wird der Farb Index *i*<sub>r</sub> des Fragments durch ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4fba1-159">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Gleichung, die den Farb Index des fogged-Fragments als Funktion des Mischungs Faktors und der indizierten Farbe anzeigt.](images/fog05.png)

<span data-ttu-id="4fba1-161">Die folgenden Funktionen rufen Informationen im Zusammenhang mit den **glfog** -Funktionen ab:</span><span class="sxs-lookup"><span data-stu-id="4fba1-161">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="4fba1-162">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Nebelfarbe</span><span class="sxs-lookup"><span data-stu-id="4fba1-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="4fba1-163">**glget** mit dem Argument GL- \_ Nebel \_ Index</span><span class="sxs-lookup"><span data-stu-id="4fba1-163">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="4fba1-164">**glget** mit dem Argument GL- \_ Nebel \_ Dichte</span><span class="sxs-lookup"><span data-stu-id="4fba1-164">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="4fba1-165">**glget** mit dem Argument GL \_ Nebel \_ Start</span><span class="sxs-lookup"><span data-stu-id="4fba1-165">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="4fba1-166">**glget** mit dem Argument GL- \_ Nebel \_ Ende</span><span class="sxs-lookup"><span data-stu-id="4fba1-166">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="4fba1-167">**glget** mit dem Argument GL- \_ Nebel \_ Modus</span><span class="sxs-lookup"><span data-stu-id="4fba1-167">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="4fba1-168">[**glisenabled**](glisenabled.md) mit Argument GL \_ Nebel</span><span class="sxs-lookup"><span data-stu-id="4fba1-168">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="4fba1-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fba1-169">Requirements</span></span>



| <span data-ttu-id="4fba1-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fba1-170">Requirement</span></span> | <span data-ttu-id="4fba1-171">Wert</span><span class="sxs-lookup"><span data-stu-id="4fba1-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fba1-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fba1-172">Minimum supported client</span></span><br/> | <span data-ttu-id="4fba1-173">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fba1-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4fba1-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fba1-174">Minimum supported server</span></span><br/> | <span data-ttu-id="4fba1-175">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fba1-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4fba1-176">Header</span><span class="sxs-lookup"><span data-stu-id="4fba1-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fba1-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4fba1-178">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4fba1-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fba1-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4fba1-180">DLL</span><span class="sxs-lookup"><span data-stu-id="4fba1-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fba1-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fba1-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fba1-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fba1-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fba1-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4fba1-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4fba1-184">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="4fba1-184">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="4fba1-185">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="4fba1-185">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="4fba1-186">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4fba1-186">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4fba1-187">**glget**</span><span class="sxs-lookup"><span data-stu-id="4fba1-187">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4fba1-188">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="4fba1-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





