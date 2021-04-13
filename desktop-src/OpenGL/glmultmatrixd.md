---
title: glmultmatrixd Function (GL. h)
description: Die Funktion "glmultmatrixd" multipliziert die aktuelle Matrix mit einer beliebigen Matrix. | glmultmatrixd Function (GL. h)
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- glmultmatrixd-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24993fe5873be0af8713e3d127b86a7c593cd82
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353788"
---
# <a name="glmultmatrixd-function"></a><span data-ttu-id="90d58-105">glmultmatrixd-Funktion</span><span class="sxs-lookup"><span data-stu-id="90d58-105">glMultMatrixd function</span></span>

<span data-ttu-id="90d58-106">Die Funktionen " **glmultmatrixd** " und " [**glmultmatrixf**](glmultmatrixf.md) " multiplizieren die aktuelle Matrix mit einer beliebigen Matrix.</span><span class="sxs-lookup"><span data-stu-id="90d58-106">The **glMultMatrixd** and [**glMultMatrixf**](glmultmatrixf.md) functions multiply the current matrix by an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d58-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="90d58-107">Syntax</span></span>


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="90d58-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="90d58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90d58-109">*m*</span><span class="sxs-lookup"><span data-stu-id="90d58-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="90d58-110">Ein Zeiger auf eine 4 x 4-Matrix, die in Spalten Hauptreihen Folge als 16 aufeinander folgende Werte gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="90d58-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90d58-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90d58-111">Return value</span></span>

<span data-ttu-id="90d58-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="90d58-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="90d58-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="90d58-113">Error codes</span></span>

<span data-ttu-id="90d58-114">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="90d58-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="90d58-115">Name</span><span class="sxs-lookup"><span data-stu-id="90d58-115">Name</span></span>                                                                                                  | <span data-ttu-id="90d58-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90d58-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90d58-117"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="90d58-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="90d58-118">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="90d58-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="90d58-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90d58-119">Remarks</span></span>

<span data-ttu-id="90d58-120">Die **glmultmatrix** -Funktion multipliziert die aktuelle Matrix mit der in *m* angegebenen.</span><span class="sxs-lookup"><span data-stu-id="90d58-120">The **glMultMatrix** function multiplies the current matrix by the one specified in *m*.</span></span> <span data-ttu-id="90d58-121">Das heißt, wenn m die aktuelle Matrix und T die an **glmultmatrix** weiter gegebene Matrix ist, wird m durch m T ersetzt.</span><span class="sxs-lookup"><span data-stu-id="90d58-121">That is, if M is the current matrix and T is the matrix passed to **glMultMatrix**, then M is replaced with M   T.</span></span>

<span data-ttu-id="90d58-122">Die aktuelle Matrix ist die Projektions Matrix, die Modelview-Matrix oder die Textur Matrix, die durch den aktuellen Matrix Modus bestimmt wird (siehe [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="90d58-122">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="90d58-123">Der *m* -Parameter verweist auf eine 4 x 4-Matrix mit Gleit Komma Werten mit einfacher Genauigkeit oder Gleit Komma Werten mit doppelter Genauigkeit, die in der Spalte-Haupt Reihenfolge gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="90d58-123">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="90d58-124">Das heißt, die Matrix wird wie in der folgenden Abbildung dargestellt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="90d58-124">That is, the matrix is stored as shown in the following image.</span></span>

![! [Diagramm mit der 4 x 4-Matrix, auf die der m-Parameter zeigt.]](images/multi01.png)

<span data-ttu-id="90d58-126">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glmultmatrix** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="90d58-126">The following functions retrieve information related to **glMultMatrix**:</span></span>

<span data-ttu-id="90d58-127">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="90d58-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="90d58-128">**glget** mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="90d58-128">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="90d58-129">**glget** mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="90d58-129">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="90d58-130">**glget** mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="90d58-130">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="90d58-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90d58-131">Requirements</span></span>



| <span data-ttu-id="90d58-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90d58-132">Requirement</span></span> | <span data-ttu-id="90d58-133">Wert</span><span class="sxs-lookup"><span data-stu-id="90d58-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90d58-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90d58-134">Minimum supported client</span></span><br/> | <span data-ttu-id="90d58-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90d58-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="90d58-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90d58-136">Minimum supported server</span></span><br/> | <span data-ttu-id="90d58-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90d58-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="90d58-138">Header</span><span class="sxs-lookup"><span data-stu-id="90d58-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="90d58-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="90d58-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="90d58-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="90d58-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="90d58-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90d58-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="90d58-142">DLL</span><span class="sxs-lookup"><span data-stu-id="90d58-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90d58-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90d58-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90d58-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90d58-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d58-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="90d58-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="90d58-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="90d58-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="90d58-147">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="90d58-147">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="90d58-148">**glloadmatrix**</span><span class="sxs-lookup"><span data-stu-id="90d58-148">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="90d58-149">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="90d58-149">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="90d58-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="90d58-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





