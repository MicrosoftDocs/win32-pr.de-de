---
title: gldelta etelists-Funktion (GL. h)
description: Die Funktion "gldelta etelists" löscht eine zusammenhängende Gruppe von Anzeigelisten.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- gldelta etelists-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339335"
---
# <a name="gldeletelists-function"></a><span data-ttu-id="8a881-104">gldelta etelists-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a881-104">glDeleteLists function</span></span>

<span data-ttu-id="8a881-105">Die Funktion " **gldelta etelists** " löscht eine zusammenhängende Gruppe von Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="8a881-105">The **glDeleteLists** function deletes a contiguous group of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a881-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a881-106">Syntax</span></span>


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="8a881-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a881-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a881-108">*list*</span><span class="sxs-lookup"><span data-stu-id="8a881-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="8a881-109">Der ganzzahlige Name der ersten zu löschenden Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="8a881-109">The integer name of the first display list to delete.</span></span>

</dd> <dt>

<span data-ttu-id="8a881-110">*range*</span><span class="sxs-lookup"><span data-stu-id="8a881-110">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="8a881-111">Die Anzahl der zu löschenden Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="8a881-111">The number of display lists to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a881-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a881-112">Return value</span></span>

<span data-ttu-id="8a881-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8a881-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8a881-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8a881-114">Error codes</span></span>

<span data-ttu-id="8a881-115">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8a881-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8a881-116">Name</span><span class="sxs-lookup"><span data-stu-id="8a881-116">Name</span></span>                                                                                                  | <span data-ttu-id="8a881-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a881-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a881-118"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="8a881-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8a881-119">der *Bereich* war negativ.</span><span class="sxs-lookup"><span data-stu-id="8a881-119">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="8a881-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="8a881-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8a881-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8a881-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8a881-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a881-122">Remarks</span></span>

<span data-ttu-id="8a881-123">Die Funktion " **gldelta etelists** " bewirkt, dass eine zusammenhängende Gruppe von Anzeigelisten gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="8a881-123">The **glDeleteLists** function causes a contiguous group of display lists to be deleted.</span></span> <span data-ttu-id="8a881-124">Der *List* -Parameter ist der Name der ersten zu löschenden Anzeigeliste, und *Range* steht für die Anzahl der zu löschenden Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="8a881-124">The *list* parameter is the name of the first display list to be deleted, and *range* is the number of display lists to delete.</span></span> <span data-ttu-id="8a881-125">Alle Anzeigelisten *d* mit *Listen*  =    =    +  *Bereich* -1 werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8a881-125">All display lists *d* with *list* = *d* = *list* + *range* - 1 are deleted.</span></span>

<span data-ttu-id="8a881-126">Alle Speicherorte, die den angegebenen anzeigen Listen zugeordnet sind, werden freigegeben, und die Namen können zu einem späteren Zeitpunkt wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a881-126">All storage locations allocated to the specified display lists are freed, and the names are available for reuse at a later time.</span></span> <span data-ttu-id="8a881-127">Namen innerhalb des Bereichs, die keine zugeordnete Anzeigeliste aufweisen, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8a881-127">Names within the range that do not have an associated display list are ignored.</span></span> <span data-ttu-id="8a881-128">Wenn *Range* gleich NULL ist, geschieht nichts.</span><span class="sxs-lookup"><span data-stu-id="8a881-128">If *range* is zero, nothing happens.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a881-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a881-129">Requirements</span></span>



| <span data-ttu-id="8a881-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a881-130">Requirement</span></span> | <span data-ttu-id="8a881-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8a881-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a881-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a881-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8a881-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a881-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8a881-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a881-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8a881-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a881-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a881-136">Header</span><span class="sxs-lookup"><span data-stu-id="8a881-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a881-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a881-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8a881-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a881-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a881-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a881-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8a881-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8a881-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a881-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a881-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a881-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a881-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a881-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8a881-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8a881-144">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="8a881-144">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="8a881-145">**glcalllists**</span><span class="sxs-lookup"><span data-stu-id="8a881-145">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="8a881-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8a881-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8a881-147">**glgenlists**</span><span class="sxs-lookup"><span data-stu-id="8a881-147">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="8a881-148">**glislist**</span><span class="sxs-lookup"><span data-stu-id="8a881-148">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="8a881-149">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="8a881-149">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





