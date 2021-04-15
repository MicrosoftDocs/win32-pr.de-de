---
title: gllightmodelfv-Funktion (GL. h)
description: Die gllightmodelfv-Funktion legt Beleuchtungsmodell Parameter fest.
ms.assetid: a62bcf3b-1769-48a3-8121-8f2b41266183
keywords:
- gllightmodelfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLightModelfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c20aea0851c542fd0d2c81de26da21a692fdb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517378"
---
# <a name="gllightmodelfv-function"></a><span data-ttu-id="548da-104">gllightmodelfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="548da-104">glLightModelfv function</span></span>

<span data-ttu-id="548da-105">Die [**gllightmodelfv**](gllightfv.md) -Funktion legt Beleuchtungsmodell Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="548da-105">The [**glLightModelfv**](gllightfv.md) function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="548da-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="548da-106">Syntax</span></span>


```C++
void WINAPI glLightModelfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="548da-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="548da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="548da-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="548da-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="548da-109">Ein Beleuchtungsmodell Parameter.</span><span class="sxs-lookup"><span data-stu-id="548da-109">A lighting model parameter.</span></span> <span data-ttu-id="548da-110">Die folgenden Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="548da-110">The following values are accepted.</span></span>



| <span data-ttu-id="548da-111">Wert</span><span class="sxs-lookup"><span data-stu-id="548da-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="548da-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="548da-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <span data-ttu-id="548da-113"><dt>**GL- \_ Light- \_ Modell \_ AMBIENT**</dt></span><span class="sxs-lookup"><span data-stu-id="548da-113"><dt>**GL\_LIGHT\_MODEL\_AMBIENT**</dt></span></span> </dl>                 | <span data-ttu-id="548da-114">Der Parameter *para* meters enthält vier Gleit Komma Werte, die die Umgebungs-RGBA-Intensität der gesamten Szene angeben.</span><span class="sxs-lookup"><span data-stu-id="548da-114">The *params* parameter contains four floating-point values that specify the ambient RGBA intensity of the entire scene.</span></span> <span data-ttu-id="548da-115">Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0.</span><span class="sxs-lookup"><span data-stu-id="548da-115">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="548da-116">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="548da-116">Floating-point values are mapped directly.</span></span> <span data-ttu-id="548da-117">Keine ganzzahligen oder Gleit Komma Werte werden geklammert.</span><span class="sxs-lookup"><span data-stu-id="548da-117">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="548da-118">Die Standard Intensität der Umgebungs Szene ist (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="548da-118">The default ambient scene intensity is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="548da-119"><dt>**\_ \_ \_ lokaler \_ Viewer für GL-Light-Modell**</dt></span><span class="sxs-lookup"><span data-stu-id="548da-119"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="548da-120">Der Parameter *para* Meters ist ein einzelner Gleit Komma Wert, der angibt, wie Glanz Winkel der Reflektion berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="548da-120">The *params* parameter is a single floating-point value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="548da-121">Wenn *param* den Wert 0 (oder 0,0) hat, nehmen Glanz reflektionswinkel die Ansichts Richtung an, und die Richtung der-*z* -Achse ist unabhängig von der Position des Scheitel Punkts in den Augen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="548da-121">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="548da-122">Andernfalls werden Glanz Spiegelung vom Ursprung des Augen Koordinatensystems berechnet.</span><span class="sxs-lookup"><span data-stu-id="548da-122">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="548da-123">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="548da-123">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="548da-124"><dt>**GL- \_ Light- \_ Modell auf \_ zwei \_ Seiten**</dt></span><span class="sxs-lookup"><span data-stu-id="548da-124"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="548da-125">Der Parameter *para* Meters ist ein einzelner Gleit Komma Wert, der angibt, ob einseitige oder zweiseitige Beleuchtungsberechnungen für Polygone durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="548da-125">The *params* parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="548da-126">Dies hat keine Auswirkung auf die Beleuchtungsberechnungen für Punkte, Linien oder Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="548da-126">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="548da-127">Wenn *param* 0 (oder 0,0) ist, wird eine einseitige Beleuchtung angegeben, und nur die Front-Material-Parameter werden in der Beleuchtungs Gleichung verwendet.</span><span class="sxs-lookup"><span data-stu-id="548da-127">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="548da-128">Andernfalls wird eine zweiseitige Beleuchtung angegeben.</span><span class="sxs-lookup"><span data-stu-id="548da-128">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="548da-129">In diesem Fall werden Vertices von rückwärts gerichteten Polygonen mit den backmaterialparametern beleuchtet und deren normale umgekehrt, bevor die Beleuchtungs Gleichung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="548da-129">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="548da-130">Vertices von nach vorne gerichteten Polygonen werden immer mit den Front-Material-Parametern beleuchtet, ohne dass ihre normale geändert werden.</span><span class="sxs-lookup"><span data-stu-id="548da-130">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="548da-131">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="548da-131">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="548da-132">*params*</span><span class="sxs-lookup"><span data-stu-id="548da-132">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="548da-133">Ein Zeiger auf den Wert oder die Werte, auf den Parameter fest *gelegt werden.*</span><span class="sxs-lookup"><span data-stu-id="548da-133">A pointer to the value or values to which *params* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="548da-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="548da-134">Return value</span></span>

<span data-ttu-id="548da-135">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="548da-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="548da-136">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="548da-136">Error codes</span></span>

<span data-ttu-id="548da-137">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="548da-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="548da-138">Name</span><span class="sxs-lookup"><span data-stu-id="548da-138">Name</span></span>                                                                                                  | <span data-ttu-id="548da-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="548da-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="548da-140"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="548da-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="548da-141">*PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="548da-141">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="548da-142"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="548da-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="548da-143">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="548da-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="548da-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="548da-144">Remarks</span></span>

<span data-ttu-id="548da-145">Die **gllightmodelfv** -Funktion legt den Beleuchtungsmodell Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="548da-145">The **glLightModelfv** function sets lighting model parameter.</span></span> <span data-ttu-id="548da-146">Der Parameter " *PName* " benennt einen *Parameter und gibt* den neuen Wert an. der Wert oder die Werte einzelner Licht Quellparameter.</span><span class="sxs-lookup"><span data-stu-id="548da-146">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="548da-147">Im RGBA-Modus ist die Farbe eines Scheitel Punkts die Summe der Material-Emissionsintensität, das Produkt der Material Ambient-Reflektion und das Beleuchtungsmodell der Umgebungs Intensität in voller Szene und der Anteil der einzelnen aktivierten Lichtquellen.</span><span class="sxs-lookup"><span data-stu-id="548da-147">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="548da-148">Jede helle Quelle trägt die Summe von drei Begriffen bei: Ambient, diffuses und specarität.</span><span class="sxs-lookup"><span data-stu-id="548da-148">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="548da-149">Der Ambient-Lichtquellen Beitrag ist das Produkt der Material Ambient Reflektion und der Umgebungs Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="548da-149">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="548da-150">Der Anteil der diffusen Lichtquelle ist das Produkt der Material diffctance, der diffusen Intensität des Lichts und des Punkt Produkts der normalen Vertex mit dem normalisierten Vektor aus dem Scheitelpunkt und der Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="548da-150">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="548da-151">Der Glanz der Glanzlicht Quelle ist das Produkt der hellen Glanz Reflektion, die Glanz Intensität des Lichts und das Punktprodukt der normalisierten Scheitelpunkt-zu-Auge-und Vertex-zu-Licht-Vektoren, die an die Leistungsfähigkeit des Materials hervorgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="548da-151">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="548da-152">Alle drei Lichtquellen Beiträge werden gleichmäßig auf Grundlage der Entfernung zwischen dem Scheitelpunkt und der Lichtquelle und der Lichtquelle, dem Spread-Exponent und dem Spread-Umstellungs-Winkel verringert.</span><span class="sxs-lookup"><span data-stu-id="548da-152">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="548da-153">Alle Punkt Produkte werden durch 0 (null) ersetzt, wenn Sie einen negativen Wert ergeben.</span><span class="sxs-lookup"><span data-stu-id="548da-153">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="548da-154">Die Alpha Komponente der resultierenden beleuchteten Farbe wird auf den Alpha-Wert der Material diffctance festgelegt.</span><span class="sxs-lookup"><span data-stu-id="548da-154">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="548da-155">Im Farb Index Modus wird der Wert des beleuchteten Indexes eines Scheitel Punkts von der Ambient-zu den Glanzwerten, die mithilfe von GL-Farbindizes an [**glmaterial**](glmaterial-functions.md) übergeben werden \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="548da-155">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="548da-156">Diffuse und glanzvolle Koeffizienten, berechnet mit einer (. 30,. 59, .11) Gewichtung der hellen Farben, dem Glanz des Materials und denselben Reflektions-und Dämpfungs Gleichungen wie im RGBA-Fall, legen fest, wie viel oben in der Umgebung der resultierende Index ist.</span><span class="sxs-lookup"><span data-stu-id="548da-156">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="548da-157">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **gllightmodelfv** -Funktion ab:</span><span class="sxs-lookup"><span data-stu-id="548da-157">The following functions retrieve information related to the **glLightModelfv** function:</span></span>

<span data-ttu-id="548da-158">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Light \_ Model \_ local \_ Viewer</span><span class="sxs-lookup"><span data-stu-id="548da-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="548da-159">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Light \_ Model \_ Two \_ Side</span><span class="sxs-lookup"><span data-stu-id="548da-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="548da-160">[**glisenabled**](glisenabled.md) mit dem Argument GL- \_ Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="548da-160">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="548da-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="548da-161">Requirements</span></span>



| <span data-ttu-id="548da-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="548da-162">Requirement</span></span> | <span data-ttu-id="548da-163">Wert</span><span class="sxs-lookup"><span data-stu-id="548da-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="548da-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="548da-164">Minimum supported client</span></span><br/> | <span data-ttu-id="548da-165">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="548da-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="548da-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="548da-166">Minimum supported server</span></span><br/> | <span data-ttu-id="548da-167">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="548da-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="548da-168">Header</span><span class="sxs-lookup"><span data-stu-id="548da-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="548da-169"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="548da-169"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="548da-170">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="548da-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="548da-171"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="548da-171"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="548da-172">DLL</span><span class="sxs-lookup"><span data-stu-id="548da-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="548da-173"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="548da-173"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548da-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="548da-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548da-175">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="548da-175">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="548da-176">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="548da-176">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="548da-177">**gllight**</span><span class="sxs-lookup"><span data-stu-id="548da-177">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="548da-178">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="548da-178">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





