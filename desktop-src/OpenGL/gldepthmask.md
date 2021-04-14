---
title: gldepthmask-Funktion (GL. h)
description: Die Funktion "gldepthmask" aktiviert oder deaktiviert das Schreiben in den tiefen Puffer.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- gldepthmask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5873d517770f1ce61f9a2eaad3ea7cce7b4fd7ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391991"
---
# <a name="gldepthmask-function"></a><span data-ttu-id="b9ecf-104">gldepthmask-Funktion</span><span class="sxs-lookup"><span data-stu-id="b9ecf-104">glDepthMask function</span></span>

<span data-ttu-id="b9ecf-105">Die Funktion " **gldepthmask** " aktiviert oder deaktiviert das Schreiben in den tiefen Puffer.</span><span class="sxs-lookup"><span data-stu-id="b9ecf-105">The **glDepthMask** function enables or disables writing into the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ecf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9ecf-106">Syntax</span></span>


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="b9ecf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9ecf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ecf-108">*flag*</span><span class="sxs-lookup"><span data-stu-id="b9ecf-108">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="b9ecf-109">Gibt an, ob der tiefen Puffer zum Schreiben aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b9ecf-109">Specifies whether the depth buffer is enabled for writing.</span></span> <span data-ttu-id="b9ecf-110">Wenn *Flag* 0 (null) ist, ist das Schreiben von tiefen Puffern deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9ecf-110">If *flag* is zero, depth-buffer writing is disabled.</span></span> <span data-ttu-id="b9ecf-111">Andernfalls ist es aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9ecf-111">Otherwise, it is enabled.</span></span> <span data-ttu-id="b9ecf-112">Zunächst ist der tiefen Puffer Schreibvorgang aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9ecf-112">Initially, depth-buffer writing is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ecf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9ecf-113">Return value</span></span>

<span data-ttu-id="b9ecf-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b9ecf-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9ecf-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b9ecf-115">Error codes</span></span>

<span data-ttu-id="b9ecf-116">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b9ecf-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b9ecf-117">Name</span><span class="sxs-lookup"><span data-stu-id="b9ecf-117">Name</span></span>                                                                                                  | <span data-ttu-id="b9ecf-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b9ecf-118">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9ecf-119"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ecf-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b9ecf-120">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b9ecf-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9ecf-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9ecf-121">Remarks</span></span>

<span data-ttu-id="b9ecf-122">Die folgende Funktion Ruft Informationen im Zusammenhang mit " **gldepthmask**" ab:</span><span class="sxs-lookup"><span data-stu-id="b9ecf-122">The following function retrieves information related to **glDepthMask**:</span></span>

<span data-ttu-id="b9ecf-123">**glget** mit Argument GL- \_ tiefen \_ schreibfrage</span><span class="sxs-lookup"><span data-stu-id="b9ecf-123">**glGet** with argument GL\_DEPTH\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ecf-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9ecf-124">Requirements</span></span>



| <span data-ttu-id="b9ecf-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9ecf-125">Requirement</span></span> | <span data-ttu-id="b9ecf-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b9ecf-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ecf-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9ecf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ecf-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9ecf-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9ecf-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9ecf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ecf-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9ecf-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9ecf-131">Header</span><span class="sxs-lookup"><span data-stu-id="b9ecf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9ecf-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ecf-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b9ecf-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9ecf-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9ecf-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9ecf-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9ecf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b9ecf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9ecf-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9ecf-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ecf-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9ecf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ecf-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b9ecf-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b9ecf-139">**glcolormask**</span><span class="sxs-lookup"><span data-stu-id="b9ecf-139">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="b9ecf-140">**gldepthfunc**</span><span class="sxs-lookup"><span data-stu-id="b9ecf-140">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="b9ecf-141">**gldepthrange**</span><span class="sxs-lookup"><span data-stu-id="b9ecf-141">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="b9ecf-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b9ecf-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b9ecf-143">**glget**</span><span class="sxs-lookup"><span data-stu-id="b9ecf-143">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b9ecf-144">**glindexmask**</span><span class="sxs-lookup"><span data-stu-id="b9ecf-144">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="b9ecf-145">**glstencilmask**</span><span class="sxs-lookup"><span data-stu-id="b9ecf-145">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





