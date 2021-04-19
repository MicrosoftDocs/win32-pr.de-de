---
title: gltexparameterf-Funktion (GL. h)
description: Legt Textur Parameter fest. | gltexparameterf-Funktion (GL. h)
ms.assetid: 20b9f2d5-66e1-41cd-9571-8caa38ef033d
keywords:
- gltexparameterf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexParameterf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f749513757ee32f6fe468dadbe968b8657a06f3d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366592"
---
# <a name="gltexparameterf-function"></a><span data-ttu-id="ffed6-105">gltexparameterf-Funktion</span><span class="sxs-lookup"><span data-stu-id="ffed6-105">glTexParameterf function</span></span>

<span data-ttu-id="ffed6-106">Legt Textur Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="ffed6-106">Sets texture parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffed6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffed6-107">Syntax</span></span>


```C++
void WINAPI glTexParameterf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="ffed6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffed6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffed6-109">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="ffed6-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="ffed6-110">Die Ziel Textur, die entweder GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D sein muss.</span><span class="sxs-lookup"><span data-stu-id="ffed6-110">The target texture, which must be either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="ffed6-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="ffed6-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="ffed6-112">Der symbolische Name eines einwertigen Textur Parameters.</span><span class="sxs-lookup"><span data-stu-id="ffed6-112">The symbolic name of a single valued texture parameter.</span></span> <span data-ttu-id="ffed6-113">Die folgenden Symbole werden in " *PName*" akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="ffed6-113">The following symbols are accepted in *pname*.</span></span>



| <span data-ttu-id="ffed6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ffed6-114">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="ffed6-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ffed6-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="ffed6-116"><dt>**GL- \_ Textur- \_ Min- \_ Filter**</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-116"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="ffed6-117">Die Textur miniierungsfunktion wird immer dann verwendet, wenn das zu Textende Pixel einem Bereich zugeordnet wird, der größer als ein Textur Element ist.</span><span class="sxs-lookup"><span data-stu-id="ffed6-117">The texture minifying function is used whenever the pixel being textured maps to an area greater than one texture element.</span></span> <span data-ttu-id="ffed6-118">Es gibt sechs definierte minisierungs Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ffed6-118">There are six defined minifying functions.</span></span> <span data-ttu-id="ffed6-119">Zwei von Ihnen verwenden das nächstgelegene oder das nächste vier Textur Element, um den Textur Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ffed6-119">Two of them use the nearest one or nearest four texture elements to compute the texture value.</span></span> <span data-ttu-id="ffed6-120">Die anderen vier verwenden Mipmaps.</span><span class="sxs-lookup"><span data-stu-id="ffed6-120">The other four use mipmaps.</span></span><br/> <span data-ttu-id="ffed6-121">Eine MipMap ist eine geordnete Gruppe von Arrays, die das gleiche Bild bei progressiv niedrigeren Auflösungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="ffed6-121">A mipmap is an ordered set of arrays representing the same image at progressively lower resolutions.</span></span> <span data-ttu-id="ffed6-122">Wenn die Textur Dimensionen 2nx2<sup>m</sup> aufweist, sind Max (n, m) + 1 Mipmaps vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ffed6-122">If the texture has dimensions 2nx2<sup>m</sup> there are max(n, m) + 1 mipmaps.</span></span> <span data-ttu-id="ffed6-123">Die erste MipMap ist die ursprüngliche Textur mit den Dimensionen 2nx2<sup>m</sup>.</span><span class="sxs-lookup"><span data-stu-id="ffed6-123">The first mipmap is the original texture, with dimensions 2nx2<sup>m</sup>.</span></span> <span data-ttu-id="ffed6-124">Jede nachfolgende MipMap weist die Dimensionen 2<sup>k</sup>1X2<sup>l</sup>1 auf, wobei 2<sup>k</sup>x2<sup>l</sup> die Dimensionen der vorherigen MipMap sind, bis entweder k = 0 oder l = 0.</span><span class="sxs-lookup"><span data-stu-id="ffed6-124">Each subsequent mipmap has dimensions 2<sup>k</sup>1x2<sup>l</sup>1 where 2<sup>k</sup>x2<sup>l</sup> are the dimensions of the previous mipmap, until either k = 0 or l = 0.</span></span> <span data-ttu-id="ffed6-125">An diesem Punkt verfügen nachfolgende Mipmaps über die Dimension 1X2<sup>l</sup>1 oder 2<sup>k</sup>1x1 bis zur endgültigen MipMap mit der Dimension 1x1.</span><span class="sxs-lookup"><span data-stu-id="ffed6-125">At that point, subsequent mipmaps have dimension 1x2<sup>l</sup>1 or 2<sup>k</sup>1x1 until the final mipmap, which has dimension 1x1.</span></span> <span data-ttu-id="ffed6-126">Mipmaps werden mithilfe von [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md) mit dem Detail Argument definiert, das die Reihenfolge der Mipmaps angibt.</span><span class="sxs-lookup"><span data-stu-id="ffed6-126">Mipmaps are defined using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md) with the level-of-detail argument indicating the order of the mipmaps.</span></span> <span data-ttu-id="ffed6-127">Ebene 0 ist die ursprüngliche Textur. der Höchstwert für die Fett formatierte Ebene (n, m) ist die abschließende 1x1-MipMap.</span><span class="sxs-lookup"><span data-stu-id="ffed6-127">Level 0 is the original texture; level bold max(n, m) is the final 1x1 mipmap.</span></span><br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="ffed6-128"><dt>**GL- \_ Textur- \_ mag- \_ Filter**</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-128"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="ffed6-129">Die Textur Vergrößerungsfunktion wird verwendet, wenn das zu strukturierte Pixel einem Bereich entspricht, der kleiner oder gleich einem Textur Element ist.</span><span class="sxs-lookup"><span data-stu-id="ffed6-129">The texture magnification function is used when the pixel being textured maps to an area less than or equal to one texture element.</span></span> <span data-ttu-id="ffed6-130">Der Wert für die Textur Vergrößerung wird entweder auf "GL \_ Next" oder "GL linear" festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="ffed6-130">It sets the texture magnification function to either GL\_NEAREST or GL\_LINEAR.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="ffed6-131"><dt>**GL- \_ Textur Umbruch \_ \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-131"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>             | <span data-ttu-id="ffed6-132">Legt den Wrap-Parameter für Texturkoordinaten s auf die GL- \_ Klammer oder die GL- \_ Wiederholung fest.</span><span class="sxs-lookup"><span data-stu-id="ffed6-132">Sets the wrap parameter for texture coordinate s to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="ffed6-133">\_Die GL-Klammer bewirkt, dass die Koordinaten an den Bereich \[ 0, 1 gebunden werden, \] und ist nützlich, um das Umwickeln von Artefakten beim Mapping eines einzelnen Bilds zu einem Objekt zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ffed6-133">GL\_CLAMP causes s coordinates to be clamped to the range \[0,1\] and is useful for preventing wrapping artifacts when mapping a single image onto an object.</span></span> <span data-ttu-id="ffed6-134">GL \_ Repeat bewirkt, dass der ganzzahlige Teil der s-Koordinate ignoriert wird. OpenGL verwendet nur die Bruchteile und erstellt dadurch ein sich wiederholendes Muster.</span><span class="sxs-lookup"><span data-stu-id="ffed6-134">GL\_REPEAT causes the integer part of the s coordinate to be ignored; OpenGL uses only the fractional part, thereby creating a repeating pattern.</span></span> <span data-ttu-id="ffed6-135">Auf Rahmen Textur Elemente wird nur zugegriffen, wenn Wrapping auf GL-Klammer festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="ffed6-135">Border texture elements are accessed only if wrapping is set to GL\_CLAMP.</span></span> <span data-ttu-id="ffed6-136">Zunächst ist GL \_ Texture \_ Wrap \_ S auf GL Repeat festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="ffed6-136">Initially, GL\_TEXTURE\_WRAP\_S is set to GL\_REPEAT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="ffed6-137"><dt>**GL- \_ Textur Umbruch \_ \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-137"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>             | <span data-ttu-id="ffed6-138">Legt den Wrap-Parameter für die Texturkoordinaten t entweder auf die GL- \_ Klammer oder die GL- \_ Wiederholung fest.</span><span class="sxs-lookup"><span data-stu-id="ffed6-138">Sets the wrap parameter for texture coordinate t to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="ffed6-139">Weitere Informationen finden Sie unter GL \_ Texture \_ Wrap \_ S.</span><span class="sxs-lookup"><span data-stu-id="ffed6-139">See the discussion under GL\_TEXTURE\_WRAP\_S.</span></span> <span data-ttu-id="ffed6-140">Anfänglich \_ ist GL Texture \_ Wrap \_ T auf GL Repeat festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="ffed6-140">Initially, GL\_TEXTURE\_WRAP\_T is set to GL\_REPEAT</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="ffed6-141">*param*</span><span class="sxs-lookup"><span data-stu-id="ffed6-141">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="ffed6-142">Der Wert von " *PName*".</span><span class="sxs-lookup"><span data-stu-id="ffed6-142">The value of *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffed6-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffed6-143">Return value</span></span>

<span data-ttu-id="ffed6-144">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ffed6-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ffed6-145">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ffed6-145">Error codes</span></span>

<span data-ttu-id="ffed6-146">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ffed6-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ffed6-147">Name</span><span class="sxs-lookup"><span data-stu-id="ffed6-147">Name</span></span>                                                                                                  | <span data-ttu-id="ffed6-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ffed6-148">Meaning</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ffed6-149"><dt>**GL \_ . Ungültige \_** Aufzählung.</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-149"><dt>**GL\_INVALID\_ENUM** </dt></span></span> </dl>     | <span data-ttu-id="ffed6-150">*target* oder *PName* war keiner der zulässigen Werte oder, wenn *param* einen definierten Konstanten Wert aufweisen sollte (basierend auf dem Wert von *PName*) und nicht.</span><span class="sxs-lookup"><span data-stu-id="ffed6-150">*target* or *pname* was not one of the accepted defined values, or when *param* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="ffed6-151"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ffed6-152">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ffed6-152">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="ffed6-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffed6-153">Remarks</span></span>

<span data-ttu-id="ffed6-154">Die Textur Zuordnung ist eine Technik, die ein Bild auf die Oberfläche eines Objekts anwendet, als ob es sich bei dem Bild um eine Debug-oder Cellophane-Verkleinerung handelt.</span><span class="sxs-lookup"><span data-stu-id="ffed6-154">Texture mapping is a technique that applies an image onto an object's surface as if the image were a decal or cellophane shrink-wrap.</span></span> <span data-ttu-id="ffed6-155">Das Bild wird im Textur Raum mit einem-Koordinatensystem (*s*, *t*) erstellt.</span><span class="sxs-lookup"><span data-stu-id="ffed6-155">The image is created in texture space, with an (*s*, *t*) coordinate system.</span></span> <span data-ttu-id="ffed6-156">Eine Textur ist ein ein-oder zweidimensionales Bild und eine Reihe von Parametern, die bestimmen, wie Beispiele vom Bild abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ffed6-156">A texture is a one- or two-dimensional image and a set of parameters that determine how samples are derived from the image.</span></span>

<span data-ttu-id="ffed6-157">Die Funktion " **gltexparameter** " weist den Wert oder die Werte in den Parametern dem als "pname" angegebenen Textur Parameter zu.</span><span class="sxs-lookup"><span data-stu-id="ffed6-157">The **glTexParameter** function assigns the value or values in params to the texture parameter specified as pname.</span></span> <span data-ttu-id="ffed6-158">Der Zielparameter definiert die Ziel Textur, entweder GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="ffed6-158">The target parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="ffed6-159">Wenn bei der Minimierung mehr Textur Elemente als Stichprobe genommen werden, werden weniger Aliasing-Artefakte offensichtlich.</span><span class="sxs-lookup"><span data-stu-id="ffed6-159">As more texture elements are sampled in the minification process, fewer aliasing artifacts will be apparent.</span></span> <span data-ttu-id="ffed6-160">Obwohl die \_ Funktionen von "adnext" und "GL \_ linear Minimierung" schneller als die anderen vier sind, werden nur ein oder vier Textur Elemente als Stichprobe für den Textur Wert des gerenderten Pixels festgelegt, und es können Muster oder unregelmäßige Übergänge erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="ffed6-160">While the GL\_NEAREST and GL\_LINEAR minification functions can be faster than the other four, they sample only one or four texture elements to determine the texture value of the pixel being rendered and can produce moire patterns or ragged transitions.</span></span> <span data-ttu-id="ffed6-161">Der Standardwert des GL- \_ Textur \_ Min- \_ Filters ist GL \_ nächstgelegene \_ MipMap \_ linear.</span><span class="sxs-lookup"><span data-stu-id="ffed6-161">The default value of GL\_TEXTURE\_MIN\_FILTER is GL\_NEAREST\_MIPMAP\_LINEAR.</span></span>

<span data-ttu-id="ffed6-162">Angenommen, die Texturierung ist aktiviert (durch Aufrufen von [**glEnable**](glenable.md) mit dem Argument GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D), und der GL- \_ Textur \_ Min- \_ Filter wird auf eine der Funktionen festgelegt, für die eine MipMap erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ffed6-162">Suppose that texturing is enabled (by calling [**glEnable**](glenable.md) with argument GL\_TEXTURE\_1D or GL\_TEXTURE\_2D) and GL\_TEXTURE\_MIN\_FILTER is set to one of the functions that requires a mipmap.</span></span> <span data-ttu-id="ffed6-163">Wenn entweder die Dimensionen der derzeit definierten Textur Bilder (mit vorherigen Aufrufen von [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md)) nicht der richtigen Reihenfolge für Mipmaps entsprechen oder weniger Textur Bilder definiert sind, als erforderlich sind, oder wenn der Satz von Textur Bildern eine abweichende Anzahl von texturkomponenten hat, ist dies so, als ob die Textur Zuordnung deaktiviert wäre.</span><span class="sxs-lookup"><span data-stu-id="ffed6-163">If either the dimensions of the texture images currently defined (with previous calls to [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md)) do not follow the proper sequence for mipmaps, or there are fewer texture images defined than are needed, or the set of texture images have differing numbers of texture components, then it is as if texture mapping were disabled.</span></span> <span data-ttu-id="ffed6-164">Die lineare Filterung greift auf die vier nächsten Textur Elemente nur in 2D-Texturen zu.</span><span class="sxs-lookup"><span data-stu-id="ffed6-164">Linear filtering accesses the four nearest texture elements only in 2-D textures.</span></span> <span data-ttu-id="ffed6-165">Bei 1-D-Texturen greift die lineare Filterung auf die beiden nächsten Textur Elemente zu.</span><span class="sxs-lookup"><span data-stu-id="ffed6-165">In 1-D textures, linear filtering accesses the two nearest texture elements.</span></span> <span data-ttu-id="ffed6-166">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexparameterf**, **gltexparameteri**, **gltexparameterfv** und **gltexparameteriv** ab.</span><span class="sxs-lookup"><span data-stu-id="ffed6-166">The following function retrieves information related to **glTexParameterf**, **glTexParameteri**, **glTexParameterfv**, and **glTexParameteriv**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffed6-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffed6-167">Requirements</span></span>



| <span data-ttu-id="ffed6-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffed6-168">Requirement</span></span> | <span data-ttu-id="ffed6-169">Wert</span><span class="sxs-lookup"><span data-stu-id="ffed6-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffed6-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffed6-170">Minimum supported client</span></span><br/> | <span data-ttu-id="ffed6-171">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffed6-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ffed6-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffed6-172">Minimum supported server</span></span><br/> | <span data-ttu-id="ffed6-173">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffed6-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ffed6-174">Header</span><span class="sxs-lookup"><span data-stu-id="ffed6-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffed6-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ffed6-176">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ffed6-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="ffed6-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ffed6-178">DLL</span><span class="sxs-lookup"><span data-stu-id="ffed6-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffed6-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffed6-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffed6-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffed6-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffed6-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ffed6-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ffed6-182">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="ffed6-182">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="ffed6-183">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="ffed6-183">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="ffed6-184">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ffed6-184">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ffed6-185">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ffed6-185">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ffed6-186">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="ffed6-186">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="ffed6-187">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="ffed6-187">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="ffed6-188">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ffed6-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ffed6-189">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="ffed6-189">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="ffed6-190">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="ffed6-190">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="ffed6-191">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="ffed6-191">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="ffed6-192">**glpriorizetexturen**</span><span class="sxs-lookup"><span data-stu-id="ffed6-192">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="ffed6-193">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="ffed6-193">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="ffed6-194">**gltexgen**</span><span class="sxs-lookup"><span data-stu-id="ffed6-194">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="ffed6-195">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ffed6-195">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ffed6-196">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ffed6-196">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ffed6-197">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="ffed6-197">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="ffed6-198">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="ffed6-198">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





