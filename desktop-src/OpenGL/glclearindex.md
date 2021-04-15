---
title: glclearindex-Funktion (GL. h)
description: Die Funktion "glclearindex" gibt den eindeutigen Wert für die Farb Index Puffer an.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- glclearindex-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477241"
---
# <a name="glclearindex-function"></a><span data-ttu-id="f09e2-104">glclearindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="f09e2-104">glClearIndex function</span></span>

<span data-ttu-id="f09e2-105">Die Funktion " **glclearindex** " gibt den eindeutigen Wert für die Farb Index Puffer an.</span><span class="sxs-lookup"><span data-stu-id="f09e2-105">The **glClearIndex** function specifies the clear value for the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f09e2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f09e2-106">Syntax</span></span>


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a><span data-ttu-id="f09e2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f09e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f09e2-108">*c*</span><span class="sxs-lookup"><span data-stu-id="f09e2-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="f09e2-109">Der Index, der verwendet wird, wenn die Farb Index Puffer gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f09e2-109">The index used when the color-index buffers are cleared.</span></span> <span data-ttu-id="f09e2-110">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f09e2-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f09e2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f09e2-111">Return value</span></span>

<span data-ttu-id="f09e2-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f09e2-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f09e2-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f09e2-113">Error codes</span></span>

<span data-ttu-id="f09e2-114">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f09e2-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f09e2-115">Name</span><span class="sxs-lookup"><span data-stu-id="f09e2-115">Name</span></span>                                                                                                  | <span data-ttu-id="f09e2-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f09e2-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f09e2-117"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f09e2-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f09e2-118">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f09e2-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f09e2-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f09e2-119">Remarks</span></span>

<span data-ttu-id="f09e2-120">Die Funktion " **glclearindex** " gibt den von [**glClear**](glclear.md) verwendeten Index zum Löschen der Farb Index Puffer an.</span><span class="sxs-lookup"><span data-stu-id="f09e2-120">The **glClearIndex** function specifies the index used by [**glClear**](glclear.md) to clear the color-index buffers.</span></span> <span data-ttu-id="f09e2-121">Der *c* -Parameter ist nicht gebunden.</span><span class="sxs-lookup"><span data-stu-id="f09e2-121">The *c* parameter is not clamped.</span></span> <span data-ttu-id="f09e2-122">Stattdessen wird *c* in einen fest Komma Wert mit nicht spezifizierter Genauigkeit rechts neben dem Binär Punkt konvertiert.</span><span class="sxs-lookup"><span data-stu-id="f09e2-122">Rather, *c* is converted to a fixed-point value with unspecified precision to the right of the binary point.</span></span> <span data-ttu-id="f09e2-123">Der ganzzahlige Teil dieses Werts wird dann mit 2 <sup>m</sup>  -1 maskiert, wobei *m* die Anzahl der Bits in einem im Framebuffer gespeicherten Farbindex ist.</span><span class="sxs-lookup"><span data-stu-id="f09e2-123">The integer part of this value is then masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in a color index stored in the framebuffer.</span></span>

<span data-ttu-id="f09e2-124">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glclearindex** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="f09e2-124">The following functions retrieve information related to **glClearIndex**:</span></span>

<span data-ttu-id="f09e2-125">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Index \_ Clear- \_ Wert</span><span class="sxs-lookup"><span data-stu-id="f09e2-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="f09e2-126">**glget** mit Argument GL- \_ Index \_ Bits</span><span class="sxs-lookup"><span data-stu-id="f09e2-126">**glGet** with argument GL\_INDEX\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="f09e2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f09e2-127">Requirements</span></span>



| <span data-ttu-id="f09e2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f09e2-128">Requirement</span></span> | <span data-ttu-id="f09e2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f09e2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f09e2-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f09e2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f09e2-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f09e2-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f09e2-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f09e2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f09e2-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f09e2-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f09e2-134">Header</span><span class="sxs-lookup"><span data-stu-id="f09e2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f09e2-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f09e2-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f09e2-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f09e2-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="f09e2-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f09e2-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f09e2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f09e2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f09e2-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f09e2-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09e2-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f09e2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09e2-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f09e2-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f09e2-142">**glClear**</span><span class="sxs-lookup"><span data-stu-id="f09e2-142">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="f09e2-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f09e2-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f09e2-144">**glget**</span><span class="sxs-lookup"><span data-stu-id="f09e2-144">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





