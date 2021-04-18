---
title: glmateriali-Funktion (GL. h)
description: Die Funktion "-glmateriali" gibt Materialparameter für das Beleuchtungsmodell an.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- glmateriali-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc4f1bf6628f1674cf9c3534b9f0c9d028246d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338716"
---
# <a name="glmateriali-function"></a><span data-ttu-id="e196a-104">glmateriali-Funktion</span><span class="sxs-lookup"><span data-stu-id="e196a-104">glMateriali function</span></span>

<span data-ttu-id="e196a-105">Die **glmateriali** -Funktion gibt Materialparameter für das Beleuchtungsmodell an.</span><span class="sxs-lookup"><span data-stu-id="e196a-105">The **glMateriali** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="e196a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e196a-106">Syntax</span></span>


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="e196a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e196a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e196a-108">*mit*</span><span class="sxs-lookup"><span data-stu-id="e196a-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="e196a-109">Die Gesichter oder Gesichter, die aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e196a-109">The face or faces that are being updated.</span></span> <span data-ttu-id="e196a-110">Muss eines der folgenden sein: GL \_ Front, GL \_ Back, GL \_ Front und GL \_ Back.</span><span class="sxs-lookup"><span data-stu-id="e196a-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="e196a-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="e196a-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="e196a-112">Der einwertige Materialparameter der Gesichts-oder Gesichter, die aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e196a-112">The single-valued material parameter of the face or faces being updated.</span></span> <span data-ttu-id="e196a-113">Muss ein GL- \_ Glanz sein.</span><span class="sxs-lookup"><span data-stu-id="e196a-113">Must be GL\_SHININESS.</span></span>



| <span data-ttu-id="e196a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e196a-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="e196a-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e196a-115">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="e196a-116"><dt>**GL \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="e196a-116"><dt>**GL\_SHININESS**</dt></span></span> </dl> | <span data-ttu-id="e196a-117">Der *param* -Parameter ist eine einzelne ganze Zahl, die den Glanz der RGBA-Darstellung des Materials angibt.</span><span class="sxs-lookup"><span data-stu-id="e196a-117">The *param* parameter is a single integer that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="e196a-118">Ganzzahlige Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e196a-118">Integer values are mapped directly.</span></span> <span data-ttu-id="e196a-119">Nur Werte im Bereich von \[ 0, 128 \] werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e196a-119">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="e196a-120">Der standardmäßige Glanz Exponent für die Vorder-und Hintergrundmaterialien ist 0.</span><span class="sxs-lookup"><span data-stu-id="e196a-120">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="e196a-121">*param*</span><span class="sxs-lookup"><span data-stu-id="e196a-121">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="e196a-122">Der Wert, auf den der Parameter GL- \_ Glanz festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e196a-122">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e196a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e196a-123">Return value</span></span>

<span data-ttu-id="e196a-124">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e196a-124">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e196a-125">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e196a-125">Error codes</span></span>

<span data-ttu-id="e196a-126">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e196a-126">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e196a-127">Name</span><span class="sxs-lookup"><span data-stu-id="e196a-127">Name</span></span>                                                                                              | <span data-ttu-id="e196a-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e196a-128">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e196a-129"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e196a-129"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="e196a-130">Entweder *Face* oder *PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="e196a-130">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="e196a-131"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="e196a-131"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="e196a-132">Ein Glanz Exponent außerhalb des Bereichs von \[ 0, 128 \] wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="e196a-132">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e196a-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e196a-133">Remarks</span></span>

<span data-ttu-id="e196a-134">Die Funktion " **glmateriali** " weist Materialparametern Werte zu.</span><span class="sxs-lookup"><span data-stu-id="e196a-134">The **glMateriali** function assigns values to material parameters.</span></span> <span data-ttu-id="e196a-135">Es gibt zwei übereinstimmende Sätze von Materialparametern.</span><span class="sxs-lookup"><span data-stu-id="e196a-135">There are two matched sets of material parameters.</span></span> <span data-ttu-id="e196a-136">Eine, die *Front-End-* Gruppe, wird zum Schattieren von Punkten, Linien, Bitmaps und allen Polygonen verwendet (wenn die zweiseitige Beleuchtung deaktiviert ist), oder nur mit Front-End-Polygonen (bei aktivierter zweiseitiger Beleuchtung).</span><span class="sxs-lookup"><span data-stu-id="e196a-136">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="e196a-137">Der andere Satz, mit dem *Hintergrund*, wird verwendet, um nur rückwärts gerichtete Polygone zu schattieren, wenn die zweiseitige Beleuchtung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e196a-137">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="e196a-138">Ausführliche Informationen zu einseitigen und zweiseitigen Beleuchtungsberechnungen finden Sie unter " [**gllightmodel**](gllightmodel-functions.md) ".</span><span class="sxs-lookup"><span data-stu-id="e196a-138">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="e196a-139">Die **glmateriali** -Funktion erfordert drei Argumente.</span><span class="sxs-lookup"><span data-stu-id="e196a-139">The **glMateriali** function takes three arguments.</span></span> <span data-ttu-id="e196a-140">*Mit* dem ersten, dem Vordergrund, wird angegeben, ob die GL \_ -Front-Materialien, die GL \_ -Back-Materialien oder die \_ Vorder \_ -und \_ Hintergrundmaterialien von GL geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e196a-140">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="e196a-141">Der zweite Wert, *PName*, gibt an, welche von mehreren Parametern in einem oder beiden Sätzen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e196a-141">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="e196a-142">Der dritte Parameter gibt *an, welcher* Wert dem angegebenen Parameter zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e196a-142">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="e196a-143">Material Parameter werden in der Beleuchtungs Gleichung verwendet, die optional auf jeden Scheitelpunkt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e196a-143">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="e196a-144">Die Gleichung wird in " [**gllightmodel**](gllightmodel-functions.md)" erläutert.</span><span class="sxs-lookup"><span data-stu-id="e196a-144">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="e196a-145">Die Materialparameter können jederzeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e196a-145">The material parameters can be updated at any time.</span></span> <span data-ttu-id="e196a-146">Insbesondere kann **glmateriali** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e196a-146">In particular, **glMateriali** can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="e196a-147">Wenn nur ein einzelner Materialparameter pro Scheitelpunkt geändert werden soll, wird [**glcolormaterial**](glcolormaterial.md) gegenüber **glmateriali** bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="e196a-147">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMateriali**.</span></span>

<span data-ttu-id="e196a-148">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glmateriali** ab:</span><span class="sxs-lookup"><span data-stu-id="e196a-148">The following function retrieves information related to **glMateriali**:</span></span>

[<span data-ttu-id="e196a-149">**glgetmaterial**</span><span class="sxs-lookup"><span data-stu-id="e196a-149">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="e196a-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e196a-150">Requirements</span></span>



| <span data-ttu-id="e196a-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e196a-151">Requirement</span></span> | <span data-ttu-id="e196a-152">Wert</span><span class="sxs-lookup"><span data-stu-id="e196a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e196a-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e196a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e196a-154">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e196a-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e196a-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e196a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e196a-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e196a-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e196a-157">Header</span><span class="sxs-lookup"><span data-stu-id="e196a-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="e196a-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e196a-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e196a-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e196a-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="e196a-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e196a-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e196a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="e196a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e196a-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e196a-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e196a-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e196a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e196a-164">**glcolormaterial**</span><span class="sxs-lookup"><span data-stu-id="e196a-164">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="e196a-165">**gllight**</span><span class="sxs-lookup"><span data-stu-id="e196a-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="e196a-166">**gllightmodel**</span><span class="sxs-lookup"><span data-stu-id="e196a-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





