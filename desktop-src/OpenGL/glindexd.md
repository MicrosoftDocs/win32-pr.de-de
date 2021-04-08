---
title: glindexd-Funktion (GL. h)
description: Die Funktion "glindexd" legt den aktuellen Farbindex fest.
ms.assetid: 4cd72d32-e796-4c94-94cb-591f1ee3b26e
keywords:
- glindexd-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d1e7cce6ad2ae39e5ca107ef89b3b86147596e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949581"
---
# <a name="glindexd-function"></a><span data-ttu-id="8d9f9-104">glindexd-Funktion</span><span class="sxs-lookup"><span data-stu-id="8d9f9-104">glIndexd function</span></span>

<span data-ttu-id="8d9f9-105">Die Funktion " **glindexd** " legt den aktuellen Farbindex fest.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-105">The **glIndexd** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9f9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d9f9-106">Syntax</span></span>


```C++
void WINAPI glIndexd(
   GLdouble c
);
```



## <a name="parameters"></a><span data-ttu-id="8d9f9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d9f9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9f9-108">*c*</span><span class="sxs-lookup"><span data-stu-id="8d9f9-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="8d9f9-109">Der neue Wert für den aktuellen Farb Index.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-109">The new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9f9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d9f9-110">Return value</span></span>

<span data-ttu-id="8d9f9-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9f9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d9f9-112">Remarks</span></span>

<span data-ttu-id="8d9f9-113">Die Funktion " **glindexd** " aktualisiert den aktuellen Farbindex (mit einem Wert).</span><span class="sxs-lookup"><span data-stu-id="8d9f9-113">The **glIndexd** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="8d9f9-114">Es wird ein Argument benötigt: der neue Wert für den aktuellen Farbindex.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="8d9f9-115">Der aktuelle Index wird als Gleit Komma Wert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="8d9f9-116">Ganzzahlige Werte werden ohne besondere Zuordnung direkt in Gleit Komma Werte konvertiert.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="8d9f9-117">Index Werte außerhalb des darstellbaren Bereichs des Farb Index Puffers werden nicht gebunden.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="8d9f9-118">Vor der Deaktivierung eines Indexes (sofern aktiviert) und dem Schreiben in den Framebuffer wird der Index jedoch in ein festes Punkt Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="8d9f9-119">Alle Bits im ganzzahligen Teil des resultierenden fest Komma Werts, die nicht Bits im Frame Puffer entsprechen, werden maskiert.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="8d9f9-120">Der aktuelle Index kann jederzeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-120">The current index can be updated at any time.</span></span> <span data-ttu-id="8d9f9-121">Insbesondere kann **glindexd** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8d9f9-121">In particular, **glIndexd** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="8d9f9-122">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glindexd** ab:</span><span class="sxs-lookup"><span data-stu-id="8d9f9-122">The following function retrieves information related to **glIndexd**:</span></span>

<span data-ttu-id="8d9f9-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Current \_ Index"</span><span class="sxs-lookup"><span data-stu-id="8d9f9-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="8d9f9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d9f9-124">Requirements</span></span>



| <span data-ttu-id="8d9f9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d9f9-125">Requirement</span></span> | <span data-ttu-id="8d9f9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8d9f9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9f9-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d9f9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8d9f9-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d9f9-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8d9f9-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d9f9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8d9f9-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d9f9-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8d9f9-131">Header</span><span class="sxs-lookup"><span data-stu-id="8d9f9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d9f9-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f9-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8d9f9-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8d9f9-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d9f9-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f9-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d9f9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8d9f9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d9f9-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f9-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d9f9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d9f9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9f9-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8d9f9-139">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="8d9f9-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8d9f9-141">**glget**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

