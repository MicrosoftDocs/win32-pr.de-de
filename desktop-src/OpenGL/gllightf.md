---
title: gllightf-Funktion (GL. h)
description: Die gllightf-Funktion gibt Werte für helle Quellparameter zurück.
ms.assetid: d9f93fd9-6674-486f-a3fc-c10255dd37e7
keywords:
- gllightf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLightf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 099490461f5fbf6feb009e98c0228165938326d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743121"
---
# <a name="gllightf-function"></a><span data-ttu-id="3f218-104">gllightf-Funktion</span><span class="sxs-lookup"><span data-stu-id="3f218-104">glLightf function</span></span>

<span data-ttu-id="3f218-105">Die **gllightf** -Funktion gibt Werte für helle Quellparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="3f218-105">The **glLightf** function returns light source parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f218-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f218-106">Syntax</span></span>


```C++
void WINAPI glLightf(
   GLenum  light,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="3f218-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f218-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f218-108">*light*</span><span class="sxs-lookup"><span data-stu-id="3f218-108">*light*</span></span> 
</dt> <dd>

<span data-ttu-id="3f218-109">Der Bezeichner eines Lichts.</span><span class="sxs-lookup"><span data-stu-id="3f218-109">The identifier of a light.</span></span> <span data-ttu-id="3f218-110">Die Anzahl der möglichen Lichter hängt von der Implementierung ab, aber es werden mindestens acht Leuchten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f218-110">The number of possible lights depends on the implementation, but at least eight lights are supported.</span></span> <span data-ttu-id="3f218-111">Sie werden durch symbolische Namen der Form GL \_ Light *i* identifiziert, bei  der es sich um einen Wert handelt: 0 bis GL \_ Max \_ Lights-1.</span><span class="sxs-lookup"><span data-stu-id="3f218-111">They are identified by symbolic names of the form GL\_LIGHT *i* where *i* is a value: 0 to GL\_MAX\_LIGHTS - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3f218-112">*pName*</span><span class="sxs-lookup"><span data-stu-id="3f218-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="3f218-113">Ein einwertiger Light-Quellparameter für *Light*.</span><span class="sxs-lookup"><span data-stu-id="3f218-113">A single-valued light source parameter for *light*.</span></span> <span data-ttu-id="3f218-114">Die folgenden symbolischen Namen werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3f218-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="3f218-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3f218-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="3f218-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3f218-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <span data-ttu-id="3f218-117"><dt>**GL- \_ Spot- \_ Exponent**</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-117"><dt>**GL\_SPOT\_EXPONENT**</dt></span></span> </dl>                                                                                                                                                                             | <span data-ttu-id="3f218-118">Der Parameter *param* ist ein einzelner Gleit Komma Wert, der die Intensität des Lichts angibt.</span><span class="sxs-lookup"><span data-stu-id="3f218-118">The *param* parameter is a single floating-point value that specifies the intensity distribution of the light.</span></span> <span data-ttu-id="3f218-119">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3f218-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="3f218-120">Nur Werte im Bereich von \[ 0, 128 \] werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3f218-120">Only values in the range \[0, 128\] are accepted.</span></span> <br/> <span data-ttu-id="3f218-121">Die effektive Lichtintensität wird durch den Kosinus des Winkels zwischen der Richtung des Lichts und der Richtung vom Licht zum Vertex, der beleuchtet wird, und bis zur Potenz des Spot Exponenten verringert.</span><span class="sxs-lookup"><span data-stu-id="3f218-121">Effective light intensity is attenuated by the cosine of the angle between the direction of the light and the direction from the light to the vertex being lighted, raised to the power of the spot exponent.</span></span> <span data-ttu-id="3f218-122">Daher führen höhere Spot-expenten zu einer gezielteren Lichtquelle, unabhängig vom Punkt Umstellungs Winkel.</span><span class="sxs-lookup"><span data-stu-id="3f218-122">Thus, higher spot exponents result in a more focused light source, regardless of the spot cutoff angle.</span></span> <span data-ttu-id="3f218-123">Der standardmäßige Spot-Exponent ist 0 (null) und ergibt eine einheitliche Lichtverteilung.</span><span class="sxs-lookup"><span data-stu-id="3f218-123">The default spot exponent is 0, resulting in uniform light distribution.</span></span><br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <span data-ttu-id="3f218-124"><dt>**GL. \_ Spot- \_ cuumff**</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-124"><dt>**GL\_SPOT\_CUTOFF**</dt></span></span> </dl>                                                                                                                                                                                   | <span data-ttu-id="3f218-125">Der Parameter *param* ist ein einzelner Gleit Komma Wert, der den maximalen breitenwinkel einer Lichtquelle angibt.</span><span class="sxs-lookup"><span data-stu-id="3f218-125">The *param* parameter is a single floating-point value that specifies the maximum spread angle of a light source.</span></span> <span data-ttu-id="3f218-126">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3f218-126">Floating-point values are mapped directly.</span></span> <span data-ttu-id="3f218-127">Nur Werte im Bereich \[ 0, 90 \] und der spezielle Wert 180 werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3f218-127">Only values in the range \[0, 90\], and the special value 180, are accepted.</span></span> <br/> <span data-ttu-id="3f218-128">Wenn der Winkel zwischen der Richtung des Lichts und der Richtung vom Licht zum Scheitelpunkt größer als der Winkel Umstellungs Winkel ist, wird das Licht vollständig maskiert.</span><span class="sxs-lookup"><span data-stu-id="3f218-128">If the angle between the direction of the light and the direction from the light to the vertex being lighted is greater than the spot cutoff angle, then the light is completely masked.</span></span> <span data-ttu-id="3f218-129">Andernfalls wird die Intensität durch den Spot Exponent und die Dämpfungsfaktoren gesteuert.</span><span class="sxs-lookup"><span data-stu-id="3f218-129">Otherwise, its intensity is controlled by the spot exponent and the attenuation factors.</span></span> <span data-ttu-id="3f218-130">Der Standardwert für die Spot-Umstellungs Funktion ist 180, was eine einheitliche Lichtverteilung zur Folge hat.</span><span class="sxs-lookup"><span data-stu-id="3f218-130">The default spot cutoff is 180, resulting in uniform light distribution.</span></span><br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <span data-ttu-id="3f218-131"><dt>**GL- \_ Konstante \_ Dämpfung, GL- \_ lineare \_ Dämpfung, GL- \_ quadratische \_ Dämpfung**</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-131"><dt>**GL\_CONSTANT\_ATTENUATION, GL\_LINEAR\_ATTENUATION, GL\_QUADRATIC\_ATTENUATION**</dt></span></span> </dl> | <span data-ttu-id="3f218-132">Der Parameter *param* ist ein einzelner Gleit Komma Wert, der einen der drei Licht Dämpfungsfaktoren angibt.</span><span class="sxs-lookup"><span data-stu-id="3f218-132">The *param* parameter is a single floating-point value that specifies one of the three light attenuation factors.</span></span> <span data-ttu-id="3f218-133">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3f218-133">Floating-point values are mapped directly.</span></span> <span data-ttu-id="3f218-134">Nur nicht negative Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3f218-134">Only nonnegative values are accepted.</span></span> <br/> <span data-ttu-id="3f218-135">Wenn das Licht positionell und nicht direktional ist, wird seine Intensität durch die gegenseitige Summe der Summe von verringert: der Konstante Faktor, der lineare Faktor multipliziert mit dem Abstand zwischen dem Licht und dem Vertex, der beleuchtet wird, und der quadratische Faktor multipliziert mit dem Quadrat desselben Abstands.</span><span class="sxs-lookup"><span data-stu-id="3f218-135">If the light is positional, rather than directional, its intensity is attenuated by the reciprocal of the sum of: the constant factor, the linear factor multiplied by the distance between the light and the vertex being lighted, and the quadratic factor multiplied by the square of the same distance.</span></span> <span data-ttu-id="3f218-136">Die standardmäßigen Dämpfungsfaktoren sind (1, 0, 0), was zu einer nicht Dämpfung führt.</span><span class="sxs-lookup"><span data-stu-id="3f218-136">The default attenuation factors are (1,0,0), resulting in no attenuation.</span></span><br/>                   |



 

</dd> <dt>

<span data-ttu-id="3f218-137">*param*</span><span class="sxs-lookup"><span data-stu-id="3f218-137">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="3f218-138">Gibt den Wert an, auf den der Parameter " *PName* " von Light Source *Light* festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3f218-138">Specifies the value that parameter *pname* of light source *light* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f218-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f218-139">Return value</span></span>

<span data-ttu-id="3f218-140">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3f218-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3f218-141">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3f218-141">Error codes</span></span>

<span data-ttu-id="3f218-142">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3f218-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3f218-143">Name</span><span class="sxs-lookup"><span data-stu-id="3f218-143">Name</span></span>                                                                                                  | <span data-ttu-id="3f218-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3f218-144">Meaning</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f218-145"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3f218-146">*Light* oder *PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="3f218-146">*light* or *pname* was not an accepted value.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="3f218-147"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="3f218-148">Ein Spot Exponent-Wert wurde außerhalb des Bereichs \[ 0, 128 \] oder der Spot-cuum angegeben, der außerhalb des Bereichs \[ 0, 90 \] (mit Ausnahme des sonderwerts 180) angegeben wurde, oder es wurde ein negativer Dämpfungsfaktor angegeben.</span><span class="sxs-lookup"><span data-stu-id="3f218-148">A spot exponent value was specified outside the range \[0, 128\], or spot cutoff was specified outside the range \[0, 90\] (except for the special value 180), or a negative attenuation factor was specified.</span></span><br/> |
| <dl> <span data-ttu-id="3f218-149"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3f218-150">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3f218-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="3f218-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f218-151">Remarks</span></span>

<span data-ttu-id="3f218-152">Die **gllightf** -Funktion legt den Wert oder die Werte einzelner Lichtquellen Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="3f218-152">The **glLightf** function sets the value or values of individual light source parameters.</span></span> <span data-ttu-id="3f218-153">Der *Light* -Parameter benennt das Licht und ist ein symbolischer Name der Form GL \_ Light *i*, wobei 0 = *i* < GL \_ Max \_ Lights ist.</span><span class="sxs-lookup"><span data-stu-id="3f218-153">The *light* parameter names the light and is a symbolic name of the form GL\_LIGHT *i*, where 0 = *i* < GL\_MAX\_LIGHTS.</span></span>

<span data-ttu-id="3f218-154">Der *PName* -Parameter gibt einen der hellen Quellparameter an, und zwar erneut durch einen symbolischen Namen.</span><span class="sxs-lookup"><span data-stu-id="3f218-154">The *pname* parameter specifies one of the light source parameters, again by symbolic name.</span></span> <span data-ttu-id="3f218-155">Der Parameter *param* ist entweder ein einzelner Wert oder ein Zeiger auf ein Array, das die neuen Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="3f218-155">The *param* parameter is either a single value or a pointer to an array that contains the new values.</span></span>

<span data-ttu-id="3f218-156">Die Beleuchtungs Berechnung wird mithilfe von " [**glEnable**](glenable.md) " und " [**glEnable**](gldisable.md) " mit dem Argument "GL Beleuchtung" aktiviert \_</span><span class="sxs-lookup"><span data-stu-id="3f218-156">Lighting calculation is enabled and disabled using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_LIGHTING.</span></span> <span data-ttu-id="3f218-157">Wenn Beleuchtung aktiviert ist, tragen helle Quellen, die aktiviert sind, zur Beleuchtungs Berechnung bei.</span><span class="sxs-lookup"><span data-stu-id="3f218-157">When lighting is enabled, light sources that are enabled contribute to the lighting calculation.</span></span> <span data-ttu-id="3f218-158">Light Source *i* wird mithilfe von **glEnable** und **gldeaktiviert** mit dem Argument GL \_ Light *i* aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3f218-158">Light source *i* is enabled and disabled using **glEnable** and **glDisable** with argument GL\_LIGHT *i*.</span></span>

<span data-ttu-id="3f218-159">Es ist immer der Fall, dass GL \_ Light *i* = GL \_ LIGHT0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="3f218-159">It is always the case that GL\_LIGHT *i* = GL\_LIGHT0 + *i*.</span></span>

<span data-ttu-id="3f218-160">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **gllightf** -Funktion ab:</span><span class="sxs-lookup"><span data-stu-id="3f218-160">The following functions retrieve information related to the **glLightf** function:</span></span>

[<span data-ttu-id="3f218-161">**glgetlight**</span><span class="sxs-lookup"><span data-stu-id="3f218-161">**glGetLight**</span></span>](glgetlight.md)

<span data-ttu-id="3f218-162">[**glisenabled**](glisenabled.md) mit dem Argument GL- \_ Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="3f218-162">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="3f218-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f218-163">Requirements</span></span>



| <span data-ttu-id="3f218-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f218-164">Requirement</span></span> | <span data-ttu-id="3f218-165">Wert</span><span class="sxs-lookup"><span data-stu-id="3f218-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f218-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f218-166">Minimum supported client</span></span><br/> | <span data-ttu-id="3f218-167">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f218-167">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3f218-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f218-168">Minimum supported server</span></span><br/> | <span data-ttu-id="3f218-169">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f218-169">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f218-170">Header</span><span class="sxs-lookup"><span data-stu-id="3f218-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f218-171"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-171"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3f218-172">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f218-172">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f218-173"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-173"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f218-174">DLL</span><span class="sxs-lookup"><span data-stu-id="3f218-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f218-175"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f218-175"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f218-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f218-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f218-177">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3f218-177">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3f218-178">**glcolormaterial**</span><span class="sxs-lookup"><span data-stu-id="3f218-178">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="3f218-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3f218-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3f218-180">**gllightmodel**</span><span class="sxs-lookup"><span data-stu-id="3f218-180">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="3f218-181">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="3f218-181">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





