---
title: glclearcolor-Funktion (GL. h)
description: Die Funktion "glclearcolor" gibt eindeutige Werte für die Farb Puffer an.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glclearcolor-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741937"
---
# <a name="glclearcolor-function"></a><span data-ttu-id="056c8-104">glclearcolor-Funktion</span><span class="sxs-lookup"><span data-stu-id="056c8-104">glClearColor function</span></span>

<span data-ttu-id="056c8-105">Die Funktion " **glclearcolor** " gibt eindeutige Werte für die Farb Puffer an.</span><span class="sxs-lookup"><span data-stu-id="056c8-105">The **glClearColor** function specifies clear values for the color buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="056c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="056c8-106">Syntax</span></span>


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a><span data-ttu-id="056c8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="056c8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="056c8-108">*Red*</span><span class="sxs-lookup"><span data-stu-id="056c8-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="056c8-109">Der rote Wert, den [**glClear**](glclear.md) verwendet, um die Farb Puffer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="056c8-109">The red value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="056c8-110">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="056c8-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="056c8-111">*Grünbuchs*</span><span class="sxs-lookup"><span data-stu-id="056c8-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="056c8-112">Der grüne Wert, den [**glClear**](glclear.md) verwendet, um die Farb Puffer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="056c8-112">The green value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="056c8-113">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="056c8-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="056c8-114">*blauen*</span><span class="sxs-lookup"><span data-stu-id="056c8-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="056c8-115">Der blaue Wert, den [**glClear**](glclear.md) verwendet, um die Farb Puffer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="056c8-115">The blue value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="056c8-116">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="056c8-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="056c8-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="056c8-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="056c8-118">Der Alpha-Wert, den [**glClear**](glclear.md) verwendet, um die Farb Puffer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="056c8-118">The alpha value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="056c8-119">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="056c8-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="056c8-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="056c8-120">Return value</span></span>

<span data-ttu-id="056c8-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="056c8-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="056c8-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="056c8-122">Error codes</span></span>

<span data-ttu-id="056c8-123">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="056c8-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="056c8-124">Name</span><span class="sxs-lookup"><span data-stu-id="056c8-124">Name</span></span>                                                                                                  | <span data-ttu-id="056c8-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="056c8-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="056c8-126"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="056c8-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="056c8-127">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="056c8-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="056c8-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="056c8-128">Remarks</span></span>

<span data-ttu-id="056c8-129">Die Funktion " **glclearcolor** " gibt die Werte für Rot, grün, blau und Alpha an, die von [**glClear**](glclear.md) zum Löschen der Farb Puffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="056c8-129">The **glClearColor** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the color buffers.</span></span> <span data-ttu-id="056c8-130">Die von **glclearcolor** angegebenen Werte werden an den Bereich \[ 0, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="056c8-130">Values specified by **glClearColor** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="056c8-131">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glclearcolor** " ab:</span><span class="sxs-lookup"><span data-stu-id="056c8-131">The following functions retrieve information related to the **glClearColor** function:</span></span>

<span data-ttu-id="056c8-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Accum \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="056c8-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="056c8-133">**glget** mit dem Argument GL \_ Color \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="056c8-133">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="056c8-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="056c8-134">Requirements</span></span>



| <span data-ttu-id="056c8-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="056c8-135">Requirement</span></span> | <span data-ttu-id="056c8-136">Wert</span><span class="sxs-lookup"><span data-stu-id="056c8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="056c8-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="056c8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="056c8-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="056c8-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="056c8-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="056c8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="056c8-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="056c8-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="056c8-141">Header</span><span class="sxs-lookup"><span data-stu-id="056c8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="056c8-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="056c8-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="056c8-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="056c8-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="056c8-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="056c8-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="056c8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="056c8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="056c8-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="056c8-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="056c8-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="056c8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056c8-148">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="056c8-148">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="056c8-149">**glClear**</span><span class="sxs-lookup"><span data-stu-id="056c8-149">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="056c8-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="056c8-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="056c8-151">**glget**</span><span class="sxs-lookup"><span data-stu-id="056c8-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





