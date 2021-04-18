---
title: glloadmatrixf-Funktion (GL. h)
description: Die Funktion "glloadmatrixf" ersetzt die aktuelle Matrix durch eine beliebige Matrix. | glloadmatrixf-Funktion (GL. h)
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- glloadmatrixf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0c54f4f7f7255b2dde724cf018d57fab6cf3e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365251"
---
# <a name="glloadmatrixf-function"></a><span data-ttu-id="74639-105">glloadmatrixf-Funktion</span><span class="sxs-lookup"><span data-stu-id="74639-105">glLoadMatrixf function</span></span>

<span data-ttu-id="74639-106">Die Funktionen " [**glloadmatrixd**](glloadmatrixd.md) " und " **glloadmatrixf** " ersetzen die aktuelle Matrix durch eine beliebige Matrix.</span><span class="sxs-lookup"><span data-stu-id="74639-106">The [**glLoadMatrixd**](glloadmatrixd.md) and **glLoadMatrixf** functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="74639-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74639-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a><span data-ttu-id="74639-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74639-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74639-109">*m*</span><span class="sxs-lookup"><span data-stu-id="74639-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="74639-110">Ein Zeiger auf eine 4 x 4-Matrix, die in Spalten Hauptreihen Folge als 16 aufeinander folgende Werte gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="74639-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74639-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74639-111">Return value</span></span>

<span data-ttu-id="74639-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="74639-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74639-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="74639-113">Error codes</span></span>

<span data-ttu-id="74639-114">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="74639-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="74639-115">Name</span><span class="sxs-lookup"><span data-stu-id="74639-115">Name</span></span>                                                                                                  | <span data-ttu-id="74639-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="74639-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74639-117"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="74639-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="74639-118">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="74639-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="74639-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74639-119">Remarks</span></span>

<span data-ttu-id="74639-120">Die Funktion " **glloadmatrix** " ersetzt die aktuelle Matrix durch die in *m* angegebene.</span><span class="sxs-lookup"><span data-stu-id="74639-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="74639-121">Die aktuelle Matrix ist die Projektions Matrix, die Modelview-Matrix oder die Textur Matrix, die durch den aktuellen Matrix Modus bestimmt wird (siehe [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="74639-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="74639-122">Der *m* -Parameter verweist auf eine 4 x 4-Matrix mit Gleit Komma Werten mit einfacher Genauigkeit oder Gleit Komma Werten mit doppelter Genauigkeit, die in der Spalte-Haupt Reihenfolge gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="74639-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="74639-123">Das heißt, die Matrix wird wie in der folgenden Abbildung dargestellt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="74639-123">That is, the matrix is stored as shown in the following image.</span></span>

![Diagramm mit der 4 x 4-Matrix, auf die der m-Parameter zeigt.](images/load02.png)

<span data-ttu-id="74639-125">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glloadmatrix** ab:</span><span class="sxs-lookup"><span data-stu-id="74639-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="74639-126">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="74639-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="74639-127">**glget** mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="74639-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="74639-128">**glget** mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="74639-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="74639-129">**glget** mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="74639-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="74639-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74639-130">Requirements</span></span>



| <span data-ttu-id="74639-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74639-131">Requirement</span></span> | <span data-ttu-id="74639-132">Wert</span><span class="sxs-lookup"><span data-stu-id="74639-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74639-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74639-133">Minimum supported client</span></span><br/> | <span data-ttu-id="74639-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74639-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="74639-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74639-135">Minimum supported server</span></span><br/> | <span data-ttu-id="74639-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74639-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74639-137">Header</span><span class="sxs-lookup"><span data-stu-id="74639-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="74639-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="74639-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="74639-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="74639-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="74639-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74639-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="74639-141">DLL</span><span class="sxs-lookup"><span data-stu-id="74639-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74639-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74639-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74639-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74639-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74639-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="74639-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="74639-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="74639-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="74639-146">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="74639-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="74639-147">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="74639-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="74639-148">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="74639-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="74639-149">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="74639-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





