---
title: glscissor-Funktion (GL. h)
description: Die Funktion "glscissor" definiert das Feld "Scheren".
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glscissor-Funktion OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479131"
---
# <a name="glscissor-function"></a><span data-ttu-id="c04ce-104">glscissor-Funktion</span><span class="sxs-lookup"><span data-stu-id="c04ce-104">glScissor function</span></span>

<span data-ttu-id="c04ce-105">Die Funktion " **glscissor** " definiert das Feld "Scheren".</span><span class="sxs-lookup"><span data-stu-id="c04ce-105">The **glScissor** function defines the scissor box.</span></span>

## <a name="syntax"></a><span data-ttu-id="c04ce-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c04ce-106">Syntax</span></span>


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="c04ce-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c04ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c04ce-108">*x*</span><span class="sxs-lookup"><span data-stu-id="c04ce-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="c04ce-109">Die x-Koordinate (vertikale Achse) für die untere linke Ecke des Scheren Felds.</span><span class="sxs-lookup"><span data-stu-id="c04ce-109">The x (vertical axis) coordinate for the lower-left corner of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="c04ce-110">*y*</span><span class="sxs-lookup"><span data-stu-id="c04ce-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="c04ce-111">Die y-Koordinate (horizontale Achse) für die untere linke Ecke des Scheren Felds.</span><span class="sxs-lookup"><span data-stu-id="c04ce-111">The y (horizontal axis) coordinate for the lower-left corner of the scissor box.</span></span> <span data-ttu-id="c04ce-112">In kombinieren Sie x und y in der unteren linken Ecke des Scheren Felds.</span><span class="sxs-lookup"><span data-stu-id="c04ce-112">Together, x and y specify the lower-left corner of the scissor box.</span></span> <span data-ttu-id="c04ce-113">Anfänglich (0,0).</span><span class="sxs-lookup"><span data-stu-id="c04ce-113">Initially (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="c04ce-114">*width*</span><span class="sxs-lookup"><span data-stu-id="c04ce-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="c04ce-115">Die Breite des Scheren Felds.</span><span class="sxs-lookup"><span data-stu-id="c04ce-115">The width of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="c04ce-116">*height*</span><span class="sxs-lookup"><span data-stu-id="c04ce-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="c04ce-117">Die Höhe des Scheren Felds.</span><span class="sxs-lookup"><span data-stu-id="c04ce-117">The height of the scissor box.</span></span> <span data-ttu-id="c04ce-118">Wenn ein OpenGL-Kontext zum *ersten Mal* an ein Fenster angefügt wird, werden *Breite* und *Höhe* auf die Abmessungen dieses Fensters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c04ce-118">When an OpenGL context is *first* attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c04ce-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c04ce-119">Return value</span></span>

<span data-ttu-id="c04ce-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c04ce-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c04ce-121">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c04ce-121">Error codes</span></span>

<span data-ttu-id="c04ce-122">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c04ce-122">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c04ce-123">Name</span><span class="sxs-lookup"><span data-stu-id="c04ce-123">Name</span></span>                                                                                                  | <span data-ttu-id="c04ce-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c04ce-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c04ce-125"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="c04ce-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c04ce-126">Die *Breite* oder *Höhe* war negativ.</span><span class="sxs-lookup"><span data-stu-id="c04ce-126">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="c04ce-127"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="c04ce-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c04ce-128">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c04ce-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c04ce-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c04ce-129">Remarks</span></span>

<span data-ttu-id="c04ce-130">Die Funktion " **glscissor** " definiert ein Rechteck, das als "Scheren"-Feld bezeichnet wird, in Fenster Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="c04ce-130">The **glScissor** function defines a rectangle, called the scissor box, in window coordinates.</span></span> <span data-ttu-id="c04ce-131">Die ersten beiden Parameter *x* und *y* geben die untere linke Ecke des Felds an.</span><span class="sxs-lookup"><span data-stu-id="c04ce-131">The first two parameters, *x* and *y*, specify the lower-left corner of the box.</span></span> <span data-ttu-id="c04ce-132">Die *Width* -und *height* -Parameter geben die Breite und Höhe des Felds an.</span><span class="sxs-lookup"><span data-stu-id="c04ce-132">The *width* and *height* parameters specify the width and height of the box.</span></span>

<span data-ttu-id="c04ce-133">Der Scheren-Test wird mit " [**glEnable**](glenable.md) " und " **gldeaktivieren** " mit dem Argument "GL \_ Scheren Test" aktiviert und deaktiviert \_ .</span><span class="sxs-lookup"><span data-stu-id="c04ce-133">The scissor test is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_SCISSOR\_TEST.</span></span> <span data-ttu-id="c04ce-134">Während der Scheren-Test aktiviert ist, können nur Pixel, die im Feld Scheren liegen, durch Zeichnen von Befehlen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c04ce-134">While the scissor test is enabled, only pixels that lie within the scissor box can be modified by drawing commands.</span></span> <span data-ttu-id="c04ce-135">Fenster Koordinaten verfügen über ganzzahlige Werte in den freigegebenen Ecken von Frame Puffer Pixel, sodass mit **glscissor**(0, 0, 1, 1) nur das untere linke Pixel im Fenster geändert werden kann, und **glscissor**(0, 0, 0, 0) lässt Änderungen an allen Pixeln im Fenster nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c04ce-135">Window coordinates have integer values at the shared corners of framebuffer pixels, so **glScissor**(0,0,1,1) allows only the lower-left pixel in the window to be modified, and **glScissor**(0,0,0,0) disallows modification to all pixels in the window.</span></span>

<span data-ttu-id="c04ce-136">Wenn der Scheren-Test deaktiviert ist, ist es so, als ob das Feld Scheren das gesamte Fenster enthält.</span><span class="sxs-lookup"><span data-stu-id="c04ce-136">When the scissor test is disabled, it is as though the scissor box includes the entire window.</span></span>

<span data-ttu-id="c04ce-137">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glscissor** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="c04ce-137">The following functions retrieve information related to **glScissor**:</span></span>

<span data-ttu-id="c04ce-138">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Scissor \_ Box</span><span class="sxs-lookup"><span data-stu-id="c04ce-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SCISSOR\_BOX</span></span>

<span data-ttu-id="c04ce-139">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Scissor \_ Test</span><span class="sxs-lookup"><span data-stu-id="c04ce-139">[**glIsEnabled**](glisenabled.md) with argument GL\_SCISSOR\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="c04ce-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c04ce-140">Requirements</span></span>



| <span data-ttu-id="c04ce-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c04ce-141">Requirement</span></span> | <span data-ttu-id="c04ce-142">Wert</span><span class="sxs-lookup"><span data-stu-id="c04ce-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c04ce-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c04ce-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c04ce-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c04ce-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c04ce-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c04ce-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c04ce-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c04ce-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c04ce-147">Header</span><span class="sxs-lookup"><span data-stu-id="c04ce-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="c04ce-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c04ce-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c04ce-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c04ce-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="c04ce-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c04ce-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c04ce-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c04ce-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c04ce-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c04ce-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c04ce-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c04ce-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04ce-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c04ce-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c04ce-155">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="c04ce-155">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="c04ce-156">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c04ce-156">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c04ce-157">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="c04ce-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="c04ce-158">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="c04ce-158">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





