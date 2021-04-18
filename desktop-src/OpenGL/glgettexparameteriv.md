---
title: glgettexparameteriv-Funktion (GL. h)
description: Die Funktionen "glgettexparameterfv" und "glgettexparameteriv" geben Textur Parameterwerte zurück. | glgettexparameteriv-Funktion (GL. h)
ms.assetid: b89d10f1-5e30-4d25-8953-fbd59781fdac
keywords:
- glgettexparameteriv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78983594487fd22917c15a5b211c529b6b14d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351899"
---
# <a name="glgettexparameteriv-function"></a><span data-ttu-id="fddb5-105">glgettexparameteriv-Funktion</span><span class="sxs-lookup"><span data-stu-id="fddb5-105">glGetTexParameteriv function</span></span>

<span data-ttu-id="fddb5-106">Die Funktionen " [**glgettexparameterfv**](glgettexparameterfv.md) " und " **glgettexparameteriv** " geben Textur Parameterwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="fddb5-106">The [**glGetTexParameterfv**](glgettexparameterfv.md) and **glGetTexParameteriv** functions return texture parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fddb5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fddb5-107">Syntax</span></span>


```C++
void WINAPI glGetTexParameteriv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="fddb5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fddb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fddb5-109">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="fddb5-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="fddb5-110">Der symbolische Name der Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="fddb5-110">The symbolic name of the target texture.</span></span> <span data-ttu-id="fddb5-111">GL \_ Texture \_ 1D und GL \_ Texture \_ 2D werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fddb5-111">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="fddb5-112">*pName*</span><span class="sxs-lookup"><span data-stu-id="fddb5-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="fddb5-113">Der symbolische Name eines Textur Parameters.</span><span class="sxs-lookup"><span data-stu-id="fddb5-113">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="fddb5-114">Die folgenden Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fddb5-114">The following values are accepted.</span></span>



| <span data-ttu-id="fddb5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fddb5-115">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="fddb5-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fddb5-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="fddb5-117"><dt>**GL- \_ Textur- \_ mag- \_ Filter**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-117"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="fddb5-118">Gibt den einwertigen Textur Vergrößerungs Filter zurück, eine symbolische Konstante.</span><span class="sxs-lookup"><span data-stu-id="fddb5-118">Returns the single-valued texture magnification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="fddb5-119"><dt>**GL- \_ Textur- \_ Min- \_ Filter**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-119"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="fddb5-120">Gibt den einwertigen Textur Minimierung-Filter zurück, eine symbolische Konstante.</span><span class="sxs-lookup"><span data-stu-id="fddb5-120">Returns the single-valued texture minification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="fddb5-121"><dt>**GL- \_ Textur Umbruch \_ \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-121"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="fddb5-122">Gibt die einwertige Wrapping Funktion für Texturkoordinaten *s* zurück, eine symbolische Konstante.</span><span class="sxs-lookup"><span data-stu-id="fddb5-122">Returns the single-valued wrapping function for texture coordinate *s*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="fddb5-123"><dt>**GL- \_ Textur Umbruch \_ \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-123"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="fddb5-124">Gibt die einwertige Wrapping Funktion für die Textur Koordinate *t* zurück, eine symbolische Konstante.</span><span class="sxs-lookup"><span data-stu-id="fddb5-124">Returns the single-valued wrapping function for texture coordinate *t*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="fddb5-125"><dt>**Rahmenfarbe des GL- \_ Textur Rahmens \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-125"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="fddb5-126">Gibt vier ganzzahlige oder Gleit Komma Zahlen zurück, die die RGBA-Farbe des Textur Rahmens bilden.</span><span class="sxs-lookup"><span data-stu-id="fddb5-126">Returns four integer or floating-point numbers that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="fddb5-127">Gleit Komma Werte werden im Bereich \[ 0, 1 zurückgegeben \] .</span><span class="sxs-lookup"><span data-stu-id="fddb5-127">Floating-point values are returned in the range \[0,1\].</span></span> <span data-ttu-id="fddb5-128">Ganzzahlige Werte werden als lineare Zuordnung der internen Gleit Komma Darstellung zurückgegeben, sodass 1,0 der positivsten darstellbaren Ganzzahl und-1,0 der negativsten darstellbaren Ganzzahl zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="fddb5-128">Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.</span></span><br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="fddb5-129"><dt>**GL- \_ Textur \_ Priorität**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-129"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="fddb5-130">Gibt die Residenz Priorität der Ziel Textur zurück (oder die an Sie gebundene benannte Textur).</span><span class="sxs-lookup"><span data-stu-id="fddb5-130">Returns the residence priority of the target texture (or the named texture bound to it).</span></span> <span data-ttu-id="fddb5-131">Der Anfangswert ist 1.</span><span class="sxs-lookup"><span data-stu-id="fddb5-131">The initial value is 1.</span></span> <span data-ttu-id="fddb5-132">Siehe [**glpriorizetexturen**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="fddb5-132">See [**glPrioritizeTextures**](glprioritizetextures.md).</span></span><br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <span data-ttu-id="fddb5-133"><dt>**GL- \_ Textur \_ residente**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-133"><dt>**GL\_TEXTURE\_RESIDENT**</dt></span></span> </dl>              | <span data-ttu-id="fddb5-134">Gibt den Wohnsitz Status der Ziel Textur zurück.</span><span class="sxs-lookup"><span data-stu-id="fddb5-134">Returns the residence status of the target texture.</span></span> <span data-ttu-id="fddb5-135">Wenn der Wert, der in Parametern zurückgegeben wird \_ , GL true ist, ist die Textur im Texturspeicher ansässig.</span><span class="sxs-lookup"><span data-stu-id="fddb5-135">If the value returned in params is GL\_TRUE, the texture is resident in texture memory.</span></span> <span data-ttu-id="fddb5-136">Siehe [**glaretexturesresidente**](glaretexturesresident.md).</span><span class="sxs-lookup"><span data-stu-id="fddb5-136">See [**glAreTexturesResident**](glaretexturesresident.md).</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="fddb5-137">*params*</span><span class="sxs-lookup"><span data-stu-id="fddb5-137">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fddb5-138">Gibt die Textur Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fddb5-138">Returns the texture parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fddb5-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fddb5-139">Return value</span></span>

<span data-ttu-id="fddb5-140">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fddb5-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fddb5-141">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="fddb5-141">Error codes</span></span>

<span data-ttu-id="fddb5-142">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fddb5-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fddb5-143">Name</span><span class="sxs-lookup"><span data-stu-id="fddb5-143">Name</span></span>                                                                                                  | <span data-ttu-id="fddb5-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fddb5-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fddb5-145"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fddb5-146">Das *Ziel* oder der *Name* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="fddb5-146">*target* or *name* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="fddb5-147"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fddb5-148">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fddb5-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fddb5-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fddb5-149">Remarks</span></span>

<span data-ttu-id="fddb5-150">Die Funktion " **glgettexparameter** " *gibt in Parameter* den Wert oder die Werte des als " *PName*" angegebenen Textur Parameters zurück.</span><span class="sxs-lookup"><span data-stu-id="fddb5-150">The **glGetTexParameter** function returns in *params* the value or values of the texture parameter specified as *pname*.</span></span> <span data-ttu-id="fddb5-151">Der *target* -Parameter definiert die Ziel Textur (GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D), um eindimensionale oder zweidimensionale Texturierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fddb5-151">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="fddb5-152">Der *PName* -Parameter akzeptiert dieselben Symbole wie [**gltexparameter**](gltexparameter-functions.md)mit denselben Interpretationen.</span><span class="sxs-lookup"><span data-stu-id="fddb5-152">The *pname* parameter accepts the same symbols as [**glTexParameter**](gltexparameter-functions.md), with the same interpretations.</span></span>

<span data-ttu-id="fddb5-153">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *para* Metern vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="fddb5-153">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="fddb5-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fddb5-154">Requirements</span></span>



| <span data-ttu-id="fddb5-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fddb5-155">Requirement</span></span> | <span data-ttu-id="fddb5-156">Wert</span><span class="sxs-lookup"><span data-stu-id="fddb5-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fddb5-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fddb5-157">Minimum supported client</span></span><br/> | <span data-ttu-id="fddb5-158">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fddb5-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fddb5-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fddb5-159">Minimum supported server</span></span><br/> | <span data-ttu-id="fddb5-160">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fddb5-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fddb5-161">Header</span><span class="sxs-lookup"><span data-stu-id="fddb5-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="fddb5-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fddb5-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fddb5-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="fddb5-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fddb5-165">DLL</span><span class="sxs-lookup"><span data-stu-id="fddb5-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fddb5-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fddb5-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fddb5-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fddb5-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fddb5-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fddb5-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fddb5-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fddb5-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fddb5-170">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="fddb5-170">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





