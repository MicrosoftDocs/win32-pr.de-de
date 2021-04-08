---
title: glgenlists-Funktion (GL. h)
description: Die Funktion "glgenlists" generiert einen zusammenhängenden Satz leerer Anzeigelisten.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- glgenlists-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740480"
---
# <a name="glgenlists-function"></a><span data-ttu-id="856b1-104">glgenlists-Funktion</span><span class="sxs-lookup"><span data-stu-id="856b1-104">glGenLists function</span></span>

<span data-ttu-id="856b1-105">Die Funktion " **glgenlists** " generiert einen zusammenhängenden Satz leerer Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="856b1-105">The **glGenLists** function generates a contiguous set of empty display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="856b1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="856b1-106">Syntax</span></span>


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="856b1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="856b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="856b1-108">*range*</span><span class="sxs-lookup"><span data-stu-id="856b1-108">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="856b1-109">Die Anzahl der zusammenhängenden leeren Anzeigelisten, die generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="856b1-109">The number of contiguous empty display lists to be generated.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="856b1-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="856b1-110">Error codes</span></span>

<span data-ttu-id="856b1-111">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="856b1-111">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="856b1-112">Name</span><span class="sxs-lookup"><span data-stu-id="856b1-112">Name</span></span>                                                                                                  | <span data-ttu-id="856b1-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="856b1-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="856b1-114"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="856b1-114"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="856b1-115">der *Bereich* war negativ.</span><span class="sxs-lookup"><span data-stu-id="856b1-115">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="856b1-116"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="856b1-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="856b1-117">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="856b1-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="856b1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="856b1-118">Remarks</span></span>

<span data-ttu-id="856b1-119">Die Funktion " **glgenlists** " weist ein Argument *auf.*</span><span class="sxs-lookup"><span data-stu-id="856b1-119">The **glGenLists** function has one argument, *range*.</span></span> <span data-ttu-id="856b1-120">Er gibt eine ganze Zahl *n* zurück, die den *Bereich* zusammenhängender leerer Anzeigelisten mit dem Namen *n*, *n* + 1, enthält.</span><span class="sxs-lookup"><span data-stu-id="856b1-120">It returns an integer *n* such that *range* contiguous empty display lists, named *n*, *n* + 1, .</span></span> <span data-ttu-id="856b1-121">.</span><span class="sxs-lookup"><span data-stu-id="856b1-121">.</span></span> <span data-ttu-id="856b1-122">., *n* + (*Bereich* -1), werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="856b1-122">., *n* + (*range* - 1), are created.</span></span> <span data-ttu-id="856b1-123">Wenn *Range* gleich 0 (null) ist, wenn keine *Gruppe von zusammen* hängenden Namen verfügbar ist oder wenn ein Fehler generiert wird, werden keine anzeigen Listen generiert und NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="856b1-123">If *range* is zero, if there is no group of *range* contiguous names available, or if any error is generated, then no display lists are generated and zero is returned.</span></span>

<span data-ttu-id="856b1-124">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glgenlists** ab:</span><span class="sxs-lookup"><span data-stu-id="856b1-124">The following function retrieves information related to **glGenLists**:</span></span>

[<span data-ttu-id="856b1-125">**glislist**</span><span class="sxs-lookup"><span data-stu-id="856b1-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="856b1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="856b1-126">Requirements</span></span>



| <span data-ttu-id="856b1-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="856b1-127">Requirement</span></span> | <span data-ttu-id="856b1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="856b1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="856b1-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="856b1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="856b1-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="856b1-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="856b1-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="856b1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="856b1-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="856b1-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="856b1-133">Header</span><span class="sxs-lookup"><span data-stu-id="856b1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="856b1-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="856b1-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="856b1-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="856b1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="856b1-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="856b1-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="856b1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="856b1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="856b1-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="856b1-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="856b1-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="856b1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856b1-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="856b1-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="856b1-141">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="856b1-141">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="856b1-142">**glcalllists**</span><span class="sxs-lookup"><span data-stu-id="856b1-142">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="856b1-143">**gldelta etelists**</span><span class="sxs-lookup"><span data-stu-id="856b1-143">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="856b1-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="856b1-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="856b1-145">**glislist**</span><span class="sxs-lookup"><span data-stu-id="856b1-145">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="856b1-146">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="856b1-146">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





