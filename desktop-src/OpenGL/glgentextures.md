---
title: glgentexturen-Funktion (GL. h)
description: Die Funktion "glgentexturen" generiert Textur Namen.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- glgentexturen-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957080"
---
# <a name="glgentextures-function"></a><span data-ttu-id="ce286-104">glgentexturen-Funktion</span><span class="sxs-lookup"><span data-stu-id="ce286-104">glGenTextures function</span></span>

<span data-ttu-id="ce286-105">Die Funktion " **glgentexturen** " generiert Textur Namen.</span><span class="sxs-lookup"><span data-stu-id="ce286-105">The **glGenTextures** function generates texture names.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce286-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce286-106">Syntax</span></span>


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="ce286-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce286-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce286-108">*n*</span><span class="sxs-lookup"><span data-stu-id="ce286-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="ce286-109">Die Anzahl der zu generierenden Textur Namen.</span><span class="sxs-lookup"><span data-stu-id="ce286-109">The number of texture names to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="ce286-110">*Textur*</span><span class="sxs-lookup"><span data-stu-id="ce286-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="ce286-111">Ein Zeiger auf das erste Element eines Arrays, in dem die generierten Textur Namen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ce286-111">A pointer to the first element of an array in which the generated texture names are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce286-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce286-112">Return value</span></span>

<span data-ttu-id="ce286-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ce286-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ce286-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ce286-114">Error codes</span></span>

<span data-ttu-id="ce286-115">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ce286-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ce286-116">Name</span><span class="sxs-lookup"><span data-stu-id="ce286-116">Name</span></span>                                                                                                  | <span data-ttu-id="ce286-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce286-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce286-118"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="ce286-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ce286-119">*n* war ein negativer Wert.</span><span class="sxs-lookup"><span data-stu-id="ce286-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="ce286-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="ce286-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ce286-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ce286-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce286-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce286-122">Remarks</span></span>

<span data-ttu-id="ce286-123">Die **glgentexturen** -Funktion gibt *n* Textur Namen im *Texturen* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="ce286-123">The **glGenTextures** function returns *n* texture names in the *textures* parameter.</span></span> <span data-ttu-id="ce286-124">Bei den Textur Namen handelt es sich nicht unbedingt um einen zusammenhängenden Satz von Ganzzahlen, aber keine der zurückgegebenen Namen können unmittelbar vor dem Aufrufen der Funktion " **glgentexturen** " verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce286-124">The texture names are not necessarily a contiguous set of integers, however, none of the returned names can have been in use immediately prior to calling the **glGenTextures** function.</span></span> <span data-ttu-id="ce286-125">Die generierten Texturen übernehmen die Dimensionalität des Textur Ziels, an das Sie zuerst mit der [**glBindTexture**](glbindtexture.md) -Funktion gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="ce286-125">The generated textures assume the dimensionality of the texture target to which they are first bound with the [**glBindTexture**](glbindtexture.md) function.</span></span> <span data-ttu-id="ce286-126">Von **glgentexturen** zurückgegebene Textur Namen werden nicht durch nachfolgende Aufrufe von **glgentexturen** zurückgegeben, es sei denn, Sie werden zuerst durch Aufrufen von [**gldeletetexturen**](gldeletetextures.md)gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ce286-126">Texture names returned by **glGenTextures** are not returned by subsequent calls to **glGenTextures** unless they are first deleted by calling [**glDeleteTextures**](gldeletetextures.md).</span></span>

<span data-ttu-id="ce286-127">Sie können " **glgentexturen** " nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="ce286-127">You cannot include **glGenTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="ce286-128">Die **glgentexturen** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce286-128">The **glGenTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="ce286-129">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glgentexturen** ab:</span><span class="sxs-lookup"><span data-stu-id="ce286-129">The following function retrieves information related to **glGenTextures**:</span></span>

-   [<span data-ttu-id="ce286-130">**glistexture**</span><span class="sxs-lookup"><span data-stu-id="ce286-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="ce286-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce286-131">Requirements</span></span>



| <span data-ttu-id="ce286-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce286-132">Requirement</span></span> | <span data-ttu-id="ce286-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ce286-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce286-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce286-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ce286-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce286-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ce286-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce286-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ce286-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce286-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce286-138">Header</span><span class="sxs-lookup"><span data-stu-id="ce286-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce286-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce286-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ce286-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce286-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce286-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce286-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce286-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ce286-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce286-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce286-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce286-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce286-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce286-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ce286-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ce286-146">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="ce286-146">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="ce286-147">**gldeletetexturen**</span><span class="sxs-lookup"><span data-stu-id="ce286-147">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="ce286-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ce286-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ce286-149">**glget**</span><span class="sxs-lookup"><span data-stu-id="ce286-149">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="ce286-150">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="ce286-150">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="ce286-151">**glistexture**</span><span class="sxs-lookup"><span data-stu-id="ce286-151">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="ce286-152">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ce286-152">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ce286-153">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ce286-153">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ce286-154">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="ce286-154">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





