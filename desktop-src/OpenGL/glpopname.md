---
title: glpopname-Funktion (GL. h)
description: Die Funktionen "glpushname" und "glpopname" schieben den namens Stapel per Push und Pop. | glpopname-Funktion (GL. h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- glpopname-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 830c4937b30cca64de3063b42ad16dd3adc87c89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355767"
---
# <a name="glpopname-function"></a><span data-ttu-id="3dc9a-105">glpopname-Funktion</span><span class="sxs-lookup"><span data-stu-id="3dc9a-105">glPopName function</span></span>

<span data-ttu-id="3dc9a-106">Die Funktionen " [**glpushname**](glpushname.md) " und " **glpopname** " schieben den namens Stapel per Push und Pop.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-106">The [**glPushName**](glpushname.md) and **glPopName** functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc9a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dc9a-107">Syntax</span></span>


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a><span data-ttu-id="3dc9a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dc9a-108">Parameters</span></span>

<span data-ttu-id="3dc9a-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3dc9a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dc9a-110">Return value</span></span>

<span data-ttu-id="3dc9a-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3dc9a-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3dc9a-112">Error codes</span></span>

<span data-ttu-id="3dc9a-113">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3dc9a-114">Name</span><span class="sxs-lookup"><span data-stu-id="3dc9a-114">Name</span></span>                                                                                                  | <span data-ttu-id="3dc9a-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3dc9a-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3dc9a-116"><dt>**GL. \_ Stapel \_ Unterlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="3dc9a-116"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="3dc9a-117">Die Funktion wurde aufgerufen, während der aktuelle Matrix Stapel nur eine einzelne Matrix enthielt.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-117">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="3dc9a-118"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="3dc9a-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3dc9a-119">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3dc9a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dc9a-120">Remarks</span></span>

<span data-ttu-id="3dc9a-121">Die [**glpushname**](glpushname.md) -Funktion bewirkt, dass der Name auf dem namens Stapel abgelegt wird, der anfänglich leer ist.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-121">The [**glPushName**](glpushname.md) function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="3dc9a-122">Die Funktion " **glpopname** " holt einen Namen vom oberen Rand des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-122">The **glPopName** function pops one name off the top of the stack.</span></span> <span data-ttu-id="3dc9a-123">Der namens Stapel wird im Auswahlmodus verwendet, damit Sätze von renderingbefehlen eindeutig identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-123">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="3dc9a-124">Sie besteht aus einer geordneten Menge von Ganzzahlen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-124">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="3dc9a-125">Der namens Stapel ist immer leer, während der Rendermodus nicht die GL Select-Option ist \_ .</span><span class="sxs-lookup"><span data-stu-id="3dc9a-125">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="3dc9a-126">Aufrufe von [**glpushname**](glpushname.md) oder **glpopname** , während der Rendermodus nicht gl SELECT ist, \_ werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3dc9a-126">Calls to [**glPushName**](glpushname.md) or **glPopName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="3dc9a-127">Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glpushname**](glpushname.md) und **glpopname** ab:</span><span class="sxs-lookup"><span data-stu-id="3dc9a-127">The following functions retrieve information related to [**glPushName**](glpushname.md) and **glPopName**:</span></span>

<span data-ttu-id="3dc9a-128">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Name \_ Stack- \_ Tiefe"</span><span class="sxs-lookup"><span data-stu-id="3dc9a-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="3dc9a-129">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max \_ Name Stack- \_ \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="3dc9a-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc9a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dc9a-130">Requirements</span></span>



| <span data-ttu-id="3dc9a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dc9a-131">Requirement</span></span> | <span data-ttu-id="3dc9a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3dc9a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc9a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dc9a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc9a-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dc9a-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3dc9a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dc9a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc9a-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dc9a-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3dc9a-137">Header</span><span class="sxs-lookup"><span data-stu-id="3dc9a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dc9a-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dc9a-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3dc9a-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3dc9a-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="3dc9a-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dc9a-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3dc9a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3dc9a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dc9a-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dc9a-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dc9a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dc9a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc9a-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3dc9a-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3dc9a-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3dc9a-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3dc9a-146">**glinitnames**</span><span class="sxs-lookup"><span data-stu-id="3dc9a-146">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="3dc9a-147">**glloadname**</span><span class="sxs-lookup"><span data-stu-id="3dc9a-147">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="3dc9a-148">**glrendermode**</span><span class="sxs-lookup"><span data-stu-id="3dc9a-148">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="3dc9a-149">**glselectbuffer**</span><span class="sxs-lookup"><span data-stu-id="3dc9a-149">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





