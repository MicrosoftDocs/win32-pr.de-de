---
title: gluBuild1DMipmaps-Funktion (glu. h)
description: Die gluBuild1DMipmaps-Funktion erstellt 1-D-Mipmaps.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- gluBuild1DMipmaps-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338529"
---
# <a name="glubuild1dmipmaps-function"></a><span data-ttu-id="b4fb5-104">gluBuild1DMipmaps-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4fb5-104">gluBuild1DMipmaps function</span></span>

<span data-ttu-id="b4fb5-105">Die **gluBuild1DMipmaps** -Funktion erstellt 1-D-Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-105">The **gluBuild1DMipmaps** function creates 1-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fb5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4fb5-106">Syntax</span></span>


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="b4fb5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4fb5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4fb5-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="b4fb5-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="b4fb5-109">Die Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-109">The target texture.</span></span> <span data-ttu-id="b4fb5-110">Muss "GL \_ Texture \_ 1D" lauten.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="b4fb5-111">*components*</span><span class="sxs-lookup"><span data-stu-id="b4fb5-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="b4fb5-112">Die Anzahl der Farbkomponenten in der Textur.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-112">The number of color components in the texture.</span></span> <span data-ttu-id="b4fb5-113">Muss 1, 2, 3 oder 4 sein.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="b4fb5-114">*width*</span><span class="sxs-lookup"><span data-stu-id="b4fb5-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="b4fb5-115">Die Breite des Textur Bilds.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="b4fb5-116">*format*</span><span class="sxs-lookup"><span data-stu-id="b4fb5-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="b4fb5-117">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-117">The format of the pixel data.</span></span> <span data-ttu-id="b4fb5-118">Die folgenden Werte sind gültig: GL \_ Color \_ Index, GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance oder GL \_ Luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-118">The following values are valid: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="b4fb5-119">*type*</span><span class="sxs-lookup"><span data-stu-id="b4fb5-119">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b4fb5-120">Der Datentyp für *Daten*.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-120">The data type for *data*.</span></span> <span data-ttu-id="b4fb5-121">Die folgenden Werte sind gültig: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int oder GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-121">The following values are valid: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="b4fb5-122">*data*</span><span class="sxs-lookup"><span data-stu-id="b4fb5-122">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="b4fb5-123">Ein Zeiger auf die Bilddaten im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-123">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4fb5-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4fb5-124">Return value</span></span>

<span data-ttu-id="b4fb5-125">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4fb5-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4fb5-126">Remarks</span></span>

<span data-ttu-id="b4fb5-127">Die **gluBuild1DMipmaps** -Funktion Ruft das Eingabebild ab und generiert alle MipMap-Bilder (mit " [**gluscaleimage**](gluscaleimage.md)"), sodass das Eingabebild als ein mipzugeordnetes Textur Bild verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-127">The **gluBuild1DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so that the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="b4fb5-128">Die [**glTexImage1D**](glteximage1d.md) -Funktion wird dann aufgerufen, um die einzelnen Bilder zu laden.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-128">The [**glTexImage1D**](glteximage1d.md) function is then called to load each of the images.</span></span> <span data-ttu-id="b4fb5-129">Wenn die Breite des Eingabe Bilds keine Potenz von zwei ist, wird das Bild auf die nächste Potenz von zwei skaliert, bevor die Mipmaps generiert werden.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-129">If the width of the input image is not a power of two, then the image is scaled to the nearest power of two before the mipmaps are generated.</span></span>

<span data-ttu-id="b4fb5-130">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-130">A return value of zero indicates success.</span></span> <span data-ttu-id="b4fb5-131">Andernfalls wird ein glu-Fehlercode zurückgegeben (siehe [**gluerrorstring**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="b4fb5-131">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="b4fb5-132">Eine Beschreibung der zulässigen Werte für den *Format* -Parameter finden Sie unter **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="b4fb5-132">For a description of the acceptable values for the *format* parameter, see **glTexImage1D**.</span></span> <span data-ttu-id="b4fb5-133">Eine Beschreibung der zulässigen Werte für den *Typparameter* finden Sie unter [**gldrawpixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="b4fb5-133">For a description of the acceptable values for the *type* parameter, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4fb5-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4fb5-134">Requirements</span></span>



| <span data-ttu-id="b4fb5-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4fb5-135">Requirement</span></span> | <span data-ttu-id="b4fb5-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b4fb5-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fb5-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4fb5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fb5-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4fb5-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b4fb5-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4fb5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fb5-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4fb5-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b4fb5-141">Header</span><span class="sxs-lookup"><span data-stu-id="b4fb5-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4fb5-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4fb5-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b4fb5-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4fb5-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4fb5-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4fb5-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4fb5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b4fb5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4fb5-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4fb5-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4fb5-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4fb5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4fb5-148">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="b4fb5-148">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b4fb5-149">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b4fb5-149">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b4fb5-150">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="b4fb5-150">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="b4fb5-151">**gluscaleimage**</span><span class="sxs-lookup"><span data-stu-id="b4fb5-151">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





