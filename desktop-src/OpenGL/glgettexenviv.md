---
title: glgettexenviv-Funktion (GL. h)
description: Die Funktionen "glgettexgetvfv" und "glgettexenviv" geben Textur Umgebungsparameter zurück. | glgettexenviv-Funktion (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- glgettexenviv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354311"
---
# <a name="glgettexenviv-function"></a><span data-ttu-id="3f95b-105">glgettexenviv-Funktion</span><span class="sxs-lookup"><span data-stu-id="3f95b-105">glGetTexEnviv function</span></span>

<span data-ttu-id="3f95b-106">Die Funktionen " [**glgettexgetvfv**](glgettexenvfv.md) " und " **glgettexenviv** " geben Textur Umgebungsparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="3f95b-106">The [**glGetTexEnvfv**](glgettexenvfv.md) and **glGetTexEnviv** functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f95b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f95b-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="3f95b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f95b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f95b-109">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="3f95b-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="3f95b-110">Eine Textur Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3f95b-110">A texture environment.</span></span> <span data-ttu-id="3f95b-111">Muss "GL \_ Texture" sein \_ .</span><span class="sxs-lookup"><span data-stu-id="3f95b-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="3f95b-112">*pName*</span><span class="sxs-lookup"><span data-stu-id="3f95b-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="3f95b-113">Der symbolische Name eines Textur Umgebungs Parameters.</span><span class="sxs-lookup"><span data-stu-id="3f95b-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="3f95b-114">Die folgenden Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3f95b-114">The following values are accepted.</span></span>



| <span data-ttu-id="3f95b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3f95b-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="3f95b-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3f95b-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="3f95b-117"><dt>**GL- \_ Textur \_ env- \_ Modus**</dt></span><span class="sxs-lookup"><span data-stu-id="3f95b-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="3f95b-118">Der Parameter *para* meters gibt den einwertigen Textur Umgebungs Modus zurück, eine symbolische Konstante.</span><span class="sxs-lookup"><span data-stu-id="3f95b-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="3f95b-119"><dt>**GL- \_ Textur Gesamt \_ \_ Farbe**</dt></span><span class="sxs-lookup"><span data-stu-id="3f95b-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="3f95b-120">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Farbe der Textur Umgebung sind.</span><span class="sxs-lookup"><span data-stu-id="3f95b-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="3f95b-121">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 der positivsten darstellbaren Ganzzahl zugeordnet ist und-1,0 der negativsten darstellbaren Ganzzahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="3f95b-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3f95b-122">*params*</span><span class="sxs-lookup"><span data-stu-id="3f95b-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="3f95b-123">Gibt die angeforderten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="3f95b-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f95b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f95b-124">Return value</span></span>

<span data-ttu-id="3f95b-125">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3f95b-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3f95b-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3f95b-126">Error codes</span></span>

<span data-ttu-id="3f95b-127">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3f95b-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3f95b-128">Name</span><span class="sxs-lookup"><span data-stu-id="3f95b-128">Name</span></span>                                                                                                  | <span data-ttu-id="3f95b-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3f95b-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f95b-130"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f95b-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3f95b-131">*target* oder *PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="3f95b-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="3f95b-132"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="3f95b-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3f95b-133">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3f95b-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3f95b-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f95b-134">Remarks</span></span>

<span data-ttu-id="3f95b-135">Die **glgettexenv** -Funktion gibt *in Parameter* ausgewählte Werte einer Textur Umgebung zurück, die mit [**gltexenv**](gltexenv-functions.md)angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3f95b-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="3f95b-136">Der *Ziel* Parameter gibt eine Textur Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="3f95b-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="3f95b-137">Zurzeit wird nur eine Textur Umgebung definiert und unterstützt: GL Texture-Version \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3f95b-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="3f95b-138">Der *PName* -Parameter benennt einen bestimmten Textur Umgebungsparameter.</span><span class="sxs-lookup"><span data-stu-id="3f95b-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="3f95b-139">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *para* Metern vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="3f95b-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f95b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f95b-140">Requirements</span></span>



| <span data-ttu-id="3f95b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f95b-141">Requirement</span></span> | <span data-ttu-id="3f95b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="3f95b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f95b-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f95b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3f95b-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f95b-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3f95b-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f95b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3f95b-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f95b-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f95b-147">Header</span><span class="sxs-lookup"><span data-stu-id="3f95b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f95b-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f95b-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3f95b-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f95b-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f95b-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f95b-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f95b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3f95b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f95b-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f95b-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f95b-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f95b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f95b-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3f95b-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3f95b-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3f95b-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3f95b-156">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="3f95b-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





