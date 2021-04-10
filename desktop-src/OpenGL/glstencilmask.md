---
title: glstencilmask-Funktion (GL. h)
description: Die Funktion "glstencilmask" steuert das Schreiben einzelner Bits in den Schablonen Ebenen.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- glstencilmask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106400"
---
# <a name="glstencilmask-function"></a><span data-ttu-id="9d0d7-104">glstencilmask-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d0d7-104">glStencilMask function</span></span>

<span data-ttu-id="9d0d7-105">Die Funktion " **glstencilmask** " steuert das Schreiben einzelner Bits in den Schablonen Ebenen.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-105">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d0d7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d0d7-106">Syntax</span></span>


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="9d0d7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d0d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d0d7-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="9d0d7-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0d7-109">Eine Bitmaske zum Aktivieren und Deaktivieren der Erstellung einzelner Bits in den Schablonen Ebenen.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-109">A bit mask to enable and disable writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="9d0d7-110">Anfänglich ist die Maske alle.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d0d7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d0d7-111">Return value</span></span>

<span data-ttu-id="9d0d7-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d0d7-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9d0d7-113">Error codes</span></span>

<span data-ttu-id="9d0d7-114">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9d0d7-115">Name</span><span class="sxs-lookup"><span data-stu-id="9d0d7-115">Name</span></span>                                                                                                  | <span data-ttu-id="9d0d7-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9d0d7-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d0d7-117"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="9d0d7-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9d0d7-118">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9d0d7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d0d7-119">Remarks</span></span>

<span data-ttu-id="9d0d7-120">Die Funktion " **glstencilmask** " steuert das Schreiben einzelner Bits in den Schablonen Ebenen.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-120">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="9d0d7-121">Die am wenigsten signifikanten *n* Bits der *Maske*, wobei *n* die Anzahl der Bits im Schablonen Puffer ist, geben eine Maske an.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-121">The least significant *n* bits of *mask*, where *n* is the number of bits in the stencil buffer, specify a mask.</span></span> <span data-ttu-id="9d0d7-122">Wenn eine in der Maske angezeigt wird, wird das entsprechende Bit im Schablonen Puffer beschreibbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-122">Wherever a one appears in the mask, the corresponding bit in the stencil buffer is made writable.</span></span> <span data-ttu-id="9d0d7-123">Wenn ein NULL-Wert angezeigt wird, ist das Bit schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-123">Where a zero appears, the bit is write-protected.</span></span> <span data-ttu-id="9d0d7-124">Anfänglich werden alle Bits zum Schreiben aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9d0d7-124">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="9d0d7-125">Die folgenden Funktionen rufen Informationen im Zusammenhang mit " **glstencilmask**" ab:</span><span class="sxs-lookup"><span data-stu-id="9d0d7-125">The following functions retrieve information related to **glStencilMask**:</span></span>

<span data-ttu-id="9d0d7-126">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Stencil \_ schreibfrage</span><span class="sxs-lookup"><span data-stu-id="9d0d7-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_WRITEMASK</span></span>

<span data-ttu-id="9d0d7-127">glget mit Argument GL- \_ Schablonen \_ Bits</span><span class="sxs-lookup"><span data-stu-id="9d0d7-127">glGet with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="9d0d7-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d0d7-128">Requirements</span></span>



| <span data-ttu-id="9d0d7-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d0d7-129">Requirement</span></span> | <span data-ttu-id="9d0d7-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9d0d7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0d7-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d0d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9d0d7-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d0d7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d0d7-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d0d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9d0d7-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d0d7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d0d7-135">Header</span><span class="sxs-lookup"><span data-stu-id="9d0d7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d0d7-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d0d7-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9d0d7-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d0d7-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d0d7-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d0d7-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d0d7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9d0d7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d0d7-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d0d7-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d0d7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d0d7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d0d7-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9d0d7-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9d0d7-143">**glcolormask**</span><span class="sxs-lookup"><span data-stu-id="9d0d7-143">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="9d0d7-144">**gldepthmask**</span><span class="sxs-lookup"><span data-stu-id="9d0d7-144">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="9d0d7-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9d0d7-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9d0d7-146">**glindexmask**</span><span class="sxs-lookup"><span data-stu-id="9d0d7-146">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="9d0d7-147">**glstencilfunc**</span><span class="sxs-lookup"><span data-stu-id="9d0d7-147">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="9d0d7-148">**glstencilop**</span><span class="sxs-lookup"><span data-stu-id="9d0d7-148">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





