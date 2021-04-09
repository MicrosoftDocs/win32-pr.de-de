---
title: glNormal3d-Funktion (GL. h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3d-Funktion (GL. h)
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- glNormal3d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ab158e298ff20cce635ab4002f38ca82fdaa2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050813"
---
# <a name="glnormal3d-function"></a><span data-ttu-id="e3b18-105">glNormal3d-Funktion</span><span class="sxs-lookup"><span data-stu-id="e3b18-105">glNormal3d function</span></span>

<span data-ttu-id="e3b18-106">Legt den aktuellen normalen Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="e3b18-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b18-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3b18-107">Syntax</span></span>


```C++
void WINAPI glNormal3d(
   GLdouble nx,
   GLdouble ny,
   GLdouble nz
);
```



## <a name="parameters"></a><span data-ttu-id="e3b18-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3b18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b18-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="e3b18-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="e3b18-110">Gibt die x-Koordinate für den neuen aktuellen normalen Vektor an.</span><span class="sxs-lookup"><span data-stu-id="e3b18-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="e3b18-111">*geile*</span><span class="sxs-lookup"><span data-stu-id="e3b18-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="e3b18-112">Gibt die y-Koordinate für den neuen aktuellen normalen Vektor an.</span><span class="sxs-lookup"><span data-stu-id="e3b18-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="e3b18-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="e3b18-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="e3b18-114">Gibt die z-Koordinate für den neuen aktuellen normalen Vektor an.</span><span class="sxs-lookup"><span data-stu-id="e3b18-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b18-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3b18-115">Return value</span></span>

<span data-ttu-id="e3b18-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e3b18-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b18-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3b18-117">Remarks</span></span>

<span data-ttu-id="e3b18-118">Der aktuelle Normalwert ist auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3d**-Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3b18-118">The current normal is set to the given coordinates whenever you call the **glNormal3d** function.</span></span>

<span data-ttu-id="e3b18-119">Byte-, kurz-oder ganzzahlige Argumente werden in das Gleit Komma Format konvertiert, indem eine lineare Zuordnung verwendet wird, die den positivsten darstellbaren ganzzahligen Wert 1,0 und den negativsten darstellbaren ganzzahligen Wert zu-1,0 zuordnet.</span><span class="sxs-lookup"><span data-stu-id="e3b18-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="e3b18-120">Mit **glNormal3d** angegebene normale müssen keine Einheitslänge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e3b18-120">Normals specified by using **glNormal3d** need not have unit length.</span></span> <span data-ttu-id="e3b18-121">Wenn Normalisierung aktiviert ist, werden normale, die mit **glNormal3d** angegeben werden, nach der Transformation normalisiert.</span><span class="sxs-lookup"><span data-stu-id="e3b18-121">If normalization is enabled, then normals specified with **glNormal3d** are normalized after transformation.</span></span> <span data-ttu-id="e3b18-122">Sie können die Normalisierung mithilfe von [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md) mit dem Argument GL \_ normalize steuern.</span><span class="sxs-lookup"><span data-stu-id="e3b18-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="e3b18-123">Standardmäßig ist die Normalisierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e3b18-123">By default, normalization is disabled.</span></span> <span data-ttu-id="e3b18-124">Sie können die aktuelle Normalzeit jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e3b18-124">You can update the current normal at any time.</span></span> <span data-ttu-id="e3b18-125">Vor allem können Sie **glNormal3d** zwischen einem " [**glBegin**](glbegin.md) "-Befehl und dem entsprechenden " [**glEnd**](glend.md)"-Aufrufe aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3b18-125">In particular, you can call **glNormal3d** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="e3b18-126">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3d** ab:</span><span class="sxs-lookup"><span data-stu-id="e3b18-126">The following functions retrieve information related to **glNormal3d**:</span></span>

<span data-ttu-id="e3b18-127">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="e3b18-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="e3b18-128">[**glisenable**](glisenabled.md) mit dem Argument GL \_ normalize</span><span class="sxs-lookup"><span data-stu-id="e3b18-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b18-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3b18-129">Requirements</span></span>



| <span data-ttu-id="e3b18-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3b18-130">Requirement</span></span> | <span data-ttu-id="e3b18-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e3b18-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b18-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3b18-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b18-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3b18-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e3b18-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3b18-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b18-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3b18-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3b18-136">Header</span><span class="sxs-lookup"><span data-stu-id="e3b18-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3b18-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b18-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e3b18-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e3b18-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3b18-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3b18-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e3b18-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e3b18-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3b18-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3b18-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b18-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3b18-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b18-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e3b18-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e3b18-144">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="e3b18-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="e3b18-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e3b18-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e3b18-146">**glindex**</span><span class="sxs-lookup"><span data-stu-id="e3b18-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="e3b18-147">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="e3b18-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="e3b18-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="e3b18-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





