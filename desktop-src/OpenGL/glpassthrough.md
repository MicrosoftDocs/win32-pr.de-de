---
title: glpassthrough-Funktion (GL. h)
description: Die Funktion "glpassthrough" platziert einen Marker im Feedback Puffer.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glpassthrough-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741136"
---
# <a name="glpassthrough-function"></a><span data-ttu-id="71515-104">glpassthrough-Funktion</span><span class="sxs-lookup"><span data-stu-id="71515-104">glPassThrough function</span></span>

<span data-ttu-id="71515-105">Die Funktion " **glpassthrough** " platziert einen Marker im Feedback Puffer.</span><span class="sxs-lookup"><span data-stu-id="71515-105">The **glPassThrough** function places a marker in the feedback buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="71515-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="71515-106">Syntax</span></span>


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a><span data-ttu-id="71515-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="71515-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71515-108">*token*</span><span class="sxs-lookup"><span data-stu-id="71515-108">*token*</span></span> 
</dt> <dd>

<span data-ttu-id="71515-109">Ein Markerwert, der in den Feedback Puffer eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71515-109">A marker value to be placed in the feedback buffer.</span></span> <span data-ttu-id="71515-110">Dies wird durch den folgenden eindeutigen identifizierenden Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="71515-110">It is indicated with the following unique identifying value.</span></span>



| <span data-ttu-id="71515-111">Wert</span><span class="sxs-lookup"><span data-stu-id="71515-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="71515-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71515-112">Meaning</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <span data-ttu-id="71515-113"><dt>**GL- \_ Pass- \_ through- \_ Token**</dt></span><span class="sxs-lookup"><span data-stu-id="71515-113"><dt>**GL\_PASS\_THROUGH\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="71515-114">Die Reihenfolge der **glpassthrough** -Befehle in Bezug auf die Spezifikation von Grafik primitiven wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="71515-114">The order of **glPassThrough** commands with respect to the specification of graphics primitives is maintained.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71515-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71515-115">Return value</span></span>

<span data-ttu-id="71515-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71515-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71515-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="71515-117">Error codes</span></span>

<span data-ttu-id="71515-118">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71515-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71515-119">Name</span><span class="sxs-lookup"><span data-stu-id="71515-119">Name</span></span>                                                                                                  | <span data-ttu-id="71515-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71515-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71515-121"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="71515-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71515-122">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="71515-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71515-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71515-123">Remarks</span></span>

<span data-ttu-id="71515-124">Feedback ist ein OpenGL-Rendermodus, der durch Aufrufen von [**glrendermode**](glrendermode.md) mit GL-Feedback ausgewählt wird \_ .</span><span class="sxs-lookup"><span data-stu-id="71515-124">Feedback is an OpenGL render mode selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="71515-125">Wenn OpenGL im Feedback Modus ist, werden von der rasterisierung keine Pixel erzeugt.</span><span class="sxs-lookup"><span data-stu-id="71515-125">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="71515-126">Stattdessen werden Informationen über primitive, die gerengt worden wären, von OpenGL an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71515-126">Instead, information about primitives that would have been rasterized is fed back to the application by OpenGL.</span></span> <span data-ttu-id="71515-127">Eine Beschreibung des Feedback Puffers und der darin verwendeten Werte finden Sie unter [**glfeedbackbuffer**](glfeedbackbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="71515-127">See [**glFeedbackBuffer**](glfeedbackbuffer.md) for a description of the feedback buffer and the values in it.</span></span>

<span data-ttu-id="71515-128">Die **glpassthrough** -Funktion fügt einen benutzerdefinierten Marker in den Feedback Puffer ein, wenn er im Feedback Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71515-128">The **glPassThrough** function inserts a user-defined marker in the feedback buffer when it is executed in feedback mode.</span></span> <span data-ttu-id="71515-129">Der *tokenparameter* wird zurückgegeben, als ob es sich um einen primitiven handelt.</span><span class="sxs-lookup"><span data-stu-id="71515-129">The *token* parameter is returned as if it were a primitive.</span></span>

<span data-ttu-id="71515-130">Die **glpassthrough** -Funktion wird ignoriert, wenn OpenGL nicht im Feedback Modus ist.</span><span class="sxs-lookup"><span data-stu-id="71515-130">The **glPassThrough** function is ignored if OpenGL is not in feedback mode.</span></span>

<span data-ttu-id="71515-131">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glpassthrough** ab:</span><span class="sxs-lookup"><span data-stu-id="71515-131">The following function retrieves information related to **glPassThrough**:</span></span>

<span data-ttu-id="71515-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Rendermodus</span><span class="sxs-lookup"><span data-stu-id="71515-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="71515-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71515-133">Requirements</span></span>



| <span data-ttu-id="71515-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71515-134">Requirement</span></span> | <span data-ttu-id="71515-135">Wert</span><span class="sxs-lookup"><span data-stu-id="71515-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71515-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71515-136">Minimum supported client</span></span><br/> | <span data-ttu-id="71515-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71515-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71515-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71515-138">Minimum supported server</span></span><br/> | <span data-ttu-id="71515-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71515-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71515-140">Header</span><span class="sxs-lookup"><span data-stu-id="71515-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="71515-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71515-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71515-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71515-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="71515-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71515-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71515-144">DLL</span><span class="sxs-lookup"><span data-stu-id="71515-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71515-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71515-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71515-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71515-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71515-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71515-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71515-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71515-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71515-149">**glfeedbackbuffer**</span><span class="sxs-lookup"><span data-stu-id="71515-149">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="71515-150">**glrendermode**</span><span class="sxs-lookup"><span data-stu-id="71515-150">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





