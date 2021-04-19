---
title: glpopattrb-Funktion (GL. h)
description: Springt den Attribut Stapel.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glpopattrb-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338345"
---
# <a name="glpopattrib-function"></a><span data-ttu-id="6c325-104">glpopattrb-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c325-104">glPopAttrib function</span></span>

<span data-ttu-id="6c325-105">Springt den Attribut Stapel.</span><span class="sxs-lookup"><span data-stu-id="6c325-105">Pops the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c325-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c325-106">Syntax</span></span>


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="6c325-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c325-107">Parameters</span></span>

<span data-ttu-id="6c325-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6c325-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c325-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c325-109">Return value</span></span>

<span data-ttu-id="6c325-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6c325-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6c325-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6c325-111">Error codes</span></span>

<span data-ttu-id="6c325-112">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6c325-112">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6c325-113">Name</span><span class="sxs-lookup"><span data-stu-id="6c325-113">Name</span></span>                                                                                                  | <span data-ttu-id="6c325-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6c325-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c325-115"><dt>**GL. \_ Stapel \_ Unterlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="6c325-115"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="6c325-116">Die Funktion wurde aufgerufen, während der Attribut Stapel leer war.</span><span class="sxs-lookup"><span data-stu-id="6c325-116">The function was called while the attribute stack was empty.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="6c325-117"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="6c325-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6c325-118">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6c325-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6c325-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c325-119">Remarks</span></span>

<span data-ttu-id="6c325-120">Die Funktion " [**glpushatpub**](glpushattrib.md) " erfordert ein Argument, eine Maske, die angibt, welche Gruppen von Zustandsvariablen im Attribut Stapel gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c325-120">The [**glPushAttrib**](glpushattrib.md) function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="6c325-121">Symbolische Konstanten werden verwendet, um Bits in der Maske festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6c325-121">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="6c325-122">Der mask-Parameter wird in der Regel von erstellt, **oder** es werden mehrere dieser Konstanten erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c325-122">The mask parameter is typically constructed by **OR** ing several of these constants together.</span></span> <span data-ttu-id="6c325-123">Die besondere Maske GL \_ alle \_ atzb- \_ Bits können zum Speichern aller Stackable-Zustände verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c325-123">The special mask GL\_ALL\_ATTRIB\_BITS can be used to save all stackable states.</span></span>

<span data-ttu-id="6c325-124">Die Funktion " **glpopatpub** " stellt die Werte der Zustandsvariablen wieder her, die mit dem letzten Befehl " [**glpushatpub**](glpushattrib.md) " gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c325-124">The **glPopAttrib** function restores the values of the state variables saved with the last [**glPushAttrib**](glpushattrib.md) command.</span></span> <span data-ttu-id="6c325-125">Die nicht gespeicherten Änderungen bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="6c325-125">Those not saved are left unchanged.</span></span>

<span data-ttu-id="6c325-126">Es ist ein Fehler, Attribute auf einen vollständigen Stapel zu übersetzen oder Attribute aus einem leeren Stapel zu Pop.</span><span class="sxs-lookup"><span data-stu-id="6c325-126">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="6c325-127">In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="6c325-127">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="6c325-128">Der Attribut Stapel ist zunächst leer.</span><span class="sxs-lookup"><span data-stu-id="6c325-128">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="6c325-129">Nicht alle Werte für den OpenGL-Zustand können im Attribut Stapel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6c325-129">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="6c325-130">Beispielsweise können das Pixel Paket und der Debugzustand, der rendermoduszustand und der Status "Select" und "Feedback" nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6c325-130">For example, pixel pack and unpack state, render mode state, and select and feedback state cannot be saved.</span></span>

<span data-ttu-id="6c325-131">Die Tiefe des Attribut Stapels hängt von der Implementierung ab, muss jedoch mindestens 16 sein.</span><span class="sxs-lookup"><span data-stu-id="6c325-131">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="6c325-132">Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glpushatpub**](glpushattrib.md) und **glpopatpub** ab:</span><span class="sxs-lookup"><span data-stu-id="6c325-132">The following functions retrieve information related to [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**:</span></span>

<span data-ttu-id="6c325-133">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ \_ Stapel \_ Tiefe des Argument-GL</span><span class="sxs-lookup"><span data-stu-id="6c325-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="6c325-134">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ maximalen \_ attrb- \_ Stapel \_ Tiefe des Arguments</span><span class="sxs-lookup"><span data-stu-id="6c325-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="6c325-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c325-135">Requirements</span></span>



| <span data-ttu-id="6c325-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c325-136">Requirement</span></span> | <span data-ttu-id="6c325-137">Wert</span><span class="sxs-lookup"><span data-stu-id="6c325-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c325-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c325-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6c325-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c325-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6c325-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c325-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6c325-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c325-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c325-142">Header</span><span class="sxs-lookup"><span data-stu-id="6c325-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c325-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c325-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6c325-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c325-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c325-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c325-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c325-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6c325-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c325-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c325-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c325-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c325-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c325-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6c325-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6c325-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6c325-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6c325-151">**glget**</span><span class="sxs-lookup"><span data-stu-id="6c325-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6c325-152">**glgetclipplane**</span><span class="sxs-lookup"><span data-stu-id="6c325-152">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="6c325-153">**glgeterror**</span><span class="sxs-lookup"><span data-stu-id="6c325-153">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="6c325-154">**glgetlight**</span><span class="sxs-lookup"><span data-stu-id="6c325-154">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="6c325-155">**glgetmap**</span><span class="sxs-lookup"><span data-stu-id="6c325-155">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="6c325-156">**glgetmaterial**</span><span class="sxs-lookup"><span data-stu-id="6c325-156">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="6c325-157">**glgetpixelmap**</span><span class="sxs-lookup"><span data-stu-id="6c325-157">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="6c325-158">**glgetpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="6c325-158">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="6c325-159">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="6c325-159">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="6c325-160">**glgettex-v**</span><span class="sxs-lookup"><span data-stu-id="6c325-160">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="6c325-161">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="6c325-161">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="6c325-162">**glgetteximage**</span><span class="sxs-lookup"><span data-stu-id="6c325-162">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="6c325-163">**glgettexlevelparameter**</span><span class="sxs-lookup"><span data-stu-id="6c325-163">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="6c325-164">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="6c325-164">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="6c325-165">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="6c325-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





