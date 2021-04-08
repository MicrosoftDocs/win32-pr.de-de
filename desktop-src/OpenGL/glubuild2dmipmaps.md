---
title: gluBuild2DMipmaps-Funktion (glu. h)
description: Die gluBuild2DMipmaps-Funktion erstellt 2-D-Mipmaps.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- gluBuild2DMipmaps-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949579"
---
# <a name="glubuild2dmipmaps-function"></a><span data-ttu-id="f113c-104">gluBuild2DMipmaps-Funktion</span><span class="sxs-lookup"><span data-stu-id="f113c-104">gluBuild2DMipmaps function</span></span>

<span data-ttu-id="f113c-105">Die **gluBuild2DMipmaps** -Funktion erstellt 2-D-Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="f113c-105">The **gluBuild2DMipmaps** function creates 2-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="f113c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f113c-106">Syntax</span></span>


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="f113c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f113c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f113c-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="f113c-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="f113c-109">Die Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="f113c-109">The target texture.</span></span> <span data-ttu-id="f113c-110">Muss "GL \_ Texture \_ 2D" lauten.</span><span class="sxs-lookup"><span data-stu-id="f113c-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="f113c-111">*components*</span><span class="sxs-lookup"><span data-stu-id="f113c-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="f113c-112">Die Anzahl der Farbkomponenten in der Textur.</span><span class="sxs-lookup"><span data-stu-id="f113c-112">The number of color components in the texture.</span></span> <span data-ttu-id="f113c-113">Muss 1, 2, 3 oder 4 sein.</span><span class="sxs-lookup"><span data-stu-id="f113c-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="f113c-114">*width*</span><span class="sxs-lookup"><span data-stu-id="f113c-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="f113c-115">Die Breite des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="f113c-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="f113c-116">*height*</span><span class="sxs-lookup"><span data-stu-id="f113c-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="f113c-117">Die Höhe des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="f113c-117">The height of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="f113c-118">*format*</span><span class="sxs-lookup"><span data-stu-id="f113c-118">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="f113c-119">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="f113c-119">The format of the pixel data.</span></span> <span data-ttu-id="f113c-120">Muss einer der folgenden sein: GL \_ Color \_ Index, GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance oder GL \_ Luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="f113c-120">Must be one of the following: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="f113c-121">*type*</span><span class="sxs-lookup"><span data-stu-id="f113c-121">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f113c-122">Der Datentyp für *Daten*.</span><span class="sxs-lookup"><span data-stu-id="f113c-122">The data type for *data*.</span></span> <span data-ttu-id="f113c-123">Muss eines der folgenden sein: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int oder GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="f113c-123">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="f113c-124">*data*</span><span class="sxs-lookup"><span data-stu-id="f113c-124">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="f113c-125">Ein Zeiger auf die Bilddaten im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f113c-125">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f113c-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f113c-126">Return value</span></span>

<span data-ttu-id="f113c-127">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f113c-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f113c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f113c-128">Remarks</span></span>

<span data-ttu-id="f113c-129">Die **gluBuild2DMipmaps** -Funktion Ruft das Eingabebild ab und generiert alle MipMap-Bilder (mit " [**gluscaleimage**](gluscaleimage.md)"), sodass das Eingabebild als ein mipzugeordnetes Textur Bild verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f113c-129">The **gluBuild2DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="f113c-130">Um jedes Abbild zu laden, wenden Sie [**glTexImage2D**](glteximage2d.md)an.</span><span class="sxs-lookup"><span data-stu-id="f113c-130">To load each of the images, call [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="f113c-131">Wenn die Dimensionen des Eingabe Bilds keine Kräfte von zwei sind, wird das Bild so skaliert, dass sowohl die Breite als auch die Höhe die Kräfte von zwei sind, bevor die Mipmaps generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f113c-131">If the dimensions of the input image are not powers of two, then the image is scaled so that both the width and height are powers of two before the mipmaps are generated.</span></span>

<span data-ttu-id="f113c-132">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="f113c-132">A return value of zero indicates success.</span></span> <span data-ttu-id="f113c-133">Andernfalls wird ein glu-Fehlercode zurückgegeben (siehe [**gluerrorstring**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="f113c-133">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="f113c-134">Eine Beschreibung der zulässigen Werte für den *Format* -Parameter finden Sie unter **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="f113c-134">For a description of the acceptable values for the *format* parameter, see **glTexImage2D**.</span></span> <span data-ttu-id="f113c-135">Eine Beschreibung der zulässigen Werte für *Type* finden Sie unter [**gldrawpixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="f113c-135">For a description of the acceptable values for *type*, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f113c-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f113c-136">Requirements</span></span>



| <span data-ttu-id="f113c-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f113c-137">Requirement</span></span> | <span data-ttu-id="f113c-138">Wert</span><span class="sxs-lookup"><span data-stu-id="f113c-138">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f113c-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f113c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f113c-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f113c-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f113c-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f113c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f113c-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f113c-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f113c-143">Header</span><span class="sxs-lookup"><span data-stu-id="f113c-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f113c-144"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f113c-144"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f113c-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f113c-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="f113c-146"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f113c-146"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f113c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f113c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f113c-148"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f113c-148"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f113c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f113c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f113c-150">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="f113c-150">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="f113c-151">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="f113c-151">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="f113c-152">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="f113c-152">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="f113c-153">**gluscaleimage**</span><span class="sxs-lookup"><span data-stu-id="f113c-153">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





