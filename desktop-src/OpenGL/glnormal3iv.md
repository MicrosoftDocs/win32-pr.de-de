---
title: glNormal3iv-Funktion (GL. h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3iv-Funktion (GL. h)
ms.assetid: cf50e801-a34c-43bd-b7eb-facb84a6472d
keywords:
- glNormal3iv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5629a12d6c388da2aa133fbe72177646b4f95d63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961514"
---
# <a name="glnormal3iv-function"></a><span data-ttu-id="18ea5-105">glNormal3iv-Funktion</span><span class="sxs-lookup"><span data-stu-id="18ea5-105">glNormal3iv function</span></span>

<span data-ttu-id="18ea5-106">Legt den aktuellen normalen Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="18ea5-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ea5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="18ea5-107">Syntax</span></span>


```C++
void WINAPI glNormal3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="18ea5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="18ea5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ea5-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="18ea5-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="18ea5-110">Ein Zeiger auf ein Array von drei Elementen: die x-, y-und z-Koordinaten der neuen aktuellen normalen.</span><span class="sxs-lookup"><span data-stu-id="18ea5-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ea5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18ea5-111">Return value</span></span>

<span data-ttu-id="18ea5-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="18ea5-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ea5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18ea5-113">Remarks</span></span>

<span data-ttu-id="18ea5-114">Der aktuelle Normalwert ist auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3iv**-Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="18ea5-114">The current normal is set to the given coordinates whenever you call the **glNormal3iv** function.</span></span>

<span data-ttu-id="18ea5-115">Byte-, kurz-oder ganzzahlige Argumente werden in das Gleit Komma Format mit einer linearen Zuordnung konvertiert, die den positivsten darstellbaren ganzzahligen Wert 1,0 und den am meisten negativen darstellbaren ganzzahligen Wert zu-1,0 zuordnet.</span><span class="sxs-lookup"><span data-stu-id="18ea5-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="18ea5-116">Mit **glNormal3iv** angegebene normale müssen keine Einheitslänge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="18ea5-116">Normals specified by using **glNormal3iv** need not have unit length.</span></span> <span data-ttu-id="18ea5-117">Wenn Normalisierung aktiviert ist, werden normale, die mit **glNormal3iv** angegeben werden, nach der Transformation normalisiert.</span><span class="sxs-lookup"><span data-stu-id="18ea5-117">If normalization is enabled, then normals specified with **glNormal3iv** are normalized after transformation.</span></span> <span data-ttu-id="18ea5-118">Sie können die Normalisierung mithilfe von [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md) mit dem Argument GL \_ normalize steuern.</span><span class="sxs-lookup"><span data-stu-id="18ea5-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="18ea5-119">Standardmäßig ist die Normalisierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="18ea5-119">By default, normalization is disabled.</span></span> <span data-ttu-id="18ea5-120">Sie können die aktuelle Normalzeit jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="18ea5-120">You can update the current normal at any time.</span></span> <span data-ttu-id="18ea5-121">Vor allem können Sie **glNormal3iv** zwischen einem " [**glBegin**](glbegin.md) "-Befehl und dem entsprechenden " [**glEnd**](glend.md)"-Aufrufe aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="18ea5-121">In particular, you can call **glNormal3iv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="18ea5-122">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3iv** ab:</span><span class="sxs-lookup"><span data-stu-id="18ea5-122">The following functions retrieve information related to **glNormal3iv**:</span></span>

<span data-ttu-id="18ea5-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="18ea5-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="18ea5-124">[**glisenable**](glisenabled.md) mit dem Argument GL \_ normalize</span><span class="sxs-lookup"><span data-stu-id="18ea5-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="18ea5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18ea5-125">Requirements</span></span>



| <span data-ttu-id="18ea5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18ea5-126">Requirement</span></span> | <span data-ttu-id="18ea5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="18ea5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18ea5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18ea5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="18ea5-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18ea5-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="18ea5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18ea5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="18ea5-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18ea5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18ea5-132">Header</span><span class="sxs-lookup"><span data-stu-id="18ea5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ea5-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ea5-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="18ea5-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="18ea5-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="18ea5-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18ea5-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="18ea5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="18ea5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18ea5-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18ea5-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ea5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18ea5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ea5-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="18ea5-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="18ea5-140">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="18ea5-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="18ea5-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="18ea5-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="18ea5-142">**glindex**</span><span class="sxs-lookup"><span data-stu-id="18ea5-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="18ea5-143">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="18ea5-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="18ea5-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="18ea5-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





