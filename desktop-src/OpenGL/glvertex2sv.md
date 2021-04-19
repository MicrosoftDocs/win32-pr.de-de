---
title: glVertex2sv-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex2sv-Funktion (GL. h)
ms.assetid: 4e13356a-a74b-4fb6-a001-1fffc28dd7a1
keywords:
- glVertex2sv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex2sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e865ab8999e08f9c13ad46443ba039be1cda9e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363929"
---
# <a name="glvertex2sv-function"></a><span data-ttu-id="dfbb4-105">glVertex2sv-Funktion</span><span class="sxs-lookup"><span data-stu-id="dfbb4-105">glVertex2sv function</span></span>

<span data-ttu-id="dfbb4-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="dfbb4-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbb4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfbb4-107">Syntax</span></span>


```C++
void WINAPI glVertex2sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="dfbb4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfbb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfbb4-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="dfbb4-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbb4-110">Ein Zeiger auf ein Array mit zwei-Elementen.</span><span class="sxs-lookup"><span data-stu-id="dfbb4-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="dfbb4-111">Die Elemente sind die x-und y-Koordinaten eines Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="dfbb4-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfbb4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfbb4-112">Return value</span></span>

<span data-ttu-id="dfbb4-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dfbb4-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfbb4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfbb4-114">Requirements</span></span>



| <span data-ttu-id="dfbb4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfbb4-115">Requirement</span></span> | <span data-ttu-id="dfbb4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="dfbb4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbb4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfbb4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dfbb4-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfbb4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dfbb4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfbb4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dfbb4-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfbb4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfbb4-121">Header</span><span class="sxs-lookup"><span data-stu-id="dfbb4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfbb4-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfbb4-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dfbb4-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dfbb4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfbb4-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfbb4-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dfbb4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dfbb4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfbb4-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfbb4-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfbb4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfbb4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfbb4-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-130">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-131">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-133">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-134">**glindex**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-135">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-136">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-137">**glrect**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="dfbb4-138">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="dfbb4-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





