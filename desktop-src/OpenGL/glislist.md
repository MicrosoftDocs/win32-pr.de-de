---
title: glislist-Funktion (GL. h)
description: Die gllslist-Funktion testet, ob die Anzeigeliste vorhanden ist.
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- glislist-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fdc67d0a7dad18f8850c283f0d5eb224ff9ebbd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341037"
---
# <a name="glislist-function"></a><span data-ttu-id="fbd81-104">glislist-Funktion</span><span class="sxs-lookup"><span data-stu-id="fbd81-104">glIsList function</span></span>

<span data-ttu-id="fbd81-105">Die **gllslist** -Funktion testet, ob die Anzeigeliste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fbd81-105">The **gllsList** function tests for display list existence.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd81-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbd81-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="fbd81-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbd81-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbd81-108">*list*</span><span class="sxs-lookup"><span data-stu-id="fbd81-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="fbd81-109">Ein potenzieller Anzeigelisten Name.</span><span class="sxs-lookup"><span data-stu-id="fbd81-109">A potential display list name.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="fbd81-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="fbd81-110">Error codes</span></span>

<span data-ttu-id="fbd81-111">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fbd81-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fbd81-112">Name</span><span class="sxs-lookup"><span data-stu-id="fbd81-112">Name</span></span>                                                                                                  | <span data-ttu-id="fbd81-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fbd81-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbd81-114"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="fbd81-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fbd81-115">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fbd81-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fbd81-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbd81-116">Remarks</span></span>

<span data-ttu-id="fbd81-117">Die **gllslist** -Funktion gibt "GL true" zurück, \_ Wenn " *List* " der Name einer Anzeigeliste ist und andernfalls "GL false" zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="fbd81-117">The **gllsList** function returns GL\_TRUE if *list* is the name of a display list and returns GL\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd81-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbd81-118">Requirements</span></span>



| <span data-ttu-id="fbd81-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbd81-119">Requirement</span></span> | <span data-ttu-id="fbd81-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fbd81-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd81-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbd81-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fbd81-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbd81-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fbd81-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbd81-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fbd81-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbd81-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fbd81-125">Header</span><span class="sxs-lookup"><span data-stu-id="fbd81-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbd81-126"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbd81-126"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fbd81-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fbd81-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="fbd81-128"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbd81-128"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fbd81-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fbd81-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbd81-130"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbd81-130"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbd81-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbd81-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd81-132">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fbd81-132">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fbd81-133">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="fbd81-133">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="fbd81-134">**glcalllists**</span><span class="sxs-lookup"><span data-stu-id="fbd81-134">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="fbd81-135">**gldelta etelists**</span><span class="sxs-lookup"><span data-stu-id="fbd81-135">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="fbd81-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fbd81-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fbd81-137">**glgenlists**</span><span class="sxs-lookup"><span data-stu-id="fbd81-137">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="fbd81-138">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="fbd81-138">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





