---
title: glVertex4iv-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex4iv-Funktion (GL. h)
ms.assetid: 7b56777a-f904-4a9d-8d3d-84a38cbf0b45
keywords:
- glVertex4iv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex4iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff55c5534245843d5caa8797b2b529c7cfe00f9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870064"
---
# <a name="glvertex4iv-function"></a><span data-ttu-id="03984-105">glVertex4iv-Funktion</span><span class="sxs-lookup"><span data-stu-id="03984-105">glVertex4iv function</span></span>

<span data-ttu-id="03984-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="03984-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="03984-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="03984-107">Syntax</span></span>


```C++
void WINAPI glVertex4iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="03984-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03984-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03984-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="03984-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="03984-110">Ein Zeiger auf ein Array aus vier Elementen.</span><span class="sxs-lookup"><span data-stu-id="03984-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="03984-111">Die Elemente sind die x-, y-, z-und w-Koordinaten eines Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="03984-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03984-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03984-112">Return value</span></span>

<span data-ttu-id="03984-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="03984-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03984-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03984-114">Requirements</span></span>



| <span data-ttu-id="03984-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03984-115">Requirement</span></span> | <span data-ttu-id="03984-116">Wert</span><span class="sxs-lookup"><span data-stu-id="03984-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03984-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03984-117">Minimum supported client</span></span><br/> | <span data-ttu-id="03984-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03984-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="03984-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03984-119">Minimum supported server</span></span><br/> | <span data-ttu-id="03984-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03984-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03984-121">Header</span><span class="sxs-lookup"><span data-stu-id="03984-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="03984-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="03984-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="03984-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03984-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="03984-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03984-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="03984-125">DLL</span><span class="sxs-lookup"><span data-stu-id="03984-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03984-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03984-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03984-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03984-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03984-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="03984-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="03984-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="03984-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="03984-130">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="03984-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="03984-131">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="03984-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="03984-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="03984-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="03984-133">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="03984-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="03984-134">**glindex**</span><span class="sxs-lookup"><span data-stu-id="03984-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="03984-135">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="03984-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="03984-136">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="03984-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="03984-137">**glrect**</span><span class="sxs-lookup"><span data-stu-id="03984-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="03984-138">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="03984-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





