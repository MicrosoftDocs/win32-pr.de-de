---
title: glistexture-Funktion (GL. h)
description: Die Funktion "glistexture" bestimmt, ob ein Name einer Textur entspricht.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- Funktion "glistexture" OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478711"
---
# <a name="glistexture-function"></a><span data-ttu-id="1adbd-104">glistexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="1adbd-104">glIsTexture function</span></span>

<span data-ttu-id="1adbd-105">Die Funktion " **glistexture** " bestimmt, ob ein Name einer Textur entspricht.</span><span class="sxs-lookup"><span data-stu-id="1adbd-105">The **glIsTexture** function determines if a name corresponds to a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1adbd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1adbd-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="1adbd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1adbd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1adbd-108">*Konsistenz*</span><span class="sxs-lookup"><span data-stu-id="1adbd-108">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="1adbd-109">Ein-Wert, der den Namen einer Textur ist.</span><span class="sxs-lookup"><span data-stu-id="1adbd-109">A value that is the name of a texture.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="1adbd-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1adbd-110">Error codes</span></span>

<span data-ttu-id="1adbd-111">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1adbd-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1adbd-112">Name</span><span class="sxs-lookup"><span data-stu-id="1adbd-112">Name</span></span>                                                                                                  | <span data-ttu-id="1adbd-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1adbd-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1adbd-114"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="1adbd-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1adbd-115">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1adbd-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1adbd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1adbd-116">Remarks</span></span>

<span data-ttu-id="1adbd-117">Wenn der *Textur* Parameter derzeit der Name einer Textur ist, gibt die Funktion " **glistexture** " den Wert "GL true" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="1adbd-117">If the *texture* parameter is currently the name of a texture, the **glIsTexture** function returns GL\_TRUE.</span></span> <span data-ttu-id="1adbd-118">Die Funktion " **glistexture** " gibt "GL false" zurück, \_ Wenn *Textur* NULL ist.</span><span class="sxs-lookup"><span data-stu-id="1adbd-118">The **glIsTexture** function returns GL\_FALSE if *texture* is zero.</span></span> <span data-ttu-id="1adbd-119">Außerdem wird "GL false" zurückgegeben, \_ Wenn es sich um einen Wert ungleich 0 (null) handelt, der derzeit nicht der Name einer Textur ist, oder wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1adbd-119">It also returns GL\_FALSE if it is a non-zero value that is not currently the name of a texture, or if an error occurs.</span></span>

<span data-ttu-id="1adbd-120">Sie können keine Aufrufe von " **glistexture** " in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="1adbd-120">You cannot include calls to **glIsTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="1adbd-121">Die Funktion " **glistexture** " ist nur in OpenGL, Version 1,1 oder höher, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1adbd-121">The **glIsTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1adbd-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1adbd-122">Requirements</span></span>



| <span data-ttu-id="1adbd-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1adbd-123">Requirement</span></span> | <span data-ttu-id="1adbd-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1adbd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1adbd-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1adbd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1adbd-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1adbd-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1adbd-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1adbd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1adbd-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1adbd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1adbd-129">Header</span><span class="sxs-lookup"><span data-stu-id="1adbd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1adbd-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1adbd-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1adbd-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1adbd-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="1adbd-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1adbd-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1adbd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1adbd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1adbd-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1adbd-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1adbd-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1adbd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1adbd-136">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1adbd-136">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1adbd-137">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="1adbd-137">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="1adbd-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1adbd-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1adbd-139">**glgentexturen**</span><span class="sxs-lookup"><span data-stu-id="1adbd-139">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="1adbd-140">**glget**</span><span class="sxs-lookup"><span data-stu-id="1adbd-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="1adbd-141">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="1adbd-141">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="1adbd-142">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1adbd-142">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1adbd-143">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1adbd-143">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1adbd-144">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="1adbd-144">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





