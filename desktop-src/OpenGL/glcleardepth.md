---
title: glcleartiefe-Funktion (GL. h)
description: Die glcleartiefe-Funktion gibt den undeutlichen Wert für den tiefen Puffer an.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- glcleartiefe-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340778"
---
# <a name="glcleardepth-function"></a><span data-ttu-id="c71df-104">glcleartiefe-Funktion</span><span class="sxs-lookup"><span data-stu-id="c71df-104">glClearDepth function</span></span>

<span data-ttu-id="c71df-105">Die **glcleartiefe** -Funktion gibt den undeutlichen Wert für den tiefen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="c71df-105">The **glClearDepth** function specifies the clear value for the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71df-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c71df-106">Syntax</span></span>


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a><span data-ttu-id="c71df-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c71df-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71df-108">*Eingeh*</span><span class="sxs-lookup"><span data-stu-id="c71df-108">*depth*</span></span> 
</dt> <dd>

<span data-ttu-id="c71df-109">Der tiefen Wert, der verwendet wird, wenn der tiefen Puffer gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c71df-109">The depth value used when the depth buffer is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71df-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c71df-110">Return value</span></span>

<span data-ttu-id="c71df-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c71df-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c71df-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c71df-112">Error codes</span></span>

<span data-ttu-id="c71df-113">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c71df-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c71df-114">Name</span><span class="sxs-lookup"><span data-stu-id="c71df-114">Name</span></span>                                                                                                  | <span data-ttu-id="c71df-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c71df-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c71df-116"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="c71df-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c71df-117">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c71df-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c71df-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c71df-118">Remarks</span></span>

<span data-ttu-id="c71df-119">Die **glcleartiefe** -Funktion gibt den Tiefen Wert an, der von [**glClear**](glclear.md) verwendet wird, um den tiefen Puffer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c71df-119">The **glClearDepth** function specifies the depth value used by [**glClear**](glclear.md) to clear the depth buffer.</span></span> <span data-ttu-id="c71df-120">Die von **glcleartiefe** angegebenen Werte werden an den Bereich \[ 0, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="c71df-120">Values specified by **glClearDepth** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="c71df-121">Die folgende Funktion Ruft Informationen im Zusammenhang mit der Funktion " **glcleartiefe** " ab:</span><span class="sxs-lookup"><span data-stu-id="c71df-121">The following function retrieves information related to the **glClearDepth** function:</span></span>

<span data-ttu-id="c71df-122">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Tiefe \_ Clear- \_ Wert</span><span class="sxs-lookup"><span data-stu-id="c71df-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="c71df-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c71df-123">Requirements</span></span>



| <span data-ttu-id="c71df-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c71df-124">Requirement</span></span> | <span data-ttu-id="c71df-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c71df-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c71df-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c71df-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c71df-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c71df-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c71df-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c71df-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c71df-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c71df-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c71df-130">Header</span><span class="sxs-lookup"><span data-stu-id="c71df-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c71df-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c71df-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c71df-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c71df-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c71df-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c71df-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c71df-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c71df-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c71df-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c71df-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c71df-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c71df-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71df-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c71df-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c71df-138">**glClear**</span><span class="sxs-lookup"><span data-stu-id="c71df-138">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="c71df-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c71df-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c71df-140">**glget**</span><span class="sxs-lookup"><span data-stu-id="c71df-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





