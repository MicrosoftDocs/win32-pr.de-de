---
title: glgettexlevelparameterfv-Funktion (GL. h)
description: Die Funktionen "glgettexlevelparameterfv" und "glgettexlevelparameteriv" geben Textur Parameterwerte für eine bestimmte Detailebene zurück. | glgettexlevelparameterfv-Funktion (GL. h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- glgettexlevelparameterfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92f8b55b41d3538f116241a0401cedf643a5e55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365037"
---
# <a name="glgettexlevelparameterfv-function"></a><span data-ttu-id="1e9a4-105">glgettexlevelparameterfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="1e9a4-105">glGetTexLevelParameterfv function</span></span>

<span data-ttu-id="1e9a4-106">Die Funktionen " **glgettexlevelparameterfv** " und " [**glgettexlevelparameteriv**](glgettexlevelparameteriv.md) " geben Textur Parameterwerte für eine bestimmte Detailebene zurück.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-106">The **glGetTexLevelParameterfv** and [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e9a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e9a4-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="1e9a4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e9a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e9a4-109">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="1e9a4-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9a4-110">Der symbolische Name der Ziel Textur: GL \_ Texture \_ 1D, GL \_ Texture \_ 2D, GL \_ Proxy \_ Textur \_ 1D oder GL \_ \_ -Proxy Textur \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="1e9a4-111">*level*</span><span class="sxs-lookup"><span data-stu-id="1e9a4-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9a4-112">Die Detailstufe des gewünschten Bilds.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="1e9a4-113">Ebene 0 ist die Basis Image Ebene.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-113">Level 0 is the base image level.</span></span> <span data-ttu-id="1e9a4-114">Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="1e9a4-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="1e9a4-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9a4-116">Der symbolische Name eines Textur Parameters.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="1e9a4-117">Die folgenden Parameternamen werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="1e9a4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1e9a4-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="1e9a4-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e9a4-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="1e9a4-120"><dt>**GL- \_ Textur \_ Breite**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="1e9a4-121">Der Parameter *para* meters gibt einen einzelnen Wert zurück, der die Breite des Textur Bilds enthält.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="1e9a4-122">Dieser Wert enthält den Rahmen des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="1e9a4-123"><dt>**GL- \_ Textur \_ Höhe**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="1e9a4-124">Der Parameter *para* meters gibt einen einzelnen Wert zurück, der die Höhe des Textur Bilds enthält.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="1e9a4-125">Dieser Wert enthält den Rahmen des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="1e9a4-126"><dt>**Format der GL- \_ Textur \_ intern \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="1e9a4-127">Der Parameter *para* meters gibt einen einzelnen Wert zurück, der das Texturformat der Textur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="1e9a4-128"><dt>**GL- \_ Textur Rahmen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="1e9a4-129">Der Parameter *para* meters gibt einen einzelnen Wert zurück: die Breite des Rahmens des Textur Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="1e9a4-130"><dt>**\_Größe der \_ \_ Größen Größe von GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="1e9a4-131">Die interne speicherauflösung der roten Komponente eines Texels.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="1e9a4-132">Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="1e9a4-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="1e9a4-133"><dt>**GL- \_ Textur- \_ grün \_ Größe**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="1e9a4-134">Die interne speicherauflösung der grünen Komponente eines Texels.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="1e9a4-135">Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="1e9a4-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="1e9a4-136"><dt>**GL- \_ Textur \_ blau- \_ Größe**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="1e9a4-137">Die interne speicherauflösung der blauen Komponente eines Texels.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="1e9a4-138">Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="1e9a4-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="1e9a4-139"><dt>**GL- \_ Textur \_ alpha \_ Größe**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="1e9a4-140">Die interne speicherauflösung der Alpha Komponente eines Texels.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="1e9a4-141">Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="1e9a4-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="1e9a4-142"><dt>**GL- \_ Textur- \_ Beleuchtungs \_ Größe**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="1e9a4-143">Die interne speicherauflösung der Leuchtkraft Komponente eines Texels.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="1e9a4-144">Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="1e9a4-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="1e9a4-145"><dt>**Größe der GL- \_ Textur \_ Intensität \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="1e9a4-146">Die interne speicherauflösung der Intensität-Komponente eines Texels.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="1e9a4-147">Die Auflösung, die durch den OpenGL ausgewählt wird, ist eine genaue Entsprechung für die vom Benutzer angeforderte Auflösung mit dem Component-Argument [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="1e9a4-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="1e9a4-148"><dt>**GL- \_ Textur \_ Komponenten**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="1e9a4-149">Der Parameter *para* meters gibt einen einzelnen Wert zurück: die Anzahl der Komponenten im Textur Bild.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="1e9a4-150">*params*</span><span class="sxs-lookup"><span data-stu-id="1e9a4-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9a4-151">Gibt die angeforderten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e9a4-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e9a4-152">Return value</span></span>

<span data-ttu-id="1e9a4-153">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1e9a4-154">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1e9a4-154">Error codes</span></span>

<span data-ttu-id="1e9a4-155">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1e9a4-156">Name</span><span class="sxs-lookup"><span data-stu-id="1e9a4-156">Name</span></span>                                                                                                  | <span data-ttu-id="1e9a4-157">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e9a4-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e9a4-158"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1e9a4-159">*target* oder *PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="1e9a4-160"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1e9a4-161">die *Ebene* ist kleiner als 0 (null) oder größer als *Log* 2 *(max)*, wobei *Max* der zurückgegebene Wert von GL \_ Max \_ texture size ist \_ .</span><span class="sxs-lookup"><span data-stu-id="1e9a4-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="1e9a4-162"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1e9a4-163">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1e9a4-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e9a4-164">Remarks</span></span>

<span data-ttu-id="1e9a4-165">Die Funktion " **glgettexlevelparameter** " *gibt in* parameterparameterwerten für eine bestimmte Detailstufe, die als *Ebene* angegeben ist, zurück.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="1e9a4-166">Der *Ziel* Parameter definiert die Ziel Textur, entweder GL \_ Texture \_ 1D, GL \_ Texture \_ 2D, GL \_ Proxy \_ Textur \_ 1D oder GL \_ -Proxy \_ Textur \_ 2D, um eindimensionale oder zweidimensionale Texturierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="1e9a4-167">Der *PName* -Parameter gibt den Texture-Parameter an, dessen Wert oder Werte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="1e9a4-168">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *para* Metern vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1e9a4-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9a4-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e9a4-169">Requirements</span></span>



| <span data-ttu-id="1e9a4-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e9a4-170">Requirement</span></span> | <span data-ttu-id="1e9a4-171">Wert</span><span class="sxs-lookup"><span data-stu-id="1e9a4-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9a4-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e9a4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="1e9a4-173">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e9a4-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1e9a4-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e9a4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="1e9a4-175">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e9a4-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e9a4-176">Header</span><span class="sxs-lookup"><span data-stu-id="1e9a4-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e9a4-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1e9a4-178">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e9a4-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e9a4-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1e9a4-180">DLL</span><span class="sxs-lookup"><span data-stu-id="1e9a4-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e9a4-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e9a4-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e9a4-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e9a4-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9a4-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1e9a4-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1e9a4-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1e9a4-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1e9a4-185">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="1e9a4-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="1e9a4-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1e9a4-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1e9a4-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1e9a4-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1e9a4-188">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="1e9a4-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





