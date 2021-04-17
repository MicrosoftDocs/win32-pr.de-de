---
title: glViewport-Funktion (GL. h)
description: Die Funktion "glViewport" legt den Viewport fest.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- glViewport-Funktion OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104559284"
---
# <a name="glviewport-function"></a><span data-ttu-id="a3a32-104">glViewport-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3a32-104">glViewport function</span></span>

<span data-ttu-id="a3a32-105">Die Funktion " **glViewport** " legt den Viewport fest.</span><span class="sxs-lookup"><span data-stu-id="a3a32-105">The **glViewport** function sets the viewport.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a32-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3a32-106">Syntax</span></span>


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="a3a32-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3a32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3a32-108">*x*</span><span class="sxs-lookup"><span data-stu-id="a3a32-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a3a32-109">Die linke untere Ecke des Viewportrechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a3a32-109">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="a3a32-110">Der Standardwert ist (0,0).</span><span class="sxs-lookup"><span data-stu-id="a3a32-110">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="a3a32-111">*y*</span><span class="sxs-lookup"><span data-stu-id="a3a32-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a3a32-112">Die linke untere Ecke des Viewportrechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a3a32-112">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="a3a32-113">Der Standardwert ist (0,0).</span><span class="sxs-lookup"><span data-stu-id="a3a32-113">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="a3a32-114">*width*</span><span class="sxs-lookup"><span data-stu-id="a3a32-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="a3a32-115">Die Breite des Viewports.</span><span class="sxs-lookup"><span data-stu-id="a3a32-115">The width of the viewport.</span></span> <span data-ttu-id="a3a32-116">Wenn ein OpenGL-Kontext zum ersten Mal an ein Fenster angefügt wird, werden *Breite* und *Höhe* auf die Abmessungen dieses Fensters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a3a32-116">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> <dt>

<span data-ttu-id="a3a32-117">*height*</span><span class="sxs-lookup"><span data-stu-id="a3a32-117">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="a3a32-118">Die Höhe des Viewports.</span><span class="sxs-lookup"><span data-stu-id="a3a32-118">The height of the viewport.</span></span> <span data-ttu-id="a3a32-119">Wenn ein OpenGL-Kontext zum ersten Mal an ein Fenster angefügt wird, werden *Breite* und *Höhe* auf die Abmessungen dieses Fensters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a3a32-119">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3a32-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3a32-120">Return value</span></span>

<span data-ttu-id="a3a32-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3a32-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3a32-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a3a32-122">Error codes</span></span>

<span data-ttu-id="a3a32-123">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a3a32-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a3a32-124">Name</span><span class="sxs-lookup"><span data-stu-id="a3a32-124">Name</span></span>                                                                                                  | <span data-ttu-id="a3a32-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a3a32-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3a32-126"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="a3a32-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a3a32-127">Die *Breite* oder *Höhe* war negativ.</span><span class="sxs-lookup"><span data-stu-id="a3a32-127">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="a3a32-128"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="a3a32-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a3a32-129">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a3a32-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a3a32-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3a32-130">Remarks</span></span>

<span data-ttu-id="a3a32-131">Die Funktion " **glViewport** " gibt die affine Transformation von *x* und *y* von normalisierten Geräte Koordinaten zu Fenster Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="a3a32-131">The **glViewport** function specifies the affine transformation of *x* and *y* from normalized device coordinates to window coordinates.</span></span> <span data-ttu-id="a3a32-132">Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) sind normalisierte Geräte Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="a3a32-132">Let (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) be normalized device coordinates.</span></span> <span data-ttu-id="a3a32-133">Die Fenster Koordinaten (*x*<sub>w</sub> , *y*<sub>w</sub> ) werden dann wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="a3a32-133">The window coordinates (*x*<sub>w</sub> , *y*<sub>w</sub> ) are then computed as follows:</span></span>

![Gleichung, die die Berechnung der Fenster Koordinaten anzeigt.](images/view01.png)

<span data-ttu-id="a3a32-135">Breite und Höhe des Viewports werden automatisch an einen Bereich gebunden, der von der Implementierung abhängt.</span><span class="sxs-lookup"><span data-stu-id="a3a32-135">Viewport width and height are silently clamped to a range that depends on the implementation.</span></span> <span data-ttu-id="a3a32-136">Dieser Bereich wird durch Aufrufen von **glget** mit dem Argument GL \_ Max \_ Viewport \_ DiMS abgefragt.</span><span class="sxs-lookup"><span data-stu-id="a3a32-136">This range is queried by calling **glGet** with argument GL\_MAX\_VIEWPORT\_DIMS.</span></span>

<span data-ttu-id="a3a32-137">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glViewport** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="a3a32-137">The following functions retrieve information related to **glViewport**:</span></span>

<span data-ttu-id="a3a32-138">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Viewport</span><span class="sxs-lookup"><span data-stu-id="a3a32-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VIEWPORT</span></span>

<span data-ttu-id="a3a32-139">**glget** mit dem Argument GL \_ Max \_ Viewport \_ DiMS</span><span class="sxs-lookup"><span data-stu-id="a3a32-139">**glGet** with argument GL\_MAX\_VIEWPORT\_DIMS</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a32-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3a32-140">Requirements</span></span>



| <span data-ttu-id="a3a32-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3a32-141">Requirement</span></span> | <span data-ttu-id="a3a32-142">Wert</span><span class="sxs-lookup"><span data-stu-id="a3a32-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a32-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3a32-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a32-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3a32-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a3a32-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3a32-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a32-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3a32-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3a32-147">Header</span><span class="sxs-lookup"><span data-stu-id="a3a32-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3a32-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3a32-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a3a32-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3a32-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3a32-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3a32-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3a32-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a3a32-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3a32-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3a32-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3a32-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3a32-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a32-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a3a32-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a3a32-155">**gldepthrange**</span><span class="sxs-lookup"><span data-stu-id="a3a32-155">**glDepthRange**</span></span>](gldepthrange.md)
</dt> </dl>

 

 





