---
title: glaccum-Funktion (GL. h)
description: Die Funktion "glaccum" wird auf den Akkumulations Puffer angewendet.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glaccum-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741945"
---
# <a name="glaccum-function"></a><span data-ttu-id="92bed-104">glaccum-Funktion</span><span class="sxs-lookup"><span data-stu-id="92bed-104">glAccum function</span></span>

<span data-ttu-id="92bed-105">Die Funktion " **glaccum** " wird auf den Akkumulations Puffer angewendet.</span><span class="sxs-lookup"><span data-stu-id="92bed-105">The **glAccum** function operates on the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="92bed-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="92bed-106">Syntax</span></span>


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a><span data-ttu-id="92bed-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="92bed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92bed-108">*schel*</span><span class="sxs-lookup"><span data-stu-id="92bed-108">*op*</span></span> 
</dt> <dd>

<span data-ttu-id="92bed-109">Der Akkumulations Puffer Vorgang.</span><span class="sxs-lookup"><span data-stu-id="92bed-109">The accumulation buffer operation.</span></span> <span data-ttu-id="92bed-110">Die akzeptierten symbolischen Konstanten lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="92bed-110">The accepted symbolic constants are as follows.</span></span>



| <span data-ttu-id="92bed-111">Wert</span><span class="sxs-lookup"><span data-stu-id="92bed-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="92bed-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="92bed-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <span data-ttu-id="92bed-113"><dt>**GL- \_ Accum**</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-113"><dt>**GL\_ACCUM**</dt></span></span> </dl>    | <span data-ttu-id="92bed-114">Ruft R, G, B und einen Wert aus dem Puffer ab, der derzeit zum Lesen ausgewählt ist (siehe [**glreadbuffer**](glreadbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="92bed-114">Obtains R, G, B, and A values from the buffer currently selected for reading (see [**glReadBuffer**](glreadbuffer.md)).</span></span> <span data-ttu-id="92bed-115">Jeder Komponenten Wert wird durch 2 *n*  1 dividiert, wobei *n* die Anzahl der Bits ist, die jeder Farbkomponente im aktuell ausgewählten Puffer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92bed-115">Each component value is divided by 2 *n*  1, where *n* is the number of bits allocated to each color component in the currently selected buffer.</span></span> <span data-ttu-id="92bed-116">Das Ergebnis ist ein Gleit Komma Wert im Bereich \[ von 0, 1 \] , der mit einem *Wert* multipliziert und der entsprechenden Pixel Komponente im Akkumulations Puffer hinzugefügt wird, wodurch der Akkumulations Puffer aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="92bed-116">The result is a floating-point value in the range \[0,1\], which is multiplied by *value* and added to the corresponding pixel component in the accumulation buffer, thereby updating the accumulation buffer.</span></span><br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <span data-ttu-id="92bed-117"><dt>**GL \_ Laden**</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-117"><dt>**GL\_LOAD**</dt></span></span> </dl>       | <span data-ttu-id="92bed-118">Ähnelt dem GL- \_ Accum, mit der Ausnahme, dass der aktuelle Wert im Akkumulations Puffer nicht in der Berechnung des neuen Werts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92bed-118">Similar to GL\_ACCUM, except that the current value in the accumulation buffer is not used in the calculation of the new value.</span></span> <span data-ttu-id="92bed-119">Das heißt, die R-, G-, B-und A-Werte aus dem aktuell ausgewählten Puffer werden durch 2 *n*  1 dividiert, multipliziert mit *Wert* und werden dann in der entsprechenden Akkumulations Puffer Zelle gespeichert und überschreiben den aktuellen Wert.</span><span class="sxs-lookup"><span data-stu-id="92bed-119">That is, the R, G, B, and A values from the currently selected buffer are divided by 2 *n*  1, multiplied by *value*, and then stored in the corresponding accumulation buffer cell, overwriting the current value.</span></span><br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <span data-ttu-id="92bed-120"><dt>**GL \_ Hinzufügen**</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-120"><dt>**GL\_ADD**</dt></span></span> </dl>          | <span data-ttu-id="92bed-121">Fügt jedem R-, G-, B-und a-Wert im Akkumulations Puffer einen *Wert* hinzu.</span><span class="sxs-lookup"><span data-stu-id="92bed-121">Adds *value* to each R, G, B, and A in the accumulation buffer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <span data-ttu-id="92bed-122"><dt>**GL \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-122"><dt>**GL\_MULT**</dt></span></span> </dl>       | <span data-ttu-id="92bed-123">Multipliziert alle R-, G-, B-und a-Werte im Akkumulations Puffer nach *Wert* und gibt die skalierte Komponente an den entsprechenden akkumulationpufferort zurück.</span><span class="sxs-lookup"><span data-stu-id="92bed-123">Multiplies each R, G, B, and A in the accumulation buffer by *value* and returns the scaled component to its corresponding accumulation buffer location.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <span data-ttu-id="92bed-124"><dt>**GL- \_ Rückgabe**</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-124"><dt>**GL\_RETURN**</dt></span></span> </dl> | <span data-ttu-id="92bed-125">Überträgt akkumulationspufferwerte an den Farb Puffer oder die Puffer, die zurzeit zum Schreiben ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="92bed-125">Transfers accumulation buffer values to the color buffer or buffers currently selected for writing.</span></span> <span data-ttu-id="92bed-126">Jede R-, G-, B-und eine-Komponente wird mit einem *Wert* multipliziert und dann mit 2 *n*  1 multipliziert, an den Bereich \[ 0, 2 *n*  1 gebunden \] und in der entsprechenden Anzeige Puffer Zelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="92bed-126">Each R, G, B, and A component is multiplied by *value*, then multiplied by 2 *n*  1, clamped to the range \[0, 2 *n*  1 \], and stored in the corresponding display buffer cell.</span></span> <span data-ttu-id="92bed-127">Die einzigen fragmentvorgänge, die auf diese Übertragung angewendet werden, sind Pixel Besitz, Scissor, Dithering und Color Write.</span><span class="sxs-lookup"><span data-stu-id="92bed-127">The only fragment operations that are applied to this transfer are pixel ownership, scissor, dithering, and color writemasks.</span></span><br/>                                                                        |



 

</dd> <dt>

<span data-ttu-id="92bed-128">*value*</span><span class="sxs-lookup"><span data-stu-id="92bed-128">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="92bed-129">Ein Gleit Komma Wert, der beim Akkumulations Puffer Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92bed-129">A floating-point value used in the accumulation buffer operation.</span></span> <span data-ttu-id="92bed-130">Der *op* -Parameter bestimmt, wie der *Wert* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92bed-130">The *op* parameter determines how *value* is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92bed-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92bed-131">Return value</span></span>

<span data-ttu-id="92bed-132">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="92bed-132">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="92bed-133">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="92bed-133">Error codes</span></span>

<span data-ttu-id="92bed-134">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92bed-134">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="92bed-135">Name</span><span class="sxs-lookup"><span data-stu-id="92bed-135">Name</span></span>                                                                                                  | <span data-ttu-id="92bed-136">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="92bed-136">Meaning</span></span>                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92bed-137"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-137"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="92bed-138">" *op* " war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="92bed-138">*op* was not an accepted value.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="92bed-139"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="92bed-140">Es war kein Akkumulations Puffer vorhanden, oder die Funktion " **glaccum** " wurde zwischen einem Aufruf von " [**glBegin**](glbegin.md) " und dem entsprechenden Aufruf von " [**glEnd**](glend.md)" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="92bed-140">There was no accumulation buffer or the function **glAccum** was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="92bed-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92bed-141">Remarks</span></span>

<span data-ttu-id="92bed-142">Der Akkumulations Puffer ist ein Farb Puffer mit erweitertem Bereich.</span><span class="sxs-lookup"><span data-stu-id="92bed-142">The accumulation buffer is an extended-range color buffer.</span></span> <span data-ttu-id="92bed-143">Bilder werden nicht in Sie gerendert.</span><span class="sxs-lookup"><span data-stu-id="92bed-143">Images are not rendered into it.</span></span> <span data-ttu-id="92bed-144">Stattdessen werden dem Inhalt des Akkumulations Puffers nach dem Rendering Bilder hinzugefügt, die in einem der Farb Puffer gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="92bed-144">Rather, images rendered into one of the color buffers are added to the contents of the accumulation buffer after rendering.</span></span> <span data-ttu-id="92bed-145">Sie können Effekte wie Antialiasing (von Punkten, Linien und Polygone), Bewegungsunschärfe und Tiefe des Felds erstellen, indem Sie mit unterschiedlichen Transformations Matrizen generierte Bilder sammeln.</span><span class="sxs-lookup"><span data-stu-id="92bed-145">You can create effects such as antialiasing (of points, lines, and polygons), motion blur, and depth of field by accumulating images generated with different transformation matrices.</span></span>

<span data-ttu-id="92bed-146">Jedes Pixel im Akkumulations Puffer besteht aus roten, grünen, blauen und Alpha Werten.</span><span class="sxs-lookup"><span data-stu-id="92bed-146">Each pixel in the accumulation buffer consists of red, green, blue, and alpha values.</span></span> <span data-ttu-id="92bed-147">Die Anzahl der Bits pro Komponente im Akkumulations Puffer hängt von der Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="92bed-147">The number of bits per component in the accumulation buffer depends on the implementation.</span></span> <span data-ttu-id="92bed-148">Sie können diese Zahl überprüfen, indem Sie [**glgetintegerv**](glgetintegerv.md) viermal aufrufen, mit den Argumenten GL \_ Accum \_ Red \_ Bits, GL \_ Accum \_ Green \_ Bits, GL \_ Accum \_ Blue \_ Bits und GL \_ Accum \_ alpha \_ Bits bzw.</span><span class="sxs-lookup"><span data-stu-id="92bed-148">You can examine this number by calling [**glGetIntegerv**](glgetintegerv.md) four times, with the arguments GL\_ACCUM\_RED\_BITS, GL\_ACCUM\_GREEN\_BITS, GL\_ACCUM\_BLUE\_BITS, and GL\_ACCUM\_ALPHA\_BITS, respectively.</span></span> <span data-ttu-id="92bed-149">Unabhängig von der Anzahl der Bits pro Komponente beträgt der von jeder Komponente gespeicherte Wertebereich \[ 1,? 1 \] .</span><span class="sxs-lookup"><span data-stu-id="92bed-149">Regardless of the number of bits per component, however, the range of values stored by each component is \[ 1,?1\].</span></span> <span data-ttu-id="92bed-150">Die Akkumulations Puffer Pixel werden mit Frame Puffer Pixel eins-zu-eins zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="92bed-150">The accumulation buffer pixels are mapped one-to-one with framebuffer pixels.</span></span>

<span data-ttu-id="92bed-151">Die Funktion " **glaccum** " wird auf den Akkumulations Puffer angewendet.</span><span class="sxs-lookup"><span data-stu-id="92bed-151">The **glAccum** function operates on the accumulation buffer.</span></span> <span data-ttu-id="92bed-152">Das erste Argument ( *op*) ist eine symbolische Konstante, die einen Akkumulations Puffer Vorgang auswählt.</span><span class="sxs-lookup"><span data-stu-id="92bed-152">The first argument, *op*, is a symbolic constant that selects an accumulation buffer operation.</span></span> <span data-ttu-id="92bed-153">Das zweite Argument, *value*, ist ein Gleit Komma Wert, der in diesem Vorgang verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="92bed-153">The second argument, *value*, is a floating-point value to be used in that operation.</span></span> <span data-ttu-id="92bed-154">Es werden fünf Vorgänge angegeben: GL \_ Accum, GL \_ Load, GL \_ Add, GL \_ mult und GL \_ Return.</span><span class="sxs-lookup"><span data-stu-id="92bed-154">Five operations are specified: GL\_ACCUM, GL\_LOAD, GL\_ADD, GL\_MULT, and GL\_RETURN.</span></span>

<span data-ttu-id="92bed-155">Alle Akkumulations Puffer Vorgänge sind auf den Bereich des aktuellen Scheren Felds beschränkt und werden identisch mit den Komponenten rot, grün, blau und Alpha der einzelnen Pixel angewendet.</span><span class="sxs-lookup"><span data-stu-id="92bed-155">All accumulation buffer operations are limited to the area of the current scissor box and are applied identically to the red, green, blue, and alpha components of each pixel.</span></span> <span data-ttu-id="92bed-156">Der Inhalt einer Metadatenkomponente des Akkumulations Puffers ist nicht definiert, wenn der **glaccum** -Vorgang einen Wert außerhalb des Bereichs \[ 1, 1 ergibt \] .</span><span class="sxs-lookup"><span data-stu-id="92bed-156">The contents of an accumulation buffer pixel component are undefined if the **glAccum** operation results in a value outside the range \[ 1,1\].</span></span>

<span data-ttu-id="92bed-157">Verwenden Sie zum Löschen des Akkumulations Puffers die Funktion " [**glclearaccum**](glclearaccum.md) ", um die Werte für R, G, B und a festzulegen, und geben Sie eine [**glClear**](glclear.md) -Funktion mit aktiviertem Akkumulations Puffer aus.</span><span class="sxs-lookup"><span data-stu-id="92bed-157">To clear the accumulation buffer, use the [**glClearAccum**](glclearaccum.md) function to specify R, G, B, and A values to set it to, and issue a [**glClear**](glclear.md) function with the accumulation buffer enabled.</span></span>

<span data-ttu-id="92bed-158">Nur die Pixel innerhalb des aktuellen Scheren Felds werden von einem beliebigen **glaccum** -Vorgang aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="92bed-158">Only those pixels within the current scissor box are updated by any **glAccum** operation.</span></span>

<span data-ttu-id="92bed-159">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glaccum** " ab:</span><span class="sxs-lookup"><span data-stu-id="92bed-159">The following functions retrieve information related to the **glAccum** function:</span></span>

<span data-ttu-id="92bed-160">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Accum- \_ roten \_ Bits</span><span class="sxs-lookup"><span data-stu-id="92bed-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_RED\_BITS</span></span>

<span data-ttu-id="92bed-161">**glget** mit Argument GL- \_ Accum- \_ grünen \_ Bits</span><span class="sxs-lookup"><span data-stu-id="92bed-161">**glGet** with argument GL\_ACCUM\_GREEN\_BITS</span></span>

<span data-ttu-id="92bed-162">**glget** mit dem Argument GL \_ Accum \_ Blue \_ Bits</span><span class="sxs-lookup"><span data-stu-id="92bed-162">**glGet** with argument GL\_ACCUM\_BLUE\_BITS</span></span>

<span data-ttu-id="92bed-163">**glget** mit dem Argument GL \_ Accum \_ alpha \_ Bits</span><span class="sxs-lookup"><span data-stu-id="92bed-163">**glGet** with argument GL\_ACCUM\_ALPHA\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="92bed-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92bed-164">Requirements</span></span>



| <span data-ttu-id="92bed-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92bed-165">Requirement</span></span> | <span data-ttu-id="92bed-166">Wert</span><span class="sxs-lookup"><span data-stu-id="92bed-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92bed-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92bed-167">Minimum supported client</span></span><br/> | <span data-ttu-id="92bed-168">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92bed-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="92bed-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92bed-169">Minimum supported server</span></span><br/> | <span data-ttu-id="92bed-170">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92bed-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="92bed-171">Header</span><span class="sxs-lookup"><span data-stu-id="92bed-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="92bed-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="92bed-173">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="92bed-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="92bed-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="92bed-175">DLL</span><span class="sxs-lookup"><span data-stu-id="92bed-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92bed-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92bed-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92bed-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92bed-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92bed-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="92bed-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="92bed-179">**glblendfunc**</span><span class="sxs-lookup"><span data-stu-id="92bed-179">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="92bed-180">**glClear**</span><span class="sxs-lookup"><span data-stu-id="92bed-180">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="92bed-181">**glclearaccum**</span><span class="sxs-lookup"><span data-stu-id="92bed-181">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="92bed-182">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="92bed-182">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="92bed-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="92bed-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="92bed-184">**glget**</span><span class="sxs-lookup"><span data-stu-id="92bed-184">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="92bed-185">**gllogicop**</span><span class="sxs-lookup"><span data-stu-id="92bed-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="92bed-186">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="92bed-186">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="92bed-187">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="92bed-187">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="92bed-188">**glread Buffer**</span><span class="sxs-lookup"><span data-stu-id="92bed-188">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="92bed-189">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="92bed-189">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="92bed-190">**glscissor**</span><span class="sxs-lookup"><span data-stu-id="92bed-190">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="92bed-191">**glstencilop**</span><span class="sxs-lookup"><span data-stu-id="92bed-191">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





