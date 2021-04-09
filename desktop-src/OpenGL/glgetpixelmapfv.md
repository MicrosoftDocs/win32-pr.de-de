---
title: glgetpixelmapfv-Funktion (GL. h)
description: Die Funktionen "glgetpixelmapfv", "glgetpixelmapuiv" und "glgetpixelmapusv" geben die angegebene Pixel Map zurück. | glgetpixelmapfv-Funktion (GL. h)
ms.assetid: b09f4799-8e36-4d4f-90d8-4a8ed3d15718
keywords:
- glgetpixelmapfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f73fb817c347832dfc6a09636173641e5c869b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869783"
---
# <a name="glgetpixelmapfv-function"></a><span data-ttu-id="192e7-105">glgetpixelmapfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="192e7-105">glGetPixelMapfv function</span></span>

<span data-ttu-id="192e7-106">Die Funktionen " **glgetpixelmapfv**", " [**glgetpixelmapuiv**](glgetpixelmapuiv.md)" und " [**glgetpixelmapusv**](glgetpixelmapusv.md) " geben die angegebene Pixel Map zurück.</span><span class="sxs-lookup"><span data-stu-id="192e7-106">The **glGetPixelMapfv**, [**glGetPixelMapuiv**](glgetpixelmapuiv.md), and [**glGetPixelMapusv**](glgetpixelmapusv.md) functions return the specified pixel map.</span></span>

## <a name="syntax"></a><span data-ttu-id="192e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="192e7-107">Syntax</span></span>


```C++
void WINAPI glGetPixelMapfv(
   GLenum  map,
   GLfloat *values
);
```



## <a name="parameters"></a><span data-ttu-id="192e7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="192e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="192e7-109">*map*</span><span class="sxs-lookup"><span data-stu-id="192e7-109">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="192e7-110">Der Name der zurück zugebende Pixel Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="192e7-110">The name of the pixel map to return.</span></span> <span data-ttu-id="192e7-111">Akzeptierte Werte sind GL \_ Pixel \_ map \_ i \_ to \_ i, GL \_ Pixel \_ map \_ s \_ to \_ s, GL \_ Pixel \_ map \_ i \_ to \_ r, GL \_ Pixel \_ map \_ i \_ to \_ g, GL \_ Pixel \_ map \_ i \_ to \_ b, GL \_ Pixel \_ map \_ i \_ to \_ a, GL \_ Pixel \_ map \_ r \_ to \_ r, GL \_ Pixel \_ map \_ g \_ to \_ G, GL \_ Pixel \_ map \_ b \_ to \_ b und GL \_ Pixel \_ map \_ a \_ to \_ a.</span><span class="sxs-lookup"><span data-stu-id="192e7-111">Accepted values are GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, GL\_PIXEL\_MAP\_I\_TO\_A, GL\_PIXEL\_MAP\_R\_TO\_R, GL\_PIXEL\_MAP\_G\_TO\_G, GL\_PIXEL\_MAP\_B\_TO\_B, and GL\_PIXEL\_MAP\_A\_TO\_A.</span></span>

</dd> <dt>

<span data-ttu-id="192e7-112">*Werte*</span><span class="sxs-lookup"><span data-stu-id="192e7-112">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="192e7-113">Gibt den Pixel Karteninhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="192e7-113">Returns the pixel map contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="192e7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="192e7-114">Return value</span></span>

<span data-ttu-id="192e7-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="192e7-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="192e7-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="192e7-116">Error codes</span></span>

<span data-ttu-id="192e7-117">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="192e7-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="192e7-118">Name</span><span class="sxs-lookup"><span data-stu-id="192e7-118">Name</span></span>                                                                                                  | <span data-ttu-id="192e7-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="192e7-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="192e7-120"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="192e7-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="192e7-121">*map* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="192e7-121">*map* was not an accepted value.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="192e7-122"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="192e7-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="192e7-123">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="192e7-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="192e7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="192e7-124">Remarks</span></span>

<span data-ttu-id="192e7-125">Eine Beschreibung der zulässigen Werte für den *map* -Parameter finden Sie unter [**glpixelmap**](glpixelmap.md) .</span><span class="sxs-lookup"><span data-stu-id="192e7-125">See [**glPixelMap**](glpixelmap.md) for a description of the acceptable values for the *map* parameter.</span></span> <span data-ttu-id="192e7-126">Die **glgetpixelmap** -Funktion gibt den Inhalt der in *map* angegebenen Pixel Zuordnung in den *Werten* zurück.</span><span class="sxs-lookup"><span data-stu-id="192e7-126">The **glGetPixelMap** function returns in *values* the contents of the pixel map specified in *map*.</span></span> <span data-ttu-id="192e7-127">Verwenden Sie Pixel Zuordnungen während der Ausführung von [**glread Pixel**](glreadpixels.md), [**gldrawpixels**](gldrawpixels.md), [**glcopypixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)und [**glTexImage2D**](glteximage2d.md) , um Farbindizes, Schablone-Indizes, Farbkomponenten und tiefen Komponenten anderen Werten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="192e7-127">Use pixel maps during the execution of [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md), and [**glTexImage2D**](glteximage2d.md) to map color indexes, stencil indexes, color components, and depth components to other values.</span></span>

<span data-ttu-id="192e7-128">Ganzzahlige Werte ohne Vorzeichen werden, falls angefordert, linear aus der internen Fixed-oder Gleit Komma Darstellung zugeordnet, sodass 1,0 dem größten darstellbaren ganzzahligen Wert zugeordnet ist und 0,0 0 (null) zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="192e7-128">Unsigned integer values, if requested, are linearly mapped from the internal fixed or floating-point representation such that 1.0 maps to the largest representable integer value, and 0.0 maps to zero.</span></span> <span data-ttu-id="192e7-129">Die Rückgabe ganzzahliger Werte ohne Vorzeichen sind nicht definiert, wenn der Zuordnungs Wert nicht im Bereich von \[ 0, 1 liegt \] .</span><span class="sxs-lookup"><span data-stu-id="192e7-129">Return unsigned integer values are undefined if the map value was not in the range \[0,1\].</span></span>

<span data-ttu-id="192e7-130">Um die erforderliche Größe von *map* zu ermitteln, nennen [**Sie glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der entsprechenden symbolischen Konstante.</span><span class="sxs-lookup"><span data-stu-id="192e7-130">To determine the required size of *map*, call [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with the appropriate symbolic constant.</span></span>

<span data-ttu-id="192e7-131">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der *Werte* vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="192e7-131">If an error is generated, no change is made to the contents of *values*.</span></span>

<span data-ttu-id="192e7-132">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glgetpixelmap** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="192e7-132">The following functions retrieve information related to **glGetPixelMap**:</span></span>

<span data-ttu-id="192e7-133">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Pixel \_ map \_ i \_ to \_ i \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="192e7-134">**glget** mit dem Argument GL \_ Pixel \_ map \_ s \_ to \_ s \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-134">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="192e7-135">**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ R \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-135">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="192e7-136">**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ G \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-136">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="192e7-137">**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ B \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-137">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="192e7-138">**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ A \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-138">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="192e7-139">**glget** mit dem Argument GL \_ Pixel \_ map \_ r \_ to \_ r \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-139">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="192e7-140">**glget** mit dem Argument GL \_ Pixel \_ map \_ g \_ bis \_ g \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-140">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="192e7-141">**glget** mit Argument GL \_ Pixel \_ map \_ b \_ bis \_ b \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-141">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="192e7-142">**glget** mit dem Argument GL \_ Pixel \_ map \_ a \_ to \_ a \_ size</span><span class="sxs-lookup"><span data-stu-id="192e7-142">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="192e7-143">**glget** mit dem Argument GL \_ Max \_ Pixel \_ map \_ Table</span><span class="sxs-lookup"><span data-stu-id="192e7-143">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="192e7-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="192e7-144">Requirements</span></span>



| <span data-ttu-id="192e7-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="192e7-145">Requirement</span></span> | <span data-ttu-id="192e7-146">Wert</span><span class="sxs-lookup"><span data-stu-id="192e7-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="192e7-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="192e7-147">Minimum supported client</span></span><br/> | <span data-ttu-id="192e7-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="192e7-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="192e7-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="192e7-149">Minimum supported server</span></span><br/> | <span data-ttu-id="192e7-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="192e7-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="192e7-151">Header</span><span class="sxs-lookup"><span data-stu-id="192e7-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="192e7-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="192e7-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="192e7-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="192e7-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="192e7-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="192e7-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="192e7-155">DLL</span><span class="sxs-lookup"><span data-stu-id="192e7-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="192e7-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="192e7-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="192e7-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="192e7-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="192e7-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="192e7-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="192e7-159">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="192e7-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="192e7-160">**gldrawpixels**</span><span class="sxs-lookup"><span data-stu-id="192e7-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="192e7-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="192e7-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="192e7-162">**glget**</span><span class="sxs-lookup"><span data-stu-id="192e7-162">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="192e7-163">**glpixelmap**</span><span class="sxs-lookup"><span data-stu-id="192e7-163">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="192e7-164">**glpixeltransfer**</span><span class="sxs-lookup"><span data-stu-id="192e7-164">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="192e7-165">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="192e7-165">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="192e7-166">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="192e7-166">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="192e7-167">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="192e7-167">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





