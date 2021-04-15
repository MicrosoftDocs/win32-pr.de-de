---
title: glBindTexture-Funktion (GL. h)
description: Die glBindTexture-Funktion ermöglicht das Erstellen einer benannten Textur, die an ein Textur Ziel gebunden ist.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391997"
---
# <a name="glbindtexture-function"></a><span data-ttu-id="74c97-104">glBindTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="74c97-104">glBindTexture function</span></span>

<span data-ttu-id="74c97-105">Die **glBindTexture** -Funktion ermöglicht das Erstellen einer benannten Textur, die an ein Textur Ziel gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="74c97-105">The **glBindTexture** function enables the creation of a named texture that is bound to a texture target.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c97-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="74c97-106">Syntax</span></span>


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="74c97-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="74c97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c97-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="74c97-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="74c97-109">Das Ziel, an das die Textur gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="74c97-109">The target to which the texture is bound.</span></span> <span data-ttu-id="74c97-110">Muss den Wert "GL \_ Texture \_ 1D" oder "GL \_ Texture \_ 2D" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="74c97-110">Must have the value GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="74c97-111">*Konsistenz*</span><span class="sxs-lookup"><span data-stu-id="74c97-111">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="74c97-112">Der Name einer Textur. der Textur Name darf derzeit nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74c97-112">The name of a texture; the texture name cannot currently be in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c97-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74c97-113">Return value</span></span>

<span data-ttu-id="74c97-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="74c97-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74c97-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="74c97-115">Error codes</span></span>

<span data-ttu-id="74c97-116">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="74c97-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="74c97-117">Name</span><span class="sxs-lookup"><span data-stu-id="74c97-117">Name</span></span>                                                                                                  | <span data-ttu-id="74c97-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="74c97-118">Meaning</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74c97-119"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="74c97-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="74c97-120">Das Parameter *Ziel* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="74c97-120">The parameter *target* was not an accepted value.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="74c97-121"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="74c97-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="74c97-122">Die Parameter *Textur* enthielt nicht die gleiche Dimensionalität wie das *Ziel*, oder die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="74c97-122">The parameter *texture* did not have the same dimensionality as *target*, or the function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="74c97-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74c97-123">Remarks</span></span>

<span data-ttu-id="74c97-124">Mit der **glBindTexture** -Funktion können Sie eine benannte Textur erstellen.</span><span class="sxs-lookup"><span data-stu-id="74c97-124">The **glBindTexture** function enables you to create a named texture.</span></span> <span data-ttu-id="74c97-125">Der Aufruf von **glBindTexture** , bei dem das *Ziel* auf GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D festgelegt ist, und die *Textur* werden auf den Namen der neuen Textur festgelegt, die Sie erstellt haben, binden den Textur Namen an das entsprechende Textur Ziel.</span><span class="sxs-lookup"><span data-stu-id="74c97-125">Calling **glBindTexture** with *target* set to GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, and *texture* set to the name of the new texture you have created binds the texture name to the appropriate texture target.</span></span> <span data-ttu-id="74c97-126">Wenn eine Textur an ein Ziel gebunden ist, ist die vorherige Bindung für dieses Ziel nicht mehr wirksam.</span><span class="sxs-lookup"><span data-stu-id="74c97-126">When a texture is bound to a target, the previous binding for that target is no longer in effect.</span></span>

<span data-ttu-id="74c97-127">Textur Namen sind ganze Zahlen ohne Vorzeichen, wobei der Wert 0 (null) für die Darstellung der Standard Textur für die einzelnen Textur Ziele reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="74c97-127">Texture names are unsigned integers with the value zero reserved to represent the default texture for each texture target.</span></span> <span data-ttu-id="74c97-128">Textur Namen und die entsprechenden Textur Inhalte sind lokal im freigegebenen Anzeigelisten Bereich des aktuellen OpenGL-renderingkontexts. zwei renderingkontexte geben Textur Namen nur dann frei, wenn Sie auch anzeigen Listen freigeben.</span><span class="sxs-lookup"><span data-stu-id="74c97-128">Texture names and the corresponding texture contents are local to the shared display-list space of the current OpenGL rendering context; two rendering contexts share texture names only if they also share display lists.</span></span> <span data-ttu-id="74c97-129">Sie können mit [**glgentexturen**](glgentextures.md)eine Reihe neuer Textur Namen generieren.</span><span class="sxs-lookup"><span data-stu-id="74c97-129">You can generate a set of new texture names using [**glGenTextures**](glgentextures.md).</span></span>

<span data-ttu-id="74c97-130">Wenn eine Textur zum ersten Mal gebunden wird, wird davon ausgegangen, dass die Dimensionalität des zugehörigen Textur Ziels liegt. eine Textur, die an GL \_ Texture \_ 1D gebunden ist, wird eindimensional, und eine Textur, die an GL \_ Texture 2D gebunden ist, \_ wird zweidimensional.</span><span class="sxs-lookup"><span data-stu-id="74c97-130">When a texture is first bound, it assumes the dimensionality of its texture target; a texture bound to GL\_TEXTURE\_1D becomes one-dimensional and a texture bound to GL\_TEXTURE\_2D becomes two-dimensional.</span></span> <span data-ttu-id="74c97-131">Vorgänge, die Sie für ein Textur Ziel ausführen, wirken sich auch auf eine Textur aus, die an das Ziel gebunden</span><span class="sxs-lookup"><span data-stu-id="74c97-131">Operations you perform on a texture target also affect a texture bound to the target.</span></span> <span data-ttu-id="74c97-132">Wenn Sie ein Textur Ziel Abfragen, ist der Rückgabewert der Zustand der an ihn gebundenen Textur.</span><span class="sxs-lookup"><span data-stu-id="74c97-132">When you query a texture target, the return value is the state of the texture bound to it.</span></span> <span data-ttu-id="74c97-133">Textur Ziele werden Aliase für Texturen, die zurzeit an Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="74c97-133">Texture targets become aliases for textures currently bound to them.</span></span>

<span data-ttu-id="74c97-134">Wenn Sie eine Textur mit **glBindTexture** binden, bleibt die Bindung aktiv, bis eine andere Textur an dasselbe Ziel gebunden ist oder Sie die gebundene Textur mit der Funktion " [**gldeletetexturen**](gldeletetextures.md) " löschen.</span><span class="sxs-lookup"><span data-stu-id="74c97-134">When you bind a texture with **glBindTexture**, the binding remains active until a different texture is bound to the same target or you delete the bound texture with the [**glDeleteTextures**](gldeletetextures.md) function.</span></span> <span data-ttu-id="74c97-135">Nachdem Sie eine benannte Textur erstellt haben, können Sie Sie an ein Textur Ziel binden, das über dieselbe Dimensionalität verfügt wie bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="74c97-135">Once you create a named texture you can bind it to a texture target that has the same dimensionality as often as needed.</span></span>

<span data-ttu-id="74c97-136">Es ist in der Regel viel schneller, eine vorhandene benannte Textur mithilfe von **glBindTexture** an eines der Textur Ziele zu binden, als das Textur Bild mithilfe von [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md)neu zu laden.</span><span class="sxs-lookup"><span data-stu-id="74c97-136">It is usually much faster to use **glBindTexture** to bind an existing named texture to one of the texture targets than it is to reload the texture image using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="74c97-137">Verwenden Sie zum zusätzlichen Steuern der texturierungs Leistung [**glpriorizetexturen**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="74c97-137">For additional control of texturing performance, use [**glPrioritizeTextures**](glprioritizetextures.md).</span></span>

<span data-ttu-id="74c97-138">Sie können Aufrufe von **glBindTexture** in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="74c97-138">You can include calls to **glBindTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="74c97-139">Die **glBindTexture** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="74c97-139">The **glBindTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="74c97-140">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glBindTexture** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="74c97-140">The following functions retrieve information related to **glBindTexture**:</span></span>

-   <span data-ttu-id="74c97-141">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Texture \_ 1D \_ Binding</span><span class="sxs-lookup"><span data-stu-id="74c97-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_1D\_BINDING</span></span>

<span data-ttu-id="74c97-142">**glget** mit Argument GL \_ Texture \_ 2D \_ Binding</span><span class="sxs-lookup"><span data-stu-id="74c97-142">**glGet** with argument GL\_TEXTURE\_2D\_BINDING</span></span>

## <a name="requirements"></a><span data-ttu-id="74c97-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74c97-143">Requirements</span></span>



| <span data-ttu-id="74c97-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74c97-144">Requirement</span></span> | <span data-ttu-id="74c97-145">Wert</span><span class="sxs-lookup"><span data-stu-id="74c97-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74c97-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74c97-146">Minimum supported client</span></span><br/> | <span data-ttu-id="74c97-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74c97-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="74c97-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74c97-148">Minimum supported server</span></span><br/> | <span data-ttu-id="74c97-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74c97-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74c97-150">Header</span><span class="sxs-lookup"><span data-stu-id="74c97-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="74c97-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="74c97-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="74c97-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="74c97-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="74c97-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74c97-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="74c97-154">DLL</span><span class="sxs-lookup"><span data-stu-id="74c97-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74c97-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74c97-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74c97-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74c97-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c97-157">**glaretexturesresidente**</span><span class="sxs-lookup"><span data-stu-id="74c97-157">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="74c97-158">**gldeletetexturen**</span><span class="sxs-lookup"><span data-stu-id="74c97-158">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="74c97-159">**glgentexturen**</span><span class="sxs-lookup"><span data-stu-id="74c97-159">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="74c97-160">**glget**</span><span class="sxs-lookup"><span data-stu-id="74c97-160">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="74c97-161">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="74c97-161">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="74c97-162">**glistexture**</span><span class="sxs-lookup"><span data-stu-id="74c97-162">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="74c97-163">**glpriorizetexturen**</span><span class="sxs-lookup"><span data-stu-id="74c97-163">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="74c97-164">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="74c97-164">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="74c97-165">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="74c97-165">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="74c97-166">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="74c97-166">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





