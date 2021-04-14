---
title: glpolygonoffset-Funktion (GL. h)
description: Die Funktion "glpolygonoffset" legt die Skala und Einheiten fest, die OpenGL zum Berechnen von tiefen Werten verwendet.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glpolygonoffset-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391989"
---
# <a name="glpolygonoffset-function"></a><span data-ttu-id="9237b-104">glpolygonoffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="9237b-104">glPolygonOffset function</span></span>

<span data-ttu-id="9237b-105">Die Funktion " **glpolygonoffset** " legt die Skala und Einheiten fest, die OpenGL zum Berechnen von tiefen Werten verwendet.</span><span class="sxs-lookup"><span data-stu-id="9237b-105">The **glPolygonOffset** function sets the scale and units OpenGL uses to calculate depth values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9237b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9237b-106">Syntax</span></span>


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a><span data-ttu-id="9237b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9237b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9237b-108">*gebend*</span><span class="sxs-lookup"><span data-stu-id="9237b-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="9237b-109">Gibt einen Skalierungsfaktor an, der zum Erstellen eines Variablen tiefen Offsets für jedes Polygon verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9237b-109">Specifies a scale factor that is used to create a variable depth offset for each polygon.</span></span> <span data-ttu-id="9237b-110">Der Anfangswert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9237b-110">The initial value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="9237b-111">*Einrichtungen*</span><span class="sxs-lookup"><span data-stu-id="9237b-111">*units*</span></span> 
</dt> <dd>

<span data-ttu-id="9237b-112">Gibt einen Wert an, der mit einem Implementierungs spezifischen Wert multipliziert wird, um einen konstanten tiefen Offset zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9237b-112">Specifies a value that is multiplied by an implementation-specific value to create a constant depth offset.</span></span> <span data-ttu-id="9237b-113">Der Anfangswert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9237b-113">The initial value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9237b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9237b-114">Return value</span></span>

<span data-ttu-id="9237b-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9237b-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9237b-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9237b-116">Error codes</span></span>

<span data-ttu-id="9237b-117">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9237b-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9237b-118">Name</span><span class="sxs-lookup"><span data-stu-id="9237b-118">Name</span></span>                                                                                                  | <span data-ttu-id="9237b-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9237b-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9237b-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="9237b-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9237b-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9237b-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9237b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9237b-122">Remarks</span></span>

<span data-ttu-id="9237b-123">Wenn \_ der GL \_ -Polygon Offset aktiviert ist, wird der tiefen Wert jedes Fragments versetzt, nachdem er von den tiefen Werten der entsprechenden Scheitel Punkte interpoliert wurde.</span><span class="sxs-lookup"><span data-stu-id="9237b-123">When GL\_POLYGON\_OFFSET is enabled, each fragment's depth value will be offset after it is interpolated from the depth values of the appropriate vertices.</span></span> <span data-ttu-id="9237b-124">Der Wert des Offsets ist *Factor* \* ? z + r- \* *Einheiten*, wobei? z eine Maßeinheit für die Tiefe der Änderung relativ zum Bildschirmbereich des Polygons ist, und r ist der kleinste Wert, der garantiert einen auflösbaren Offset für eine bestimmte Implementierung erzeugt.</span><span class="sxs-lookup"><span data-stu-id="9237b-124">The value of the offset is *factor* \* ?z + r \**units*, where ?z is a measurement of the change in depth relative to the screen area of the polygon, and r is the smallest value that is guaranteed to produce a resolvable offset for a given implementation.</span></span> <span data-ttu-id="9237b-125">Der Offset wird hinzugefügt, bevor der tiefen Test durchgeführt wird und bevor der Wert in den tiefen Puffer geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="9237b-125">The offset is added before the depth test is performed and before the value is written into the depth buffer.</span></span>

<span data-ttu-id="9237b-126">Die Funktion " **glpolygonoffset** " eignet sich zum Rendern von ausgeblendeten Bildern, zum Anwenden von decds auf Oberflächen und zum Rendern von Festplatten mit hervorgehobenen Kanten.</span><span class="sxs-lookup"><span data-stu-id="9237b-126">The **glPolygonOffset** function is useful for rendering hidden-line images, for applying decals to surfaces, and for rendering solids with highlighted edges.</span></span>

<span data-ttu-id="9237b-127">Die Funktion " **glpolygonoffset** " hat keine Auswirkung auf die tiefen Koordinaten, die im Feedback Puffer abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9237b-127">The **glPolygonOffset** function has no effect on depth coordinates placed in the feedback buffer.</span></span> <span data-ttu-id="9237b-128">Außerdem hat es keine Auswirkung auf die Auswahl.</span><span class="sxs-lookup"><span data-stu-id="9237b-128">It also has no effect on selection.</span></span>

<span data-ttu-id="9237b-129">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpolygonoffset** ab:</span><span class="sxs-lookup"><span data-stu-id="9237b-129">The following functions retrieve information related to **glPolygonOffset**:</span></span>

-   <span data-ttu-id="9237b-130">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Polygon- \_ Offset \_ Faktor</span><span class="sxs-lookup"><span data-stu-id="9237b-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_FACTOR</span></span>
-   <span data-ttu-id="9237b-131">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Polygon- \_ Offset \_ Einheiten</span><span class="sxs-lookup"><span data-stu-id="9237b-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_UNITS</span></span>
-   <span data-ttu-id="9237b-132">[**glisenabled**](glisenabled.md) mit Argument GL \_ Polygon \_ Offset \_ Fill</span><span class="sxs-lookup"><span data-stu-id="9237b-132">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_FILL</span></span>
-   <span data-ttu-id="9237b-133">[**glisenabled**](glisenabled.md) mit Argument GL \_ Polygon- \_ Versatz \_ Linie</span><span class="sxs-lookup"><span data-stu-id="9237b-133">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_LINE</span></span>
-   <span data-ttu-id="9237b-134">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Polygon \_ Offset \_ Point</span><span class="sxs-lookup"><span data-stu-id="9237b-134">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_POINT</span></span>

> [!Note]  
> <span data-ttu-id="9237b-135">Die Funktion " **glpolygonoffset** " ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9237b-135">The **glPolygonOffset** function is only available in OpenGl version 1.1 or greater.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9237b-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9237b-136">Requirements</span></span>



| <span data-ttu-id="9237b-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9237b-137">Requirement</span></span> | <span data-ttu-id="9237b-138">Wert</span><span class="sxs-lookup"><span data-stu-id="9237b-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9237b-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9237b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9237b-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9237b-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9237b-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9237b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9237b-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9237b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9237b-143">Header</span><span class="sxs-lookup"><span data-stu-id="9237b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9237b-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9237b-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9237b-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9237b-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="9237b-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9237b-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9237b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9237b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9237b-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9237b-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9237b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9237b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9237b-150">**gldepthfunc**</span><span class="sxs-lookup"><span data-stu-id="9237b-150">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="9237b-151">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="9237b-151">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="9237b-152">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="9237b-152">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="9237b-153">**glget**</span><span class="sxs-lookup"><span data-stu-id="9237b-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9237b-154">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="9237b-154">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="9237b-155">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="9237b-155">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="9237b-156">**glstencilop**</span><span class="sxs-lookup"><span data-stu-id="9237b-156">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="9237b-157">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="9237b-157">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





