---
title: gluloadsamplingmatrices-Funktion (glu. h)
description: Die Funktion "gluloadsamplingmatrices" lädt nicht einheitliche, nicht einheitliche Rational B-Spline (NURBS)-samplingmatrizen.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluloadsamplingmatrices-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337311"
---
# <a name="gluloadsamplingmatrices-function"></a><span data-ttu-id="d5c68-104">gluloadsamplingmatrices-Funktion</span><span class="sxs-lookup"><span data-stu-id="d5c68-104">gluLoadSamplingMatrices function</span></span>

<span data-ttu-id="d5c68-105">Die Funktion " **gluloadsamplingmatrices** " lädt nicht einheitliche, nicht einheitliche Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))-samplingmatrizen.</span><span class="sxs-lookup"><span data-stu-id="d5c68-105">The **gluLoadSamplingMatrices** function loads Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) sampling and culling matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c68-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5c68-106">Syntax</span></span>


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="d5c68-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5c68-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c68-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="d5c68-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c68-109">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="d5c68-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d5c68-110">*modelmatrix*</span><span class="sxs-lookup"><span data-stu-id="d5c68-110">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c68-111">Eine Modelview-Matrix (wie bei einem [**glgetfloatv**](glgetfloatv.md) -Befehl).</span><span class="sxs-lookup"><span data-stu-id="d5c68-111">A modelview matrix (as from a [**glGetFloatv**](glgetfloatv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="d5c68-112">*projmatrix*</span><span class="sxs-lookup"><span data-stu-id="d5c68-112">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c68-113">Eine Projektions Matrix (wie bei einem **glgetfloatv** -Befehl).</span><span class="sxs-lookup"><span data-stu-id="d5c68-113">A projection matrix (as from a **glGetFloatv** call).</span></span>

</dd> <dt>

<span data-ttu-id="d5c68-114">*Viewport*</span><span class="sxs-lookup"><span data-stu-id="d5c68-114">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c68-115">Ein Viewport (wie bei einem [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) -Befehl).</span><span class="sxs-lookup"><span data-stu-id="d5c68-115">A viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c68-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5c68-116">Return value</span></span>

<span data-ttu-id="d5c68-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d5c68-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c68-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5c68-118">Remarks</span></span>

<span data-ttu-id="d5c68-119">Die Funktion " **gluloadsamplingmatrices** " verwendet " *modelmatrix*", " *projmatrix*" und "Viewport", um die in *nobj* gespeicherten samplingund immatrixmatrizen neu zu berechnen. </span><span class="sxs-lookup"><span data-stu-id="d5c68-119">The **gluLoadSamplingMatrices** function uses *modelMatrix*, *projMatrix*, and *viewport* to recompute the sampling and culling matrices stored in *nobj*.</span></span> <span data-ttu-id="d5c68-120">Die Stichproben Matrix bestimmt, wie gut eine nursb-Kurve oder-Oberfläche im Mosaik Prozess berücksichtigt werden muss, um die Stichproben Toleranz zu erfüllen (wie durch die Eigenschaft für die- \_ Stichproben \_ Toleranz bestimmt).</span><span class="sxs-lookup"><span data-stu-id="d5c68-120">The sampling matrix determines how finely a NURBS curve or surface must be tessellated to satisfy the sampling tolerance (as determined by the GLU\_SAMPLING\_TOLERANCE property).</span></span> <span data-ttu-id="d5c68-121">Die culult-Matrix wird bei der Entscheidung verwendet, ob eine nursb-Kurve oder-Oberfläche vor dem Rendern vor dem Rendering (bei aktivierter \_ engisteringeigenschaft) gekettet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5c68-121">The culling matrix is used in deciding if a NURBS curve or surface should be culled before rendering (when the GLU\_CULLING property is turned on).</span></span>

<span data-ttu-id="d5c68-122">Die Funktion " **gluloadsamplingmatrices** " ist nur erforderlich, wenn die "glu \_ \_ autoload Matrix"- \_ Eigenschaft ausgeschaltet ist (siehe [**glunurbsproperty**](glunurbsproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="d5c68-122">The **gluLoadSamplingMatrices** function is necessary only if the GLU\_AUTO\_LOAD\_MATRIX property is turned off (see [**gluNurbsProperty**](glunurbsproperty.md)).</span></span> <span data-ttu-id="d5c68-123">Obwohl es sinnvoll sein kann, die Eigenschaften für die \_ Automatische Load-Matrix von Glu zu aktivieren \_ \_ , erfordert dies einen Roundtrip zum OpenGL-Server, um die aktuellen Werte der Modelview-Matrix, der Projektions Matrix und des Viewports abzurufen.)</span><span class="sxs-lookup"><span data-stu-id="d5c68-123">Although it can be convenient to leave the GLU\_AUTO\_LOAD\_MATRIX property turned on, doing so necessitates a round trip to the OpenGL server to get the current values of the modelview matrix, projection matrix, and viewport.)</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c68-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5c68-124">Requirements</span></span>



| <span data-ttu-id="d5c68-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5c68-125">Requirement</span></span> | <span data-ttu-id="d5c68-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c68-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c68-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5c68-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c68-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5c68-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d5c68-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5c68-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c68-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5c68-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d5c68-131">Header</span><span class="sxs-lookup"><span data-stu-id="d5c68-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c68-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c68-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d5c68-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5c68-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5c68-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5c68-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5c68-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d5c68-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5c68-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c68-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c68-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5c68-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c68-138">**glgetfloatv**</span><span class="sxs-lookup"><span data-stu-id="d5c68-138">**glGetFloatv**</span></span>](glgetfloatv.md)
</dt> <dt>

[<span data-ttu-id="d5c68-139">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="d5c68-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="d5c68-140">**glugetnurbsproperty**</span><span class="sxs-lookup"><span data-stu-id="d5c68-140">**gluGetNurbsProperty**</span></span>](glugetnurbsproperty.md)
</dt> <dt>

[<span data-ttu-id="d5c68-141">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="d5c68-141">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





