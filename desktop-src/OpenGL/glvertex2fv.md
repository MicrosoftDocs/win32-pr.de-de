---
title: glVertex2fv-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex2fv-Funktion (GL. h)
ms.assetid: bae32d27-2a19-40d5-a3f7-0e7a41918034
keywords:
- glVertex2fv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd7a57aff2166f3605d7007cd194f5cff04784
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361148"
---
# <a name="glvertex2fv-function"></a><span data-ttu-id="3661c-105">glVertex2fv-Funktion</span><span class="sxs-lookup"><span data-stu-id="3661c-105">glVertex2fv function</span></span>

<span data-ttu-id="3661c-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="3661c-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3661c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3661c-107">Syntax</span></span>


```C++
void WINAPI glVertex2fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="3661c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3661c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3661c-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="3661c-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="3661c-110">Ein Zeiger auf ein Array mit zwei-Elementen.</span><span class="sxs-lookup"><span data-stu-id="3661c-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="3661c-111">Die Elemente sind die x-und y-Koordinaten eines Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="3661c-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3661c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3661c-112">Return value</span></span>

<span data-ttu-id="3661c-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3661c-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3661c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3661c-114">Requirements</span></span>



| <span data-ttu-id="3661c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3661c-115">Requirement</span></span> | <span data-ttu-id="3661c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3661c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3661c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3661c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3661c-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3661c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3661c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3661c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3661c-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3661c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3661c-121">Header</span><span class="sxs-lookup"><span data-stu-id="3661c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3661c-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3661c-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3661c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3661c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3661c-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3661c-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3661c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3661c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3661c-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3661c-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3661c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3661c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3661c-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3661c-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3661c-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="3661c-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="3661c-130">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="3661c-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3661c-131">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="3661c-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="3661c-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3661c-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3661c-133">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="3661c-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3661c-134">**glindex**</span><span class="sxs-lookup"><span data-stu-id="3661c-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3661c-135">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="3661c-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="3661c-136">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="3661c-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3661c-137">**glrect**</span><span class="sxs-lookup"><span data-stu-id="3661c-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="3661c-138">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="3661c-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





