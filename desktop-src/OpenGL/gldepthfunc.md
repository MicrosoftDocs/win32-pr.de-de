---
title: gldepthfunc-Funktion (GL. h)
description: Die Funktion "gldepthfunc" gibt den Wert an, der für tiefen Puffer Vergleiche verwendet wird.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- gldepthfunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475843"
---
# <a name="gldepthfunc-function"></a><span data-ttu-id="6c4d1-104">gldepthfunc-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c4d1-104">glDepthFunc function</span></span>

<span data-ttu-id="6c4d1-105">Die Funktion " **gldepthfunc** " gibt den Wert an, der für tiefen Puffer Vergleiche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-105">The **glDepthFunc** function specifies the value used for depth-buffer comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4d1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c4d1-106">Syntax</span></span>


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a><span data-ttu-id="6c4d1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c4d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4d1-108">*func*</span><span class="sxs-lookup"><span data-stu-id="6c4d1-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4d1-109">Gibt die Tiefe Vergleichsfunktion an.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-109">Specifies the depth-comparison function.</span></span> <span data-ttu-id="6c4d1-110">Die folgenden symbolischen Konstanten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-110">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="6c4d1-111">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4d1-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="6c4d1-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6c4d1-112">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="6c4d1-113"><dt>**GL \_ nie**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="6c4d1-114">Läuft nie ab.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-114">Never passes.</span></span><br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="6c4d1-115"><dt>**GL \_ weniger**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="6c4d1-116">Übergibt, wenn der eingehende *z* -Wert kleiner als der gespeicherte *z* -Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-116">Passes if the incoming *z* value is less than the stored *z* value.</span></span> <span data-ttu-id="6c4d1-117">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-117">This is the default value.</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="6c4d1-118"><dt>**GL \_ lequal**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-118"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="6c4d1-119">Übergibt, wenn der eingehende z-Wert kleiner oder gleich dem gespeicherten z-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-119">Passes if the incoming z value is less than or equal to the stored z value.</span></span><br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="6c4d1-120"><dt>**GL \_ gleich**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-120"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="6c4d1-121">Übergibt, wenn der eingehende z-Wert gleich dem gespeicherten z-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-121">Passes if the incoming z value is equal to the stored z value.</span></span><br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="6c4d1-122"><dt>**GL \_ größer**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-122"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="6c4d1-123">Übergibt, wenn der eingehende z-Wert größer als der gespeicherte z-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-123">Passes if the incoming z value is greater than the stored z value.</span></span><br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="6c4d1-124"><dt>**GL- \_ NotEqual**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-124"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="6c4d1-125">Übergibt, wenn der eingehende z-Wert nicht gleich dem gespeicherten z-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-125">Passes if the incoming z value is not equal to the stored z value.</span></span><br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="6c4d1-126"><dt>**GL \_ gequal**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-126"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="6c4d1-127">Übergibt, wenn der eingehende z-Wert größer oder gleich dem gespeicherten z-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-127">Passes if the incoming z value is greater than or equal to the stored z value.</span></span><br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="6c4d1-128"><dt>**immer GL. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="6c4d1-129">Übergibt immer.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-129">Always passes.</span></span><br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c4d1-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c4d1-130">Return value</span></span>

<span data-ttu-id="6c4d1-131">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6c4d1-132">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6c4d1-132">Error codes</span></span>

<span data-ttu-id="6c4d1-133">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-133">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6c4d1-134">Name</span><span class="sxs-lookup"><span data-stu-id="6c4d1-134">Name</span></span>                                                                                                  | <span data-ttu-id="6c4d1-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6c4d1-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c4d1-136"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6c4d1-137">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6c4d1-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c4d1-138">Remarks</span></span>

<span data-ttu-id="6c4d1-139">Die Funktion " **gldepthfunc** " gibt die Funktion an, mit der die einzelnen eingehenden Pixel- *z* -Werte mit dem im tiefen Puffer vorhandenen *z* -Wert verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-139">The **glDepthFunc** function specifies the function used to compare each incoming pixel *z* value with the *z* value present in the depth buffer.</span></span> <span data-ttu-id="6c4d1-140">Der Vergleich wird nur durchgeführt, wenn tiefen Tests aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-140">The comparison is performed only if depth testing is enabled.</span></span> <span data-ttu-id="6c4d1-141">(Siehe [**glEnable**](glenable.md) mit dem Argument GL \_ . tiefen \_ Test.)</span><span class="sxs-lookup"><span data-stu-id="6c4d1-141">(See [**glEnable**](glenable.md) with the argument GL\_DEPTH\_TEST.)</span></span>

<span data-ttu-id="6c4d1-142">Zunächst sind die tiefen Tests deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c4d1-142">Initially, depth testing is disabled.</span></span>

<span data-ttu-id="6c4d1-143">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **gldepthfunc** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="6c4d1-143">The following functions retrieve information related to **glDepthFunc**:</span></span>

<span data-ttu-id="6c4d1-144">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Tiefe \_ Func</span><span class="sxs-lookup"><span data-stu-id="6c4d1-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_FUNC</span></span>

<span data-ttu-id="6c4d1-145">[**glisenabled**](glisenabled.md) mit dem Argument GL- \_ tiefen \_ Test</span><span class="sxs-lookup"><span data-stu-id="6c4d1-145">[**glIsEnabled**](glisenabled.md) with argument GL\_DEPTH\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="6c4d1-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c4d1-146">Requirements</span></span>



| <span data-ttu-id="6c4d1-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c4d1-147">Requirement</span></span> | <span data-ttu-id="6c4d1-148">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4d1-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4d1-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c4d1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6c4d1-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c4d1-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6c4d1-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c4d1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6c4d1-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c4d1-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c4d1-153">Header</span><span class="sxs-lookup"><span data-stu-id="6c4d1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c4d1-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6c4d1-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c4d1-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c4d1-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c4d1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6c4d1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c4d1-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c4d1-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c4d1-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c4d1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4d1-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6c4d1-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6c4d1-161">**gldepthrange**</span><span class="sxs-lookup"><span data-stu-id="6c4d1-161">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="6c4d1-162">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="6c4d1-162">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="6c4d1-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6c4d1-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6c4d1-164">**glget**</span><span class="sxs-lookup"><span data-stu-id="6c4d1-164">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6c4d1-165">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="6c4d1-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





