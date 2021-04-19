---
title: glVertex3fv-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex3fv-Funktion (GL. h)
ms.assetid: d8790ffe-73b1-49d8-a7f5-2117177573ac
keywords:
- glVertex3fv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3bcbe73d071bc18e3a1a58ef2f505fa9bd6a3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357192"
---
# <a name="glvertex3fv-function"></a><span data-ttu-id="a1786-105">glVertex3fv-Funktion</span><span class="sxs-lookup"><span data-stu-id="a1786-105">glVertex3fv function</span></span>

<span data-ttu-id="a1786-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="a1786-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1786-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1786-107">Syntax</span></span>


```C++
void WINAPI glVertex3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="a1786-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1786-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1786-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="a1786-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="a1786-110">Ein Zeiger auf ein Array von drei Elementen.</span><span class="sxs-lookup"><span data-stu-id="a1786-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="a1786-111">Die Elemente sind die x-, y-und z-Koordinaten eines Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="a1786-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1786-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1786-112">Return value</span></span>

<span data-ttu-id="a1786-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a1786-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1786-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1786-114">Requirements</span></span>



| <span data-ttu-id="a1786-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1786-115">Requirement</span></span> | <span data-ttu-id="a1786-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a1786-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1786-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1786-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a1786-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1786-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a1786-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1786-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a1786-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1786-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1786-121">Header</span><span class="sxs-lookup"><span data-stu-id="a1786-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1786-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1786-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a1786-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a1786-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1786-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1786-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a1786-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a1786-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1786-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1786-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1786-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1786-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1786-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a1786-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a1786-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="a1786-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a1786-130">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="a1786-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a1786-131">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="a1786-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a1786-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a1786-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a1786-133">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="a1786-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a1786-134">**glindex**</span><span class="sxs-lookup"><span data-stu-id="a1786-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a1786-135">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="a1786-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a1786-136">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="a1786-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a1786-137">**glrect**</span><span class="sxs-lookup"><span data-stu-id="a1786-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="a1786-138">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="a1786-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





