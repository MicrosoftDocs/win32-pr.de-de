---
title: glfeedbackbuffer-Funktion (GL. h)
description: Die Funktion "glfeedbackbuffer" steuert den Feedback Modus.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glfeedbackbuffer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343452"
---
# <a name="glfeedbackbuffer-function"></a><span data-ttu-id="b0f82-104">glfeedbackbuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="b0f82-104">glFeedbackBuffer function</span></span>

<span data-ttu-id="b0f82-105">Die Funktion " **glfeedbackbuffer** " steuert den Feedback Modus.</span><span class="sxs-lookup"><span data-stu-id="b0f82-105">The **glFeedbackBuffer** function controls feedback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f82-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0f82-106">Syntax</span></span>


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="b0f82-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0f82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f82-108">*size*</span><span class="sxs-lookup"><span data-stu-id="b0f82-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f82-109">Die maximale Anzahl von Werten, die in den *Puffer* geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="b0f82-109">The maximum number of values that can be written into *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="b0f82-110">*type*</span><span class="sxs-lookup"><span data-stu-id="b0f82-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f82-111">Eine symbolische Konstante, die die Informationen beschreibt, die für jeden Scheitelpunkt zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-111">A symbolic constant that describes the information that will be returned for each vertex.</span></span> <span data-ttu-id="b0f82-112">Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ Color, GL \_ 3D \_ Color \_ Texture und GL \_ 4D \_ Color \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="b0f82-112">The following symbolic constants are accepted: GL\_2D, GL\_3D, GL\_3D\_COLOR, GL\_3D\_COLOR\_TEXTURE, and GL\_4D\_COLOR\_TEXTURE.</span></span>

</dd> <dt>

<span data-ttu-id="b0f82-113">*ert*</span><span class="sxs-lookup"><span data-stu-id="b0f82-113">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f82-114">Gibt die Feedback Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="b0f82-114">Returns the feedback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f82-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0f82-115">Return value</span></span>

<span data-ttu-id="b0f82-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0f82-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0f82-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b0f82-117">Error codes</span></span>

<span data-ttu-id="b0f82-118">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b0f82-119">Name</span><span class="sxs-lookup"><span data-stu-id="b0f82-119">Name</span></span>                                                                                                  | <span data-ttu-id="b0f82-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b0f82-120">Meaning</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0f82-121"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0f82-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b0f82-122">der *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="b0f82-122">*type* was not an accepted value.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="b0f82-123"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0f82-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b0f82-124">die *Größe* war negativ.</span><span class="sxs-lookup"><span data-stu-id="b0f82-124">*size* was negative.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="b0f82-125"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b0f82-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b0f82-126">**glfeedbackbuffer** wurde aufgerufen, während der \_ Rendermodus "GL Feedback" war, oder " [**glrendermode**](glrendermode.md) " wurde mit dem Argument "GL Feedback" aufgerufen, \_ bevor " **glfeedbackbuffer** " mindestens einmal aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b0f82-126">**glFeedbackBuffer** was called while the render mode was GL\_FEEDBACK, or [**glRenderMode**](glrendermode.md) was called with argument GL\_FEEDBACK before **glFeedbackBuffer** was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="b0f82-127"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b0f82-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b0f82-128">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b0f82-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                  |



## <a name="remarks"></a><span data-ttu-id="b0f82-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0f82-129">Remarks</span></span>

<span data-ttu-id="b0f82-130">Die Funktion " **glfeedbackbuffer** " steuert das Feedback.</span><span class="sxs-lookup"><span data-stu-id="b0f82-130">The **glFeedbackBuffer** function controls feedback.</span></span> <span data-ttu-id="b0f82-131">Feedback, wie z. b. Auswahl, ist ein OpenGL-Modus.</span><span class="sxs-lookup"><span data-stu-id="b0f82-131">Feedback, like selection, is an OpenGL mode.</span></span> <span data-ttu-id="b0f82-132">Der Modus wird durch Aufrufen von [**glrendermode**](glrendermode.md) mit GL- \_ Feedback ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b0f82-132">The mode is selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="b0f82-133">Wenn OpenGL im Feedback Modus ist, werden von der rasterisierung keine Pixel erzeugt.</span><span class="sxs-lookup"><span data-stu-id="b0f82-133">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="b0f82-134">Stattdessen werden Informationen über primitive, die gerengt worden wären, über OpenGL an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0f82-134">Instead, information about primitives that would have been rasterized is fed back to the application using OpenGL.</span></span>

<span data-ttu-id="b0f82-135">Die **glfeedbackbuffer** -Funktion hat drei Argumente:</span><span class="sxs-lookup"><span data-stu-id="b0f82-135">The **glFeedbackBuffer** function has three arguments:</span></span>

-   <span data-ttu-id="b0f82-136">*buffer* ist ein Zeiger auf ein Array von Gleit Komma Werten, in die Feedback Informationen eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-136">*buffer* is a pointer to an array of floating-point values into which feedback information is placed.</span></span>
-   <span data-ttu-id="b0f82-137">*size* gibt die Größe des Arrays an.</span><span class="sxs-lookup"><span data-stu-id="b0f82-137">*size* indicates the size of the array.</span></span>
-   <span data-ttu-id="b0f82-138">*Type* ist eine symbolische Konstante, die die Informationen beschreibt, die für jeden Scheitelpunkt zurückgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-138">*type* is a symbolic constant describing the information that is fed back for each vertex.</span></span>

<span data-ttu-id="b0f82-139">Sie müssen **glfeedbackbuffer** ausgeben, bevor der Feedback Modus aktiviert ist (durch Aufrufen von **glrendermode** mit dem Argument GL- \_ Feedback).</span><span class="sxs-lookup"><span data-stu-id="b0f82-139">You must issue **glFeedbackBuffer** before feedback mode is enabled (by calling **glRenderMode** with argument GL\_FEEDBACK).</span></span> <span data-ttu-id="b0f82-140">Wenn Sie \_ das GL-Feedback ohne Einrichtung des Feedback Puffers festlegen oder " **glfeedbackbuffer** " aufrufen, während sich OpenGL im Feedback Modus befindet, ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b0f82-140">Setting GL\_FEEDBACK without establishing the feedback buffer, or calling **glFeedbackBuffer** while OpenGL is in feedback mode, is an error.</span></span>

<span data-ttu-id="b0f82-141">Akzeptieren Sie OpenGL aus dem Feedback Modus, indem Sie [**glrendermode**](glrendermode.md) mit einem anderen Parameterwert als GL- \_ Feedback aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b0f82-141">Take OpenGL out of feedback mode by calling [**glRenderMode**](glrendermode.md) with a parameter value other than GL\_FEEDBACK.</span></span> <span data-ttu-id="b0f82-142">Wenn sich OpenGL im Feedback Modus befindet, gibt " **glrendermode** " die Anzahl der Einträge zurück, die im Feedback-Array abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-142">When you do this while OpenGL is in feedback mode, **glRenderMode** returns the number of entries placed in the feedback array.</span></span> <span data-ttu-id="b0f82-143">Der zurückgegebene Wert überschreitet nie die *Größe*.</span><span class="sxs-lookup"><span data-stu-id="b0f82-143">The returned value never exceeds *size*.</span></span> <span data-ttu-id="b0f82-144">Wenn die Feedback Daten mehr Platz benötigen, als im *Puffer* verfügbar waren, gibt **glrendermode** einen negativen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0f82-144">If the feedback data required more room than was available in *buffer*, **glRenderMode** returns a negative value.</span></span>

<span data-ttu-id="b0f82-145">Im Feedback Modus generiert jedes primitive, das gerastertes wäre, einen Block von Werten, die in das Feedback Array kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-145">While in feedback mode, each primitive that would be rasterized generates a block of values that gets copied into the feedback array.</span></span> <span data-ttu-id="b0f82-146">Wenn dies dazu führen würde, dass die Anzahl der Einträge den maximalen Wert überschreitet, schreibt **glfeedbackbuffer** den Block teilweise so, dass er das Array ausfüllen soll (wenn überhaupt ein Platz übrig ist), und legt ein Überlauf Kennzeichen fest.</span><span class="sxs-lookup"><span data-stu-id="b0f82-146">If doing so would cause the number of entries to exceed the maximum, **glFeedbackBuffer** partially writes the block so as to fill the array (if there is any room left at all), and sets an overflow flag.</span></span> <span data-ttu-id="b0f82-147">Jeder Block beginnt mit einem Code, der den primitiven Typ anzeigt, gefolgt von Werten, die die Scheitel Punkte und zugeordneten Daten des primitiven beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b0f82-147">Each block begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="b0f82-148">Die **glfeedbackbuffer** -Funktion schreibt auch Einträge für Bitmaps und Pixel Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="b0f82-148">The **glFeedbackBuffer** function also writes entries for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="b0f82-149">Das Feedback tritt auf, nachdem die Polygon-und [**glpolygonmode**](glpolygonmode.md) -Interpretation von Polygonen stattfindet, sodass Polygone, die als herausgefiltert werden dienen, nicht im Feedback Puffer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-149">Feedback occurs after polygon culling and [**glPolygonMode**](glpolygonmode.md) interpretation of polygons has taken place, so polygons that are culled are not returned in the feedback buffer.</span></span> <span data-ttu-id="b0f82-150">Sie kann auch auftreten, nachdem Polygone mit mehr als drei Rändern in Dreiecke aufgeteilt wurden, wenn die OpenGL-Implementierung Polygone durch Ausführen dieser Zerlegung rendert.</span><span class="sxs-lookup"><span data-stu-id="b0f82-150">It can also occur after polygons with more than three edges are broken up into triangles, if the OpenGL implementation renders polygons by performing this decomposition.</span></span>

<span data-ttu-id="b0f82-151">Sie können einen Marker mit [**glpassthrough**](glpassthrough.md)in den Feedback Puffer einfügen.</span><span class="sxs-lookup"><span data-stu-id="b0f82-151">You can insert a marker into the feedback buffer with [**glPassThrough**](glpassthrough.md).</span></span>

<span data-ttu-id="b0f82-152">Im folgenden finden Sie die Grammatik für die Blöcke der Werte, die in den Feedback Puffer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-152">The following is the grammar for the blocks of values written into the feedback buffer.</span></span> <span data-ttu-id="b0f82-153">Jede primitive wird durch einen eindeutigen identifizierenden Wert gefolgt von einer bestimmten Anzahl von Vertices angegeben.</span><span class="sxs-lookup"><span data-stu-id="b0f82-153">Each primitive is indicated with a unique identifying value followed by some number of vertices.</span></span> <span data-ttu-id="b0f82-154">Polygon Einträge enthalten einen ganzzahligen Wert, der angibt, wie viele Scheitel Punkte folgen.</span><span class="sxs-lookup"><span data-stu-id="b0f82-154">Polygon entries include an integer value indicating how many vertices follow.</span></span> <span data-ttu-id="b0f82-155">Ein Scheitelpunkt wird als eine Reihe von Gleit Komma Werten zurückgeführt, die vom *Typ* bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-155">A vertex is fed back as some number of floating-point values, as determined by *type*.</span></span> <span data-ttu-id="b0f82-156">Farben werden als vier Werte im RGBA-Modus und ein Wert im Farb Index Modus zurückgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0f82-156">Colors are fed back as four values in RGBA mode and one value in color-index mode.</span></span>

<span data-ttu-id="b0f82-157">feedbacklist < feedbacklist feedbacklist- \| feedbackitem</span><span class="sxs-lookup"><span data-stu-id="b0f82-157">feedbackList <  feedbackItem feedbackList \| feedbackItem</span></span>

<span data-ttu-id="b0f82-158">feedbackitem < Punkt- \| LineSegment \| Polygon \| Bitmap \| Pixel Rechteck \| passthru</span><span class="sxs-lookup"><span data-stu-id="b0f82-158">feedbackItem <  point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru</span></span>

<span data-ttu-id="b0f82-159">Punkt < GL \_ - \_ punkttokenscheitel Punkt</span><span class="sxs-lookup"><span data-stu-id="b0f82-159">point <  GL\_POINT\_TOKEN vertex</span></span>

<span data-ttu-id="b0f82-160">LineSegment < GL- \_ Zeilen Token Vertex-Vertex- \_ \| \_ Zeilen Zurücksetzungs \_ Token- \_ vertexscheitel Punkt</span><span class="sxs-lookup"><span data-stu-id="b0f82-160">lineSegment <  GL\_LINE\_TOKEN vertex vertex \| GL\_LINE\_RESET\_TOKEN vertex vertex</span></span>

<span data-ttu-id="b0f82-161">Polygon-< GL- \_ Polygon- \_ Token n polyspec</span><span class="sxs-lookup"><span data-stu-id="b0f82-161">polygon <  GL\_POLYGON\_TOKEN n polySpec</span></span>

<span data-ttu-id="b0f82-162">polyspec < polyspec Scheitelpunkt Scheitelpunkt Scheitelpunkt Scheitelpunkt \|</span><span class="sxs-lookup"><span data-stu-id="b0f82-162">polySpec <  polySpec vertex \| vertex vertex vertex</span></span>

<span data-ttu-id="b0f82-163">Bitmap < GL- \_ \_ bitmaptokenscheitel Punkt</span><span class="sxs-lookup"><span data-stu-id="b0f82-163">bitmap <  GL\_BITMAP\_TOKEN vertex</span></span>

<span data-ttu-id="b0f82-164">Pixel Rechteck < GL \_ Zeichnen des \_ Pixel Tokens \_ Vertex- \| \_ \_ Pixel \_ Token-Vertex kopieren</span><span class="sxs-lookup"><span data-stu-id="b0f82-164">pixelRectangle <  GL\_DRAW\_PIXEL\_TOKEN vertex \| GL\_COPY\_PIXEL\_TOKEN vertex</span></span>

<span data-ttu-id="b0f82-165">PassThru < GL- \_ Pass- \_ through- \_ Tokenwert</span><span class="sxs-lookup"><span data-stu-id="b0f82-165">passThru <  GL\_PASS\_THROUGH\_TOKEN value</span></span>

<span data-ttu-id="b0f82-166">Vertex < 2D \| 3D- \| 3dcolor \| 3dcolortexture \| 4dcolortexture</span><span class="sxs-lookup"><span data-stu-id="b0f82-166">vertex <  2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture</span></span>

<span data-ttu-id="b0f82-167">2D-Wert für < Wert</span><span class="sxs-lookup"><span data-stu-id="b0f82-167">2d <  value value</span></span>

<span data-ttu-id="b0f82-168">Wert des 3D--< Werts</span><span class="sxs-lookup"><span data-stu-id="b0f82-168">3d <  value value value</span></span>

<span data-ttu-id="b0f82-169">3dcolor-< Wert Wert Farbe</span><span class="sxs-lookup"><span data-stu-id="b0f82-169">3dColor <  value value value color</span></span>

<span data-ttu-id="b0f82-170">3dcolortexture < Werte Wert farbtex</span><span class="sxs-lookup"><span data-stu-id="b0f82-170">3dColorTexture <  value value value color tex</span></span>

<span data-ttu-id="b0f82-171">4dcolortexture < Werte Wert farbtex</span><span class="sxs-lookup"><span data-stu-id="b0f82-171">4dColorTexture <  value value value value color tex</span></span>

<span data-ttu-id="b0f82-172">Farbe < RGBA- \| Index</span><span class="sxs-lookup"><span data-stu-id="b0f82-172">color <  rgba \| index</span></span>

<span data-ttu-id="b0f82-173">Wert des RGBA-< Wert Werts</span><span class="sxs-lookup"><span data-stu-id="b0f82-173">rgba <  value value value value</span></span>

<span data-ttu-id="b0f82-174">Index < Wert</span><span class="sxs-lookup"><span data-stu-id="b0f82-174">index <  value</span></span>

<span data-ttu-id="b0f82-175">Wert Wert Wert des Tex-< Werts</span><span class="sxs-lookup"><span data-stu-id="b0f82-175">tex <  value value value value</span></span>

<span data-ttu-id="b0f82-176">Der *value* -Parameter ist eine Gleit Komma Zahl, und *n* ist eine Gleit Komma Zahl, die die Anzahl der Scheitel Punkte im Polygon gibt.</span><span class="sxs-lookup"><span data-stu-id="b0f82-176">The *value* parameter is a floating-point number, and *n* is a floating-point integer giving the number of vertices in the polygon.</span></span> <span data-ttu-id="b0f82-177">Im folgenden finden Sie symbolische Gleit Komma Konstanten: GL- \_ Punkt \_ Token, GL- \_ Zeilen \_ Token, GL \_ -Zeilen Zurücksetzungs \_ \_ Token, GL- \_ Polygon- \_ Token, GL- \_ \_ bitmaptoken, GL \_ \_ -Pixel Token, GL \_ \_ \_ -Kopier Pixel \_ Token und GL- \_ Pass-Through- \_ \_ Token.</span><span class="sxs-lookup"><span data-stu-id="b0f82-177">The following are symbolic floating-point constants: GL\_POINT\_TOKEN, GL\_LINE\_TOKEN, GL\_LINE\_RESET\_TOKEN, GL\_POLYGON\_TOKEN, GL\_BITMAP\_TOKEN, GL\_DRAW\_PIXEL\_TOKEN, GL\_COPY\_PIXEL\_TOKEN, and GL\_PASS\_THROUGH\_TOKEN.</span></span> <span data-ttu-id="b0f82-178">\_ \_ Das Token zum Zurücksetzen von GL \_ wird zurückgegeben, wenn das Zeilen stippingmuster zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b0f82-178">GL\_LINE\_RESET\_TOKEN is returned whenever the line stipple pattern is reset.</span></span> <span data-ttu-id="b0f82-179">Die als Scheitel Punkte zurückgegebenen Daten sind vom *Feedtyp* abhängig.</span><span class="sxs-lookup"><span data-stu-id="b0f82-179">The data returned as a vertex depends on the feedback *type*.</span></span>

<span data-ttu-id="b0f82-180">In der folgenden Tabelle ist die Entsprechung zwischen *Typ* und Anzahl der Werte pro Scheitelpunkt *k* ist 1 im Farb Index Modus und 4 im RGBA-Modus.</span><span class="sxs-lookup"><span data-stu-id="b0f82-180">The following table gives the correspondence between *type* and the number of values per vertex; *k* is 1 in color-index mode and 4 in RGBA mode.</span></span>



| <span data-ttu-id="b0f82-181">type</span><span class="sxs-lookup"><span data-stu-id="b0f82-181">Type</span></span>                   | <span data-ttu-id="b0f82-182">Koordinaten</span><span class="sxs-lookup"><span data-stu-id="b0f82-182">Coordinates</span></span>        | <span data-ttu-id="b0f82-183">Color</span><span class="sxs-lookup"><span data-stu-id="b0f82-183">Color</span></span> | <span data-ttu-id="b0f82-184">Struktur</span><span class="sxs-lookup"><span data-stu-id="b0f82-184">Texture</span></span> | <span data-ttu-id="b0f82-185">Gesamtzahl der Werte</span><span class="sxs-lookup"><span data-stu-id="b0f82-185">Total number of values</span></span> |
|------------------------|--------------------|-------|---------|------------------------|
| <span data-ttu-id="b0f82-186">GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="b0f82-186">GL\_2D</span></span>                 | <span data-ttu-id="b0f82-187">*x*, *y*</span><span class="sxs-lookup"><span data-stu-id="b0f82-187">*x*, *y*</span></span>           |       |         | <span data-ttu-id="b0f82-188">2</span><span class="sxs-lookup"><span data-stu-id="b0f82-188">2</span></span>                      |
| <span data-ttu-id="b0f82-189">GL \_ 3D</span><span class="sxs-lookup"><span data-stu-id="b0f82-189">GL\_3D</span></span>                 | <span data-ttu-id="b0f82-190">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="b0f82-190">*x*, *y*, *z*</span></span>      |       |         | <span data-ttu-id="b0f82-191">3</span><span class="sxs-lookup"><span data-stu-id="b0f82-191">3</span></span>                      |
| <span data-ttu-id="b0f82-192">GL \_ 3D- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="b0f82-192">GL\_3D\_COLOR</span></span>          | <span data-ttu-id="b0f82-193">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="b0f82-193">*x*, *y*, *z*</span></span>      | <span data-ttu-id="b0f82-194">*km*</span><span class="sxs-lookup"><span data-stu-id="b0f82-194">*k*</span></span>   |         | <span data-ttu-id="b0f82-195">3 + *k*</span><span class="sxs-lookup"><span data-stu-id="b0f82-195">3 + *k*</span></span>                |
| <span data-ttu-id="b0f82-196">GL \_ 3D- \_ Farb \_ Textur</span><span class="sxs-lookup"><span data-stu-id="b0f82-196">GL\_3D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="b0f82-197">*x*, *y*, *z*,</span><span class="sxs-lookup"><span data-stu-id="b0f82-197">*x*, *y*, *z*,</span></span>     | <span data-ttu-id="b0f82-198">*km*</span><span class="sxs-lookup"><span data-stu-id="b0f82-198">*k*</span></span>   | <span data-ttu-id="b0f82-199">4</span><span class="sxs-lookup"><span data-stu-id="b0f82-199">4</span></span>       | <span data-ttu-id="b0f82-200">7 + *k*</span><span class="sxs-lookup"><span data-stu-id="b0f82-200">7 + *k*</span></span>                |
| <span data-ttu-id="b0f82-201">GL \_ 4D \_ Farb \_ Textur</span><span class="sxs-lookup"><span data-stu-id="b0f82-201">GL\_4D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="b0f82-202">*x*, *y*, *z*, *w*</span><span class="sxs-lookup"><span data-stu-id="b0f82-202">*x*, *y*, *z*, *w*</span></span> | <span data-ttu-id="b0f82-203">*km*</span><span class="sxs-lookup"><span data-stu-id="b0f82-203">*k*</span></span>   | <span data-ttu-id="b0f82-204">4</span><span class="sxs-lookup"><span data-stu-id="b0f82-204">4</span></span>       | <span data-ttu-id="b0f82-205">8 + *k*</span><span class="sxs-lookup"><span data-stu-id="b0f82-205">8 + *k*</span></span>                |



 

<span data-ttu-id="b0f82-206">Feedback-vertexkoordinaten befinden sich in Fenster Koordinaten, mit Ausnahme von " *w*", die sich in Clip Koordinaten befinden.</span><span class="sxs-lookup"><span data-stu-id="b0f82-206">Feedback vertex coordinates are in window coordinates, except *w*, which is in clip coordinates.</span></span> <span data-ttu-id="b0f82-207">Die Farben des Feedbacks werden beleuchtet, wenn Beleuchtung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b0f82-207">Feedback colors are lighted, if lighting is enabled.</span></span> <span data-ttu-id="b0f82-208">Es werden Feedback Texturkoordinaten generiert, wenn die Generierung der Textur Koordinate aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b0f82-208">Feedback texture coordinates are generated, if texture coordinate generation is enabled.</span></span> <span data-ttu-id="b0f82-209">Sie werden immer von der Textur Matrix transformiert.</span><span class="sxs-lookup"><span data-stu-id="b0f82-209">They are always transformed by the texture matrix.</span></span>

<span data-ttu-id="b0f82-210">Die **glfeedbackbuffer** -Funktion wird, wenn Sie in einer Anzeigeliste verwendet wird, nicht in die Anzeigeliste kompiliert, sondern wird sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0f82-210">The **glFeedbackBuffer** function, when used in a display list, is not compiled into the display list but rather is executed immediately.</span></span>

<span data-ttu-id="b0f82-211">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glfeedbackbuffer** ab:</span><span class="sxs-lookup"><span data-stu-id="b0f82-211">The following function retrieves information related to **glFeedbackBuffer**:</span></span>

<span data-ttu-id="b0f82-212">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Rendermodus</span><span class="sxs-lookup"><span data-stu-id="b0f82-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f82-213">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0f82-213">Requirements</span></span>



| <span data-ttu-id="b0f82-214">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0f82-214">Requirement</span></span> | <span data-ttu-id="b0f82-215">Wert</span><span class="sxs-lookup"><span data-stu-id="b0f82-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f82-216">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0f82-216">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f82-217">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0f82-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b0f82-218">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0f82-218">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f82-219">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0f82-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0f82-220">Header</span><span class="sxs-lookup"><span data-stu-id="b0f82-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0f82-221"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f82-221"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b0f82-222">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0f82-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0f82-223"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0f82-223"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0f82-224">DLL</span><span class="sxs-lookup"><span data-stu-id="b0f82-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0f82-225"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0f82-225"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f82-226">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0f82-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f82-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b0f82-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b0f82-228">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b0f82-228">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b0f82-229">**glget**</span><span class="sxs-lookup"><span data-stu-id="b0f82-229">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b0f82-230">**gllinestippel**</span><span class="sxs-lookup"><span data-stu-id="b0f82-230">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="b0f82-231">**glpassthrough**</span><span class="sxs-lookup"><span data-stu-id="b0f82-231">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="b0f82-232">**glpolygonmode**</span><span class="sxs-lookup"><span data-stu-id="b0f82-232">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="b0f82-233">**glrendermode**</span><span class="sxs-lookup"><span data-stu-id="b0f82-233">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="b0f82-234">**glselectbuffer**</span><span class="sxs-lookup"><span data-stu-id="b0f82-234">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





