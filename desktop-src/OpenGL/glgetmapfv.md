---
title: glgetmapfv-Funktion (GL. h)
description: Die Funktionen "glgetmapdv", "glgetmapfv" und "glgetmapiv" geben auswertungsparameter zurück. | glgetmapfv-Funktion (GL. h)
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- glgetmapfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02129e9637333fb36265ce9f7b631d6cb3377d0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365035"
---
# <a name="glgetmapfv-function"></a><span data-ttu-id="fb827-105">glgetmapfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="fb827-105">glGetMapfv function</span></span>

<span data-ttu-id="fb827-106">Die Funktionen " [**glgetmapdv**](glgetmapdv.md)", " **glgetmapfv**" und " [**glgetmapiv**](glgetmapiv.md) " geben auswertungsparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-106">The [**glGetMapdv**](glgetmapdv.md), **glGetMapfv**, and [**glGetMapiv**](glgetmapiv.md) functions return evaluator parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb827-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb827-107">Syntax</span></span>


```C++
void WINAPI glGetMapfv(
   GLenum  target,
   GLenum  query,
   GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="fb827-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb827-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb827-109">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="fb827-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="fb827-110">Der symbolische Name einer Karte.</span><span class="sxs-lookup"><span data-stu-id="fb827-110">The symbolic name of a map.</span></span> <span data-ttu-id="fb827-111">Folgende Werte sind zulässig: GL \_ zuordnung1 \_ Color \_ 4, GL \_ zuordnung1 \_ Index, GL \_ zuordnung1 \_ Normal, GL \_ zuordnung1 \_ Texture \_ coord \_ 1, GL \_ zuordnung1 \_ Texture \_ coord \_ 2, GL \_ zuordnung1 \_ Texture \_ coord \_ 3, GL \_ zuordnung1 \_ Textur \_ coord \_ 4, GL \_ zuordnung1 \_ Vertex \_ 3, GL \_ zuordnung1 \_ Vertex \_ 4, GL \_ map2 \_ Color \_ 4, GL \_ map2 \_ Index, GL \_ map2 \_ Normal, GL \_ map2 \_ Texture \_ coord \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL \_ map2 \_ Texture \_ coord \_ 3, GL \_ map2 \_ Texture \_ coord \_ 4, GL \_ map2 \_ Vertex \_ 3 und GL \_ map2 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="fb827-111">The following are accepted values: GL\_MAP1\_COLOR\_4, GL\_MAP1\_INDEX, GL\_MAP1\_NORMAL, GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP1\_VERTEX\_3, GL\_MAP1\_VERTEX\_4, GL\_MAP2\_COLOR\_4, GL\_MAP2\_INDEX, GL\_MAP2\_NORMAL, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, GL\_MAP2\_TEXTURE\_COORD\_4, GL\_MAP2\_VERTEX\_3, and GL\_MAP2\_VERTEX\_4.</span></span>

</dd> <dt>

<span data-ttu-id="fb827-112">*query*</span><span class="sxs-lookup"><span data-stu-id="fb827-112">*query*</span></span> 
</dt> <dd>

<span data-ttu-id="fb827-113">Gibt an, welcher Parameter zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb827-113">Specifies which parameter to return.</span></span> <span data-ttu-id="fb827-114">Die folgenden symbolischen Namen werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fb827-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="fb827-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fb827-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="fb827-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fb827-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <span data-ttu-id="fb827-117"><dt>**GL. \_ coeff**</dt></span><span class="sxs-lookup"><span data-stu-id="fb827-117"><dt>**GL\_COEFF**</dt></span></span> </dl>    | <span data-ttu-id="fb827-118">Der *v* -Parameter gibt die Kontrollpunkte für die auswerterfunktion zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-118">The *v* parameter returns the control points for the evaluator function.</span></span> <span data-ttu-id="fb827-119">Eindimensionale Evaluatoren geben *Reihen* folgen Kontrollpunkte zurück, und zweidimensionale Evaluatoren geben *uorder* *x* *Vorder* Steuerungs Punkte zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-119">One-dimensional evaluators return *order* control points, and two-dimensional evaluators return *uorder* *x* *vorder* control points.</span></span> <span data-ttu-id="fb827-120">Jeder Kontrollpunkt besteht aus einem, zwei, drei oder vier ganzzahligen Gleit Komma Werten mit einfacher Genauigkeit oder Gleit Komma Werten mit doppelter Genauigkeit, abhängig vom Typ der Auswertung.</span><span class="sxs-lookup"><span data-stu-id="fb827-120">Each control point consists of one, two, three, or four integer, single-precision floating-point, or double-precision floating-point values, depending on the type of the evaluator.</span></span> <span data-ttu-id="fb827-121">Zweidimensionale Steuerpunkte werden in der Reihenfolge der Zeilen zurückgegeben, wobei der *uorder* -Index schnell erhöht wird, und der *Vorder* -Index nach jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="fb827-121">Two-dimensional control points are returned in row-major order, incrementing the *uorder* index quickly, and the *vorder* index after each row.</span></span> <span data-ttu-id="fb827-122">Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf die nächstgelegenen ganzzahligen Werte gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="fb827-122">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <span data-ttu-id="fb827-123"><dt>**GL- \_ Bestellung**</dt></span><span class="sxs-lookup"><span data-stu-id="fb827-123"><dt>**GL\_ORDER**</dt></span></span> </dl>    | <span data-ttu-id="fb827-124">Der *v* -Parameter gibt die Reihenfolge der evaluatorfunktion zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-124">The *v* parameter returns the order of the evaluator function.</span></span> <span data-ttu-id="fb827-125">Eindimensionale Evaluatoren geben einen einzelnen Wert zurück, *Order*.</span><span class="sxs-lookup"><span data-stu-id="fb827-125">One-dimensional evaluators return a single value, *order*.</span></span> <span data-ttu-id="fb827-126">Zweidimensionale Evaluatoren geben zwei Werte zurück: *uorder* und *Vorder*.</span><span class="sxs-lookup"><span data-stu-id="fb827-126">Two-dimensional evaluators return two values, *uorder* and *vorder*.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <span data-ttu-id="fb827-127"><dt>**GL- \_ Domäne**</dt></span><span class="sxs-lookup"><span data-stu-id="fb827-127"><dt>**GL\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="fb827-128">Der *v* -Parameter gibt die linearen *u* -und *v* -Mapping-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-128">The *v* parameter returns the linear *u* and *v* mapping parameters.</span></span> <span data-ttu-id="fb827-129">Eindimensionale Evaluatoren geben zwei Werte zurück, *u* 1 und *u* 2, wie von [**glMap1**](glmap1.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="fb827-129">One-dimensional evaluators return two values, *u* 1 and *u* 2, as specified by [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="fb827-130">Zweidimensionale Evaluatoren geben gemäß [**glMap2**](glmap2.md)-Angabe vier Werte (*U1*, *U2*, *v1* und *v2*) zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-130">Two-dimensional evaluators return four values (*u1*, *u2*, *v1*, and *v2*) as specified by [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="fb827-131">Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf die nächstgelegenen ganzzahligen Werte gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="fb827-131">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="fb827-132">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="fb827-132">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="fb827-133">Gibt die angeforderten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-133">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb827-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb827-134">Return value</span></span>

<span data-ttu-id="fb827-135">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb827-136">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="fb827-136">Error codes</span></span>

<span data-ttu-id="fb827-137">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fb827-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fb827-138">Name</span><span class="sxs-lookup"><span data-stu-id="fb827-138">Name</span></span>                                                                                                  | <span data-ttu-id="fb827-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fb827-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb827-140"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb827-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fb827-141">Das *Ziel* oder die *Abfrage* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="fb827-141">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="fb827-142"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="fb827-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fb827-143">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fb827-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fb827-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb827-144">Remarks</span></span>

<span data-ttu-id="fb827-145">Die **glgetmap** -Funktion gibt evaluatorparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fb827-145">The **glGetMap** function returns evaluator parameters.</span></span> <span data-ttu-id="fb827-146">(Die **glMap1** -Funktion und die **glMap2** -Funktion definieren Evaluatoren.) Der *Ziel* Parameter gibt eine Karte an, die *Abfrage* wählt einen bestimmten Parameter aus, und *v* verweist auf den Speicher, in den die Werte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fb827-146">(The **glMap1** and **glMap2** functions define evaluators.) The *target* parameter specifies a map, *query* selects a specific parameter, and *v* points to storage where the values will be returned.</span></span>

<span data-ttu-id="fb827-147">Die zulässigen Werte für den *Ziel* Parameter werden in [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fb827-147">The acceptable values for the *target* parameter are described in [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="fb827-148">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *v* vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="fb827-148">If an error is generated, no change is made to the contents of *v*.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb827-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb827-149">Requirements</span></span>



| <span data-ttu-id="fb827-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb827-150">Requirement</span></span> | <span data-ttu-id="fb827-151">Wert</span><span class="sxs-lookup"><span data-stu-id="fb827-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb827-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb827-152">Minimum supported client</span></span><br/> | <span data-ttu-id="fb827-153">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb827-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fb827-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb827-154">Minimum supported server</span></span><br/> | <span data-ttu-id="fb827-155">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb827-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb827-156">Header</span><span class="sxs-lookup"><span data-stu-id="fb827-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb827-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb827-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fb827-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb827-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb827-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb827-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb827-160">DLL</span><span class="sxs-lookup"><span data-stu-id="fb827-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb827-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb827-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb827-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb827-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb827-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fb827-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fb827-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fb827-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fb827-165">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="fb827-165">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="fb827-166">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="fb827-166">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="fb827-167">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="fb827-167">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





