---
title: glselectbuffer-Funktion (GL. h)
description: Die Funktion "glselectbuffer" stellt einen Puffer für Werte im Auswahlmodus her.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glselectbuffer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740040"
---
# <a name="glselectbuffer-function"></a><span data-ttu-id="818eb-104">glselectbuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="818eb-104">glSelectBuffer function</span></span>

<span data-ttu-id="818eb-105">Die Funktion " **glselectbuffer** " stellt einen Puffer für Werte im Auswahlmodus her.</span><span class="sxs-lookup"><span data-stu-id="818eb-105">The **glSelectBuffer** function establishes a buffer for selection mode values.</span></span>

## <a name="syntax"></a><span data-ttu-id="818eb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="818eb-106">Syntax</span></span>


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="818eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="818eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="818eb-108">*size*</span><span class="sxs-lookup"><span data-stu-id="818eb-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="818eb-109">Die Größe des *Puffers*.</span><span class="sxs-lookup"><span data-stu-id="818eb-109">The size of *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="818eb-110">*ert*</span><span class="sxs-lookup"><span data-stu-id="818eb-110">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="818eb-111">Gibt die Auswahl Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="818eb-111">Returns the selection data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="818eb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="818eb-112">Return value</span></span>

<span data-ttu-id="818eb-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="818eb-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="818eb-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="818eb-114">Error codes</span></span>

<span data-ttu-id="818eb-115">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="818eb-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="818eb-116">Name</span><span class="sxs-lookup"><span data-stu-id="818eb-116">Name</span></span>                                                                                                  | <span data-ttu-id="818eb-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="818eb-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="818eb-118"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="818eb-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="818eb-119">die *Größe* war negativ.</span><span class="sxs-lookup"><span data-stu-id="818eb-119">*size* was negative.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="818eb-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="818eb-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="818eb-121">Die Funktion wurde aufgerufen, während der Rendermodus "GL Select" war \_ .</span><span class="sxs-lookup"><span data-stu-id="818eb-121">The function was called while the render mode was GL\_SELECT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="818eb-122"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="818eb-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="818eb-123">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="818eb-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="818eb-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="818eb-124">Remarks</span></span>

<span data-ttu-id="818eb-125">Die Funktion " **glselectbuffer** " verfügt über zwei Parameter: " *buffer* " ist ein Zeiger auf ein Array aus ganzen Zahlen ohne Vorzeichen und " *size* " gibt die Größe des Arrays an.</span><span class="sxs-lookup"><span data-stu-id="818eb-125">The **glSelectBuffer** function has two parameters: *buffer* is a pointer to an array of unsigned integers, and *size* indicates the size of the array.</span></span> <span data-ttu-id="818eb-126">Der *buffer* -Parameter gibt Werte aus dem Namen Stapel zurück (siehe [**glinitnames**](glinitnames.md), [**glloadname**](glloadname.md), [**glpushname**](glpushname.md)), wenn der Renderingmodus "GL Select" ist \_ (siehe [**glrendermode**](glrendermode.md)).</span><span class="sxs-lookup"><span data-stu-id="818eb-126">The *buffer* parameter returns values from the name stack (see [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) when the rendering mode is GL\_SELECT (see [**glRenderMode**](glrendermode.md)).</span></span> <span data-ttu-id="818eb-127">Die Funktion " **glselectbuffer** " muss ausgegeben werden, bevor der Auswahlmodus aktiviert ist, und Sie darf nicht ausgegeben werden, während der Renderingmodus "GL Select" ist \_ .</span><span class="sxs-lookup"><span data-stu-id="818eb-127">The **glSelectBuffer** function must be issued before selection mode is enabled, and it must not be issued while the rendering mode is GL\_SELECT.</span></span>

<span data-ttu-id="818eb-128">Die Auswahl wird von einem Programmierer verwendet, um zu bestimmen, welche primitiven in einem Fensterbereich gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="818eb-128">Selection is used by a programmer to determine which primitives are drawn into some region of a window.</span></span> <span data-ttu-id="818eb-129">Der Bereich wird durch die aktuelle Modelview-und perspektivische Matrizen definiert.</span><span class="sxs-lookup"><span data-stu-id="818eb-129">The region is defined by the current modelview and perspective matrices.</span></span>

<span data-ttu-id="818eb-130">Im Auswahlmodus werden keine Pixel Fragmente aus der rasterisierung erzeugt.</span><span class="sxs-lookup"><span data-stu-id="818eb-130">In selection mode, no pixel fragments are produced from rasterization.</span></span> <span data-ttu-id="818eb-131">Wenn ein primitiv das Clip Volume überschneidet, das durch die Anzeige von "Frustum" und die benutzerdefinierten Clippingebenen definiert ist, verursacht dieser Primitive stattdessen eine Auswahl Treffer.</span><span class="sxs-lookup"><span data-stu-id="818eb-131">Instead, if a primitive intersects the clip volume defined by the viewing frustum and the user-defined clipping planes, this primitive causes a selection hit.</span></span> <span data-ttu-id="818eb-132">(Bei Polygonen findet kein Treffer statt, wenn das Polygon gekullt ist.) Wenn eine Änderung am namens Stapel vorgenommen wird oder wenn " [**glrendermode**](glrendermode.md) " aufgerufen wird, wird ein Treffer Daten Satz in den *Puffer* kopiert, wenn seit dem letzten derartigen Ereignis (entweder eine namens Stapeländerung oder ein " **glrendermode** "-Aufruf) Treffer aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="818eb-132">(With polygons, no hit occurs if the polygon is culled.) When a change is made to the name stack, or when [**glRenderMode**](glrendermode.md) is called, a hit record is copied to *buffer* if any hits have occurred since the last such event (either a name stack change or a **glRenderMode** call).</span></span> <span data-ttu-id="818eb-133">Der Treffer Daten Satz besteht aus der Anzahl der Namen im Namen Stapel zum Zeitpunkt des Ereignisses. gefolgt von den minimalen und maximalen tiefen Werten aller Scheitel Punkte, die seit dem vorherigen Ereignis getroffen wurden. gefolgt vom Namen Stapel Inhalt, der untere Name wird zuerst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="818eb-133">The hit record consists of the number of names in the name stack at the time of the event; followed by the minimum and maximum depth values of all vertices that hit since the previous event; followed by the name stack contents, bottom name first.</span></span>

<span data-ttu-id="818eb-134">Zurückgegebene tiefen Werte werden so zugeordnet, dass der größte ganzzahlige Wert ohne Vorzeichen der Fenster Koordinaten Tiefe 1,0 entspricht und 0 (null) der Fenster Koordinaten Tiefe 0,0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="818eb-134">Returned depth values are mapped such that the largest unsigned integer value corresponds to window coordinate depth 1.0, and zero corresponds to window coordinate depth 0.0.</span></span>

<span data-ttu-id="818eb-135">Ein interner Index in den *Puffer* wird bei der Eingabe des Auswahlmodus auf 0 (null) zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="818eb-135">An internal index into *buffer* is reset to zero whenever selection mode is entered.</span></span> <span data-ttu-id="818eb-136">Jedes Mal, wenn ein Treffer Daten Satz in den *Puffer* kopiert wird, wird der Index inkrementiert, sodass er auf die Zelle unmittelbar nach dem Ende des Blocks von Namespace, d. h. der nächsten verfügbaren Zelle, verweist.</span><span class="sxs-lookup"><span data-stu-id="818eb-136">Each time a hit record is copied into *buffer*, the index is incremented to point to the cell just past the end of the block of namesthat is, to the next available cell.</span></span> <span data-ttu-id="818eb-137">Wenn der Treffer Daten Satz größer als die Anzahl der verbleibenden Speicherorte im *Puffer* ist, werden so viele Daten wie möglich kopiert und das Überlauf Kennzeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="818eb-137">If the hit record is larger than the number of remaining locations in *buffer*, as much data as can fit is copied, and the overflow flag is set.</span></span> <span data-ttu-id="818eb-138">Wenn der namens Stapel beim Kopieren eines Treffer Datensatzes leer ist, besteht dieser Datensatz aus 0, gefolgt von den minimalen und maximalen tiefen Werten.</span><span class="sxs-lookup"><span data-stu-id="818eb-138">If the name stack is empty when a hit record is copied, that record consists of zero followed by the minimum and maximum depth values.</span></span>

<span data-ttu-id="818eb-139">Der Auswahlmodus wird beendet, indem **glrendermode** mit einem anderen Argument als GL \_ SELECT aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="818eb-139">Selection mode is exited by calling **glRenderMode** with an argument other than GL\_SELECT.</span></span> <span data-ttu-id="818eb-140">Wenn " **glrendermode** " aufgerufen wird, während der Rendermodus "GL Select" ist \_ , gibt es die Anzahl der in den *Puffer* kopierten Treffer Datensätze zurück, setzt das Überlauf Kennzeichen und den Auswahl Puffer Zeiger zurück und initialisiert den namens Stapel, damit er leer ist.</span><span class="sxs-lookup"><span data-stu-id="818eb-140">Whenever **glRenderMode** is called while the render mode is GL\_SELECT, it returns the number of hit records copied to *buffer*, resets the overflow flag and the selection buffer pointer, and initializes the name stack to be empty.</span></span> <span data-ttu-id="818eb-141">Wenn das Überlauf Bit beim Aufrufen von **glrendermode** festgelegt wurde, wird eine negative Treffer Daten Satz Anzahl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="818eb-141">If the overflow bit was set when **glRenderMode** was called, a negative hit record count is returned.</span></span>

<span data-ttu-id="818eb-142">Der Inhalt des *Puffers* ist nicht definiert, bis [**glrendermode**](glrendermode.md) mit einem anderen Argument als GL SELECT aufgerufen wird \_ .</span><span class="sxs-lookup"><span data-stu-id="818eb-142">The contents of *buffer* are undefined until [**glRenderMode**](glrendermode.md) is called with an argument other than GL\_SELECT.</span></span>

<span data-ttu-id="818eb-143">Die **glBegin** / -**glEnd** -primitive und Aufrufe von [**glRasterPos**](glrasterpos-functions.md) können zu Treffern führen.</span><span class="sxs-lookup"><span data-stu-id="818eb-143">The **glBegin**/**glEnd** primitives and calls to [**glRasterPos**](glrasterpos-functions.md) can result in hits.</span></span>

<span data-ttu-id="818eb-144">Die folgende Funktion Ruft Informationen im Zusammenhang mit " **glselectbuffer**" ab:</span><span class="sxs-lookup"><span data-stu-id="818eb-144">The following function retrieves information related to **glSelectBuffer**:</span></span>

<span data-ttu-id="818eb-145">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Name \_ Stack- \_ Tiefe"</span><span class="sxs-lookup"><span data-stu-id="818eb-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="818eb-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="818eb-146">Requirements</span></span>



| <span data-ttu-id="818eb-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="818eb-147">Requirement</span></span> | <span data-ttu-id="818eb-148">Wert</span><span class="sxs-lookup"><span data-stu-id="818eb-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="818eb-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="818eb-149">Minimum supported client</span></span><br/> | <span data-ttu-id="818eb-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="818eb-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="818eb-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="818eb-151">Minimum supported server</span></span><br/> | <span data-ttu-id="818eb-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="818eb-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="818eb-153">Header</span><span class="sxs-lookup"><span data-stu-id="818eb-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="818eb-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="818eb-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="818eb-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="818eb-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="818eb-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="818eb-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="818eb-157">DLL</span><span class="sxs-lookup"><span data-stu-id="818eb-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="818eb-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="818eb-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="818eb-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="818eb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="818eb-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="818eb-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="818eb-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="818eb-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="818eb-162">**glfeedbackbuffer**</span><span class="sxs-lookup"><span data-stu-id="818eb-162">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="818eb-163">**glinitnames**</span><span class="sxs-lookup"><span data-stu-id="818eb-163">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="818eb-164">**glloadname**</span><span class="sxs-lookup"><span data-stu-id="818eb-164">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="818eb-165">**glpushname**</span><span class="sxs-lookup"><span data-stu-id="818eb-165">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="818eb-166">**glrendermode**</span><span class="sxs-lookup"><span data-stu-id="818eb-166">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





