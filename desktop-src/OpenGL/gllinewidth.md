---
title: glLineWidth-Funktion (GL. h)
description: Die Funktion "glLineWidth" gibt die Breite von rasterisierten Linien an.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- glLineWidth-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343066"
---
# <a name="gllinewidth-function"></a><span data-ttu-id="604be-104">glLineWidth-Funktion</span><span class="sxs-lookup"><span data-stu-id="604be-104">glLineWidth function</span></span>

<span data-ttu-id="604be-105">Die Funktion " **glLineWidth** " gibt die Breite von rasterisierten Linien an.</span><span class="sxs-lookup"><span data-stu-id="604be-105">The **glLineWidth** function specifies the width of rasterized lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="604be-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="604be-106">Syntax</span></span>


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a><span data-ttu-id="604be-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="604be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="604be-108">*width*</span><span class="sxs-lookup"><span data-stu-id="604be-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="604be-109">Die Breite von rasterisierten Linien.</span><span class="sxs-lookup"><span data-stu-id="604be-109">The width of rasterized lines.</span></span> <span data-ttu-id="604be-110">Der Standardwert ist 1.0.</span><span class="sxs-lookup"><span data-stu-id="604be-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="604be-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="604be-111">Return value</span></span>

<span data-ttu-id="604be-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="604be-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="604be-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="604be-113">Error codes</span></span>

<span data-ttu-id="604be-114">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="604be-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="604be-115">Name</span><span class="sxs-lookup"><span data-stu-id="604be-115">Name</span></span>                                                                                                  | <span data-ttu-id="604be-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="604be-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="604be-117"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="604be-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="604be-118">*Breite* war kleiner als oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="604be-118">*width* was less than or equal to zero.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="604be-119"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="604be-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="604be-120">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="604be-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="604be-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="604be-121">Remarks</span></span>

<span data-ttu-id="604be-122">Die Funktion " **glLineWidth** " gibt die gerenderte Breite sowohl von Aliasing-als auch von Antialiasing-Zeilen an.</span><span class="sxs-lookup"><span data-stu-id="604be-122">The **glLineWidth** function specifies the rasterized width of both aliased and antialiased lines.</span></span> <span data-ttu-id="604be-123">Die Verwendung einer anderen Linienbreite als 1,0 hat unterschiedliche Effekte, je nachdem, ob das linienantialiasing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="604be-123">Using a line width other than 1.0 has different effects, depending on whether line antialiasing is enabled.</span></span> <span data-ttu-id="604be-124">Das Antialiasing von Zeilen wird durch Aufrufen von [**glEnable**](glenable.md) und **gldeaktiviert** mit dem Argument GL \_ line \_ Smooth gesteuert.</span><span class="sxs-lookup"><span data-stu-id="604be-124">Line antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_SMOOTH.</span></span>

<span data-ttu-id="604be-125">Wenn das Zeilen-Antialiasing deaktiviert ist, wird die tatsächliche Breite festgelegt, indem die angegebene Breite auf die nächste ganze Zahl gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="604be-125">If line antialiasing is disabled, the actual width is determined by rounding the supplied width to the nearest integer.</span></span> <span data-ttu-id="604be-126">(Wenn die Rundung den Wert 0,0 ergibt, ist Sie so, als ob die Linienstärke 1,0 wäre.) Wenn \| ?</span><span class="sxs-lookup"><span data-stu-id="604be-126">(If the rounding results in the value 0.0, it is as if the line width were 1.0) If \| ?</span></span> <span data-ttu-id="604be-127">x \|  =  \| ?</span><span class="sxs-lookup"><span data-stu-id="604be-127">x \| = \| ?</span></span> <span data-ttu-id="604be-128">y \| , *i* Pixel werden in jede Spalte eingefügt, die rasterisiert ist, wobei *ich* den gerundeten Wert von *Width* verwende.</span><span class="sxs-lookup"><span data-stu-id="604be-128">y \|, *i* pixels are filled in each column that is rasterized, where *i* is the rounded value of *width*.</span></span> <span data-ttu-id="604be-129">Andernfalls wird jede Zeile, die gerengt wird, in " *i* Pixel" aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="604be-129">Otherwise, *i* pixels are filled in each row that is rasterized.</span></span>

<span data-ttu-id="604be-130">Wenn Antialiasing aktiviert ist, erzeugt die linienrasterisierung ein Fragment für jedes Pixel Quadrat, das den Bereich überschneidet, der innerhalb des Rechtecks liegt und dessen Breite gleich der aktuellen Linienstärke, der Länge der tatsächlichen Länge der Zeile und der zentriert auf dem mathematischen Liniensegment liegt.</span><span class="sxs-lookup"><span data-stu-id="604be-130">If antialiasing is enabled, line rasterization produces a fragment for each pixel square that intersects the region lying within the rectangle having width equal to the current line width, length equal to the actual length of the line, and centered on the mathematical line segment.</span></span> <span data-ttu-id="604be-131">Der Abdeckungs Wert für jedes Fragment ist der Fenster Koordinaten Bereich der Schnittmenge des rechteckigen Bereichs mit dem entsprechenden Pixel Quadrat.</span><span class="sxs-lookup"><span data-stu-id="604be-131">The coverage value for each fragment is the window coordinate area of the intersection of the rectangular region with the corresponding pixel square.</span></span> <span data-ttu-id="604be-132">Dieser Wert wird gespeichert und im abschließenden rasterisierungsschritt verwendet.</span><span class="sxs-lookup"><span data-stu-id="604be-132">This value is saved and used in the final rasterization step.</span></span>

<span data-ttu-id="604be-133">Nicht alle breiten können unterstützt werden, wenn das linienantialiasing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="604be-133">Not all widths can be supported when line antialiasing is enabled.</span></span> <span data-ttu-id="604be-134">Wenn eine nicht unterstützte Breite angefordert wird, wird die nächste unterstützte Breite verwendet.</span><span class="sxs-lookup"><span data-stu-id="604be-134">If an unsupported width is requested, the nearest supported width is used.</span></span> <span data-ttu-id="604be-135">Es wird sichergestellt, dass nur die Breite 1,0 unterstützt wird. andere sind von der Implementierung abhängig.</span><span class="sxs-lookup"><span data-stu-id="604be-135">Only width 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="604be-136">Der Bereich der unterstützten breiten und der Größenunterschied zwischen unterstützten breiten innerhalb des Bereichs kann durch Aufrufen von **glget** mit den Argumenten GL \_ \_ -Linienbreite \_ und- \_ \_ \_ Granularität der GL-Linie abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="604be-136">The range of supported widths and the size difference between supported widths within the range can be queried by calling **glGet** with arguments GL\_LINE\_WIDTH\_RANGE and GL\_LINE\_WIDTH\_GRANULARITY.</span></span>

<span data-ttu-id="604be-137">Die durch **glLineWidth** angegebene Linienbreite wird immer zurückgegeben, wenn die GL- \_ Linien \_ Breite abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="604be-137">The line width specified by **glLineWidth** is always returned when GL\_LINE\_WIDTH is queried.</span></span> <span data-ttu-id="604be-138">Das Spannen und Runden von Zeilen mit einem Alias und einem mit einem AntiAlias einhergehenden Zeilen haben keine Auswirkung auf den angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="604be-138">Clamping and rounding for aliased and antialiased lines have no effect on the specified value.</span></span>

<span data-ttu-id="604be-139">Die Linienbreite ohne Antialiasing kann an einen von der Implementierung abhängigen Höchstwert gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="604be-139">Non-antialiased line width may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="604be-140">Obwohl dieser Höchstwert nicht abgefragt werden kann, darf er nicht kleiner sein als der Maximalwert für Antialiasing-Zeilen, gerundet auf den nächsten ganzzahligen Wert.</span><span class="sxs-lookup"><span data-stu-id="604be-140">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased lines, rounded to the nearest integer value.</span></span>

<span data-ttu-id="604be-141">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glLineWidth** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="604be-141">The following functions retrieve information related to **glLineWidth**:</span></span>

<span data-ttu-id="604be-142">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Linien \_ Breite</span><span class="sxs-lookup"><span data-stu-id="604be-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_WIDTH</span></span>

<span data-ttu-id="604be-143">**glget** mit Argument GL- \_ Linien \_ Breite \_ Bereich</span><span class="sxs-lookup"><span data-stu-id="604be-143">**glGet** with argument GL\_LINE\_WIDTH\_RANGE</span></span>

<span data-ttu-id="604be-144">**glget** mit Argument GL- \_ Linienstärke \_ \_ Granularität</span><span class="sxs-lookup"><span data-stu-id="604be-144">**glGet** with argument GL\_LINE\_WIDTH\_GRANULARITY</span></span>

<span data-ttu-id="604be-145">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ line \_ Smooth</span><span class="sxs-lookup"><span data-stu-id="604be-145">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="604be-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="604be-146">Requirements</span></span>



| <span data-ttu-id="604be-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="604be-147">Requirement</span></span> | <span data-ttu-id="604be-148">Wert</span><span class="sxs-lookup"><span data-stu-id="604be-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="604be-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="604be-149">Minimum supported client</span></span><br/> | <span data-ttu-id="604be-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="604be-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="604be-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="604be-151">Minimum supported server</span></span><br/> | <span data-ttu-id="604be-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="604be-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="604be-153">Header</span><span class="sxs-lookup"><span data-stu-id="604be-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="604be-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="604be-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="604be-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="604be-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="604be-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="604be-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="604be-157">DLL</span><span class="sxs-lookup"><span data-stu-id="604be-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="604be-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="604be-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="604be-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="604be-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="604be-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="604be-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="604be-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="604be-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="604be-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="604be-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="604be-163">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="604be-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





