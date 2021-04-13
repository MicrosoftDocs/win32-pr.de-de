---
title: gldepthrange-Funktion (GL. h)
description: Die Funktion "gldepthrange" gibt die Zuordnung von z-Werten von normalisierten Geräte Koordinaten zu Fenster Koordinaten an.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- gldepthrange-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391710"
---
# <a name="gldepthrange-function"></a><span data-ttu-id="bcfe9-104">gldepthrange-Funktion</span><span class="sxs-lookup"><span data-stu-id="bcfe9-104">glDepthRange function</span></span>

<span data-ttu-id="bcfe9-105">Die Funktion " **gldepthrange** " gibt die Zuordnung von *z* -Werten von normalisierten Geräte Koordinaten zu Fenster Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-105">The **glDepthRange** function specifies the mapping of *z* values from normalized device coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcfe9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcfe9-106">Syntax</span></span>


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a><span data-ttu-id="bcfe9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcfe9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcfe9-108">*znear*</span><span class="sxs-lookup"><span data-stu-id="bcfe9-108">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="bcfe9-109">Die Zuordnung der Near Clipping-Ebene zu Fenster Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-109">The mapping of the near clipping plane to window coordinates.</span></span> <span data-ttu-id="bcfe9-110">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bcfe9-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="bcfe9-111">*zfar*</span><span class="sxs-lookup"><span data-stu-id="bcfe9-111">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="bcfe9-112">Die Zuordnung der weit entfernten Clippingebene zu den Fenster Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-112">The mapping of the far clipping plane to window coordinates.</span></span> <span data-ttu-id="bcfe9-113">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-113">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcfe9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bcfe9-114">Return value</span></span>

<span data-ttu-id="bcfe9-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bcfe9-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bcfe9-116">Error codes</span></span>

<span data-ttu-id="bcfe9-117">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bcfe9-118">Name</span><span class="sxs-lookup"><span data-stu-id="bcfe9-118">Name</span></span>                                                                                                  | <span data-ttu-id="bcfe9-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bcfe9-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bcfe9-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="bcfe9-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bcfe9-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bcfe9-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcfe9-122">Remarks</span></span>

<span data-ttu-id="bcfe9-123">Nach dem Abschneiden und der Division durch *w* reichen die *z* -Koordinaten zwischen 0,0 und 1,0. Dies entspricht den Near-und Far-Clipping-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-123">After clipping and division by *w*, *z* -coordinates range from 0.0 to 1.0, corresponding to the near and far clipping planes.</span></span> <span data-ttu-id="bcfe9-124">Die Funktion " **gldepthrange** " gibt eine lineare Zuordnung der normalisierten *z*-Koordinaten in diesem Bereich zu Windows *z*-Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-124">The **glDepthRange** function specifies a linear mapping of the normalized *z*-coordinates in this range to window *z*-coordinates.</span></span> <span data-ttu-id="bcfe9-125">Unabhängig von der tatsächlichen tiefen Puffer Implementierung werden Fenster Koordinaten tiefen Werte so behandelt, als wären Sie von 0,0 bis 1,0 (z. b. Farbkomponenten).</span><span class="sxs-lookup"><span data-stu-id="bcfe9-125">Regardless of the actual depth buffer implementation, window coordinate depth values are treated as though they range from 0.0 through 1.0 (like color components).</span></span> <span data-ttu-id="bcfe9-126">Folglich werden die von **gldepthrange** akzeptierten Werte an diesen Bereich gebunden, bevor Sie akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-126">Thus, the values accepted by **glDepthRange** are both clamped to this range before they are accepted.</span></span>

<span data-ttu-id="bcfe9-127">Die Standard Zuordnung von (0,0) ordnet die Near-Ebene 0 und die weite Ebene 1 zu.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-127">The default mapping of (0,1) maps the near plane to 0 and the far plane to 1.</span></span> <span data-ttu-id="bcfe9-128">Mit dieser Zuordnung wird der tiefen Pufferbereich vollständig genutzt.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-128">With this mapping, the depth buffer range is fully utilized.</span></span>

<span data-ttu-id="bcfe9-129">Es ist nicht erforderlich, dass *znear* kleiner als *zfar* ist.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-129">It is not necessary that *zNear* be less than *zFar*.</span></span> <span data-ttu-id="bcfe9-130">Umgekehrte Zuordnungen wie (1, 0) sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-130">Reverse mappings such as (1,0) are acceptable.</span></span>

<span data-ttu-id="bcfe9-131">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gldepthrange** ab:</span><span class="sxs-lookup"><span data-stu-id="bcfe9-131">The following function retrieves information related to **glDepthRange**:</span></span>

<span data-ttu-id="bcfe9-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ tiefen \_ Bereich</span><span class="sxs-lookup"><span data-stu-id="bcfe9-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_RANGE</span></span>

## <a name="requirements"></a><span data-ttu-id="bcfe9-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcfe9-133">Requirements</span></span>



| <span data-ttu-id="bcfe9-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcfe9-134">Requirement</span></span> | <span data-ttu-id="bcfe9-135">Wert</span><span class="sxs-lookup"><span data-stu-id="bcfe9-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcfe9-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bcfe9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bcfe9-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcfe9-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bcfe9-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bcfe9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bcfe9-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcfe9-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bcfe9-140">Header</span><span class="sxs-lookup"><span data-stu-id="bcfe9-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcfe9-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcfe9-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bcfe9-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bcfe9-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="bcfe9-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcfe9-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bcfe9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="bcfe9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcfe9-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcfe9-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcfe9-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcfe9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcfe9-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bcfe9-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bcfe9-148">**gldepthfunc**</span><span class="sxs-lookup"><span data-stu-id="bcfe9-148">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="bcfe9-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bcfe9-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bcfe9-150">**glget**</span><span class="sxs-lookup"><span data-stu-id="bcfe9-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="bcfe9-151">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="bcfe9-151">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





