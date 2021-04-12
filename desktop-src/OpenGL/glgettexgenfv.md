---
title: glgettexgenfv-Funktion (GL. h)
description: Die Funktionen "glgettexgendv", "glgettexgenfv" und "glgettexgeniv" geben Texturkoordinaten Generierungs Parameter zurück. | glgettexgenfv-Funktion (GL. h)
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
keywords:
- glgettexgenfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexGenfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e527d0388b8aca7239ba1c51dccdce15de3cd8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352849"
---
# <a name="glgettexgenfv-function"></a><span data-ttu-id="23e0c-105">glgettexgenfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="23e0c-105">glGetTexGenfv function</span></span>

<span data-ttu-id="23e0c-106">Die Funktionen " [**glgettexgendv**](glgettexgendv.md)", " **glgettexgenfv**" und " [**glgettexgeniv**](glgettexgeniv.md) " geben Texturkoordinaten Generierungs Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="23e0c-106">The [**glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv**, and [**glGetTexGeniv**](glgettexgeniv.md) functions return texture coordinate generation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e0c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23e0c-107">Syntax</span></span>


```C++
void WINAPI glGetTexGenfv(
   GLenum  coord,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="23e0c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="23e0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e0c-109">*Koord*</span><span class="sxs-lookup"><span data-stu-id="23e0c-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="23e0c-110">Eine Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="23e0c-110">A texture coordinate.</span></span> <span data-ttu-id="23e0c-111">Muss "GL \_ S", "GL \_ T", "GL \_ R" oder "GL \_ Q" lauten.</span><span class="sxs-lookup"><span data-stu-id="23e0c-111">Must be GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="23e0c-112">*pName*</span><span class="sxs-lookup"><span data-stu-id="23e0c-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="23e0c-113">Der symbolische Name der Werte, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="23e0c-113">The symbolic name of the value(s) to be returned.</span></span> <span data-ttu-id="23e0c-114">Muss entweder der GL- \_ Textur \_ gen- \_ Modus oder der Name einer der Gleichungen der Textur Generierungs Ebene sein: GL- \_ Objekt \_ Ebene oder GL- \_ Augen \_ Ebene.</span><span class="sxs-lookup"><span data-stu-id="23e0c-114">Must be either GL\_TEXTURE\_GEN\_MODE or the name of one of the texture generation plane equations: GL\_OBJECT\_PLANE or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="23e0c-115">Diese Werte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="23e0c-115">These values are as follows.</span></span>



| <span data-ttu-id="23e0c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="23e0c-116">Value</span></span>                                                                                                                                                                             | <span data-ttu-id="23e0c-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23e0c-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <span data-ttu-id="23e0c-118"><dt>**GL- \_ Textur \_ gen- \_ Modus**</dt></span><span class="sxs-lookup"><span data-stu-id="23e0c-118"><dt>**GL\_TEXTURE\_GEN\_MODE**</dt></span></span> </dl> | <span data-ttu-id="23e0c-119">Der Parameter *para* meters gibt die einwertige Textur Generierungs Funktion zurück, eine symbolische Konstante.</span><span class="sxs-lookup"><span data-stu-id="23e0c-119">The *params* parameter returns the single-valued texture generation function, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <span data-ttu-id="23e0c-120"><dt>**GL- \_ Objekt \_ Ebene**</dt></span><span class="sxs-lookup"><span data-stu-id="23e0c-120"><dt>**GL\_OBJECT\_PLANE**</dt></span></span> </dl>              | <span data-ttu-id="23e0c-121">Der Parameter *para* meters gibt die Gleichung der vierstufigen Gleichung zurück, die die Generierung von Objekt linearen Koordinaten angeben.</span><span class="sxs-lookup"><span data-stu-id="23e0c-121">The *params* parameter returns the four plane equation coefficients that specify object linear-coordinate generation.</span></span> <span data-ttu-id="23e0c-122">Ganzzahlige Werte werden, wenn angefordert, direkt aus der internen Gleit Komma Darstellung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="23e0c-122">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <span data-ttu-id="23e0c-123"><dt>**GL- \_ Augen \_ Ebene**</dt></span><span class="sxs-lookup"><span data-stu-id="23e0c-123"><dt>**GL\_EYE\_PLANE**</dt></span></span> </dl>                       | <span data-ttu-id="23e0c-124">Der Parameter *para* meters gibt die Gleichung der vierstufigen Gleichung zurück, die die Generierung von Augen linearen Koordinaten angeben.</span><span class="sxs-lookup"><span data-stu-id="23e0c-124">The *params* parameter returns the four plane equation coefficients that specify eye linear-coordinate generation.</span></span> <span data-ttu-id="23e0c-125">Ganzzahlige Werte werden, wenn angefordert, direkt aus der internen Gleit Komma Darstellung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="23e0c-125">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span> <span data-ttu-id="23e0c-126">Die zurückgegebenen Werte werden in den Augen Koordinaten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="23e0c-126">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="23e0c-127">Sie sind nicht mit den Werten identisch, die mithilfe von [**gltexgen**](gltexgen-functions.md)angegeben wurden, es sei denn, die Modelview-Matrix wurde zum Zeitpunkt des Aufrufs von **gltexgen** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="23e0c-127">They are not equal to the values specified using [**glTexGen**](gltexgen-functions.md), unless the modelview matrix was identified at the time **glTexGen** was called.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23e0c-128">*params*</span><span class="sxs-lookup"><span data-stu-id="23e0c-128">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="23e0c-129">Gibt die angeforderten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="23e0c-129">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23e0c-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23e0c-130">Return value</span></span>

<span data-ttu-id="23e0c-131">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="23e0c-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="23e0c-132">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="23e0c-132">Error codes</span></span>

<span data-ttu-id="23e0c-133">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="23e0c-133">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="23e0c-134">Name</span><span class="sxs-lookup"><span data-stu-id="23e0c-134">Name</span></span>                                                                                                  | <span data-ttu-id="23e0c-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23e0c-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23e0c-136"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="23e0c-136"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="23e0c-137">*coord* oder *PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="23e0c-137">*coord* or *pname* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="23e0c-138"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="23e0c-138"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="23e0c-139">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="23e0c-139">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="23e0c-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23e0c-140">Remarks</span></span>

<span data-ttu-id="23e0c-141">Die **glgettexgen** -Funktion gibt in *Parameter ausgewählte Parameter* einer Texturkoordinaten Generierungs Funktion zurück, die Sie mit **gltexgen** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="23e0c-141">The **glGetTexGen** function returns in *params* selected parameters of a texture-coordinate generation function that you specified with **glTexGen**.</span></span> <span data-ttu-id="23e0c-142">Der *coord* -Parameter benennt eine der (*s*-, *t*-, *r*-, *q*)-Texturkoordinaten, indem er die symbolische Konstante GL \_ s, GL \_ t, GL \_ r oder GL \_ q verwendet.</span><span class="sxs-lookup"><span data-stu-id="23e0c-142">The *coord* parameter names one of the (*s*, *t*, *r*, *q*) texture coordinates, using the symbolic constant GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

<span data-ttu-id="23e0c-143">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *para* Metern vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="23e0c-143">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e0c-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23e0c-144">Requirements</span></span>



| <span data-ttu-id="23e0c-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23e0c-145">Requirement</span></span> | <span data-ttu-id="23e0c-146">Wert</span><span class="sxs-lookup"><span data-stu-id="23e0c-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23e0c-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23e0c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="23e0c-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23e0c-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="23e0c-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23e0c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="23e0c-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23e0c-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23e0c-151">Header</span><span class="sxs-lookup"><span data-stu-id="23e0c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="23e0c-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="23e0c-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="23e0c-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23e0c-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="23e0c-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23e0c-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="23e0c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="23e0c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23e0c-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23e0c-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e0c-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23e0c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e0c-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="23e0c-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="23e0c-159">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="23e0c-159">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="23e0c-160">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="23e0c-160">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> </dl>

 

 





