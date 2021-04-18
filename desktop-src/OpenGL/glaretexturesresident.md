---
title: glaretexturesresidente-Funktion (GL. h)
description: Die glaretexturesresidente-Funktion bestimmt, ob angegebene Textur Objekte im Texturspeicher ansässig sind.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glaretexturesresidente-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338550"
---
# <a name="glaretexturesresident-function"></a><span data-ttu-id="47457-104">glaretexturesresidente-Funktion</span><span class="sxs-lookup"><span data-stu-id="47457-104">glAreTexturesResident function</span></span>

<span data-ttu-id="47457-105">Die **glaretexturesresidente** -Funktion bestimmt, ob angegebene Textur Objekte im Texturspeicher ansässig sind.</span><span class="sxs-lookup"><span data-stu-id="47457-105">The **glAreTexturesResident** function determines whether specified texture objects are resident in texture memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="47457-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="47457-106">Syntax</span></span>


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a><span data-ttu-id="47457-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="47457-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47457-108">*n*</span><span class="sxs-lookup"><span data-stu-id="47457-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="47457-109">Die Anzahl der Texturen, die abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47457-109">The number of textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="47457-110">*Textur*</span><span class="sxs-lookup"><span data-stu-id="47457-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="47457-111">Die Adresse eines Arrays mit den Namen der zu abgefragten Texturen.</span><span class="sxs-lookup"><span data-stu-id="47457-111">The address of an array containing the names of the textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="47457-112">*Heimen*</span><span class="sxs-lookup"><span data-stu-id="47457-112">*residences*</span></span> 
</dt> <dd>

<span data-ttu-id="47457-113">Die Adresse eines Arrays, in dem der Status der Textur Residenz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="47457-113">The address of an array in which the texture residence status is returned.</span></span> <span data-ttu-id="47457-114">Der Wohnsitz Status einer Textur, die durch ein Element von *Texturen* benannt wird, wird im entsprechenden-Element von- *Residenzen* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47457-114">The residence status of a texture named by an element of *textures* is returned in the corresponding element of *residences*.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="47457-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="47457-115">Error codes</span></span>

<span data-ttu-id="47457-116">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="47457-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="47457-117">Name</span><span class="sxs-lookup"><span data-stu-id="47457-117">Name</span></span>                                                                                                  | <span data-ttu-id="47457-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="47457-118">Meaning</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47457-119"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="47457-119"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="47457-120">*n* war ein negativer Wert, ein Element in *Texturen* war NULL, oder ein Element in *Texturen* enthielt keinen Textur Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="47457-120">*n* was a negative value, an element in *textures* was zero, or an element in *textures* did not contain a texture identifier.</span></span><br/> |
| <dl> <span data-ttu-id="47457-121"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="47457-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="47457-122">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="47457-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="47457-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47457-123">Remarks</span></span>

<span data-ttu-id="47457-124">Auf Computern mit einer begrenzten Menge an Textur Arbeitsspeicher erstellt OpenGL einen Funktions Satz von Texturen, die im Texturspeicher ansässig sind.</span><span class="sxs-lookup"><span data-stu-id="47457-124">On machines with a limited amount of texture memory, OpenGL establishes a working set of textures that are resident in texture memory.</span></span> <span data-ttu-id="47457-125">Diese Texturen können wesentlich effizienter an ein Textur Ziel gebunden werden als nicht residente Texturen.</span><span class="sxs-lookup"><span data-stu-id="47457-125">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="47457-126">Die **glaretexturesresidente** -Funktion fragt den Textur Residenz Status der *n* Texturen ab, die von den Elementen der *Texturen* benannt werden.</span><span class="sxs-lookup"><span data-stu-id="47457-126">The **glAreTexturesResident** function queries the texture residence status of the *n* textures named by the elements of *textures*.</span></span> <span data-ttu-id="47457-127">Wenn alle benannten Texturen Residenten sind, gibt **glaretexturesresidenten** den Wert "GL true" zurück \_ , und die Inhalte der residenten werden nicht beeinträchtigt. </span><span class="sxs-lookup"><span data-stu-id="47457-127">If all the named textures are resident, **glAreTexturesResident** returns GL\_TRUE, and the contents of *residences* are undisturbed.</span></span> <span data-ttu-id="47457-128">Wenn eine der benannten Texturen nicht Resident ist, gibt **glaretexturesresidenten** den Wert "GL false" zurück \_ , und der ausführliche Status wird in den *n* -Elementen von Residenten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47457-128">If any of the named textures are not resident, **glAreTexturesResident** returns GL\_FALSE, and detailed status is returned in the *n* elements of *residences*.</span></span>

<span data-ttu-id="47457-129">Wenn ein Element von *Residenzen* den Wert GL \_ true hat, ist die Textur, die durch das entsprechende Element von *Texturen* benannt ist, im Texturspeicher ansässig.</span><span class="sxs-lookup"><span data-stu-id="47457-129">If an element of *residences* is GL\_TRUE, then the texture named by the corresponding element of *textures* is resident in texture memory.</span></span>

<span data-ttu-id="47457-130">Um den Status einer einzelnen gebundenen Textur abzufragen, nennen Sie [**glgettexparameter**](glgettexparameter.md) , wobei der *Ziel* Parameter auf die Ziel Textur festgelegt ist, an die das Ziel gebunden ist, und legen Sie den Parameter " *PName* " auf "GL \_ Texture \_ residente" fest.</span><span class="sxs-lookup"><span data-stu-id="47457-130">To query the residence status of a single bound texture, call [**glGetTexParameter**](glgettexparameter.md) with the *target* parameter set to the target texture to which the target is bound and set the *pname* parameter to GL\_TEXTURE\_RESIDENT.</span></span> <span data-ttu-id="47457-131">Sie müssen diese Methode verwenden, um den residenten Status einer Standard Textur abzufragen.</span><span class="sxs-lookup"><span data-stu-id="47457-131">You must use this method to query the resident status of a default texture.</span></span>

<span data-ttu-id="47457-132">Sie können **glaretexturesresidenten** nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="47457-132">You cannot include **glAreTexturesResident** in display lists.</span></span>

<span data-ttu-id="47457-133">Die **glaretexturesresidente** -Funktion gibt den Residenz Status der Texturen zum Aufruf Zeitpunkt zurück.</span><span class="sxs-lookup"><span data-stu-id="47457-133">The **glAreTexturesResident** function returns the residency status of the textures at the time of invocation.</span></span> <span data-ttu-id="47457-134">Es wird nicht garantiert, dass die Texturen zu einem beliebigen Zeitpunkt verbleiben.</span><span class="sxs-lookup"><span data-stu-id="47457-134">It does not guarantee that the textures will remain resident at any other time.</span></span>

<span data-ttu-id="47457-135">Wenn sich Texturen im virtuellen Speicher befinden (es gibt keinen Texturspeicher), werden Sie als "immer ansässig" betrachtet.</span><span class="sxs-lookup"><span data-stu-id="47457-135">If textures reside in virtual memory (there is no texture memory), they are considered always resident.</span></span>

> [!Note]  
> <span data-ttu-id="47457-136">Die **glaretexturesresidente** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47457-136">The **glAreTexturesResident** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="47457-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47457-137">Requirements</span></span>



| <span data-ttu-id="47457-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47457-138">Requirement</span></span> | <span data-ttu-id="47457-139">Wert</span><span class="sxs-lookup"><span data-stu-id="47457-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47457-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47457-140">Minimum supported client</span></span><br/> | <span data-ttu-id="47457-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47457-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="47457-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47457-142">Minimum supported server</span></span><br/> | <span data-ttu-id="47457-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47457-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47457-144">Header</span><span class="sxs-lookup"><span data-stu-id="47457-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="47457-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="47457-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="47457-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47457-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="47457-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47457-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="47457-148">DLL</span><span class="sxs-lookup"><span data-stu-id="47457-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47457-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47457-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47457-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47457-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47457-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="47457-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="47457-152">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="47457-152">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="47457-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="47457-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="47457-154">**glgettexparameter**</span><span class="sxs-lookup"><span data-stu-id="47457-154">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="47457-155">**glpriorizetexturen**</span><span class="sxs-lookup"><span data-stu-id="47457-155">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="47457-156">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="47457-156">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="47457-157">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="47457-157">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





