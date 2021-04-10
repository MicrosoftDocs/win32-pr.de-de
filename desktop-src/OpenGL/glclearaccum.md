---
title: glclearaccum-Funktion (GL. h)
description: Die Funktion "glclearaccum" gibt die klaren Werte für den Akkumulations Puffer an.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- glclearaccum-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104127"
---
# <a name="glclearaccum-function"></a><span data-ttu-id="a842e-104">glclearaccum-Funktion</span><span class="sxs-lookup"><span data-stu-id="a842e-104">glClearAccum function</span></span>

<span data-ttu-id="a842e-105">Die Funktion " **glclearaccum** " gibt die klaren Werte für den Akkumulations Puffer an.</span><span class="sxs-lookup"><span data-stu-id="a842e-105">The **glClearAccum** function specifies the clear values for the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a842e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a842e-106">Syntax</span></span>


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a><span data-ttu-id="a842e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a842e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a842e-108">*Red*</span><span class="sxs-lookup"><span data-stu-id="a842e-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="a842e-109">Der rote Wert, der verwendet wird, wenn der Akkumulations Puffer gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a842e-109">The red value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="a842e-110">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a842e-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="a842e-111">*Grünbuchs*</span><span class="sxs-lookup"><span data-stu-id="a842e-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="a842e-112">Der grüne Wert, der verwendet wird, wenn der Akkumulations Puffer gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a842e-112">The green value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="a842e-113">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a842e-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="a842e-114">*blauen*</span><span class="sxs-lookup"><span data-stu-id="a842e-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="a842e-115">Der blaue Wert, der verwendet wird, wenn der Akkumulations Puffer gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a842e-115">The blue value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="a842e-116">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a842e-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="a842e-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="a842e-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="a842e-118">Der Alpha Wert, der verwendet wird, wenn der Akkumulations Puffer gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a842e-118">The alpha value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="a842e-119">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a842e-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a842e-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a842e-120">Return value</span></span>

<span data-ttu-id="a842e-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a842e-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a842e-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a842e-122">Error codes</span></span>

<span data-ttu-id="a842e-123">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a842e-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a842e-124">Name</span><span class="sxs-lookup"><span data-stu-id="a842e-124">Name</span></span>                                                                                                  | <span data-ttu-id="a842e-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a842e-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a842e-126"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="a842e-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a842e-127">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a842e-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a842e-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a842e-128">Remarks</span></span>

<span data-ttu-id="a842e-129">Die Funktion " **glclearaccum** " gibt die Werte rot, grün, blau und Alpha an, die von [**glClear**](glclear.md) zum Löschen des Akkumulations Puffers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a842e-129">The **glClearAccum** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the accumulation buffer.</span></span>

<span data-ttu-id="a842e-130">Die von **glclearaccum** angegebenen Werte werden an den Bereich \[ 1, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="a842e-130">Values specified by **glClearAccum** are clamped to the range \[1,1\].</span></span>

<span data-ttu-id="a842e-131">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glclearaccum** ab:</span><span class="sxs-lookup"><span data-stu-id="a842e-131">The following function retrieves information related to **glClearAccum**:</span></span>

<span data-ttu-id="a842e-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Accum \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="a842e-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="a842e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a842e-133">Requirements</span></span>



| <span data-ttu-id="a842e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a842e-134">Requirement</span></span> | <span data-ttu-id="a842e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a842e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a842e-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a842e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a842e-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a842e-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a842e-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a842e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a842e-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a842e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a842e-140">Header</span><span class="sxs-lookup"><span data-stu-id="a842e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a842e-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a842e-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a842e-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a842e-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="a842e-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a842e-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a842e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a842e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a842e-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a842e-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a842e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a842e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a842e-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a842e-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a842e-148">**glClear**</span><span class="sxs-lookup"><span data-stu-id="a842e-148">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="a842e-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a842e-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a842e-150">**glget**</span><span class="sxs-lookup"><span data-stu-id="a842e-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





