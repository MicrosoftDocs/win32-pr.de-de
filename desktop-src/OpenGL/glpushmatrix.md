---
title: glPushMatrix-Funktion (GL. h)
description: Die Funktionen "glPushMatrix" und "glPopMatrix" schieben den aktuellen Matrix Stapel per Push und Pop. | glPushMatrix-Funktion (GL. h)
ms.assetid: 97d8e644-50bb-4130-b6b7-d87df4468e73
keywords:
- glPushMatrix-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee62b03e221f44db829a7167d642a766af8e129c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961437"
---
# <a name="glpushmatrix-function"></a><span data-ttu-id="c2865-105">glPushMatrix-Funktion</span><span class="sxs-lookup"><span data-stu-id="c2865-105">glPushMatrix function</span></span>

<span data-ttu-id="c2865-106">Die Funktionen " **glPushMatrix** " und " [**glPopMatrix**](glpopmatrix.md) " schieben den aktuellen Matrix Stapel per Push und Pop.</span><span class="sxs-lookup"><span data-stu-id="c2865-106">The **glPushMatrix** and [**glPopMatrix**](glpopmatrix.md) functions push and pop the current matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2865-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2865-107">Syntax</span></span>


```C++
void WINAPI glPushMatrix(void);
```



## <a name="parameters"></a><span data-ttu-id="c2865-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2865-108">Parameters</span></span>

<span data-ttu-id="c2865-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c2865-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2865-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2865-110">Return value</span></span>

<span data-ttu-id="c2865-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c2865-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2865-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c2865-112">Error codes</span></span>

<span data-ttu-id="c2865-113">Es ist ein Fehler, einen vollständigen Matrix Stapel per Push zu übersetzen oder einen Matrix Stapel zu popzen, der nur eine einzelne Matrix enthält.</span><span class="sxs-lookup"><span data-stu-id="c2865-113">It is an error to push a full matrix stack, or to pop a matrix stack that contains only a single matrix.</span></span> <span data-ttu-id="c2865-114">In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="c2865-114">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="c2865-115">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c2865-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c2865-116">Name</span><span class="sxs-lookup"><span data-stu-id="c2865-116">Name</span></span>                                                                                                  | <span data-ttu-id="c2865-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2865-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2865-118"><dt>**GL- \_ Stapel \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="c2865-118"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="c2865-119">Die Funktion wurde aufgerufen, während der aktuelle Matrix Stapel voll war.</span><span class="sxs-lookup"><span data-stu-id="c2865-119">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="c2865-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="c2865-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c2865-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c2865-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c2865-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2865-122">Remarks</span></span>

<span data-ttu-id="c2865-123">Für jeden Matrix Modus gibt es einen Stapel von Matrizen.</span><span class="sxs-lookup"><span data-stu-id="c2865-123">There is a stack of matrices for each of the matrix modes.</span></span> <span data-ttu-id="c2865-124">Im GL- \_ Modelview-Modus ist die Stapel Tiefe mindestens 32.</span><span class="sxs-lookup"><span data-stu-id="c2865-124">In GL\_MODELVIEW mode, the stack depth is at least 32.</span></span> <span data-ttu-id="c2865-125">In den beiden anderen Modi, GL \_ Projection und GL \_ Texture, ist die Tiefe mindestens 2.</span><span class="sxs-lookup"><span data-stu-id="c2865-125">In the other two modes, GL\_PROJECTION and GL\_TEXTURE, the depth is at least 2.</span></span> <span data-ttu-id="c2865-126">Die aktuelle Matrix in einem beliebigen Modus ist die Matrix am oberen Rand des Stapels für diesen Modus.</span><span class="sxs-lookup"><span data-stu-id="c2865-126">The current matrix in any mode is the matrix on the top of the stack for that mode.</span></span>

<span data-ttu-id="c2865-127">Die **glPushMatrix** -Funktion schiebt den aktuellen Matrix Stapel um eins nach unten, wobei die aktuelle Matrix duplizieren wird.</span><span class="sxs-lookup"><span data-stu-id="c2865-127">The **glPushMatrix** function pushes the current matrix stack down by one, duplicating the current matrix.</span></span> <span data-ttu-id="c2865-128">Das heißt, nach einem **glPushMatrix** -Befehl ist die Matrix am oberen Rand des Stapels mit der darunter liegenden Matrix identisch.</span><span class="sxs-lookup"><span data-stu-id="c2865-128">That is, after a **glPushMatrix** call, the matrix on the top of the stack is identical to the one below it.</span></span> <span data-ttu-id="c2865-129">Die Funktion " **glPopMatrix** " holt den aktuellen Matrix Stapel und ersetzt dabei die aktuelle Matrix durch die im Stapel unter dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="c2865-129">The **glPopMatrix** function pops the current matrix stack, replacing the current matrix with the one below it on the stack.</span></span> <span data-ttu-id="c2865-130">Anfänglich enthält jeder Stapel eine Matrix, eine Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="c2865-130">Initially, each of the stacks contains one matrix, an identity matrix.</span></span>

<span data-ttu-id="c2865-131">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPushMatrix** und **glPopMatrix** ab:</span><span class="sxs-lookup"><span data-stu-id="c2865-131">The following functions retrieve information related to **glPushMatrix** and **glPopMatrix**:</span></span>

<span data-ttu-id="c2865-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="c2865-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="c2865-133">**glget** mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="c2865-133">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="c2865-134">**glget** mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="c2865-134">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="c2865-135">**glget** mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="c2865-135">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

<span data-ttu-id="c2865-136">**glget** mit Argument GL \_ Modelview \_ Stack- \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="c2865-136">**glGet** with argument GL\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="c2865-137">**glget** mit der \_ \_ Stapel \_ Tiefe des Arguments GL</span><span class="sxs-lookup"><span data-stu-id="c2865-137">**glGet** with argument GL\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="c2865-138">**glget** mit Argument GL- \_ Textur \_ Stapel \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="c2865-138">**glGet** with argument GL\_TEXTURE\_STACK\_DEPTH</span></span>

<span data-ttu-id="c2865-139">**glget** mit dem Argument GL \_ Max \_ Model View \_ Stack- \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="c2865-139">**glGet** with argument GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="c2865-140">**glget** mit dem Argument GL \_ Max \_ Projection Stack- \_ \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="c2865-140">**glGet** with argument GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="c2865-141">**glget** mit der \_ maximalen \_ Textur \_ Stapel \_ Tiefe des Arguments GL</span><span class="sxs-lookup"><span data-stu-id="c2865-141">**glGet** with argument GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="c2865-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2865-142">Requirements</span></span>



| <span data-ttu-id="c2865-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2865-143">Requirement</span></span> | <span data-ttu-id="c2865-144">Wert</span><span class="sxs-lookup"><span data-stu-id="c2865-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2865-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2865-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c2865-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2865-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2865-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2865-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c2865-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2865-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2865-149">Header</span><span class="sxs-lookup"><span data-stu-id="c2865-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2865-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2865-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c2865-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2865-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2865-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2865-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2865-153">DLL</span><span class="sxs-lookup"><span data-stu-id="c2865-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2865-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2865-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2865-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2865-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2865-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c2865-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c2865-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c2865-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c2865-158">**glfrustum**</span><span class="sxs-lookup"><span data-stu-id="c2865-158">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="c2865-159">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="c2865-159">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="c2865-160">**glloadmatrix**</span><span class="sxs-lookup"><span data-stu-id="c2865-160">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="c2865-161">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="c2865-161">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="c2865-162">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="c2865-162">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="c2865-163">**glortho**</span><span class="sxs-lookup"><span data-stu-id="c2865-163">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="c2865-164">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="c2865-164">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="c2865-165">**glrotation**</span><span class="sxs-lookup"><span data-stu-id="c2865-165">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="c2865-166">**glscale**</span><span class="sxs-lookup"><span data-stu-id="c2865-166">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="c2865-167">**gltranslate**</span><span class="sxs-lookup"><span data-stu-id="c2865-167">**glTranslate**</span></span>](gltranslate.md)
</dt> <dt>

[<span data-ttu-id="c2865-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="c2865-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





