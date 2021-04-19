---
title: glVertex4fv-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex4fv-Funktion (GL. h)
ms.assetid: c2a766fd-3ad8-463b-8f09-36d0673e6716
keywords:
- glVertex4fv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex4fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e05551268b697ba4444c29d5f2b9bdfb0e832e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361807"
---
# <a name="glvertex4fv-function"></a><span data-ttu-id="f0279-105">glVertex4fv-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0279-105">glVertex4fv function</span></span>

<span data-ttu-id="f0279-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="f0279-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0279-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0279-107">Syntax</span></span>


```C++
void WINAPI glVertex4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="f0279-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0279-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0279-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="f0279-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="f0279-110">Ein Zeiger auf ein Array aus vier Elementen.</span><span class="sxs-lookup"><span data-stu-id="f0279-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="f0279-111">Die Elemente sind die x-, y-, z-und w-Koordinaten eines Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="f0279-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0279-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0279-112">Return value</span></span>

<span data-ttu-id="f0279-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f0279-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0279-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0279-114">Requirements</span></span>



| <span data-ttu-id="f0279-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0279-115">Requirement</span></span> | <span data-ttu-id="f0279-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f0279-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0279-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0279-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0279-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0279-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f0279-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0279-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0279-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0279-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0279-121">Header</span><span class="sxs-lookup"><span data-stu-id="f0279-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0279-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0279-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f0279-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0279-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0279-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0279-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f0279-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f0279-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0279-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0279-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0279-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0279-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0279-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f0279-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f0279-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="f0279-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="f0279-130">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="f0279-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f0279-131">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="f0279-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="f0279-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f0279-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f0279-133">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="f0279-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f0279-134">**glindex**</span><span class="sxs-lookup"><span data-stu-id="f0279-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="f0279-135">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="f0279-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="f0279-136">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="f0279-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="f0279-137">**glrect**</span><span class="sxs-lookup"><span data-stu-id="f0279-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="f0279-138">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="f0279-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





