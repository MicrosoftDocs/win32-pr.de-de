---
title: glNormal3s-Funktion (GL. h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3s-Funktion (GL. h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- glNormal3s-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7941fa4e2c4e5ef00a5a14ce1eb913fb22a1f58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219252"
---
# <a name="glnormal3s-function"></a><span data-ttu-id="dbbba-105">glNormal3s-Funktion</span><span class="sxs-lookup"><span data-stu-id="dbbba-105">glNormal3s function</span></span>

<span data-ttu-id="dbbba-106">Legt den aktuellen normalen Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="dbbba-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbbba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbbba-107">Syntax</span></span>


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a><span data-ttu-id="dbbba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbbba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbbba-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="dbbba-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="dbbba-110">Gibt die x-Koordinate des neuen aktuellen normalen Vektors an.</span><span class="sxs-lookup"><span data-stu-id="dbbba-110">Specifies the x-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-111">*geile*</span><span class="sxs-lookup"><span data-stu-id="dbbba-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="dbbba-112">Gibt die y-Koordinate des neuen aktuellen normalen Vektors an.</span><span class="sxs-lookup"><span data-stu-id="dbbba-112">Specifies the y-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="dbbba-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="dbbba-114">Gibt die z-Koordinate des neuen aktuellen normalen Vektors an.</span><span class="sxs-lookup"><span data-stu-id="dbbba-114">Specifies the z-coordinate of the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbbba-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbbba-115">Return value</span></span>

<span data-ttu-id="dbbba-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dbbba-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbbba-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbbba-117">Remarks</span></span>

<span data-ttu-id="dbbba-118">Der aktuelle Normalwert ist auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3s**-Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="dbbba-118">The current normal is set to the given coordinates whenever you call the **glNormal3s** function.</span></span>

<span data-ttu-id="dbbba-119">Byte-, kurz-oder ganzzahlige Argumente werden in das Gleit Komma Format mit einer linearen Zuordnung konvertiert, die den positivsten darstellbaren ganzzahligen Wert 1,0 und den am meisten negativen darstellbaren ganzzahligen Wert zu-1,0 zuordnet.</span><span class="sxs-lookup"><span data-stu-id="dbbba-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="dbbba-120">Mit **glNormal3s** angegebene normale müssen keine Einheitslänge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dbbba-120">Normals specified by using **glNormal3s** need not have unit length.</span></span> <span data-ttu-id="dbbba-121">Wenn Normalisierung aktiviert ist, werden normale, die mit **glNormal3s** angegeben werden, nach der Transformation normalisiert.</span><span class="sxs-lookup"><span data-stu-id="dbbba-121">If normalization is enabled, then normals specified with **glNormal3s** are normalized after transformation.</span></span> <span data-ttu-id="dbbba-122">Sie können normalizationmithilfe von [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) mit dem Argument GL \_ normalize steuern.</span><span class="sxs-lookup"><span data-stu-id="dbbba-122">You can control normalizationby using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="dbbba-123">Standardmäßig ist die Normalisierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="dbbba-123">By default, normalization is disabled.</span></span> <span data-ttu-id="dbbba-124">Sie können die aktuelle Normalzeit jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="dbbba-124">You can update the current normal at any time.</span></span> <span data-ttu-id="dbbba-125">Vor allem können Sie **glNormal3s** zwischen einem " [**glBegin**](glbegin.md) "-Befehl und dem entsprechenden " [**glEnd**](glend.md)"-Aufrufe aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="dbbba-125">In particular, you can call **glNormal3s** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="dbbba-126">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3s** ab:</span><span class="sxs-lookup"><span data-stu-id="dbbba-126">The following functions retrieve information related to **glNormal3s**:</span></span>

<span data-ttu-id="dbbba-127">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="dbbba-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="dbbba-128">[**glisenable**](glisenabled.md) mit dem Argument GL \_ normalize</span><span class="sxs-lookup"><span data-stu-id="dbbba-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="dbbba-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbbba-129">Requirements</span></span>



| <span data-ttu-id="dbbba-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbbba-130">Requirement</span></span> | <span data-ttu-id="dbbba-131">Wert</span><span class="sxs-lookup"><span data-stu-id="dbbba-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbbba-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbbba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dbbba-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dbbba-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbbba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dbbba-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dbbba-136">Header</span><span class="sxs-lookup"><span data-stu-id="dbbba-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbbba-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbbba-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dbbba-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dbbba-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbbba-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbbba-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dbbba-140">DLL</span><span class="sxs-lookup"><span data-stu-id="dbbba-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbbba-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbbba-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbbba-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbbba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbbba-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="dbbba-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dbbba-144">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="dbbba-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="dbbba-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="dbbba-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dbbba-146">**glindex**</span><span class="sxs-lookup"><span data-stu-id="dbbba-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="dbbba-147">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="dbbba-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="dbbba-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="dbbba-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





