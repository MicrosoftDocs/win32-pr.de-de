---
title: gllinestippel-Funktion (GL. h)
description: Die gllinestippel-Funktion gibt das Zeilen stippingmuster an.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- gllinestippel-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739800"
---
# <a name="gllinestipple-function"></a><span data-ttu-id="d354b-104">gllinestippel-Funktion</span><span class="sxs-lookup"><span data-stu-id="d354b-104">glLineStipple function</span></span>

<span data-ttu-id="d354b-105">Die **gllinestippel** -Funktion gibt das Zeilen stippingmuster an.</span><span class="sxs-lookup"><span data-stu-id="d354b-105">The **glLineStipple** function specifies the line stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="d354b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d354b-106">Syntax</span></span>


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a><span data-ttu-id="d354b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d354b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d354b-108">*gebend*</span><span class="sxs-lookup"><span data-stu-id="d354b-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="d354b-109">Ein Multiplikator für jedes Bit im Zeilen stippingmuster.</span><span class="sxs-lookup"><span data-stu-id="d354b-109">A multiplier for each bit in the line stipple pattern.</span></span> <span data-ttu-id="d354b-110">Wenn der *Faktor* z. b. 3 ist, wird jedes Bit im Muster dreimal verwendet, bevor das nächste Bit im Muster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d354b-110">If *factor* is 3, for example, each bit in the pattern will be used three times before the next bit in the pattern is used.</span></span> <span data-ttu-id="d354b-111">Der *Faktor* Parameter wird an den Bereich \[ 1, 256 und der \] Standardwert auf einen Wert gebunden.</span><span class="sxs-lookup"><span data-stu-id="d354b-111">The *factor* parameter is clamped to the range \[1, 256\] and defaults to one.</span></span>

</dd> <dt>

<span data-ttu-id="d354b-112">*pattern*</span><span class="sxs-lookup"><span data-stu-id="d354b-112">*pattern*</span></span> 
</dt> <dd>

<span data-ttu-id="d354b-113">Eine 16-Bit-Ganzzahl, deren Bitmuster bestimmt, welche Fragmente einer Linie gezeichnet werden, wenn die Linie gerengt wird.</span><span class="sxs-lookup"><span data-stu-id="d354b-113">A 16-bit integer whose bit pattern determines which fragments of a line will be drawn when the line is rasterized.</span></span> <span data-ttu-id="d354b-114">Zuerst wird Bit 0 verwendet, und das Standardmuster ist.</span><span class="sxs-lookup"><span data-stu-id="d354b-114">Bit zero is used first, and the default pattern is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d354b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d354b-115">Return value</span></span>

<span data-ttu-id="d354b-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d354b-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d354b-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d354b-117">Error codes</span></span>

<span data-ttu-id="d354b-118">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d354b-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d354b-119">Name</span><span class="sxs-lookup"><span data-stu-id="d354b-119">Name</span></span>                                                                                                  | <span data-ttu-id="d354b-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d354b-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d354b-121"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="d354b-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d354b-122">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d354b-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d354b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d354b-123">Remarks</span></span>

<span data-ttu-id="d354b-124">Die **gllinestippel** -Funktion gibt das Zeilen stippingmuster an.</span><span class="sxs-lookup"><span data-stu-id="d354b-124">The **glLineStipple** function specifies the line stipple pattern.</span></span> <span data-ttu-id="d354b-125">Zeilen stippling maskiert bestimmte Fragmente, die von der rasterization erzeugt werden. Diese Fragmente werden nicht gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d354b-125">Line stippling masks out certain fragments produced by rasterization; those fragments will not be drawn.</span></span> <span data-ttu-id="d354b-126">Die Maskierung wird durch die Verwendung von drei Parametern erreicht: das Muster *Muster* für 16-Bit-Zeilen Stippel, der Wiederholungs Zähler *Faktor* und ein ganzzahliger stippingzähler *.*</span><span class="sxs-lookup"><span data-stu-id="d354b-126">The masking is achieved by using three parameters: the 16-bit line stipple pattern *pattern*, the repeat count *factor*, and an integer stipple counter *s*.</span></span>

<span data-ttu-id="d354b-127">Der Wert für " *s* " wird auf 0 (null) zurückgesetzt, wenn " [**glBegin**](glbegin.md) " aufgerufen wird und bevor jedes Liniensegment einer **glBegin**(GL \_ Lines)/**glEnd** -Sequenz generiert wird.</span><span class="sxs-lookup"><span data-stu-id="d354b-127">Counter *s* is reset to zero whenever [**glBegin**](glbegin.md) is called, and before each line segment of a **glBegin**(GL\_LINES)/**glEnd** sequence is generated.</span></span> <span data-ttu-id="d354b-128">Sie wird inkrementiert, nachdem jedes Fragment eines Einheiten Bereichs mit einem einzelnen Zeilen Segment generiert wurde, oder nachdem die einzelnen *i* -Fragmente eines *i* -breiten Linien Segments generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d354b-128">It is incremented after each fragment of a unit width aliased line segment is generated, or after each *i* fragments of an *i* width line segment are generated.</span></span> <span data-ttu-id="d354b-129">Die der Anzahl *s* zugeordneten *i* -Fragmente werden maskiert, wenn der *Pattern* -Bit (*s*-  /  *Faktor*) mod 16 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="d354b-129">The *i* fragments associated with count *s* are masked out if *pattern* bit (*s* / *factor*) mod 16 is zero.</span></span> <span data-ttu-id="d354b-130">Andernfalls werden diese Fragmente an den Framebuffer-Puffer gesendet.</span><span class="sxs-lookup"><span data-stu-id="d354b-130">Otherwise these fragments are sent to the framebuffer.</span></span> <span data-ttu-id="d354b-131">Bit 0 (null) des *Musters* ist das am wenigsten bedeutende Bit.</span><span class="sxs-lookup"><span data-stu-id="d354b-131">Bit zero of *pattern* is the least significant bit.</span></span>

<span data-ttu-id="d354b-132">Antialiasing-Zeilen werden als Sequenz von 1X-*breiten* Rechtecke für stippling behandelt.</span><span class="sxs-lookup"><span data-stu-id="d354b-132">Antialiased lines are treated as a sequence of 1x *width* rectangles for purposes of stippling.</span></span> <span data-ttu-id="d354b-133">Die *Rechtecke* sind rasterisiert oder nicht basierend auf der fragmentregel, die für Alias Zeilen beschrieben wird. Sie zählt anstelle von Gruppen von Fragmenten Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="d354b-133">Rectangle *s* is rasterized or not based on the fragment rule described for aliased lines; it counts rectangles rather than groups of fragments.</span></span>

<span data-ttu-id="d354b-134">Das Zeilen stippling ist mit " [**glEnable**](glenable.md) " und " **glEnable** " mit dem Argument "GL \_ Line Stippel" aktiviert oder deaktiviert \_ .</span><span class="sxs-lookup"><span data-stu-id="d354b-134">Line stippling is enabled or disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_STIPPLE.</span></span> <span data-ttu-id="d354b-135">Wenn diese Option aktiviert ist, wird das Zeilen stippingmuster wie oben beschrieben angewendet.</span><span class="sxs-lookup"><span data-stu-id="d354b-135">When enabled, the line stipple pattern is applied as described above.</span></span> <span data-ttu-id="d354b-136">Wenn diese Option deaktiviert ist, ist es so, als ob es sich um das Muster handelt.</span><span class="sxs-lookup"><span data-stu-id="d354b-136">When disabled, it is as if the pattern were all ones.</span></span> <span data-ttu-id="d354b-137">Anfänglich ist das Zeilen stippling deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d354b-137">Initially, line stippling is disabled.</span></span>

<span data-ttu-id="d354b-138">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **gllinestippel** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="d354b-138">The following functions retrieve information related to **glLineStipple**:</span></span>

<span data-ttu-id="d354b-139">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument-GL- \_ Zeilen \_ stippingmuster \_</span><span class="sxs-lookup"><span data-stu-id="d354b-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_STIPPLE\_PATTERN</span></span>

<span data-ttu-id="d354b-140">**glget** mit dem Argument GL \_ Zeilen \_ Stippel \_ Wiederholen</span><span class="sxs-lookup"><span data-stu-id="d354b-140">**glGet** with argument GL\_LINE\_STIPPLE\_REPEAT</span></span>

<span data-ttu-id="d354b-141">[**glisenabled**](glisenabled.md) mit Argument GL- \_ Zeilen \_ Stippel</span><span class="sxs-lookup"><span data-stu-id="d354b-141">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="d354b-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d354b-142">Requirements</span></span>



| <span data-ttu-id="d354b-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d354b-143">Requirement</span></span> | <span data-ttu-id="d354b-144">Wert</span><span class="sxs-lookup"><span data-stu-id="d354b-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d354b-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d354b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d354b-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d354b-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d354b-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d354b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d354b-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d354b-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d354b-149">Header</span><span class="sxs-lookup"><span data-stu-id="d354b-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="d354b-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d354b-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d354b-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d354b-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="d354b-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d354b-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d354b-153">DLL</span><span class="sxs-lookup"><span data-stu-id="d354b-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d354b-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d354b-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d354b-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d354b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d354b-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d354b-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d354b-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d354b-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d354b-158">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="d354b-158">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="d354b-159">**glpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="d354b-159">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





