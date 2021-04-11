---
title: glMatrixMode-Funktion (GL. h)
description: Die glMatrixMode-Funktion gibt an, welche Matrix die aktuelle Matrix ist.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- glMatrixMode-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104679"
---
# <a name="glmatrixmode-function"></a><span data-ttu-id="ac1e8-104">glMatrixMode-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac1e8-104">glMatrixMode function</span></span>

<span data-ttu-id="ac1e8-105">Die **glMatrixMode** -Funktion gibt an, welche Matrix die aktuelle Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-105">The **glMatrixMode** function specifies which matrix is the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1e8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac1e8-106">Syntax</span></span>


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="ac1e8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac1e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac1e8-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="ac1e8-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="ac1e8-109">Der Matrix Stapel, der das Ziel für nachfolgende Matrix Vorgänge ist.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-109">The matrix stack that is the target for subsequent matrix operations.</span></span> <span data-ttu-id="ac1e8-110">Der *Mode* -Parameter kann einen von drei Werten annehmen.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-110">The *mode* parameter can assume one of three values.</span></span>



| <span data-ttu-id="ac1e8-111">Wert</span><span class="sxs-lookup"><span data-stu-id="ac1e8-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="ac1e8-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ac1e8-112">Meaning</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <span data-ttu-id="ac1e8-113"><dt>**GL \_ Modelview**</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e8-113"><dt>**GL\_MODELVIEW**</dt></span></span> </dl>    | <span data-ttu-id="ac1e8-114">Wendet nachfolgende Matrix Vorgänge auf den Modelview-Matrix Stapel an.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-114">Applies subsequent matrix operations to the modelview matrix stack.</span></span><br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <span data-ttu-id="ac1e8-115"><dt>**GL- \_ Projektion**</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e8-115"><dt>**GL\_PROJECTION**</dt></span></span> </dl> | <span data-ttu-id="ac1e8-116">Wendet nachfolgende Matrix Vorgänge auf den Projektions Matrix Stapel an.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-116">Applies subsequent matrix operations to the projection matrix stack.</span></span><br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <span data-ttu-id="ac1e8-117"><dt>**GL- \_ Textur**</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e8-117"><dt>**GL\_TEXTURE**</dt></span></span> </dl>          | <span data-ttu-id="ac1e8-118">Wendet nachfolgende Matrix Vorgänge auf den Textur Matrix Stapel an.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-118">Applies subsequent matrix operations to the texture matrix stack.</span></span><br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac1e8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac1e8-119">Return value</span></span>

<span data-ttu-id="ac1e8-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ac1e8-121">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ac1e8-121">Error codes</span></span>

<span data-ttu-id="ac1e8-122">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ac1e8-123">Name</span><span class="sxs-lookup"><span data-stu-id="ac1e8-123">Name</span></span>                                                                                                  | <span data-ttu-id="ac1e8-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ac1e8-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac1e8-125"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e8-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ac1e8-126">der *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-126">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="ac1e8-127"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e8-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ac1e8-128">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ac1e8-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac1e8-129">Remarks</span></span>

<span data-ttu-id="ac1e8-130">Die **glMatrixMode** -Funktion legt den aktuellen Matrix Modus fest.</span><span class="sxs-lookup"><span data-stu-id="ac1e8-130">The **glMatrixMode** function sets the current matrix mode.</span></span>

<span data-ttu-id="ac1e8-131">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glMatrixMode** ab:</span><span class="sxs-lookup"><span data-stu-id="ac1e8-131">The following function retrieves information related to **glMatrixMode**:</span></span>

<span data-ttu-id="ac1e8-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="ac1e8-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="ac1e8-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac1e8-133">Requirements</span></span>



| <span data-ttu-id="ac1e8-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac1e8-134">Requirement</span></span> | <span data-ttu-id="ac1e8-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ac1e8-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1e8-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac1e8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1e8-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac1e8-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ac1e8-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac1e8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1e8-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac1e8-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac1e8-140">Header</span><span class="sxs-lookup"><span data-stu-id="ac1e8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac1e8-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e8-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ac1e8-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac1e8-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac1e8-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e8-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac1e8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ac1e8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac1e8-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e8-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac1e8-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac1e8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac1e8-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ac1e8-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ac1e8-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ac1e8-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ac1e8-149">**glloadmatrix**</span><span class="sxs-lookup"><span data-stu-id="ac1e8-149">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="ac1e8-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="ac1e8-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





