---
title: glgetteximage-Funktion (GL. h)
description: Die Funktion "glgetteximage" gibt ein Textur Bild zurück.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glgetteximage-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342660"
---
# <a name="glgetteximage-function"></a><span data-ttu-id="f1353-104">glgetteximage-Funktion</span><span class="sxs-lookup"><span data-stu-id="f1353-104">glGetTexImage function</span></span>

<span data-ttu-id="f1353-105">Die Funktion " **glgetteximage** " gibt ein Textur Bild zurück.</span><span class="sxs-lookup"><span data-stu-id="f1353-105">The **glGetTexImage** function returns a texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1353-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1353-106">Syntax</span></span>


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="f1353-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1353-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1353-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="f1353-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="f1353-109">Gibt an, welche Textur abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1353-109">Specifies which texture is to be obtained.</span></span> <span data-ttu-id="f1353-110">GL \_ Texture \_ 1D und GL \_ Texture \_ 2D werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f1353-110">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f1353-111">*level*</span><span class="sxs-lookup"><span data-stu-id="f1353-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="f1353-112">Die Detailstufe des gewünschten Bilds.</span><span class="sxs-lookup"><span data-stu-id="f1353-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="f1353-113">Ebene 0 ist die Basis Image Ebene.</span><span class="sxs-lookup"><span data-stu-id="f1353-113">Level 0 is the base image level.</span></span> <span data-ttu-id="f1353-114">Ebene *n* ist das *n*-te MipMap-Reduzierungs Bild.</span><span class="sxs-lookup"><span data-stu-id="f1353-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="f1353-115">*format*</span><span class="sxs-lookup"><span data-stu-id="f1353-115">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="f1353-116">Ein Pixel Format für die zurückgegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="f1353-116">A pixel format for the returned data.</span></span> <span data-ttu-id="f1353-117">Die unterstützten Formate sind GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ Luminance, GL \_ BGR \_ ext, GL \_ BGRA \_ ext und GL \_ Luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="f1353-117">The supported formats are GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_LUMINANCE, GL\_BGR\_EXT, GL\_BGRA\_EXT, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="f1353-118">*type*</span><span class="sxs-lookup"><span data-stu-id="f1353-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f1353-119">Ein Pixeltyp für die zurückgegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="f1353-119">A pixel type for the returned data.</span></span> <span data-ttu-id="f1353-120">Die unterstützten Typen sind GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int und GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="f1353-120">The supported types are GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="f1353-121">*Pixel*</span><span class="sxs-lookup"><span data-stu-id="f1353-121">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="f1353-122">Gibt das Textur Bild zurück.</span><span class="sxs-lookup"><span data-stu-id="f1353-122">Returns the texture image.</span></span> <span data-ttu-id="f1353-123">Muss ein Zeiger auf ein Array des Typs sein, der durch den- *Typ* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f1353-123">Should be a pointer to an array of the type specified by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1353-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1353-124">Return value</span></span>

<span data-ttu-id="f1353-125">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f1353-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f1353-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f1353-126">Error codes</span></span>

<span data-ttu-id="f1353-127">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f1353-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f1353-128">Name</span><span class="sxs-lookup"><span data-stu-id="f1353-128">Name</span></span>                                                                                                  | <span data-ttu-id="f1353-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f1353-129">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1353-130"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1353-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f1353-131">*Ziel*, *Format* oder *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="f1353-131">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="f1353-132"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="f1353-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="f1353-133">die *Ebene* ist kleiner als 0 (null) oder größer als *Log* 2 (*Max*), wobei *Max* der zurückgegebene Wert von GL \_ Max \_ Texture \_ size ist.</span><span class="sxs-lookup"><span data-stu-id="f1353-133">*level* is less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="f1353-134"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f1353-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f1353-135">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f1353-135">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) .</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f1353-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1353-136">Remarks</span></span>

<span data-ttu-id="f1353-137">Die Funktion " **glgetteximage** " gibt ein Textur Bild in *Pixel* zurück.</span><span class="sxs-lookup"><span data-stu-id="f1353-137">The **glGetTexImage** function returns a texture image into *pixels*.</span></span> <span data-ttu-id="f1353-138">Der *target* -Parameter gibt an, ob das gewünschte Textur Bild durch [**glTexImage1D**](glteximage1d.md)**(** GL \_ Texture \_ 1D **)** oder durch [**glTexImage2D**](glteximage2d.md)**(** GL \_ Texture \_ 2D **)** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f1353-138">The *target* parameter specifies whether the desired texture image is one specified by [**glTexImage1D**](glteximage1d.md)**(** GL\_TEXTURE\_1D **)** or by [**glTexImage2D**](glteximage2d.md)**(** GL\_TEXTURE\_2D **)**.</span></span> <span data-ttu-id="f1353-139">Der *Level* -Parameter gibt die Detailstufe des gewünschten Bilds an.</span><span class="sxs-lookup"><span data-stu-id="f1353-139">The *level* parameter specifies the level-of-detail number of the desired image.</span></span> <span data-ttu-id="f1353-140">Die *Format* -und *Typparameter* geben das Format und den Typ des gewünschten Bilds an.</span><span class="sxs-lookup"><span data-stu-id="f1353-140">The *format* and *type* parameters specify the format and type of the desired image array.</span></span> <span data-ttu-id="f1353-141">Eine Beschreibung der zulässigen Werte für die *Format* -und *Typparameter* finden Sie unter **glTexImage1D** und [**gldrawpixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="f1353-141">For a description of the acceptable values for the *format* and *type* parameters, respectively, see **glTexImage1D** and [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="f1353-142">Der Vorgang von **glgetteximage** ist am besten zu verstehen, indem das ausgewählte, interne Textur Bild mit vier Komponenten als RGBA-Farb Puffer für die Größe des Bilds betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="f1353-142">Operation of **glGetTexImage** is best understood by considering the selected internal four-component texture image to be an RGBA color buffer the size of the image.</span></span> <span data-ttu-id="f1353-143">Die Semantik von **glgetteximage** ist dann identisch mit denen von [**glread Pixel**](glreadpixels.md) , die mit dem gleichen *Format* und *Typ* aufgerufen werden. Wenn *x* und *y* auf 0 (null) festgelegt sind, wird die *Breite* auf die Breite des Textur Bilds (einschließlich des Rahmens, falls angegeben) und die *Höhe* auf 1 für 1-d-Bilder festgelegt, oder auf die Höhe des Textur Bilds (einschließlich des Rahmens, sofern angegeben) für 2D-Bilder.</span><span class="sxs-lookup"><span data-stu-id="f1353-143">The semantics of **glGetTexImage** are then identical to those of [**glReadPixels**](glreadpixels.md) called with the same *format* and *type*, with *x* and *y* set to zero, *width* set to the width of the texture image (including border if one was specified), and *height* set to one for 1-D images, or to the height of the texture image (including border, if one was specified) for 2-D images.</span></span>

<span data-ttu-id="f1353-144">Da es sich bei dem internen Textur Bild um ein RGBA-Bild handelt, werden die Pixel Formate "GL \_ Color \_ Index", "GL \_ Stencil \_ Index" und "GL- \_ tiefen Komponente" \_ nicht akzeptiert, und die Bitmap "Pixel Type GL" \_ wird</span><span class="sxs-lookup"><span data-stu-id="f1353-144">Because the internal texture image is an RGBA image, pixel formats GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, and GL\_DEPTH\_COMPONENT are not accepted, and pixel type GL\_BITMAP is not accepted.</span></span>

<span data-ttu-id="f1353-145">Wenn das ausgewählte Textur Bild keine vier Komponenten enthält, werden die folgenden Zuordnungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="f1353-145">If the selected texture image does not contain four components, the following mappings are applied.</span></span> <span data-ttu-id="f1353-146">Texturen mit einer einzelnen Komponente werden als RGBA-Puffer behandelt, wobei rot auf den Einzelkomponenten Wert festgelegt ist und grün, blau und Alpha auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f1353-146">Single-component textures are treated as RGBA buffers with red set to the single-component value, and green, blue, and alpha set to zero.</span></span>

<span data-ttu-id="f1353-147">Texturen mit zwei Komponenten werden als RGBA-Puffer behandelt, wobei rot auf den Wert von Komponente NULL, Alpha auf den Wert von Komponente 1 und grün und blau auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f1353-147">Two-component textures are treated as RGBA buffers, with red set to the value of component zero, alpha set to the value of component one, and green and blue set to zero.</span></span> <span data-ttu-id="f1353-148">Schließlich werden drei komponententexturen als RGBA-Puffer behandelt, wobei rot auf Komponente 0 (null), grün auf Komponente 1, blau auf Komponente 2 und Alpha auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f1353-148">Finally, three-component textures are treated as RGBA buffers with red set to component zero, green set to component one, blue set to component two, and alpha set to zero.</span></span>

<span data-ttu-id="f1353-149">Um die erforderliche Größe von *Pixeln* zu ermitteln, verwenden Sie [**glgettexlevelparameter**](glgettexlevelparameter.md) , um die Dimensionen des internen Textur Bilds zu ermitteln, und Skalieren Sie dann die erforderliche Anzahl von Pixeln nach dem für die einzelnen Pixel erforderlichen Speicher, basierend auf *Format* und *Typ*.</span><span class="sxs-lookup"><span data-stu-id="f1353-149">To determine the required size of *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) to ascertain the dimensions of the internal texture image, and then scale the required number of pixels by the storage required for each pixel, based on *format* and *type*.</span></span> <span data-ttu-id="f1353-150">Stellen Sie sicher, dass die Parameter für die Pixel Speicherung berücksichtigt werden, insbesondere die Ausrichtung von GL \_ Pack \_ .</span><span class="sxs-lookup"><span data-stu-id="f1353-150">Be sure to take the pixel-storage parameters into account, especially GL\_PACK\_ALIGNMENT.</span></span>

<span data-ttu-id="f1353-151">Wenn ein Fehler generiert wird, wird keine Änderung an dem Inhalt der *Pixel* vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="f1353-151">If an error is generated, no change is made to the contents of *pixels*.</span></span>

<span data-ttu-id="f1353-152">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit " **glgetteximage**" abgerufen:</span><span class="sxs-lookup"><span data-stu-id="f1353-152">The following functions retrieve information related to **glGetTexImage**:</span></span>

<span data-ttu-id="f1353-153">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Pack \_ -Ausrichtung und anderen</span><span class="sxs-lookup"><span data-stu-id="f1353-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PACK\_ALIGNMENT and others</span></span>

<span data-ttu-id="f1353-154">[**glgettexlevelparameter**](glgettexlevelparameter.md) mit Argument GL \_ Textur \_ Width</span><span class="sxs-lookup"><span data-stu-id="f1353-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) with argument GL\_TEXTURE\_WIDTH</span></span>

<span data-ttu-id="f1353-155">**glgettexlevelparameter** mit Argument GL \_ Textur \_ Height</span><span class="sxs-lookup"><span data-stu-id="f1353-155">**glGetTexLevelParameter** with argument GL\_TEXTURE\_HEIGHT</span></span>

<span data-ttu-id="f1353-156">**glgettexlevelparameter** mit dem Argument "GL \_ Texture \_ Border"</span><span class="sxs-lookup"><span data-stu-id="f1353-156">**glGetTexLevelParameter** with argument GL\_TEXTURE\_BORDER</span></span>

<span data-ttu-id="f1353-157">**glgettexlevelparameter** mit Argument GL- \_ Textur \_ Komponenten</span><span class="sxs-lookup"><span data-stu-id="f1353-157">**glGetTexLevelParameter** with argument GL\_TEXTURE\_COMPONENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="f1353-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1353-158">Requirements</span></span>



| <span data-ttu-id="f1353-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1353-159">Requirement</span></span> | <span data-ttu-id="f1353-160">Wert</span><span class="sxs-lookup"><span data-stu-id="f1353-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1353-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1353-161">Minimum supported client</span></span><br/> | <span data-ttu-id="f1353-162">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1353-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f1353-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1353-163">Minimum supported server</span></span><br/> | <span data-ttu-id="f1353-164">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1353-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f1353-165">Header</span><span class="sxs-lookup"><span data-stu-id="f1353-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1353-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1353-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f1353-167">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f1353-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1353-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1353-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f1353-169">DLL</span><span class="sxs-lookup"><span data-stu-id="f1353-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1353-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1353-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1353-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1353-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1353-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f1353-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f1353-173">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="f1353-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="f1353-174">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f1353-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f1353-175">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="f1353-175">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="f1353-176">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="f1353-176">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="f1353-177">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="f1353-177">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="f1353-178">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="f1353-178">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





