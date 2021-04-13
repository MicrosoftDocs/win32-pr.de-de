---
title: gldeletetexturen-Funktion (GL. h)
description: Die Funktion "gldeletetexturen" löscht benannte Texturen.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- gldeletetexturen-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475675"
---
# <a name="gldeletetextures-function"></a><span data-ttu-id="db4a3-104">gldeletetexturen-Funktion</span><span class="sxs-lookup"><span data-stu-id="db4a3-104">glDeleteTextures function</span></span>

<span data-ttu-id="db4a3-105">Die Funktion " **gldeletetexturen** " löscht benannte Texturen.</span><span class="sxs-lookup"><span data-stu-id="db4a3-105">The **glDeleteTextures** function deletes named textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="db4a3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="db4a3-106">Syntax</span></span>


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="db4a3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="db4a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db4a3-108">*n*</span><span class="sxs-lookup"><span data-stu-id="db4a3-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="db4a3-109">Die Anzahl der zu löschenden Texturen.</span><span class="sxs-lookup"><span data-stu-id="db4a3-109">The number of textures to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="db4a3-110">*Textur*</span><span class="sxs-lookup"><span data-stu-id="db4a3-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="db4a3-111">Ein Array von Texturen, die gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="db4a3-111">An array of textures to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db4a3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db4a3-112">Return value</span></span>

<span data-ttu-id="db4a3-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="db4a3-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db4a3-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="db4a3-114">Error codes</span></span>

<span data-ttu-id="db4a3-115">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="db4a3-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="db4a3-116">Name</span><span class="sxs-lookup"><span data-stu-id="db4a3-116">Name</span></span>                                                                                                  | <span data-ttu-id="db4a3-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="db4a3-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db4a3-118"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="db4a3-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="db4a3-119">*n* war ein negativer Wert.</span><span class="sxs-lookup"><span data-stu-id="db4a3-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="db4a3-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="db4a3-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="db4a3-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="db4a3-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="db4a3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db4a3-122">Remarks</span></span>

<span data-ttu-id="db4a3-123">Die **gldeletetexturen** -Funktion löscht *n* Texturen, die von den Elementen der Array *Texturen* benannt werden.</span><span class="sxs-lookup"><span data-stu-id="db4a3-123">The **glDeleteTextures** function deletes *n* textures named by the elements of the array *textures*.</span></span> <span data-ttu-id="db4a3-124">Nachdem eine Textur gelöscht wurde, weist Sie keinen Inhalt oder keine Dimensionalität auf, und der Name ist für die Wiederverwendung frei (z. b. von **glgentexturen**).</span><span class="sxs-lookup"><span data-stu-id="db4a3-124">After a texture is deleted, it has no contents or dimensionality, and its name is free for reuse (for example, by **glGenTextures**).</span></span> <span data-ttu-id="db4a3-125">Die Funktion " **gldeletetexturen** " ignoriert Nullen und Namen, die nicht vorhandenen Texturen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="db4a3-125">The **glDeleteTextures** function ignores zeros and names that do not correspond to existing textures.</span></span>

<span data-ttu-id="db4a3-126">Wenn eine Textur, die gerade gebunden ist, gelöscht wird, wird die Bindung auf NULL (die Standard Textur) zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="db4a3-126">If a texture that is currently bound is deleted, the binding reverts to zero (the default texture).</span></span>

<span data-ttu-id="db4a3-127">Sie können keine Aufrufe von **gldeletetexturen** in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="db4a3-127">You cannot include calls to **glDeleteTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="db4a3-128">Die **gldeletetexturen** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db4a3-128">The **glDeleteTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="db4a3-129">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gldeletetexturen** ab:</span><span class="sxs-lookup"><span data-stu-id="db4a3-129">The following function retrieves information related to **glDeleteTextures**:</span></span>

-   [<span data-ttu-id="db4a3-130">**glistexture**</span><span class="sxs-lookup"><span data-stu-id="db4a3-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="db4a3-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db4a3-131">Requirements</span></span>



| <span data-ttu-id="db4a3-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db4a3-132">Requirement</span></span> | <span data-ttu-id="db4a3-133">Wert</span><span class="sxs-lookup"><span data-stu-id="db4a3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db4a3-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db4a3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="db4a3-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db4a3-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="db4a3-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db4a3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="db4a3-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db4a3-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db4a3-138">Header</span><span class="sxs-lookup"><span data-stu-id="db4a3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="db4a3-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="db4a3-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="db4a3-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="db4a3-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="db4a3-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db4a3-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="db4a3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="db4a3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db4a3-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db4a3-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db4a3-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db4a3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4a3-145">**glaretexturesresidente**</span><span class="sxs-lookup"><span data-stu-id="db4a3-145">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="db4a3-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="db4a3-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="db4a3-147">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="db4a3-147">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="db4a3-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="db4a3-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="db4a3-149">**glgentexturen**</span><span class="sxs-lookup"><span data-stu-id="db4a3-149">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="db4a3-150">**glget**</span><span class="sxs-lookup"><span data-stu-id="db4a3-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="db4a3-151">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="db4a3-151">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="db4a3-152">**glistexture**</span><span class="sxs-lookup"><span data-stu-id="db4a3-152">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="db4a3-153">**glpriorizetexturen**</span><span class="sxs-lookup"><span data-stu-id="db4a3-153">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="db4a3-154">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="db4a3-154">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="db4a3-155">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="db4a3-155">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="db4a3-156">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="db4a3-156">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="db4a3-157">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="db4a3-157">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





