---
title: glCallList-Funktion (GL. h)
description: Die Funktion "glCallList" führt eine Anzeigeliste aus.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- glCallList-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104132"
---
# <a name="glcalllist-function"></a><span data-ttu-id="80a06-104">glCallList-Funktion</span><span class="sxs-lookup"><span data-stu-id="80a06-104">glCallList function</span></span>

<span data-ttu-id="80a06-105">Die Funktion " **glCallList** " führt eine Anzeigeliste aus.</span><span class="sxs-lookup"><span data-stu-id="80a06-105">The **glCallList** function executes a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a06-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="80a06-106">Syntax</span></span>


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="80a06-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="80a06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a06-108">*list*</span><span class="sxs-lookup"><span data-stu-id="80a06-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="80a06-109">Der ganzzahlige Name der auszuführenden Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="80a06-109">The integer name of the display list to be executed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a06-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80a06-110">Return value</span></span>

<span data-ttu-id="80a06-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="80a06-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80a06-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80a06-112">Remarks</span></span>

<span data-ttu-id="80a06-113">Das Aufrufen der Funktion " **glCallList** " beginnt mit der Ausführung der benannten Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="80a06-113">Invoking the **glCallList** function begins execution of the named display list.</span></span> <span data-ttu-id="80a06-114">Die in der Anzeigeliste gespeicherten Funktionen werden in der richtigen Reihenfolge ausgeführt, als würden Sie ohne Anzeigeliste aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="80a06-114">The functions saved in the display list are executed in order, just as if you called them without using a display list.</span></span> <span data-ttu-id="80a06-115">Wenn *List* nicht als Anzeigeliste definiert wurde, wird **glCallList** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="80a06-115">If *list* has not been defined as a display list, **glCallList** is ignored.</span></span>

<span data-ttu-id="80a06-116">Die Funktion " **glCallList** " kann in einer Anzeigeliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="80a06-116">The **glCallList** function can appear inside a display list.</span></span> <span data-ttu-id="80a06-117">Um die Möglichkeit der unendlichen Rekursion zu vermeiden, die sich aus Anzeigelisten ergibt, wird während der Ausführung der Anzeigeliste eine Beschränkung auf der Schachtelungs Ebene der Anzeigelisten platziert.</span><span class="sxs-lookup"><span data-stu-id="80a06-117">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display-list execution.</span></span> <span data-ttu-id="80a06-118">Dieser Grenzwert ist mindestens 64, hängt jedoch von der Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="80a06-118">This limit is at least 64, however, it depends on the implementation.</span></span>

<span data-ttu-id="80a06-119">Der OpenGL-Zustand wird nicht in einem Aufruf von **glCallList** gespeichert und wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="80a06-119">The OpenGL state is not saved and restored across a call to **glCallList**.</span></span> <span data-ttu-id="80a06-120">Folglich verbleiben Änderungen, die während der Ausführung einer Anzeigeliste an dem OpenGL-Zustand vorgenommen werden, nach Abschluss der Ausführung der Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="80a06-120">Thus, changes made to the OpenGL state during the execution of a display list remain after execution of the display list is completed.</span></span> <span data-ttu-id="80a06-121">Um den OpenGL-Zustand über **glCallList** -Aufrufe beizubehalten, verwenden Sie " [**glpushattab**](glpushattrib.md)", " [**glpopattab**](glpopattrib.md)", " [**glPushMatrix**](glpushmatrix.md)" und " [**glPopMatrix**](glpopmatrix.md)".</span><span class="sxs-lookup"><span data-stu-id="80a06-121">To preserve the OpenGL state across **glCallList** calls, use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md).</span></span>

<span data-ttu-id="80a06-122">Sie können Anzeigelisten zwischen einem Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden " [**glEnd**](glend.md)"-Befehl ausführen, solange die Anzeigeliste nur Funktionen enthält, die in diesem Intervall zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="80a06-122">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="80a06-123">Die folgenden Funktionen rufen Informationen im Zusammenhang mit " **glCallList**" ab:</span><span class="sxs-lookup"><span data-stu-id="80a06-123">The following functions retrieve information related to **glCallList**:</span></span>

<span data-ttu-id="80a06-124">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max. \_ Listen Schachtelung \_</span><span class="sxs-lookup"><span data-stu-id="80a06-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="80a06-125">**glislist**</span><span class="sxs-lookup"><span data-stu-id="80a06-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="80a06-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80a06-126">Requirements</span></span>



| <span data-ttu-id="80a06-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80a06-127">Requirement</span></span> | <span data-ttu-id="80a06-128">Wert</span><span class="sxs-lookup"><span data-stu-id="80a06-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80a06-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80a06-129">Minimum supported client</span></span><br/> | <span data-ttu-id="80a06-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80a06-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="80a06-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80a06-131">Minimum supported server</span></span><br/> | <span data-ttu-id="80a06-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80a06-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="80a06-133">Header</span><span class="sxs-lookup"><span data-stu-id="80a06-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="80a06-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a06-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="80a06-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="80a06-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="80a06-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80a06-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="80a06-137">DLL</span><span class="sxs-lookup"><span data-stu-id="80a06-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80a06-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80a06-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a06-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80a06-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a06-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="80a06-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="80a06-141">**glcalllists**</span><span class="sxs-lookup"><span data-stu-id="80a06-141">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="80a06-142">**gldelta etelists**</span><span class="sxs-lookup"><span data-stu-id="80a06-142">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="80a06-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="80a06-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="80a06-144">**glgenlists**</span><span class="sxs-lookup"><span data-stu-id="80a06-144">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="80a06-145">**glget**</span><span class="sxs-lookup"><span data-stu-id="80a06-145">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="80a06-146">**glislist**</span><span class="sxs-lookup"><span data-stu-id="80a06-146">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="80a06-147">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="80a06-147">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="80a06-148">**glpopattenb**</span><span class="sxs-lookup"><span data-stu-id="80a06-148">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="80a06-149">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="80a06-149">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="80a06-150">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="80a06-150">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="80a06-151">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="80a06-151">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





