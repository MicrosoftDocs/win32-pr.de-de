---
title: glmultmatrixf-Funktion (GL. h)
description: Die Funktion "glmultmatrixf" multipliziert die aktuelle Matrix mit einer beliebigen Matrix. | glmultmatrixf-Funktion (GL. h)
ms.assetid: fea5e557-09bd-4c45-89cc-9f3739b577bb
keywords:
- glmultmatrixf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f981b78dc2d9f152a4a7d1f40c4a2d1f120944b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104571727"
---
# <a name="glmultmatrixf-function"></a><span data-ttu-id="b0acf-105">glmultmatrixf-Funktion</span><span class="sxs-lookup"><span data-stu-id="b0acf-105">glMultMatrixf function</span></span>

<span data-ttu-id="b0acf-106">Die Funktionen " [**glmultmatrixd**](glmultmatrixd.md) " und " **glmultmatrixf** " multiplizieren die aktuelle Matrix mit einer beliebigen Matrix.</span><span class="sxs-lookup"><span data-stu-id="b0acf-106">The [**glMultMatrixd**](glmultmatrixd.md) and **glMultMatrixf** functions multiply the current matrix by an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0acf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0acf-107">Syntax</span></span>


```C++
void WINAPI glMultMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a><span data-ttu-id="b0acf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0acf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0acf-109">*m*</span><span class="sxs-lookup"><span data-stu-id="b0acf-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="b0acf-110">Ein Zeiger auf eine 4 x 4-Matrix, die in Spalten Hauptreihen Folge als 16 aufeinander folgende Werte gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b0acf-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0acf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0acf-111">Return value</span></span>

<span data-ttu-id="b0acf-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0acf-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0acf-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b0acf-113">Error codes</span></span>

<span data-ttu-id="b0acf-114">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b0acf-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b0acf-115">Name</span><span class="sxs-lookup"><span data-stu-id="b0acf-115">Name</span></span>                                                                                                  | <span data-ttu-id="b0acf-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b0acf-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0acf-117"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b0acf-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b0acf-118">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b0acf-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b0acf-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0acf-119">Remarks</span></span>

<span data-ttu-id="b0acf-120">Die **glmultmatrix** -Funktion multipliziert die aktuelle Matrix mit der in *m* angegebenen.</span><span class="sxs-lookup"><span data-stu-id="b0acf-120">The **glMultMatrix** function multiplies the current matrix by the one specified in *m*.</span></span> <span data-ttu-id="b0acf-121">Das heißt, wenn m die aktuelle Matrix und T die an **glmultmatrix** weiter gegebene Matrix ist, wird m durch m T ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b0acf-121">That is, if M is the current matrix and T is the matrix passed to **glMultMatrix**, then M is replaced with M   T.</span></span>

<span data-ttu-id="b0acf-122">Die aktuelle Matrix ist die Projektions Matrix, die Modelview-Matrix oder die Textur Matrix, die durch den aktuellen Matrix Modus bestimmt wird (siehe [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="b0acf-122">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="b0acf-123">Der *m* -Parameter verweist auf eine 4 x 4-Matrix mit Gleit Komma Werten mit einfacher Genauigkeit oder Gleit Komma Werten mit doppelter Genauigkeit, die in der Spalte-Haupt Reihenfolge gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b0acf-123">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="b0acf-124">Das heißt, die Matrix wird wie in der folgenden Abbildung dargestellt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b0acf-124">That is, the matrix is stored as shown in the following image.</span></span>

![! [Diagramm mit der 4 x 4-Matrix, auf die der m-Parameter zeigt.]](images/multi01.png)

<span data-ttu-id="b0acf-126">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glmultmatrix** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="b0acf-126">The following functions retrieve information related to **glMultMatrix**:</span></span>

<span data-ttu-id="b0acf-127">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="b0acf-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="b0acf-128">**glget** mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="b0acf-128">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="b0acf-129">**glget** mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="b0acf-129">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="b0acf-130">**glget** mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="b0acf-130">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="b0acf-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0acf-131">Requirements</span></span>



| <span data-ttu-id="b0acf-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0acf-132">Requirement</span></span> | <span data-ttu-id="b0acf-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b0acf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0acf-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0acf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b0acf-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0acf-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b0acf-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0acf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b0acf-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0acf-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0acf-138">Header</span><span class="sxs-lookup"><span data-stu-id="b0acf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0acf-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0acf-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b0acf-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0acf-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0acf-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0acf-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0acf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b0acf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0acf-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0acf-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0acf-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0acf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0acf-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b0acf-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b0acf-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b0acf-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b0acf-147">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="b0acf-147">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="b0acf-148">**glloadmatrix**</span><span class="sxs-lookup"><span data-stu-id="b0acf-148">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="b0acf-149">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="b0acf-149">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="b0acf-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="b0acf-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





