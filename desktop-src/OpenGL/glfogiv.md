---
title: glFogiv-Funktion (Gl.h)
description: Die Funktion "glfogiv" gibt Nebel Parameter an. | glfogiv-Funktion (GL. h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- glfogiv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFogiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fa4fefece05529cf5ff3906f19c5ad6e444249
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530692"
---
# <a name="glfogiv-function"></a><span data-ttu-id="2f54c-105">glfogiv-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f54c-105">glFogiv function</span></span>

<span data-ttu-id="2f54c-106">Die Funktion " **glfogfv** " gibt Nebel Parameter an.</span><span class="sxs-lookup"><span data-stu-id="2f54c-106">The **glFogfv** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f54c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f54c-107">Syntax</span></span>


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="2f54c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f54c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f54c-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="2f54c-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="2f54c-110">Gibt einen Nebel Parameter an.</span><span class="sxs-lookup"><span data-stu-id="2f54c-110">Specifies a fog parameter.</span></span>

<span data-ttu-id="2f54c-111">Akzeptiert einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="2f54c-111">Accepts one of the following values.</span></span>



| <span data-ttu-id="2f54c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2f54c-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="2f54c-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2f54c-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="2f54c-114"><dt>**GL- \_ Nebel \_ Modus**</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-114"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="2f54c-115">Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der die Gleichung angibt, die zum Berechnen des Nebel Blend Faktors *f* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f54c-115">The *params* parameter is a single integer value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="2f54c-116">Drei symbolische Konstanten werden akzeptiert: GL \_ linear, GL \_ exp und GL \_ exp2.</span><span class="sxs-lookup"><span data-stu-id="2f54c-116">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="2f54c-117">Die Gleichungen, die diesen symbolischen Konstanten entsprechen, werden im folgenden Abschnitt mit Hinweisen definiert.</span><span class="sxs-lookup"><span data-stu-id="2f54c-117">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="2f54c-118">Der standardnebelmodus ist GL \_ Exp.</span><span class="sxs-lookup"><span data-stu-id="2f54c-118">The default fog mode is GL\_EXP.</span></span><br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="2f54c-119"><dt>**GL- \_ Nebel \_ Dichte**</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-119"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="2f54c-120">Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der die *Dichte* angibt, die in beiden exponentiellen Nebel Gleichungen verwendete Nebeldichte.</span><span class="sxs-lookup"><span data-stu-id="2f54c-120">The *params* parameter is a single integer value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="2f54c-121">Nur nicht negative dichten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2f54c-121">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="2f54c-122">Die standardmäßige Nebeldichte ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="2f54c-122">The default fog density is 1.0.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="2f54c-123"><dt>**GL. \_ Nebel \_ Anfang**</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-123"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="2f54c-124">Der Parameter *para* Meters ist ein einzelner ganzzahliger Wert, der den *Start* angibt, wobei der Near Distance in der linearen Nebel Gleichung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f54c-124">The *params* parameter is a single integer value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="2f54c-125">Der Standardwert für fast Distance ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="2f54c-125">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="2f54c-126"><dt>**GL- \_ Nebel \_ Ende**</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-126"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="2f54c-127">Der Parameter " *para* meters" ist ein einzelner ganzzahliger Wert, der " *End*" angibt, d. h. der Abstand in der linearen Nebel Gleichung.</span><span class="sxs-lookup"><span data-stu-id="2f54c-127">The *params* parameter is a single integer value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="2f54c-128">Der Standardabstand ist 1,0.</span><span class="sxs-lookup"><span data-stu-id="2f54c-128">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="2f54c-129"><dt>**GL- \_ Nebel \_ Index**</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-129"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="2f54c-130">Der Parameter " *para* meters" ist ein einzelner ganzzahliger Wert, der *i*<sub>f</sub> angibt, dem Nebel Farbindex.</span><span class="sxs-lookup"><span data-stu-id="2f54c-130">The *params* parameter is a single integer value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="2f54c-131">Der standardmäßige Nebel Index ist 0,0.</span><span class="sxs-lookup"><span data-stu-id="2f54c-131">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <span data-ttu-id="2f54c-132"><dt>**GL- \_ Nebel \_ Farbe**</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-132"><dt>**GL\_FOG\_COLOR**</dt></span></span> </dl>       | <span data-ttu-id="2f54c-133">Der Parameter *para* meters enthält vier ganzzahlige Werte oder Gleit Komma Werte, die *C*<sub>f</sub> , die Nebelfarbe, angeben.</span><span class="sxs-lookup"><span data-stu-id="2f54c-133">The *params* parameter contains four integer or floating-point values that specify *C*<sub>f</sub> , the fog color.</span></span> <span data-ttu-id="2f54c-134">Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0.</span><span class="sxs-lookup"><span data-stu-id="2f54c-134">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="2f54c-135">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2f54c-135">Floating-point values are mapped directly.</span></span> <span data-ttu-id="2f54c-136">Nach der Konvertierung werden alle Farbkomponenten an den Bereich \[ 0, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="2f54c-136">After conversion, all color components are clamped to the range \[0,1\].</span></span> <span data-ttu-id="2f54c-137">Die standardmäßige Nebelfarbe ist (0,0).</span><span class="sxs-lookup"><span data-stu-id="2f54c-137">The default fog color is (0,0,0,0).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2f54c-138">*params*</span><span class="sxs-lookup"><span data-stu-id="2f54c-138">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="2f54c-139">Gibt den Wert oder die Werte an, die *PName* zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2f54c-139">Specifies the value or values to be assigned to *pname*.</span></span> <span data-ttu-id="2f54c-140">Die GL- \_ Nebel \_ Farbe erfordert ein Array mit vier Werten.</span><span class="sxs-lookup"><span data-stu-id="2f54c-140">GL\_FOG\_COLOR requires an array of four values.</span></span> <span data-ttu-id="2f54c-141">Alle anderen Parameter akzeptieren ein Array, das nur einen einzelnen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="2f54c-141">All other parameters accept an array containing only a single value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f54c-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f54c-142">Return value</span></span>

<span data-ttu-id="2f54c-143">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2f54c-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f54c-144">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2f54c-144">Error codes</span></span>

<span data-ttu-id="2f54c-145">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2f54c-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2f54c-146">Name</span><span class="sxs-lookup"><span data-stu-id="2f54c-146">Name</span></span>                                                                                                  | <span data-ttu-id="2f54c-147">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2f54c-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f54c-148"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2f54c-149">*PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="2f54c-149">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="2f54c-150"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2f54c-151">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2f54c-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2f54c-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f54c-152">Remarks</span></span>

<span data-ttu-id="2f54c-153">Sie aktivieren und deaktivieren den Nebel mit [**glEnable**](glenable.md) und [**glEnable**](gldisable.md)mithilfe des Arguments GL \_ Fog.</span><span class="sxs-lookup"><span data-stu-id="2f54c-153">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="2f54c-154">Wenn Sie aktiviert ist, wirkt sich der Nebel auf rasterisierte Geometrie, Bitmaps und Pixelblöcke aus, aber nicht auf Puffer Löschvorgänge.</span><span class="sxs-lookup"><span data-stu-id="2f54c-154">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="2f54c-155">Die Funktion " **glfogiv** " weist den Wert oder die Werte in den *para* Metern dem durch " *PName*" angegebenen Nebel Parameter zu.</span><span class="sxs-lookup"><span data-stu-id="2f54c-155">The **glFogiv** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="2f54c-156">Der Nebel kombiniert eine arrayfarbe mit der Post texturturfarbe jedes rasterisierten Pixel Fragments mithilfe eines Mischungs Faktors *f*.</span><span class="sxs-lookup"><span data-stu-id="2f54c-156">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="2f54c-157">Der Faktor *f* wird auf eine von drei Arten berechnet, abhängig vom Nebel Modus.</span><span class="sxs-lookup"><span data-stu-id="2f54c-157">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="2f54c-158">Lassen Sie *z* den Abstand in den Augen Koordinaten vom Ursprung zum Fragment, das gefockt wird, angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f54c-158">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="2f54c-159">Die Gleichung für den \_ linearen GL-Nebel lautet:</span><span class="sxs-lookup"><span data-stu-id="2f54c-159">The equation for GL\_LINEAR fog is:</span></span>

![Gleichung, die den Wert des Mischungs Faktors in GL_LINEAR Nebelmodus als Funktion der Entfernung anzeigt.](images/fog01.png)

<span data-ttu-id="2f54c-161">Die Gleichung für GL \_ Exp Nebel lautet:</span><span class="sxs-lookup"><span data-stu-id="2f54c-161">The equation for GL\_EXP fog is:</span></span>

![Gleichung, die den Wert des Mischungs Faktors in GL_EXP Nebel Modus anzeigt.](images/fog02.png)

<span data-ttu-id="2f54c-163">Die Gleichung für GL \_ exp2 Nebel lautet:</span><span class="sxs-lookup"><span data-stu-id="2f54c-163">The equation for GL\_EXP2 fog is:</span></span>

![Gleichung, die den Wert des Mischungs Faktors in GL_EXP2 Nebel Modus anzeigt.](images/fog03.png)

<span data-ttu-id="2f54c-165">Unabhängig vom Nebel Modus wird *f* an den Bereich \[ 0, 1, \] nach der Berechnung gebunden.</span><span class="sxs-lookup"><span data-stu-id="2f54c-165">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="2f54c-166">Wenn sich OpenGL im RGBA-Farbmodus befindet, wird die Farbe *C*<sub>r</sub> des Fragments durch ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2f54c-166">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Gleichung, die die Farbe des Foto Fragments als Funktion der Mischungs Faktor-und Nebelfarbe anzeigt.](images/fog04.png)

<span data-ttu-id="2f54c-168">Im Farb Index Modus wird der Farb Index *i*<sub>r</sub> des Fragments durch ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2f54c-168">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Gleichung, die den Farb Index des fogged-Fragments als Funktion des Mischungs Faktors und der indizierten Farbe anzeigt.](images/fog05.png)

<span data-ttu-id="2f54c-170">Die folgenden Funktionen rufen Informationen im Zusammenhang mit den **glfog** -Funktionen ab:</span><span class="sxs-lookup"><span data-stu-id="2f54c-170">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="2f54c-171">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Nebelfarbe</span><span class="sxs-lookup"><span data-stu-id="2f54c-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="2f54c-172">**glget** mit dem Argument GL- \_ Nebel \_ Index</span><span class="sxs-lookup"><span data-stu-id="2f54c-172">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="2f54c-173">**glget** mit dem Argument GL- \_ Nebel \_ Dichte</span><span class="sxs-lookup"><span data-stu-id="2f54c-173">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="2f54c-174">**glget** mit dem Argument GL \_ Nebel \_ Start</span><span class="sxs-lookup"><span data-stu-id="2f54c-174">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="2f54c-175">**glget** mit dem Argument GL- \_ Nebel \_ Ende</span><span class="sxs-lookup"><span data-stu-id="2f54c-175">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="2f54c-176">**glget** mit dem Argument GL- \_ Nebel \_ Modus</span><span class="sxs-lookup"><span data-stu-id="2f54c-176">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="2f54c-177">[**glisenabled**](glisenabled.md) mit Argument GL \_ Nebel</span><span class="sxs-lookup"><span data-stu-id="2f54c-177">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="2f54c-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f54c-178">Requirements</span></span>



| <span data-ttu-id="2f54c-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f54c-179">Requirement</span></span> | <span data-ttu-id="2f54c-180">Wert</span><span class="sxs-lookup"><span data-stu-id="2f54c-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f54c-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f54c-181">Minimum supported client</span></span><br/> | <span data-ttu-id="2f54c-182">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f54c-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2f54c-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f54c-183">Minimum supported server</span></span><br/> | <span data-ttu-id="2f54c-184">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f54c-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f54c-185">Header</span><span class="sxs-lookup"><span data-stu-id="2f54c-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f54c-186"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-186"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2f54c-187">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f54c-187">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f54c-188"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-188"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f54c-189">DLL</span><span class="sxs-lookup"><span data-stu-id="2f54c-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f54c-190"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f54c-190"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f54c-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f54c-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f54c-192">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2f54c-192">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2f54c-193">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="2f54c-193">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="2f54c-194">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="2f54c-194">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="2f54c-195">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2f54c-195">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2f54c-196">**glget**</span><span class="sxs-lookup"><span data-stu-id="2f54c-196">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2f54c-197">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="2f54c-197">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





