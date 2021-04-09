---
title: glclearstencil-Funktion (GL. h)
description: Die glclearstencil-Funktion gibt den eindeutigen Wert für den Schablonen Puffer an.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- glclearstencil-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956604"
---
# <a name="glclearstencil-function"></a><span data-ttu-id="48a95-104">glclearstencil-Funktion</span><span class="sxs-lookup"><span data-stu-id="48a95-104">glClearStencil function</span></span>

<span data-ttu-id="48a95-105">Die **glclearstencil** -Funktion gibt den eindeutigen Wert für den Schablonen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="48a95-105">The **glClearStencil** function specifies the clear value for the stencil buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a95-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="48a95-106">Syntax</span></span>


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a><span data-ttu-id="48a95-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="48a95-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a95-108">*s*</span><span class="sxs-lookup"><span data-stu-id="48a95-108">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="48a95-109">Der Index, der verwendet wird, wenn der Schablonen Puffer gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="48a95-109">The index used when the stencil buffer is cleared.</span></span> <span data-ttu-id="48a95-110">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="48a95-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a95-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48a95-111">Return value</span></span>

<span data-ttu-id="48a95-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48a95-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48a95-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="48a95-113">Error codes</span></span>

<span data-ttu-id="48a95-114">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="48a95-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="48a95-115">Name</span><span class="sxs-lookup"><span data-stu-id="48a95-115">Name</span></span>                                                                                                  | <span data-ttu-id="48a95-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="48a95-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48a95-117"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="48a95-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="48a95-118">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48a95-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48a95-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48a95-119">Remarks</span></span>

<span data-ttu-id="48a95-120">Die **glclearstencil** -Funktion gibt den von [**glClear**](glclear.md) verwendeten Index zum Löschen des Schablonen Puffers an.</span><span class="sxs-lookup"><span data-stu-id="48a95-120">The **glClearStencil** function specifies the index used by [**glClear**](glclear.md) to clear the stencil buffer.</span></span> <span data-ttu-id="48a95-121">Der *s* -Parameter wird mit 2 <sup>m</sup>  -1 maskiert, wobei *m* die Anzahl der Bits im Schablonen Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="48a95-121">The *s* parameter is masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in the stencil buffer.</span></span>

<span data-ttu-id="48a95-122">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glclearstencil** " ab:</span><span class="sxs-lookup"><span data-stu-id="48a95-122">The following functions retrieve information related to the **glClearStencil** function:</span></span>

<span data-ttu-id="48a95-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Stencil \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="48a95-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

<span data-ttu-id="48a95-124">**glget** mit Argument GL- \_ Schablonen \_ Bits</span><span class="sxs-lookup"><span data-stu-id="48a95-124">**glGet** with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="48a95-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48a95-125">Requirements</span></span>



| <span data-ttu-id="48a95-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48a95-126">Requirement</span></span> | <span data-ttu-id="48a95-127">Wert</span><span class="sxs-lookup"><span data-stu-id="48a95-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48a95-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48a95-128">Minimum supported client</span></span><br/> | <span data-ttu-id="48a95-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48a95-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="48a95-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48a95-130">Minimum supported server</span></span><br/> | <span data-ttu-id="48a95-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48a95-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48a95-132">Header</span><span class="sxs-lookup"><span data-stu-id="48a95-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a95-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="48a95-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="48a95-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48a95-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="48a95-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48a95-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="48a95-136">DLL</span><span class="sxs-lookup"><span data-stu-id="48a95-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48a95-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a95-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a95-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48a95-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a95-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="48a95-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="48a95-140">**glClear**</span><span class="sxs-lookup"><span data-stu-id="48a95-140">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="48a95-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="48a95-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="48a95-142">**glget**</span><span class="sxs-lookup"><span data-stu-id="48a95-142">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





