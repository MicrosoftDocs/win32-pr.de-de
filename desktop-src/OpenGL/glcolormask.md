---
title: glcolormask-Funktion (GL. h)
description: Die glcolormask-Funktion aktiviert und deaktiviert das Schreiben von Frame-Puffer Farbkomponenten.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glcolormask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858746"
---
# <a name="glcolormask-function"></a><span data-ttu-id="ae8da-104">glcolormask-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae8da-104">glColorMask function</span></span>

<span data-ttu-id="ae8da-105">Die **glcolormask** -Funktion aktiviert und deaktiviert das Schreiben von Frame-Puffer Farbkomponenten.</span><span class="sxs-lookup"><span data-stu-id="ae8da-105">The **glColorMask** function enables and disables writing of frame-buffer color components.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8da-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae8da-106">Syntax</span></span>


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a><span data-ttu-id="ae8da-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae8da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae8da-108">*Red*</span><span class="sxs-lookup"><span data-stu-id="ae8da-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8da-109">Geben Sie an, ob rot in den Framebuffer geschrieben werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ae8da-109">Specify whether red can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="ae8da-110">Die Standardwerte lauten "GL \_ true", was darauf hinweist, dass die Farbkomponente geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae8da-110">The default values is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="ae8da-111">*Grünbuchs*</span><span class="sxs-lookup"><span data-stu-id="ae8da-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8da-112">Geben Sie an, ob grün in den Framebuffer geschrieben werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ae8da-112">Specify whether green can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="ae8da-113">Der Standardwert ist "GL \_ true", der angibt, dass die Farbkomponente geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae8da-113">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="ae8da-114">*blauen*</span><span class="sxs-lookup"><span data-stu-id="ae8da-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8da-115">Geben Sie an, ob blau in den Framebuffer geschrieben werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ae8da-115">Specify whether blue can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="ae8da-116">Der Standardwert ist "GL \_ true", der angibt, dass die Farbkomponente geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae8da-116">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="ae8da-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="ae8da-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8da-118">Geben Sie an, ob Alpha in den Framebuffer geschrieben werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ae8da-118">Specify whether alpha can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="ae8da-119">Der Standardwert ist "GL \_ true", der angibt, dass die Farbkomponente geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae8da-119">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae8da-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae8da-120">Return value</span></span>

<span data-ttu-id="ae8da-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ae8da-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae8da-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ae8da-122">Error codes</span></span>

<span data-ttu-id="ae8da-123">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ae8da-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ae8da-124">Name</span><span class="sxs-lookup"><span data-stu-id="ae8da-124">Name</span></span>                                                                                                  | <span data-ttu-id="ae8da-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ae8da-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae8da-126"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="ae8da-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ae8da-127">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ae8da-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ae8da-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae8da-128">Remarks</span></span>

<span data-ttu-id="ae8da-129">Die **glcolormask** -Funktion gibt an, ob die einzelnen Farbkomponenten im Frame Puffer geschrieben werden können oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ae8da-129">The **glColorMask** function specifies whether the individual color components in the framebuffer can or cannot be written.</span></span> <span data-ttu-id="ae8da-130">Wenn *rot* den Wert "GL \_ false" hat, wird z. b. unabhängig vom versuchten Zeichnungs Vorgang keine Änderung an der roten Komponente eines Pixels in einem der Farb Puffer vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="ae8da-130">If *red* is GL\_FALSE, for example, no change is made to the red component of any pixel in any of the color buffers, regardless of the drawing operation attempted.</span></span>

<span data-ttu-id="ae8da-131">Änderungen an einzelnen Komponenten Komponenten können nicht gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="ae8da-131">Changes to individual bits of components cannot be controlled.</span></span> <span data-ttu-id="ae8da-132">Stattdessen werden die Änderungen für ganze Farbkomponenten aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ae8da-132">Rather, changes are either enabled or disabled for entire color components.</span></span>

<span data-ttu-id="ae8da-133">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glcolormask** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="ae8da-133">The following functions retrieve information related to **glColorMask**:</span></span>

<span data-ttu-id="ae8da-134">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Color \_ Write-Frage</span><span class="sxs-lookup"><span data-stu-id="ae8da-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_WRITEMASK</span></span>

<span data-ttu-id="ae8da-135">**glget** mit dem Argument GL \_ RGBA- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="ae8da-135">**glGet** with argument GL\_RGBA\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="ae8da-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae8da-136">Requirements</span></span>



| <span data-ttu-id="ae8da-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae8da-137">Requirement</span></span> | <span data-ttu-id="ae8da-138">Wert</span><span class="sxs-lookup"><span data-stu-id="ae8da-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8da-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae8da-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ae8da-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae8da-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ae8da-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae8da-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ae8da-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae8da-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae8da-143">Header</span><span class="sxs-lookup"><span data-stu-id="ae8da-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae8da-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae8da-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ae8da-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae8da-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae8da-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae8da-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ae8da-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ae8da-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae8da-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae8da-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae8da-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae8da-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae8da-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ae8da-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ae8da-151">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="ae8da-151">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ae8da-152">**gldepthmask**</span><span class="sxs-lookup"><span data-stu-id="ae8da-152">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="ae8da-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ae8da-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ae8da-154">**glget**</span><span class="sxs-lookup"><span data-stu-id="ae8da-154">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="ae8da-155">**glindex**</span><span class="sxs-lookup"><span data-stu-id="ae8da-155">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ae8da-156">**glindexmask**</span><span class="sxs-lookup"><span data-stu-id="ae8da-156">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="ae8da-157">**glstencilmask**</span><span class="sxs-lookup"><span data-stu-id="ae8da-157">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





