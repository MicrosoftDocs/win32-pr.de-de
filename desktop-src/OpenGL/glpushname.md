---
title: glpushname-Funktion (GL. h)
description: Die Funktionen "glpushname" und "glpopname" schieben den namens Stapel per Push und Pop. | glpushname-Funktion (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glpushname-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371856"
---
# <a name="glpushname-function"></a><span data-ttu-id="05b99-105">glpushname-Funktion</span><span class="sxs-lookup"><span data-stu-id="05b99-105">glPushName function</span></span>

<span data-ttu-id="05b99-106">Die Funktionen " **glpushname** " und " [**glpopname**](glpopname.md) " schieben den namens Stapel per Push und Pop.</span><span class="sxs-lookup"><span data-stu-id="05b99-106">The **glPushName** and [**glPopName**](glpopname.md) functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b99-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05b99-107">Syntax</span></span>


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="05b99-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05b99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05b99-109">*name*</span><span class="sxs-lookup"><span data-stu-id="05b99-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="05b99-110">Ein Name, der auf den Namen Stapel verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="05b99-110">A name that will be pushed onto the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05b99-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05b99-111">Return value</span></span>

<span data-ttu-id="05b99-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="05b99-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="05b99-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="05b99-113">Error codes</span></span>

<span data-ttu-id="05b99-114">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="05b99-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="05b99-115">Name</span><span class="sxs-lookup"><span data-stu-id="05b99-115">Name</span></span>                                                                                                  | <span data-ttu-id="05b99-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="05b99-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05b99-117"><dt>**GL- \_ Stapel \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="05b99-117"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="05b99-118">Die Funktion wurde aufgerufen, während der aktuelle Matrix Stapel voll war.</span><span class="sxs-lookup"><span data-stu-id="05b99-118">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="05b99-119"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="05b99-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="05b99-120">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="05b99-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="05b99-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05b99-121">Remarks</span></span>

<span data-ttu-id="05b99-122">Die **glpushname** -Funktion bewirkt, dass der Name auf dem namens Stapel abgelegt wird, der anfänglich leer ist.</span><span class="sxs-lookup"><span data-stu-id="05b99-122">The **glPushName** function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="05b99-123">Die Funktion " [**glpopname**](glpopname.md) " holt einen Namen vom oberen Rand des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="05b99-123">The [**glPopName**](glpopname.md) function pops one name off the top of the stack.</span></span> <span data-ttu-id="05b99-124">Der namens Stapel wird im Auswahlmodus verwendet, damit Sätze von renderingbefehlen eindeutig identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="05b99-124">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="05b99-125">Sie besteht aus einer geordneten Menge von Ganzzahlen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="05b99-125">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="05b99-126">Der namens Stapel ist immer leer, während der Rendermodus nicht die GL Select-Option ist \_ .</span><span class="sxs-lookup"><span data-stu-id="05b99-126">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="05b99-127">Aufrufe von **glpushname** oder [**glpopname**](glpopname.md) , während der Rendermodus nicht gl SELECT ist, \_ werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="05b99-127">Calls to **glPushName** or [**glPopName**](glpopname.md) while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="05b99-128">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpushname** und [**glpopname**](glpopname.md)ab:</span><span class="sxs-lookup"><span data-stu-id="05b99-128">The following functions retrieve information related to **glPushName** and [**glPopName**](glpopname.md):</span></span>

<span data-ttu-id="05b99-129">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Name \_ Stack- \_ Tiefe"</span><span class="sxs-lookup"><span data-stu-id="05b99-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="05b99-130">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max \_ Name Stack- \_ \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="05b99-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="05b99-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05b99-131">Requirements</span></span>



| <span data-ttu-id="05b99-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05b99-132">Requirement</span></span> | <span data-ttu-id="05b99-133">Wert</span><span class="sxs-lookup"><span data-stu-id="05b99-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05b99-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05b99-134">Minimum supported client</span></span><br/> | <span data-ttu-id="05b99-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05b99-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="05b99-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05b99-136">Minimum supported server</span></span><br/> | <span data-ttu-id="05b99-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05b99-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05b99-138">Header</span><span class="sxs-lookup"><span data-stu-id="05b99-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="05b99-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="05b99-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="05b99-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="05b99-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="05b99-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05b99-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="05b99-142">DLL</span><span class="sxs-lookup"><span data-stu-id="05b99-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05b99-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05b99-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05b99-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05b99-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b99-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="05b99-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="05b99-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="05b99-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="05b99-147">**glinitnames**</span><span class="sxs-lookup"><span data-stu-id="05b99-147">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="05b99-148">**glloadname**</span><span class="sxs-lookup"><span data-stu-id="05b99-148">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="05b99-149">**glrendermode**</span><span class="sxs-lookup"><span data-stu-id="05b99-149">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="05b99-150">**glselectbuffer**</span><span class="sxs-lookup"><span data-stu-id="05b99-150">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





