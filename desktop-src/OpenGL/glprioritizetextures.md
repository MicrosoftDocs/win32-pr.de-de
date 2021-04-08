---
title: glpriorizetexturen-Funktion (GL. h)
description: Die Funktion "glpriorizetexturen" legt die Residenz Priorität von Texturen fest.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- glpriorizetexturen-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740648"
---
# <a name="glprioritizetextures-function"></a><span data-ttu-id="b522a-104">glpriorizetexturen-Funktion</span><span class="sxs-lookup"><span data-stu-id="b522a-104">glPrioritizeTextures function</span></span>

<span data-ttu-id="b522a-105">Die Funktion " **glpriorizetexturen** " legt die Residenz Priorität von Texturen fest.</span><span class="sxs-lookup"><span data-stu-id="b522a-105">The **glPrioritizeTextures** function sets the residence priority of textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="b522a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b522a-106">Syntax</span></span>


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a><span data-ttu-id="b522a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b522a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b522a-108">*n*</span><span class="sxs-lookup"><span data-stu-id="b522a-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="b522a-109">Die Anzahl der Texturen, die priorisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b522a-109">The number of textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="b522a-110">*Textur*</span><span class="sxs-lookup"><span data-stu-id="b522a-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="b522a-111">Ein Zeiger auf das erste Element eines Arrays mit den Namen der Texturen, die priorisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b522a-111">A pointer to the first element of an array containing the names of the textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="b522a-112">*Prioritäten*</span><span class="sxs-lookup"><span data-stu-id="b522a-112">*priorities*</span></span> 
</dt> <dd>

<span data-ttu-id="b522a-113">Ein Zeiger auf das erste Element eines Arrays, das die Textur Prioritäten enthält.</span><span class="sxs-lookup"><span data-stu-id="b522a-113">A pointer to the first element of an array containing the texture priorities.</span></span> <span data-ttu-id="b522a-114">Eine Priorität, die in einem Element des *Prioritäten* -Parameters angegeben wird, gilt für die Textur, die durch das entsprechende Element des *Texturen* -Parameters benannt wird.</span><span class="sxs-lookup"><span data-stu-id="b522a-114">A priority given in an element of the *priorities* parameter applies to the texture named by the corresponding element of the *textures* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b522a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b522a-115">Return value</span></span>

<span data-ttu-id="b522a-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b522a-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b522a-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b522a-117">Error codes</span></span>

<span data-ttu-id="b522a-118">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b522a-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b522a-119">Name</span><span class="sxs-lookup"><span data-stu-id="b522a-119">Name</span></span>                                                                                                  | <span data-ttu-id="b522a-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b522a-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b522a-121"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="b522a-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b522a-122">*n* war ein negativer Wert.</span><span class="sxs-lookup"><span data-stu-id="b522a-122">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="b522a-123"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b522a-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b522a-124">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b522a-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b522a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b522a-125">Remarks</span></span>

<span data-ttu-id="b522a-126">Die Funktion " **glpriorizetexturen** " weist die im Parameter " *Prioritäten* " *angegebenen n-Textur Prioritäten* den *n* -Texturen zu, die im *Texturen* -Parameter genannt werden.</span><span class="sxs-lookup"><span data-stu-id="b522a-126">The **glPrioritizeTextures** function assigns the *n* texture priorities specified in the *priorities* parameter to the *n* textures named in the *textures* parameter.</span></span> <span data-ttu-id="b522a-127">Auf Computern mit einer begrenzten Menge an Textur Arbeitsspeicher erstellt OpenGL einen "Workingset" von Texturen, die im Texturspeicher ansässig sind.</span><span class="sxs-lookup"><span data-stu-id="b522a-127">On computers with a limited amount of texture memory, OpenGL establishes a "working set" of textures that are resident in texture memory.</span></span> <span data-ttu-id="b522a-128">Diese Texturen können wesentlich effizienter an ein Textur Ziel gebunden werden als nicht residente Texturen.</span><span class="sxs-lookup"><span data-stu-id="b522a-128">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="b522a-129">Durch die Angabe einer Priorität für jede Textur können Sie mit der Funktion " **glpriorizetexturen** " bestimmen, welche Texturen ansässig sein sollten.</span><span class="sxs-lookup"><span data-stu-id="b522a-129">By specifying a priority for each texture, the **glPrioritizeTextures** function enables you to determine which textures should be resident.</span></span>

<span data-ttu-id="b522a-130">Die Elemente der Textur Prioritäten *werden an* den Bereich \[ 0,0 und 1,0 gebunden, \] bevor Sie zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b522a-130">The texture priorities elements in *priorities* are clamped to the range \[0.0, 1.0\] before being assigned.</span></span> <span data-ttu-id="b522a-131">NULL gibt die niedrigste Priorität an. Daher ist die Wahrscheinlichkeit, dass Texturen mit der Priorität 0 (null) wahrscheinlich nicht in der</span><span class="sxs-lookup"><span data-stu-id="b522a-131">Zero indicates the lowest priority; thus textures with priority zero are least likely to be resident.</span></span> <span data-ttu-id="b522a-132">Der Wert 1,0 gibt die höchste Priorität an. Folglich sind Texturen mit Priorität 1,0 höchstwahrscheinlich ansässig.</span><span class="sxs-lookup"><span data-stu-id="b522a-132">The value 1.0 indicates the highest priority; thus textures with priority 1.0 are most likely to be resident.</span></span> <span data-ttu-id="b522a-133">Es ist jedoch nicht gewährleistet, dass Texturen in den residenten Leben, bis Sie gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="b522a-133">However, textures are not guaranteed to be resident until they are bound.</span></span>

<span data-ttu-id="b522a-134">Die Funktion " **glpriorizetexturen** " ignoriert Versuche, Textur 0 oder einen beliebigen Textur Namen zu priorisieren, der keiner vorhandenen Textur entspricht.</span><span class="sxs-lookup"><span data-stu-id="b522a-134">The **glPrioritizeTextures** function ignores attempts to prioritize texture 0, or any texture name that does not correspond to an existing texture.</span></span> <span data-ttu-id="b522a-135">Keine der Funktionen, die durch den *Texturen* -Parameter benannt werden, muss an ein Textur Ziel gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b522a-135">None of the functions named by the *textures* parameter need to be bound to a texture target.</span></span>

<span data-ttu-id="b522a-136">Wenn eine Textur momentan gebunden ist, können Sie auch die [**gltexparameter**](gltexparameter-functions.md) -Funktion verwenden, um die Priorität festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b522a-136">If a texture is currently bound, you can also use the [**glTexParameter**](gltexparameter-functions.md) function to set its priority.</span></span> <span data-ttu-id="b522a-137">Dies ist die einzige Möglichkeit, die Priorität einer Standard Textur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b522a-137">This is the only way to set the priority of a default texture.</span></span>

<span data-ttu-id="b522a-138">Sie können **glpriorizetexturen** in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="b522a-138">You can include **glPrioritizeTextures** in display lists.</span></span>

<span data-ttu-id="b522a-139">Die folgende Funktion Ruft die Priorität einer zurzeit gebundenen Textur ab, die sich auf **glpriorizetexturen** bezieht:</span><span class="sxs-lookup"><span data-stu-id="b522a-139">The following function retrieves the priority of a currently-bound texture related to **glPrioritizeTextures**:</span></span>

-   <span data-ttu-id="b522a-140">[**glgettexparameter**](glgettexparameter.md) mit Parameter Name GL \_ Textur \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="b522a-140">[**glGetTexParameter**](glgettexparameter.md) with parameter name GL\_TEXTURE\_PRIORITY</span></span>

> [!Note]  
> <span data-ttu-id="b522a-141">Die Funktion " **glpriorizetexturen** " ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b522a-141">The **glPrioritizeTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b522a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b522a-142">Requirements</span></span>



| <span data-ttu-id="b522a-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b522a-143">Requirement</span></span> | <span data-ttu-id="b522a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="b522a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b522a-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b522a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b522a-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b522a-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b522a-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b522a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b522a-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b522a-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b522a-149">Header</span><span class="sxs-lookup"><span data-stu-id="b522a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b522a-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b522a-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b522a-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b522a-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="b522a-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b522a-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b522a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="b522a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b522a-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b522a-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b522a-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b522a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b522a-156">**glaretexturesresidente**</span><span class="sxs-lookup"><span data-stu-id="b522a-156">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="b522a-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b522a-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b522a-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b522a-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b522a-159">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="b522a-159">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="b522a-160">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b522a-160">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b522a-161">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b522a-161">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b522a-162">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="b522a-162">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





