---
title: glpixelmapfv-Funktion (GL. h)
description: Die Funktion "glpixelmapfv" richtet Pixel Übertragungs Zuordnungen ein.
ms.assetid: 13403243-1ec4-4b1d-a9da-9a6693b6f9b8
keywords:
- glpixelmapfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97124eeca8051ec23d9a4fea03a98468d320af8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346134"
---
# <a name="glpixelmapfv-function"></a><span data-ttu-id="1af24-104">glpixelmapfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="1af24-104">glPixelMapfv function</span></span>

<span data-ttu-id="1af24-105">Die Funktion " **glpixelmapfv** " richtet Pixel Übertragungs Zuordnungen ein.</span><span class="sxs-lookup"><span data-stu-id="1af24-105">The **glPixelMapfv** function sets up pixel transfer maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af24-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1af24-106">Syntax</span></span>


```C++
void WINAPI glPixelMapfv(
         GLenum  map,
         GLsizei mapsize,
   const GLfloat *values
);
```



## <a name="parameters"></a><span data-ttu-id="1af24-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1af24-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af24-108">*map*</span><span class="sxs-lookup"><span data-stu-id="1af24-108">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="1af24-109">Ein symbolischer Zuordnungs Name.</span><span class="sxs-lookup"><span data-stu-id="1af24-109">A symbolic map name.</span></span> <span data-ttu-id="1af24-110">Die zehn Zuordnungen lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="1af24-110">The ten maps are as follows.</span></span>



| <span data-ttu-id="1af24-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1af24-111">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="1af24-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1af24-112">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <span data-ttu-id="1af24-113"><dt>**GL \_ Pixel \_ map \_ i \_ to \_ i**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-113"><dt>**GL\_PIXEL\_MAP\_I\_TO\_I**</dt></span></span> </dl> | <span data-ttu-id="1af24-114">Ordnet Farbindizes Farbindizes zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-114">Maps color indexes to color indexes.</span></span><br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <span data-ttu-id="1af24-115"><dt>**GL- \_ Pixel \_ map \_ s \_ zu \_ s**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-115"><dt>**GL\_PIXEL\_MAP\_S\_TO\_S**</dt></span></span> </dl> | <span data-ttu-id="1af24-116">Ordnet Schablonen Indizes zu Schablonen Indizes zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-116">Maps stencil indexes to stencil indexes.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <span data-ttu-id="1af24-117"><dt>**GL \_ Pixel \_ map \_ I \_ to \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-117"><dt>**GL\_PIXEL\_MAP\_I\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="1af24-118">Ordnet Farbindizes zu roten Komponenten zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-118">Maps color indexes to red components.</span></span><br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <span data-ttu-id="1af24-119"><dt>**GL \_ Pixel \_ map \_ I \_ to \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-119"><dt>**GL\_PIXEL\_MAP\_I\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="1af24-120">Ordnet Farbindizes zu grünen Komponenten zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-120">Maps color indexes to green components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <span data-ttu-id="1af24-121"><dt>**GL \_ Pixel \_ map \_ I \_ to \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-121"><dt>**GL\_PIXEL\_MAP\_I\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="1af24-122">Ordnet Farbindizes zu blauen Komponenten zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-122">Maps color indexes to blue components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <span data-ttu-id="1af24-123"><dt>**GL \_ Pixel \_ map \_ I \_ to \_ A**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-123"><dt>**GL\_PIXEL\_MAP\_I\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="1af24-124">Ordnet den Alpha Komponenten Farbindizes zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-124">Maps color indexes to alpha components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <span data-ttu-id="1af24-125"><dt>**GL \_ Pixel \_ map \_ r \_ to \_ r**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-125"><dt>**GL\_PIXEL\_MAP\_R\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="1af24-126">Ordnet rote Komponenten roten Komponenten zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-126">Maps red components to red components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <span data-ttu-id="1af24-127"><dt>**GL \_ Pixel \_ map \_ g \_ bis \_ g**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-127"><dt>**GL\_PIXEL\_MAP\_G\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="1af24-128">Ordnet die grünen Komponenten grünen Komponenten zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-128">Maps green components to green components.</span></span><br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <span data-ttu-id="1af24-129"><dt>**GL \_ Pixel \_ map \_ b \_ zu \_ b**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-129"><dt>**GL\_PIXEL\_MAP\_B\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="1af24-130">Ordnet blaue Komponenten blauen Komponenten zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-130">Maps blue components to blue components.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <span data-ttu-id="1af24-131"><dt>**GL- \_ Pixel zuordnen \_ \_ eines \_ zu \_ einem**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-131"><dt>**GL\_PIXEL\_MAP\_A\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="1af24-132">Ordnet Alpha Komponenten Alpha Komponenten zu.</span><span class="sxs-lookup"><span data-stu-id="1af24-132">Maps alpha components to alpha components.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1af24-133">*mapsize*</span><span class="sxs-lookup"><span data-stu-id="1af24-133">*mapsize*</span></span> 
</dt> <dd>

<span data-ttu-id="1af24-134">Die Größe der Karte, die definiert wird.</span><span class="sxs-lookup"><span data-stu-id="1af24-134">The size of the map being defined.</span></span>

</dd> <dt>

<span data-ttu-id="1af24-135">*Werte*</span><span class="sxs-lookup"><span data-stu-id="1af24-135">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="1af24-136">Ein Array von *mapsize* -Werten.</span><span class="sxs-lookup"><span data-stu-id="1af24-136">An array of *mapsize* values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af24-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1af24-137">Return value</span></span>

<span data-ttu-id="1af24-138">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1af24-138">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1af24-139">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1af24-139">Error codes</span></span>

<span data-ttu-id="1af24-140">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1af24-140">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1af24-141">Name</span><span class="sxs-lookup"><span data-stu-id="1af24-141">Name</span></span>                                                                                                  | <span data-ttu-id="1af24-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1af24-142">Meaning</span></span>                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1af24-143"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-143"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1af24-144">*map* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="1af24-144">*map* was not an accepted value.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="1af24-145"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-145"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1af24-146">*mapsize* war negativ oder größer als die GL- \_ Pixel \_ map- \_ Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1af24-146">*mapsize* was negative or larger than GL\_PIXEL\_MAP\_TABLE.</span></span> <br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="1af24-147"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1af24-148">*map* war GL \_ Pixel \_ map \_ i \_ to \_ i, GL \_ Pixel \_ map \_ s \_ to \_ s, GL \_ Pixel \_ map \_ i \_ to \_ R, GL \_ Pixel \_ map \_ i \_ to \_ G, GL \_ Pixel \_ map \_ i \_ to \_ B oder GL-Pixel Map i to \_ \_ a, \_ \_ \_ und *mapsize* war keine Potenz von zwei.</span><span class="sxs-lookup"><span data-stu-id="1af24-148">*map* was GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, or GL\_PIXEL\_MAP\_I\_TO\_A, and *mapsize* was not a power of two.</span></span> <br/> |
| <dl> <span data-ttu-id="1af24-149"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1af24-150">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1af24-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="1af24-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1af24-151">Remarks</span></span>

<span data-ttu-id="1af24-152">Die **glpixelmap** -Funktion richtet Übersetzungstabellen oder *Maps* ein, die von [**glcopypixel**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**gldrawpixels**](gldrawpixels.md), [**gllepixel**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)und [**glTexSubImage2D**](gltexsubimage2d.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1af24-152">The **glPixelMap** function sets up translation tables, or *maps*, used by [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md).</span></span> <span data-ttu-id="1af24-153">Die Verwendung dieser Zuordnungen wird vollständig im Thema [**glpixeltransfer**](glpixeltransfer.md) beschrieben und teilweise in den Themen für die Befehle Pixel und Textur Bild beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1af24-153">Use of these maps is described completely in the [**glPixelTransfer**](glpixeltransfer.md) topic, and partly in the topics for the pixel and texture image commands.</span></span> <span data-ttu-id="1af24-154">In diesem Thema wird nur die Spezifikation der Maps beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1af24-154">Only the specification of the maps is described in this topic.</span></span>

<span data-ttu-id="1af24-155">Der *map* -Parameter ist ein symbolischer Kartenname, der eine von zehn Zuordnungen angibt, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1af24-155">The *map* parameter is a symbolic map name, indicating one of ten maps to set.</span></span> <span data-ttu-id="1af24-156">Der *mapsize* -Parameter gibt die Anzahl der Einträge in der Zuordnung an, und *Werte* sind ein Zeiger auf ein Array von *mapsize* -Kartenwerten.</span><span class="sxs-lookup"><span data-stu-id="1af24-156">The *mapsize* parameter specifies the number of entries in the map, and *values* is a pointer to an array of *mapsize* map values.</span></span>

<span data-ttu-id="1af24-157">Die Einträge in einer Zuordnung können als Gleit Komma Zahlen mit einfacher Genauigkeit, kurze Ganzzahlen ohne Vorzeichen oder lange ganze Zahlen ohne Vorzeichen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1af24-157">The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers.</span></span> <span data-ttu-id="1af24-158">Zuordnungen, die Farb Komponentenwerte speichern (alle außer GL \_ Pixel \_ map \_ i \_ \_ und GL \_ Pixel \_ map \_ s \_ to \_ s) behalten ihre Werte im Gleit Komma Format bei, wobei nicht angegebene Mantisse und Exponent-Größen nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1af24-158">Maps that store color component values (all but GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="1af24-159">Gleit Komma Werte, die von [**glpixelmapfv**](glpixelmap.md) angegeben werden, werden direkt in das interne Gleit Komma Format dieser Zuordnungen konvertiert und dann an den Bereich \[ 0, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="1af24-159">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal floating-point format of these maps, and then clamped to the range \[0,1\].</span></span> <span data-ttu-id="1af24-160">Ganzzahlige Werte ohne Vorzeichen, die von **glpixelmapusv** und **glpixelmapuiv** angegeben werden, werden linear konvertiert, sodass die größte darstellbare Ganzzahl 1,0 und 0 (null) 0,0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="1af24-160">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.</span></span>

<span data-ttu-id="1af24-161">Zuordnungen zum Speichern von Indizes, GL \_ Pixel \_ map \_ i \_ \_ und GL \_ Pixel \_ map \_ s \_ zu \_ s, beibehalten ihrer Werte im fest Komma Format, wobei eine nicht angegebene Anzahl von Bits auf der rechten Seite des binären Punkts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1af24-161">Maps that store indexes, GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="1af24-162">Gleit Komma Werte, die von [**glpixelmapfv**](glpixelmap.md) angegeben werden, werden direkt in das interne fest Komma Format dieser Zuordnungen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="1af24-162">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal fixed-point format of these maps.</span></span> <span data-ttu-id="1af24-163">Ganzzahlige Werte ohne Vorzeichen, die von **glpixelmapusv** und **glpixelmapuiv** angegeben werden, geben ganzzahlige Werte mit allen Nullen auf der rechten Seite des binären Punkts an.</span><span class="sxs-lookup"><span data-stu-id="1af24-163">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** specify integer values, with all zeros to the right of the binary point.</span></span>

<span data-ttu-id="1af24-164">In der folgenden Tabelle werden die anfänglichen Größen und Werte für jede der Zuordnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1af24-164">The following table shows the initial sizes and values for each of the maps.</span></span> <span data-ttu-id="1af24-165">Zuordnungen, die von Farb-oder Schablonen Indizes indiziert werden, müssen *mapsize* = 2 ^ *n* für einige *n* oder Ergebnisse sind nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1af24-165">Maps that are indexed by either color or stencil indexes must have *mapsize* = 2 ^ *n* for some *n* or results are undefined.</span></span> <span data-ttu-id="1af24-166">Die maximal zulässige Größe für jede Zuordnung hängt von der Implementierung ab und kann durch Aufrufen von **glget** mit dem Argument GL \_ Max \_ Pixel \_ map \_ Table festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1af24-166">The maximum allowable size for each map depends on the implementation and can be determined by calling **glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE.</span></span> <span data-ttu-id="1af24-167">Das einzige Maximum gilt für alle Zuordnungen und ist mindestens 32.</span><span class="sxs-lookup"><span data-stu-id="1af24-167">The single maximum applies to all maps, and it is at least 32.</span></span>



| <span data-ttu-id="1af24-168">Zuordnung</span><span class="sxs-lookup"><span data-stu-id="1af24-168">Map</span></span>                      | <span data-ttu-id="1af24-169">Suchindex</span><span class="sxs-lookup"><span data-stu-id="1af24-169">Lookup Index</span></span>  | <span data-ttu-id="1af24-170">Such Wert</span><span class="sxs-lookup"><span data-stu-id="1af24-170">Lookup Value</span></span>  | <span data-ttu-id="1af24-171">Anfangsgröße</span><span class="sxs-lookup"><span data-stu-id="1af24-171">Initial Size</span></span> | <span data-ttu-id="1af24-172">Anfangswert</span><span class="sxs-lookup"><span data-stu-id="1af24-172">Initial Value</span></span> |
|--------------------------|---------------|---------------|--------------|---------------|
| <span data-ttu-id="1af24-173">GL \_ Pixel \_ map \_ i \_ to \_ i</span><span class="sxs-lookup"><span data-stu-id="1af24-173">GL\_PIXEL\_MAP\_I\_TO\_I</span></span> | <span data-ttu-id="1af24-174">Farbindex</span><span class="sxs-lookup"><span data-stu-id="1af24-174">color index</span></span>   | <span data-ttu-id="1af24-175">Farbindex</span><span class="sxs-lookup"><span data-stu-id="1af24-175">color index</span></span>   | <span data-ttu-id="1af24-176">1</span><span class="sxs-lookup"><span data-stu-id="1af24-176">1</span></span>            | <span data-ttu-id="1af24-177">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-177">0.0</span></span>           |
| <span data-ttu-id="1af24-178">GL- \_ Pixel \_ map \_ s \_ zu \_ s</span><span class="sxs-lookup"><span data-stu-id="1af24-178">GL\_PIXEL\_MAP\_S\_TO\_S</span></span> | <span data-ttu-id="1af24-179">Schablone-Index</span><span class="sxs-lookup"><span data-stu-id="1af24-179">stencil index</span></span> | <span data-ttu-id="1af24-180">Schablone-Index</span><span class="sxs-lookup"><span data-stu-id="1af24-180">stencil index</span></span> | <span data-ttu-id="1af24-181">1</span><span class="sxs-lookup"><span data-stu-id="1af24-181">1</span></span>            | <span data-ttu-id="1af24-182">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-182">0.0</span></span>           |
| <span data-ttu-id="1af24-183">GL \_ Pixel \_ map \_ I \_ to \_ R</span><span class="sxs-lookup"><span data-stu-id="1af24-183">GL\_PIXEL\_MAP\_I\_TO\_R</span></span> | <span data-ttu-id="1af24-184">Farbindex</span><span class="sxs-lookup"><span data-stu-id="1af24-184">color index</span></span>   | <span data-ttu-id="1af24-185">R</span><span class="sxs-lookup"><span data-stu-id="1af24-185">R</span></span>             | <span data-ttu-id="1af24-186">1</span><span class="sxs-lookup"><span data-stu-id="1af24-186">1</span></span>            | <span data-ttu-id="1af24-187">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-187">0.0</span></span>           |
| <span data-ttu-id="1af24-188">GL \_ Pixel \_ map \_ I \_ to \_ G</span><span class="sxs-lookup"><span data-stu-id="1af24-188">GL\_PIXEL\_MAP\_I\_TO\_G</span></span> | <span data-ttu-id="1af24-189">Farbindex</span><span class="sxs-lookup"><span data-stu-id="1af24-189">color index</span></span>   | <span data-ttu-id="1af24-190">G</span><span class="sxs-lookup"><span data-stu-id="1af24-190">G</span></span>             | <span data-ttu-id="1af24-191">1</span><span class="sxs-lookup"><span data-stu-id="1af24-191">1</span></span>            | <span data-ttu-id="1af24-192">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-192">0.0</span></span>           |
| <span data-ttu-id="1af24-193">GL \_ Pixel \_ map \_ I \_ to \_ B</span><span class="sxs-lookup"><span data-stu-id="1af24-193">GL\_PIXEL\_MAP\_I\_TO\_B</span></span> | <span data-ttu-id="1af24-194">Farbindex</span><span class="sxs-lookup"><span data-stu-id="1af24-194">color index</span></span>   | <span data-ttu-id="1af24-195">B</span><span class="sxs-lookup"><span data-stu-id="1af24-195">B</span></span>             | <span data-ttu-id="1af24-196">1</span><span class="sxs-lookup"><span data-stu-id="1af24-196">1</span></span>            | <span data-ttu-id="1af24-197">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-197">0.0</span></span>           |
| <span data-ttu-id="1af24-198">GL \_ Pixel \_ map \_ I \_ to \_ A</span><span class="sxs-lookup"><span data-stu-id="1af24-198">GL\_PIXEL\_MAP\_I\_TO\_A</span></span> | <span data-ttu-id="1af24-199">Farbindex</span><span class="sxs-lookup"><span data-stu-id="1af24-199">color index</span></span>   | <span data-ttu-id="1af24-200">A</span><span class="sxs-lookup"><span data-stu-id="1af24-200">A</span></span>             | <span data-ttu-id="1af24-201">1</span><span class="sxs-lookup"><span data-stu-id="1af24-201">1</span></span>            | <span data-ttu-id="1af24-202">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-202">0.0</span></span>           |
| <span data-ttu-id="1af24-203">GL \_ Pixel \_ map \_ r \_ to \_ r</span><span class="sxs-lookup"><span data-stu-id="1af24-203">GL\_PIXEL\_MAP\_R\_TO\_R</span></span> | <span data-ttu-id="1af24-204">R</span><span class="sxs-lookup"><span data-stu-id="1af24-204">R</span></span>             | <span data-ttu-id="1af24-205">R</span><span class="sxs-lookup"><span data-stu-id="1af24-205">R</span></span>             | <span data-ttu-id="1af24-206">1</span><span class="sxs-lookup"><span data-stu-id="1af24-206">1</span></span>            | <span data-ttu-id="1af24-207">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-207">0.0</span></span>           |
| <span data-ttu-id="1af24-208">GL \_ Pixel \_ map \_ g \_ bis \_ g</span><span class="sxs-lookup"><span data-stu-id="1af24-208">GL\_PIXEL\_MAP\_G\_TO\_G</span></span> | <span data-ttu-id="1af24-209">G</span><span class="sxs-lookup"><span data-stu-id="1af24-209">G</span></span>             | <span data-ttu-id="1af24-210">G</span><span class="sxs-lookup"><span data-stu-id="1af24-210">G</span></span>             | <span data-ttu-id="1af24-211">1</span><span class="sxs-lookup"><span data-stu-id="1af24-211">1</span></span>            | <span data-ttu-id="1af24-212">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-212">0.0</span></span>           |
| <span data-ttu-id="1af24-213">GL \_ Pixel \_ map \_ b \_ zu \_ b</span><span class="sxs-lookup"><span data-stu-id="1af24-213">GL\_PIXEL\_MAP\_B\_TO\_B</span></span> | <span data-ttu-id="1af24-214">B</span><span class="sxs-lookup"><span data-stu-id="1af24-214">B</span></span>             | <span data-ttu-id="1af24-215">B</span><span class="sxs-lookup"><span data-stu-id="1af24-215">B</span></span>             | <span data-ttu-id="1af24-216">1</span><span class="sxs-lookup"><span data-stu-id="1af24-216">1</span></span>            | <span data-ttu-id="1af24-217">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-217">0.0</span></span>           |
| <span data-ttu-id="1af24-218">GL- \_ Pixel zuordnen \_ \_ eines \_ zu \_ einem</span><span class="sxs-lookup"><span data-stu-id="1af24-218">GL\_PIXEL\_MAP\_A\_TO\_A</span></span> | <span data-ttu-id="1af24-219">Ein</span><span class="sxs-lookup"><span data-stu-id="1af24-219">A</span></span>             | <span data-ttu-id="1af24-220">A</span><span class="sxs-lookup"><span data-stu-id="1af24-220">A</span></span>             | <span data-ttu-id="1af24-221">1</span><span class="sxs-lookup"><span data-stu-id="1af24-221">1</span></span>            | <span data-ttu-id="1af24-222">0,0</span><span class="sxs-lookup"><span data-stu-id="1af24-222">0.0</span></span>           |



 

<span data-ttu-id="1af24-223">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glpixelmap** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="1af24-223">The following functions retrieve information related to **glPixelMap**:</span></span>

<span data-ttu-id="1af24-224">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Pixel \_ map \_ i \_ to \_ i \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="1af24-225">**glget** mit dem Argument GL \_ Pixel \_ map \_ s \_ to \_ s \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-225">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="1af24-226">**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ R \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-226">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="1af24-227">**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ G \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-227">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="1af24-228">**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ B \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-228">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="1af24-229">**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ A \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-229">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="1af24-230">**glget** mit dem Argument GL \_ Pixel \_ map \_ r \_ to \_ r \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-230">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="1af24-231">**glget** mit dem Argument GL \_ Pixel \_ map \_ g \_ bis \_ g \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-231">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="1af24-232">**glget** mit Argument GL \_ Pixel \_ map \_ b \_ bis \_ b \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-232">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="1af24-233">**glget** mit dem Argument GL \_ Pixel \_ map \_ a \_ to \_ a \_ size</span><span class="sxs-lookup"><span data-stu-id="1af24-233">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="1af24-234">**glget** mit dem Argument GL \_ Max \_ Pixel \_ map \_ Table</span><span class="sxs-lookup"><span data-stu-id="1af24-234">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="1af24-235">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1af24-235">Requirements</span></span>



| <span data-ttu-id="1af24-236">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1af24-236">Requirement</span></span> | <span data-ttu-id="1af24-237">Wert</span><span class="sxs-lookup"><span data-stu-id="1af24-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1af24-238">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1af24-238">Minimum supported client</span></span><br/> | <span data-ttu-id="1af24-239">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1af24-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1af24-240">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1af24-240">Minimum supported server</span></span><br/> | <span data-ttu-id="1af24-241">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1af24-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1af24-242">Header</span><span class="sxs-lookup"><span data-stu-id="1af24-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af24-243"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-243"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1af24-244">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1af24-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="1af24-245"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-245"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1af24-246">DLL</span><span class="sxs-lookup"><span data-stu-id="1af24-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1af24-247"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1af24-247"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af24-248">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1af24-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af24-249">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1af24-249">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1af24-250">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="1af24-250">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="1af24-251">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="1af24-251">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="1af24-252">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1af24-252">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1af24-253">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="1af24-253">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="1af24-254">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="1af24-254">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="1af24-255">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="1af24-255">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="1af24-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1af24-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1af24-257">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1af24-257">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





