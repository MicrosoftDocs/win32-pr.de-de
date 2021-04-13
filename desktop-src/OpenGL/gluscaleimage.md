---
title: gluscaleimage-Funktion (glu. h)
description: Die Funktion "gluscaleimage" skaliert ein Bild auf eine beliebige Größe.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluscaleimage-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391501"
---
# <a name="gluscaleimage-function"></a><span data-ttu-id="87eab-104">gluscaleimage-Funktion</span><span class="sxs-lookup"><span data-stu-id="87eab-104">gluScaleImage function</span></span>

<span data-ttu-id="87eab-105">Die Funktion " **gluscaleimage** " skaliert ein Bild auf eine beliebige Größe.</span><span class="sxs-lookup"><span data-stu-id="87eab-105">The **gluScaleImage** function scales an image to an arbitrary size.</span></span>

## <a name="syntax"></a><span data-ttu-id="87eab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="87eab-106">Syntax</span></span>


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a><span data-ttu-id="87eab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="87eab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87eab-108">*format*</span><span class="sxs-lookup"><span data-stu-id="87eab-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-109">Das Format der Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="87eab-109">The format of the pixel data.</span></span> <span data-ttu-id="87eab-110">Die folgenden symbolischen Werte sind gültig: GL \_ Color \_ Index, GL \_ Stencil \_ Index, GL- \_ tiefen \_ Komponente, GL \_ red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Helligkeit und GL \_ Luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="87eab-110">The following symbolic values are valid: GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, GL\_DEPTH\_COMPONENT, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="87eab-111">*widthin*</span><span class="sxs-lookup"><span data-stu-id="87eab-111">*widthin*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-112">Die Breite des skalierten Quell Bilds.</span><span class="sxs-lookup"><span data-stu-id="87eab-112">The width of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="87eab-113">*Erhöhung*</span><span class="sxs-lookup"><span data-stu-id="87eab-113">*heightin*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-114">Die Höhe des skalierten Quell Bilds.</span><span class="sxs-lookup"><span data-stu-id="87eab-114">The height of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="87eab-115">*typein*</span><span class="sxs-lookup"><span data-stu-id="87eab-115">*typein*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-116">Der *Datentyp für Datain*.</span><span class="sxs-lookup"><span data-stu-id="87eab-116">The data type for *datain*.</span></span> <span data-ttu-id="87eab-117">Muss eines der folgenden sein: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int oder GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="87eab-117">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="87eab-118">*Datain*</span><span class="sxs-lookup"><span data-stu-id="87eab-118">*datain*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-119">Ein Zeiger auf das Quell Bild.</span><span class="sxs-lookup"><span data-stu-id="87eab-119">A pointer to the source image.</span></span>

</dd> <dt>

<span data-ttu-id="87eab-120">*widthout*</span><span class="sxs-lookup"><span data-stu-id="87eab-120">*widthout*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-121">Die Breite des Ziel Bilds.</span><span class="sxs-lookup"><span data-stu-id="87eab-121">The width of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="87eab-122">*"heightout"*</span><span class="sxs-lookup"><span data-stu-id="87eab-122">*heightout*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-123">Die Höhe des Ziel Bilds.</span><span class="sxs-lookup"><span data-stu-id="87eab-123">The height of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="87eab-124">*meinen*</span><span class="sxs-lookup"><span data-stu-id="87eab-124">*typeout*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-125">Der *Datentyp für dataout*.</span><span class="sxs-lookup"><span data-stu-id="87eab-125">The data type for *dataout*.</span></span> <span data-ttu-id="87eab-126">Muss eines der folgenden sein: GL \_ unsigned \_ Byte, GL \_ Byte, GL \_ Bitmap, GL \_ unsigned \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int oder GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="87eab-126">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="87eab-127">*dataout*</span><span class="sxs-lookup"><span data-stu-id="87eab-127">*dataout*</span></span> 
</dt> <dd>

<span data-ttu-id="87eab-128">Ein Zeiger auf das Ziel Image.</span><span class="sxs-lookup"><span data-stu-id="87eab-128">A pointer to the destination image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87eab-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87eab-129">Return value</span></span>

<span data-ttu-id="87eab-130">Wenn die Funktion erfolgreich ist, ist der Rückgabewert „0“.</span><span class="sxs-lookup"><span data-stu-id="87eab-130">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="87eab-131">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein glu-Fehlercode (siehe [**gluerrorstring**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="87eab-131">If the function fails, the return value is a GLU error code (see [**gluErrorString**](gluerrorstring.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="87eab-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87eab-132">Remarks</span></span>

<span data-ttu-id="87eab-133">Die Funktion " **gluscaleimage** " skaliert ein Pixel Bild mithilfe der entsprechenden Pixel Speicher Modi, um Daten aus dem Quell Abbild zu entpacken und Daten in das Ziel Image zu packen.</span><span class="sxs-lookup"><span data-stu-id="87eab-133">The **gluScaleImage** function scales a pixel image using the appropriate pixel store modes to unpack data from the source image and pack data into the destination image.</span></span>

<span data-ttu-id="87eab-134">Beim Verkleinern eines Bilds verwendet " **gluscaleimage** " einen Feld Filter, um ein Beispiel für das Quell Abbild zu erstellen und Pixel für das Ziel Image zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="87eab-134">When shrinking an image, **gluScaleImage** uses a box filter to sample the source image and create pixels for the destination image.</span></span> <span data-ttu-id="87eab-135">Beim Vergrößern eines Bilds werden die Pixel des Quell Bilds linear interpoliert, um das Ziel Image zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="87eab-135">When magnifying an image, the pixels from the source image are linearly interpolated to create the destination image.</span></span>

<span data-ttu-id="87eab-136">Eine Beschreibung der zulässigen Werte für die Parameter " *Format*", " *typein*" und " *meinen* " finden Sie unter [**glread Pixels**](glreadpixels.md).</span><span class="sxs-lookup"><span data-stu-id="87eab-136">For a description of the acceptable values for the *format*, *typein*, and *typeout* parameters, see [**glReadPixels**](glreadpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87eab-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87eab-137">Requirements</span></span>



| <span data-ttu-id="87eab-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87eab-138">Requirement</span></span> | <span data-ttu-id="87eab-139">Wert</span><span class="sxs-lookup"><span data-stu-id="87eab-139">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87eab-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87eab-140">Minimum supported client</span></span><br/> | <span data-ttu-id="87eab-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87eab-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="87eab-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87eab-142">Minimum supported server</span></span><br/> | <span data-ttu-id="87eab-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87eab-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="87eab-144">Header</span><span class="sxs-lookup"><span data-stu-id="87eab-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="87eab-145"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="87eab-145"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="87eab-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87eab-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="87eab-147"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87eab-147"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="87eab-148">DLL</span><span class="sxs-lookup"><span data-stu-id="87eab-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87eab-149"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87eab-149"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87eab-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87eab-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87eab-151">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="87eab-151">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="87eab-152">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="87eab-152">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="87eab-153">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="87eab-153">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="87eab-154">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="87eab-154">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="87eab-155">**gluerrorstring**</span><span class="sxs-lookup"><span data-stu-id="87eab-155">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> </dl>

 

 





