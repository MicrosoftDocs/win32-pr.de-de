---
title: glVertex4sv-Funktion (GL. h)
description: Gibt einen Scheitelpunkt an. | glVertex4sv-Funktion (GL. h)
ms.assetid: 969ecb41-7e72-4b95-9d84-2d995f60f2a3
keywords:
- glVertex4sv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertex4sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c0497fa55b43b22e4649e7ece3eb17f6f9e5339
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870063"
---
# <a name="glvertex4sv-function"></a><span data-ttu-id="b01d2-105">glVertex4sv-Funktion</span><span class="sxs-lookup"><span data-stu-id="b01d2-105">glVertex4sv function</span></span>

<span data-ttu-id="b01d2-106">Gibt einen Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="b01d2-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="b01d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b01d2-107">Syntax</span></span>


```C++
void WINAPI glVertex4sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="b01d2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b01d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b01d2-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="b01d2-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="b01d2-110">Ein Zeiger auf ein Array aus vier Elementen.</span><span class="sxs-lookup"><span data-stu-id="b01d2-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="b01d2-111">Die Elemente sind die x-, y-, z-und w-Koordinaten eines Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="b01d2-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b01d2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b01d2-112">Return value</span></span>

<span data-ttu-id="b01d2-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b01d2-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b01d2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b01d2-114">Requirements</span></span>



| <span data-ttu-id="b01d2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b01d2-115">Requirement</span></span> | <span data-ttu-id="b01d2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b01d2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b01d2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b01d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b01d2-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b01d2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b01d2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b01d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b01d2-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b01d2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b01d2-121">Header</span><span class="sxs-lookup"><span data-stu-id="b01d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b01d2-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b01d2-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b01d2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b01d2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b01d2-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b01d2-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b01d2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b01d2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b01d2-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b01d2-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b01d2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b01d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b01d2-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b01d2-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b01d2-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="b01d2-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="b01d2-130">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="b01d2-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="b01d2-131">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="b01d2-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="b01d2-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b01d2-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b01d2-133">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="b01d2-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b01d2-134">**glindex**</span><span class="sxs-lookup"><span data-stu-id="b01d2-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="b01d2-135">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="b01d2-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="b01d2-136">**glnormal**</span><span class="sxs-lookup"><span data-stu-id="b01d2-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="b01d2-137">**glrect**</span><span class="sxs-lookup"><span data-stu-id="b01d2-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="b01d2-138">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="b01d2-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





