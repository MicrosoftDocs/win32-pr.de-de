---
title: glNormal3dv-Funktion (GL. h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3dv-Funktion (GL. h)
ms.assetid: 9d4f8d3c-f4c4-4165-a5f9-edc89319008b
keywords:
- glNormal3dv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84f2c2cefd5b0373808347e8a9ef17eb2ca2f863
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371860"
---
# <a name="glnormal3dv-function"></a><span data-ttu-id="94b2b-105">glNormal3dv-Funktion</span><span class="sxs-lookup"><span data-stu-id="94b2b-105">glNormal3dv function</span></span>

<span data-ttu-id="94b2b-106">Legt den aktuellen normalen Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="94b2b-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b2b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="94b2b-107">Syntax</span></span>


```C++
void WINAPI glNormal3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="94b2b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="94b2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94b2b-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="94b2b-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="94b2b-110">Ein Zeiger auf ein Array von drei Elementen: die x-, y-und z-Koordinaten der neuen aktuellen normalen.</span><span class="sxs-lookup"><span data-stu-id="94b2b-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94b2b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94b2b-111">Return value</span></span>

<span data-ttu-id="94b2b-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="94b2b-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94b2b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94b2b-113">Remarks</span></span>

<span data-ttu-id="94b2b-114">Der aktuelle Normalwert ist auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3dv**-Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="94b2b-114">The current normal is set to the given coordinates whenever you call the **glNormal3dv** function.</span></span>

<span data-ttu-id="94b2b-115">Byte-, kurz-oder ganzzahlige Argumente werden in das Gleit Komma Format mit einer linearen Zuordnung konvertiert, die den positivsten darstellbaren ganzzahligen Wert 1,0 und den am meisten negativen darstellbaren ganzzahligen Wert zu-1,0 zuordnet.</span><span class="sxs-lookup"><span data-stu-id="94b2b-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="94b2b-116">Mit **glNormal3dv** angegebene normale müssen keine Einheitslänge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="94b2b-116">Normals specified by using **glNormal3dv** need not have unit length.</span></span> <span data-ttu-id="94b2b-117">Wenn Normalisierung aktiviert ist, werden normale, die mit **glNormal3dv** angegeben werden, nach der Transformation normalisiert.</span><span class="sxs-lookup"><span data-stu-id="94b2b-117">If normalization is enabled, then normals specified with **glNormal3dv** are normalized after transformation.</span></span> <span data-ttu-id="94b2b-118">Sie können die Normalisierung mithilfe von [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md) mit dem Argument GL \_ normalize steuern.</span><span class="sxs-lookup"><span data-stu-id="94b2b-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="94b2b-119">Standardmäßig ist die Normalisierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="94b2b-119">By default, normalization is disabled.</span></span> <span data-ttu-id="94b2b-120">Sie können die aktuelle Normalzeit jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="94b2b-120">You can update the current normal at any time.</span></span> <span data-ttu-id="94b2b-121">Vor allem können Sie **glNormal3dv** zwischen einem " [**glBegin**](glbegin.md) "-Befehl und dem entsprechenden " [**glEnd**](glend.md)"-Aufrufe aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="94b2b-121">In particular, you can call **glNormal3dv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="94b2b-122">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3dv** ab:</span><span class="sxs-lookup"><span data-stu-id="94b2b-122">The following functions retrieve information related to **glNormal3dv**:</span></span>

<span data-ttu-id="94b2b-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="94b2b-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="94b2b-124">[**glisenable**](glisenabled.md) mit dem Argument GL \_ normalize</span><span class="sxs-lookup"><span data-stu-id="94b2b-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="94b2b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94b2b-125">Requirements</span></span>



| <span data-ttu-id="94b2b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94b2b-126">Requirement</span></span> | <span data-ttu-id="94b2b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="94b2b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94b2b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94b2b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="94b2b-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94b2b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94b2b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94b2b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="94b2b-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94b2b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94b2b-132">Header</span><span class="sxs-lookup"><span data-stu-id="94b2b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="94b2b-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="94b2b-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="94b2b-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94b2b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="94b2b-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94b2b-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94b2b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="94b2b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94b2b-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94b2b-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94b2b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94b2b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b2b-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="94b2b-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="94b2b-140">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="94b2b-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="94b2b-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="94b2b-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="94b2b-142">**glindex**</span><span class="sxs-lookup"><span data-stu-id="94b2b-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="94b2b-143">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="94b2b-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="94b2b-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="94b2b-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





