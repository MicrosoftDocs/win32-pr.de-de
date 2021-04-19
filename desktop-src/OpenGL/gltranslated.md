---
title: glsetzte-Funktion (GL. h)
description: Die gltranslation-Funktion multipliziert die aktuelle Matrix mit einer Übersetzungs Matrix.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- glsetzenfunktion OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106373412"
---
# <a name="gltranslated-function"></a><span data-ttu-id="280b3-104">glsetzte-Funktion</span><span class="sxs-lookup"><span data-stu-id="280b3-104">glTranslated function</span></span>

<span data-ttu-id="280b3-105">Die **gltranslation** -Funktion multipliziert die aktuelle Matrix mit einer Übersetzungs Matrix.</span><span class="sxs-lookup"><span data-stu-id="280b3-105">The **glTranslated** function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="280b3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="280b3-106">Syntax</span></span>


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="280b3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="280b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="280b3-108">*x*</span><span class="sxs-lookup"><span data-stu-id="280b3-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="280b3-109">Die *x* -Koordinate eines Übersetzungs Vektors.</span><span class="sxs-lookup"><span data-stu-id="280b3-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="280b3-110">*y*</span><span class="sxs-lookup"><span data-stu-id="280b3-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="280b3-111">Die *y* -Koordinate eines Übersetzungs Vektors.</span><span class="sxs-lookup"><span data-stu-id="280b3-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="280b3-112">*z*</span><span class="sxs-lookup"><span data-stu-id="280b3-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="280b3-113">Die *z* -Koordinate eines Übersetzungs Vektors.</span><span class="sxs-lookup"><span data-stu-id="280b3-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="280b3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="280b3-114">Return value</span></span>

<span data-ttu-id="280b3-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="280b3-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="280b3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="280b3-116">Remarks</span></span>

<span data-ttu-id="280b3-117">Die **gltranslation** -Funktion erzeugt die durch angegebene Übersetzung (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="280b3-117">The **glTranslated** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="280b3-118">Der Übersetzungs Vektor wird verwendet, um eine 4 x 4-Übersetzungs Matrix zu berechnen:</span><span class="sxs-lookup"><span data-stu-id="280b3-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Diagramm, das die durch x, y, z angegebene 4 x 4-Übersetzungs Matrix anzeigt.](images/trans01.png)

<span data-ttu-id="280b3-120">Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Übersetzungs Matrix multipliziert, und das Produkt ersetzt die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="280b3-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="280b3-121">Das heißt, wenn m die aktuelle Matrix und T die Übersetzungs Matrix ist, wird m durch m T ersetzt.</span><span class="sxs-lookup"><span data-stu-id="280b3-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="280b3-122">Wenn der Matrix Modus entweder eine GL \_ Modelview-oder GL- \_ Projektion ist, werden alle Objekte, die nach dem Aufruf von **glübersetzt** gezeichnet werden, übersetzt.</span><span class="sxs-lookup"><span data-stu-id="280b3-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslated** is called are translated.</span></span> <span data-ttu-id="280b3-123">Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und **glPopMatrix** , um das nicht übersetzte Koordinatensystem zu speichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="280b3-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="280b3-124">Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glübersetzt**](gltranslate.md)ab:</span><span class="sxs-lookup"><span data-stu-id="280b3-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md):</span></span>

<span data-ttu-id="280b3-125">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="280b3-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="280b3-126">**glget** mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="280b3-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="280b3-127">**glget** mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="280b3-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="280b3-128">**glget** mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="280b3-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="280b3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="280b3-129">Requirements</span></span>



| <span data-ttu-id="280b3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="280b3-130">Requirement</span></span> | <span data-ttu-id="280b3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="280b3-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="280b3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="280b3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="280b3-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="280b3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="280b3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="280b3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="280b3-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="280b3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="280b3-136">Header</span><span class="sxs-lookup"><span data-stu-id="280b3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="280b3-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="280b3-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="280b3-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="280b3-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="280b3-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="280b3-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="280b3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="280b3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="280b3-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="280b3-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="280b3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="280b3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="280b3-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="280b3-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="280b3-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="280b3-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="280b3-145">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="280b3-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="280b3-146">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="280b3-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="280b3-147">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="280b3-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="280b3-148">**glrotation**</span><span class="sxs-lookup"><span data-stu-id="280b3-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="280b3-149">**glscale**</span><span class="sxs-lookup"><span data-stu-id="280b3-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 





