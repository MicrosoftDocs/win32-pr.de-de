---
title: glgetcolortableparameterivext-Funktion (GL. h)
description: Die Funktionen "glgetcolortableparameterfvext" und "glgetcolortableparameterivext" erhalten palettenparameter aus Farbtabellen. | glgetcolortableparameterivext-Funktion (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- glgetcolortableparameterivext-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351897"
---
# <a name="glgetcolortableparameterivext-function"></a><span data-ttu-id="c7fa3-105">glgetcolortableparameterivext-Funktion</span><span class="sxs-lookup"><span data-stu-id="c7fa3-105">glGetColorTableParameterivEXT function</span></span>

<span data-ttu-id="c7fa3-106">Die Funktionen " [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) " und " **glgetcolortableparameterivext** " erhalten palettenparameter aus Farbtabellen.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-106">The [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) and **glGetColorTableParameterivEXT** functions get palette parameters from color tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fa3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7fa3-107">Syntax</span></span>


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="c7fa3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7fa3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7fa3-109">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="c7fa3-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c7fa3-110">Die Ziel Textur der Palette, für die Sie Parameterdaten benötigen.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-110">The target texture of the palette for which you want parameter data.</span></span> <span data-ttu-id="c7fa3-111">Muss Textur \_ 1D, Textur \_ 2D, Proxy \_ Textur \_ 1D oder Proxy \_ Textur \_ 2D sein.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-111">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="c7fa3-112">*pName*</span><span class="sxs-lookup"><span data-stu-id="c7fa3-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c7fa3-113">Eine symbolische Konstante für den Typ der palettenparameterdaten, auf die von *para* Metern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-113">A symbolic constant for the type of palette parameter data pointed to by *params*.</span></span>

<span data-ttu-id="c7fa3-114">Im folgenden finden Sie die akzeptierten symbolischen Konstanten und ihre Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-114">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="c7fa3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c7fa3-115">Value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="c7fa3-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c7fa3-116">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <span data-ttu-id="c7fa3-117"><dt>**GL- \_ Farb \_ Tabellen Format ( \_ \_ ext)**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa3-117"><dt>**GL\_COLOR\_TABLE\_FORMAT\_EXT**</dt></span></span> </dl>              | <span data-ttu-id="c7fa3-118">Gibt das interne Format zurück, das durch den letzten Aufrufe von [**glcolortableext**](glcolortableext.md) oder den Standardwert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-118">Return the internal format specified by the most recent call to [**glColorTableEXT**](glcolortableext.md) or the default value.</span></span><br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <span data-ttu-id="c7fa3-119"><dt>**GL- \_ Farb \_ Tabellenbreite ( \_ \_ ext)**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa3-119"><dt>**GL\_COLOR\_TABLE\_WIDTH\_EXT**</dt></span></span> </dl>                 | <span data-ttu-id="c7fa3-120">Gibt die Breite der aktuellen Palette zurück.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-120">Return the width of the current palette.</span></span><br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <span data-ttu-id="c7fa3-121"><dt>**GL \_ Color \_ Table \_ Red \_ size \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa3-121"><dt>**GL\_COLOR\_TABLE\_RED\_SIZE\_EXT**</dt></span></span> </dl>       | <span data-ttu-id="c7fa3-122">Gibt die tatsächliche Größe zurück, die intern verwendet wird, um die rote Komponente der Palettendaten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-122">Return the actual size used internally to store the red component of the palette data.</span></span><br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <span data-ttu-id="c7fa3-123"><dt>**GL \_ Color \_ Table \_ Green \_ size \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa3-123"><dt>**GL\_COLOR\_TABLE\_GREEN\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="c7fa3-124">Gibt die tatsächliche Größe zurück, die zum Speichern der grünen Komponente der Palettendaten intern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-124">Return the actual size used internally to store the green component of the palette data.</span></span><br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <span data-ttu-id="c7fa3-125"><dt>**GL \_ Color \_ Table \_ Blue \_ size \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa3-125"><dt>**GL\_COLOR\_TABLE\_BLUE\_SIZE\_EXT**</dt></span></span> </dl>    | <span data-ttu-id="c7fa3-126">Gibt die tatsächliche Größe zurück, die intern verwendet wird, um die blaue Komponente der Palettendaten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-126">Return the actual size used internally to store the blue component of the palette data.</span></span><br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <span data-ttu-id="c7fa3-127"><dt>**GL \_ Color \_ Table \_ alpha \_ size \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa3-127"><dt>**GL\_COLOR\_TABLE\_ALPHA\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="c7fa3-128">Gibt die tatsächliche Größe zurück, die zum Speichern der Alpha Komponente der Palettendaten intern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-128">Return the actual size used internally to store the alpha component of the palette data.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="c7fa3-129">*params*</span><span class="sxs-lookup"><span data-stu-id="c7fa3-129">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="c7fa3-130">Verweist auf die farbtabellenparameterdaten, die durch den *PName* -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-130">Points to the color table parameter data specified by the *pname* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7fa3-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7fa3-131">Return value</span></span>

<span data-ttu-id="c7fa3-132">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-132">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7fa3-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7fa3-133">Remarks</span></span>

<span data-ttu-id="c7fa3-134">Verwenden Sie die Funktionen " **glgetcolortableparameterivext** " und " [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) ", um bestimmte Parameterdaten aus Farbtabellen abzurufen, die mit " [**glcolortableext**](glcolortableext.md) " für gezielte Textur Paletten festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-134">You use the **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions to retrieve specific parameter data from color tables set with [**glColorTableEXT**](glcolortableext.md) for targeted texture palettes.</span></span> <span data-ttu-id="c7fa3-135">Außerdem können Sie diese Funktionen verwenden, um die Anzahl der Farb Tabelleneinträge zu bestimmen, die von **glgetcolortableext** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-135">Also you can use these functions to determine the number of color table entries that **glGetColorTableEXT** returns.</span></span>

<span data-ttu-id="c7fa3-136">Wenn der *Ziel* Parameter GL- \_ Proxy \_ Textur \_ 1D oder GL \_ \_ -Proxy Textur \_ 2D ist, und die-Implementierung die für *Format* oder *Width* angegebenen Werte nicht unter  stützt, kann bei der Erstellung der angeforderten Farbtabelle ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-136">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="c7fa3-137">In diesem Fall ist die Farbtabelle leer, und alle abgerufenen Parameter haben den Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c7fa3-137">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="c7fa3-138">Sie können bestimmen, ob OpenGL ein bestimmtes Farbtabellen Format und eine bestimmte Größe unterstützt, indem Sie **glcolortableext** mit einem Proxy Ziel aufrufen und dann **glgetcolortableparameterivext** oder [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) aufrufen, um zu bestimmen, ob der Width-Parameter mit dem von **glcolortableext** festgelegten width-Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-138">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling **glGetColorTableParameterivEXT** or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="c7fa3-139">Wenn die abgerufene Breite 0 (null) ist, ist die Farbtabellen Anforderung von **glcolortable** fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-139">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="c7fa3-140">Wenn die abgerufene Breite nicht NULL ist, können Sie **glcolortable** mit dem echten Ziel mit Textur \_ 1D oder Textur \_ 2D zum Festlegen der Farbtabelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-140">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

<span data-ttu-id="c7fa3-141">Die Funktionen " **glgetcolortableparameterivext** " und " [**glgetcolortableparameterfvext**](glgetcolortableparameterfvext.md) " sind Erweiterungsfunktionen, die nicht Teil der OpenGL-Standardbibliothek sind, aber Teil der Erweiterung "GL \_ Ext- \_ \_ Textur Erweiterung" sind.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-141">The **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions are extension functions that are not part of the standard OpenGL library but are part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="c7fa3-142">Um zu überprüfen, ob die Implementierung von OpenGL **glgetcolortableparameterivext** und **glgetcolortableparameterfvext** unterstützt, nennen Sie [**glgetstring**](glgetstring.md)**(** GL \_ Extensions **)**.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-142">To check whether your implementation of OpenGL supports **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT**, call [**glGetString**](glgetstring.md)**(** GL\_EXTENSIONS **)**.</span></span> <span data-ttu-id="c7fa3-143">Wenn Sie \_ die Struktur von GL Ext \_ -Struktur zurückgibt \_ , werden **glgetcolortableparameterivext** und **glgetcolortableparameterfvext** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-143">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** are supported.</span></span> <span data-ttu-id="c7fa3-144">Rufen Sie zum Abrufen der Funktions Adresse einer Erweiterungs Funktion [**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)auf.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-144">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fa3-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7fa3-145">Requirements</span></span>



| <span data-ttu-id="c7fa3-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7fa3-146">Requirement</span></span> | <span data-ttu-id="c7fa3-147">Wert</span><span class="sxs-lookup"><span data-stu-id="c7fa3-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c7fa3-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7fa3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fa3-149">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7fa3-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="c7fa3-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7fa3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fa3-151">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7fa3-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c7fa3-152">Header</span><span class="sxs-lookup"><span data-stu-id="c7fa3-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7fa3-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa3-153"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fa3-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7fa3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fa3-155">**glcolorsubtableext**</span><span class="sxs-lookup"><span data-stu-id="c7fa3-155">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="c7fa3-156">**glcolortableext**</span><span class="sxs-lookup"><span data-stu-id="c7fa3-156">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="c7fa3-157">**glgetcolortableext**</span><span class="sxs-lookup"><span data-stu-id="c7fa3-157">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="c7fa3-158">**glgetcolortableparameterfvext**</span><span class="sxs-lookup"><span data-stu-id="c7fa3-158">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="c7fa3-159">**wglgetprocaddress**</span><span class="sxs-lookup"><span data-stu-id="c7fa3-159">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





