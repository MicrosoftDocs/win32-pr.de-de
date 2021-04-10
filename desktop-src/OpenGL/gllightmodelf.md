---
title: gllightmodelf-Funktion (GL. h)
description: Die gllightmodelf-Funktion legt Beleuchtungsmodell Parameter fest.
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- gllightmodelf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2c17f7dc82080544a9055805cf62726227c200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040130"
---
# <a name="gllightmodelf-function"></a><span data-ttu-id="e40bf-104">gllightmodelf-Funktion</span><span class="sxs-lookup"><span data-stu-id="e40bf-104">glLightModelf function</span></span>

<span data-ttu-id="e40bf-105">Die **gllightmodelf** -Funktion legt Beleuchtungsmodell Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="e40bf-105">The **glLightModelf** function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e40bf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e40bf-106">Syntax</span></span>


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a><span data-ttu-id="e40bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e40bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e40bf-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="e40bf-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="e40bf-109">Ein einwertiger Beleuchtungsmodell Parameter.</span><span class="sxs-lookup"><span data-stu-id="e40bf-109">A single-valued lighting model parameter.</span></span> <span data-ttu-id="e40bf-110">Die folgenden Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e40bf-110">The following values are accepted.</span></span>



| <span data-ttu-id="e40bf-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e40bf-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="e40bf-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e40bf-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="e40bf-113"><dt>**\_ \_ \_ lokaler \_ Viewer für GL-Light-Modell**</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-113"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="e40bf-114">Der Parameter *param* ist ein einzelner Gleit Komma Wert, der angibt, wie Glanz Winkel der Reflektion berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="e40bf-114">The *param* parameter is a single floating-point value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="e40bf-115">Wenn *param* den Wert 0 (oder 0,0) hat, nehmen Glanz reflektionswinkel die Ansichts Richtung an, und die Richtung der-*z* -Achse ist unabhängig von der Position des Scheitel Punkts in den Augen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="e40bf-115">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="e40bf-116">Andernfalls werden Glanz Spiegelung vom Ursprung des Augen Koordinatensystems berechnet.</span><span class="sxs-lookup"><span data-stu-id="e40bf-116">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="e40bf-117">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="e40bf-117">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="e40bf-118"><dt>**GL- \_ Light- \_ Modell auf \_ zwei \_ Seiten**</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-118"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="e40bf-119">Der Parameter *param* ist ein einzelner Gleit Komma Wert, der angibt, ob einseitige oder zweiseitige Beleuchtungsberechnungen für Polygone durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e40bf-119">The *param* parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="e40bf-120">Dies hat keine Auswirkung auf die Beleuchtungsberechnungen für Punkte, Linien oder Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="e40bf-120">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="e40bf-121">Wenn *param* 0 (oder 0,0) ist, wird eine einseitige Beleuchtung angegeben, und nur die Front-Material-Parameter werden in der Beleuchtungs Gleichung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e40bf-121">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="e40bf-122">Andernfalls wird eine zweiseitige Beleuchtung angegeben.</span><span class="sxs-lookup"><span data-stu-id="e40bf-122">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="e40bf-123">In diesem Fall werden Vertices von rückwärts gerichteten Polygonen mit den backmaterialparametern beleuchtet und deren normale umgekehrt, bevor die Beleuchtungs Gleichung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="e40bf-123">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="e40bf-124">Vertices von nach vorne gerichteten Polygonen werden immer mit den Front-Material-Parametern beleuchtet, ohne dass ihre normale geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e40bf-124">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="e40bf-125">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="e40bf-125">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e40bf-126">*param*</span><span class="sxs-lookup"><span data-stu-id="e40bf-126">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="e40bf-127">Der Wert, auf den *param* festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e40bf-127">The value to which *param* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e40bf-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e40bf-128">Return value</span></span>

<span data-ttu-id="e40bf-129">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e40bf-129">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e40bf-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e40bf-130">Error codes</span></span>

<span data-ttu-id="e40bf-131">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e40bf-131">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e40bf-132">Name</span><span class="sxs-lookup"><span data-stu-id="e40bf-132">Name</span></span>                                                                                                  | <span data-ttu-id="e40bf-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e40bf-133">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e40bf-134"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-134"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e40bf-135">*PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="e40bf-135">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="e40bf-136"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e40bf-137">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e40bf-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e40bf-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e40bf-138">Remarks</span></span>

<span data-ttu-id="e40bf-139">Die **gllightmodelf** -Funktion legt den Beleuchtungsmodell Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="e40bf-139">The **glLightModelf** function sets lighting model parameter.</span></span> <span data-ttu-id="e40bf-140">Der Parameter " *PName* " benennt einen *Parameter und gibt* den neuen Wert an. der Wert oder die Werte einzelner Licht Quellparameter.</span><span class="sxs-lookup"><span data-stu-id="e40bf-140">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="e40bf-141">Im RGBA-Modus ist die Farbe eines Scheitel Punkts die Summe der Material-Emissionsintensität, das Produkt der Material Ambient-Reflektion und das Beleuchtungsmodell der Umgebungs Intensität in voller Szene und der Anteil der einzelnen aktivierten Lichtquellen.</span><span class="sxs-lookup"><span data-stu-id="e40bf-141">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="e40bf-142">Jede helle Quelle trägt die Summe von drei Begriffen bei: Ambient, diffuses und specarität.</span><span class="sxs-lookup"><span data-stu-id="e40bf-142">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="e40bf-143">Der Ambient-Lichtquellen Beitrag ist das Produkt der Material Ambient Reflektion und der Umgebungs Intensität des Lichts.</span><span class="sxs-lookup"><span data-stu-id="e40bf-143">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="e40bf-144">Der Anteil der diffusen Lichtquelle ist das Produkt der Material diffctance, der diffusen Intensität des Lichts und des Punkt Produkts der normalen Vertex mit dem normalisierten Vektor aus dem Scheitelpunkt und der Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="e40bf-144">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="e40bf-145">Der Glanz der Glanzlicht Quelle ist das Produkt der hellen Glanz Reflektion, die Glanz Intensität des Lichts und das Punktprodukt der normalisierten Scheitelpunkt-zu-Auge-und Vertex-zu-Licht-Vektoren, die an die Leistungsfähigkeit des Materials hervorgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="e40bf-145">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="e40bf-146">Alle drei Lichtquellen Beiträge werden gleichmäßig auf Grundlage der Entfernung zwischen dem Scheitelpunkt und der Lichtquelle und der Lichtquelle, dem Spread-Exponent und dem Spread-Umstellungs-Winkel verringert.</span><span class="sxs-lookup"><span data-stu-id="e40bf-146">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="e40bf-147">Alle Punkt Produkte werden durch 0 (null) ersetzt, wenn Sie einen negativen Wert ergeben.</span><span class="sxs-lookup"><span data-stu-id="e40bf-147">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="e40bf-148">Die Alpha Komponente der resultierenden beleuchteten Farbe wird auf den Alpha-Wert der Material diffctance festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e40bf-148">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="e40bf-149">Im Farb Index Modus wird der Wert des beleuchteten Indexes eines Scheitel Punkts von der Ambient-zu den Glanzwerten, die mithilfe von GL-Farbindizes an [**glmaterial**](glmaterial-functions.md) übergeben werden \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e40bf-149">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="e40bf-150">Diffuse und glanzvolle Koeffizienten, berechnet mit einer (. 30,. 59, .11) Gewichtung der hellen Farben, dem Glanz des Materials und denselben Reflektions-und Dämpfungs Gleichungen wie im RGBA-Fall, legen fest, wie viel oben in der Umgebung der resultierende Index ist.</span><span class="sxs-lookup"><span data-stu-id="e40bf-150">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="e40bf-151">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **gllightmodelf** -Funktion ab:</span><span class="sxs-lookup"><span data-stu-id="e40bf-151">The following functions retrieve information related to the **glLightModelf** function:</span></span>

<span data-ttu-id="e40bf-152">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Light \_ Model \_ local \_ Viewer</span><span class="sxs-lookup"><span data-stu-id="e40bf-152">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="e40bf-153">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Light \_ Model \_ Two \_ Side</span><span class="sxs-lookup"><span data-stu-id="e40bf-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="e40bf-154">[**glisenabled**](glisenabled.md) mit dem Argument GL- \_ Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="e40bf-154">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="e40bf-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e40bf-155">Requirements</span></span>



| <span data-ttu-id="e40bf-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e40bf-156">Requirement</span></span> | <span data-ttu-id="e40bf-157">Wert</span><span class="sxs-lookup"><span data-stu-id="e40bf-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e40bf-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e40bf-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e40bf-159">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e40bf-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e40bf-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e40bf-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e40bf-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e40bf-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e40bf-162">Header</span><span class="sxs-lookup"><span data-stu-id="e40bf-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e40bf-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e40bf-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e40bf-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="e40bf-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e40bf-166">DLL</span><span class="sxs-lookup"><span data-stu-id="e40bf-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e40bf-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e40bf-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e40bf-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40bf-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e40bf-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e40bf-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e40bf-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e40bf-171">**gllight**</span><span class="sxs-lookup"><span data-stu-id="e40bf-171">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="e40bf-172">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="e40bf-172">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





