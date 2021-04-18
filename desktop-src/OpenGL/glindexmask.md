---
title: glindexmask-Funktion (GL. h)
description: Die Funktion "glindexmask" steuert das Schreiben einzelner Bits in den Farb Index Puffern.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- glindexmask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340569"
---
# <a name="glindexmask-function"></a><span data-ttu-id="6d893-104">glindexmask-Funktion</span><span class="sxs-lookup"><span data-stu-id="6d893-104">glIndexMask function</span></span>

<span data-ttu-id="6d893-105">Die Funktion " **glindexmask** " steuert das Schreiben einzelner Bits in den Farb Index Puffern.</span><span class="sxs-lookup"><span data-stu-id="6d893-105">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d893-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d893-106">Syntax</span></span>


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="6d893-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d893-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d893-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="6d893-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="6d893-109">Eine Bitmaske, um das Schreiben einzelner Bits in den Farb Index Puffern zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6d893-109">A bit mask to enable and disable the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="6d893-110">Anfänglich ist die Maske alle.</span><span class="sxs-lookup"><span data-stu-id="6d893-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d893-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d893-111">Return value</span></span>

<span data-ttu-id="6d893-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6d893-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d893-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6d893-113">Error codes</span></span>

<span data-ttu-id="6d893-114">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6d893-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6d893-115">Name</span><span class="sxs-lookup"><span data-stu-id="6d893-115">Name</span></span>                                                                                                  | <span data-ttu-id="6d893-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6d893-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d893-117"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="6d893-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6d893-118">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6d893-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6d893-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d893-119">Remarks</span></span>

<span data-ttu-id="6d893-120">Die Funktion " **glindexmask** " steuert das Schreiben einzelner Bits in den Farb Index Puffern.</span><span class="sxs-lookup"><span data-stu-id="6d893-120">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="6d893-121">Die am wenigsten signifikanten *n* Bits der *Maske*, wobei *1* die Anzahl der Bits in einem Farb Index Puffer ist, geben eine Maske an.</span><span class="sxs-lookup"><span data-stu-id="6d893-121">The least significant *n* bits of *mask*, where *1* is the number of bits in a color-index buffer, specify a mask.</span></span> <span data-ttu-id="6d893-122">Wenn ein solches in der Maske angezeigt wird, wird das entsprechende Bit im Farb Index Puffer (oder Puffer) als beschreibbar festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d893-122">Wherever a one appears in the mask, the corresponding bit in the color-index buffer (or buffers) is made writable.</span></span> <span data-ttu-id="6d893-123">Wenn ein NULL-Wert angezeigt wird, ist das Bit schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6d893-123">Where a zero appears, the bit is write-protected.</span></span>

<span data-ttu-id="6d893-124">Diese Maske wird nur im Farb Index Modus verwendet und wirkt sich nur auf die Puffer aus, die zurzeit zum Schreiben ausgewählt werden (siehe [**gldrawbuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="6d893-124">This mask is used only in color-index mode, and it affects only the buffers currently selected for writing (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span> <span data-ttu-id="6d893-125">Anfänglich werden alle Bits zum Schreiben aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6d893-125">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="6d893-126">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glindexmask** ab:</span><span class="sxs-lookup"><span data-stu-id="6d893-126">The following function retrieves information related to **glIndexMask**:</span></span>

<span data-ttu-id="6d893-127">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Index \_ schreibfrage</span><span class="sxs-lookup"><span data-stu-id="6d893-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="6d893-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d893-128">Requirements</span></span>



| <span data-ttu-id="6d893-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d893-129">Requirement</span></span> | <span data-ttu-id="6d893-130">Wert</span><span class="sxs-lookup"><span data-stu-id="6d893-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d893-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d893-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6d893-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d893-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d893-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d893-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6d893-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d893-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d893-135">Header</span><span class="sxs-lookup"><span data-stu-id="6d893-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d893-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d893-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6d893-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d893-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d893-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d893-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d893-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6d893-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d893-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d893-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d893-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d893-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d893-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6d893-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6d893-143">**gldepthmask**</span><span class="sxs-lookup"><span data-stu-id="6d893-143">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="6d893-144">**gldrawbuffer**</span><span class="sxs-lookup"><span data-stu-id="6d893-144">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="6d893-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6d893-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6d893-146">**glindex**</span><span class="sxs-lookup"><span data-stu-id="6d893-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="6d893-147">**glstencilmask**</span><span class="sxs-lookup"><span data-stu-id="6d893-147">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





