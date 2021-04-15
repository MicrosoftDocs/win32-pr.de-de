---
title: glrotatef-Funktion (GL. h)
description: Die Funktion "glrotatef" multipliziert die aktuelle Matrix mit einer Rotations Matrix.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- glrotatef-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 953b8ffc5f89e5a4cf9901e4cb5fb5afb4c8dfdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479329"
---
# <a name="glrotatef-function"></a><span data-ttu-id="5bdc2-104">glrotatef-Funktion</span><span class="sxs-lookup"><span data-stu-id="5bdc2-104">glRotatef function</span></span>

<span data-ttu-id="5bdc2-105">Die Funktion " **glrotatef** " multipliziert die aktuelle Matrix mit einer Rotations Matrix.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-105">The **glRotatef** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bdc2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bdc2-106">Syntax</span></span>


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="5bdc2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bdc2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bdc2-108">*angle*</span><span class="sxs-lookup"><span data-stu-id="5bdc2-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="5bdc2-109">Der Drehwinkel in Grad.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="5bdc2-110">*x*</span><span class="sxs-lookup"><span data-stu-id="5bdc2-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="5bdc2-111">Die *x* -Koordinate eines Vektors.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="5bdc2-112">*y*</span><span class="sxs-lookup"><span data-stu-id="5bdc2-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="5bdc2-113">Die *y* -Koordinate eines Vektors.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="5bdc2-114">*z*</span><span class="sxs-lookup"><span data-stu-id="5bdc2-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="5bdc2-115">Die *z* -Koordinate eines Vektors.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bdc2-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bdc2-116">Return value</span></span>

<span data-ttu-id="5bdc2-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5bdc2-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="5bdc2-118">Error codes</span></span>

<span data-ttu-id="5bdc2-119">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5bdc2-120">Name</span><span class="sxs-lookup"><span data-stu-id="5bdc2-120">Name</span></span>                                                                                                  | <span data-ttu-id="5bdc2-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5bdc2-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bdc2-122"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="5bdc2-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5bdc2-123">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5bdc2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bdc2-124">Remarks</span></span>

<span data-ttu-id="5bdc2-125">Die **glrotatef** -Funktion berechnet eine Matrix, die eine Drehung gegen den Uhrzeigersinn um den *Vektor vom Ursprung* bis zum Punkt (*x*, *y*, *z*) ausführt.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-125">The **glRotatef** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="5bdc2-126">Die aktuelle Matrix (siehe [**glMatrixMode**](glmatrixmode.md)) wird mit dieser Rotations Matrix multipliziert, und das Produkt ersetzt die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="5bdc2-127">Das heißt, wenn m die aktuelle Matrix und R die Übersetzungs Matrix ist, wird m durch m r ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="5bdc2-128">Wenn der Matrix Modus entweder eine GL \_ Modelview-oder GL- \_ Projektion ist, werden alle Objekte, die nach dem Aufruf von **glrotatef** gezeichnet werden, gedreht.</span><span class="sxs-lookup"><span data-stu-id="5bdc2-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotatef** is called are rotated.</span></span> <span data-ttu-id="5bdc2-129">Verwenden Sie zum Speichern und Wiederherstellen des ungedrehten Koordinatensystems [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix**](glpopmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="5bdc2-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="5bdc2-130">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glrotatef** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="5bdc2-130">The following functions retrieve information related to **glRotatef**:</span></span>

<span data-ttu-id="5bdc2-131">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Rendermodus</span><span class="sxs-lookup"><span data-stu-id="5bdc2-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="5bdc2-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="5bdc2-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="5bdc2-133">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="5bdc2-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="5bdc2-134">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="5bdc2-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="5bdc2-135">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="5bdc2-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="5bdc2-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bdc2-136">Requirements</span></span>



| <span data-ttu-id="5bdc2-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bdc2-137">Requirement</span></span> | <span data-ttu-id="5bdc2-138">Wert</span><span class="sxs-lookup"><span data-stu-id="5bdc2-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bdc2-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bdc2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5bdc2-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bdc2-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5bdc2-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bdc2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5bdc2-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bdc2-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5bdc2-143">Header</span><span class="sxs-lookup"><span data-stu-id="5bdc2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bdc2-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bdc2-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5bdc2-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5bdc2-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="5bdc2-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bdc2-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5bdc2-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5bdc2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bdc2-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bdc2-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bdc2-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bdc2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bdc2-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5bdc2-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5bdc2-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5bdc2-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5bdc2-152">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="5bdc2-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="5bdc2-153">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="5bdc2-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="5bdc2-154">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="5bdc2-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="5bdc2-155">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="5bdc2-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="5bdc2-156">**glscale**</span><span class="sxs-lookup"><span data-stu-id="5bdc2-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="5bdc2-157">**gltranslate**</span><span class="sxs-lookup"><span data-stu-id="5bdc2-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





