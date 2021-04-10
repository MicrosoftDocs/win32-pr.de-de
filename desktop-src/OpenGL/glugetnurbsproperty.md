---
title: glugetnurbsproperty-Funktion (glu. h)
description: Die Funktion "glugetnurbsproperty" Ruft eine nicht einheitliche Rational B-Spline (NURBS)-Eigenschaft ab.
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- glugetnurbsproperty-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103426"
---
# <a name="glugetnurbsproperty-function"></a><span data-ttu-id="9e8ae-104">glugetnurbsproperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="9e8ae-104">gluGetNurbsProperty function</span></span>

<span data-ttu-id="9e8ae-105">Die Funktion " **glugetnurbsproperty** " Ruft eine nicht einheitliche Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="9e8ae-105">The **gluGetNurbsProperty** function gets a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8ae-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e8ae-106">Syntax</span></span>


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a><span data-ttu-id="9e8ae-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e8ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e8ae-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="9e8ae-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="9e8ae-109">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="9e8ae-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9e8ae-110">*property*</span><span class="sxs-lookup"><span data-stu-id="9e8ae-110">*property*</span></span> 
</dt> <dd>

<span data-ttu-id="9e8ae-111">Die Eigenschaft, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e8ae-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="9e8ae-112">Die folgenden Werte sind gültig: glu \_ - \_ samplingtoleranz, Glu- \_ Anzeige \_ Modus, Glu \_ -culult, Glu- \_ automatische \_ Lade \_ Matrix, Glu- \_ parametrimetrische \_ Toleranz, Glu- \_ Samplingmethode \_ , Glu \_ U \_ Step und glu \_ V \_ Step.</span><span class="sxs-lookup"><span data-stu-id="9e8ae-112">The following values are valid: GLU\_SAMPLING\_TOLERANCE, GLU\_DISPLAY\_MODE, GLU\_CULLING, GLU\_AUTO\_LOAD\_MATRIX, GLU\_PARAMETRIC\_TOLERANCE, GLU\_SAMPLING\_METHOD, GLU\_U\_STEP, and GLU\_V\_STEP.</span></span>

</dd> <dt>

<span data-ttu-id="9e8ae-113">*value*</span><span class="sxs-lookup"><span data-stu-id="9e8ae-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="9e8ae-114">Ein Zeiger auf den Speicherort, in den der Wert der benannten Eigenschaft geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="9e8ae-114">A pointer to the location into which the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e8ae-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e8ae-115">Return value</span></span>

<span data-ttu-id="9e8ae-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9e8ae-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e8ae-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e8ae-117">Remarks</span></span>

<span data-ttu-id="9e8ae-118">Verwenden Sie " **glugetnurbsproperty** ", um in einem nurb-Objekt gespeicherte Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9e8ae-118">Use **gluGetNurbsProperty** to retrieve properties stored in a NURBS object.</span></span> <span data-ttu-id="9e8ae-119">Diese Eigenschaften wirken sich auf die Darstellung von nursb-Kurven und-Flächen aus.</span><span class="sxs-lookup"><span data-stu-id="9e8ae-119">These properties affect the way NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="9e8ae-120">Informationen zu den Eigenschaften von nurb finden Sie unter [**glunurbsproperty**](glunurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="9e8ae-120">For information about NURBS properties, see [**gluNurbsProperty**](glunurbsproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8ae-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e8ae-121">Requirements</span></span>



| <span data-ttu-id="9e8ae-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e8ae-122">Requirement</span></span> | <span data-ttu-id="9e8ae-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9e8ae-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8ae-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e8ae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e8ae-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e8ae-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9e8ae-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e8ae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e8ae-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e8ae-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9e8ae-128">Header</span><span class="sxs-lookup"><span data-stu-id="9e8ae-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e8ae-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ae-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9e8ae-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e8ae-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e8ae-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ae-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9e8ae-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8ae-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e8ae-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ae-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e8ae-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e8ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8ae-135">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="9e8ae-135">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="9e8ae-136">**glunurbsproperty**</span><span class="sxs-lookup"><span data-stu-id="9e8ae-136">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





