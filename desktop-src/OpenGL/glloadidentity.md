---
title: glLoadIdentity-Funktion (GL. h)
description: Die Funktion "glLoadIdentity" ersetzt die aktuelle Matrix durch die Identitätsmatrix.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- glLoadIdentity-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568574"
---
# <a name="glloadidentity-function"></a><span data-ttu-id="b434e-104">glLoadIdentity-Funktion</span><span class="sxs-lookup"><span data-stu-id="b434e-104">glLoadIdentity function</span></span>

<span data-ttu-id="b434e-105">Die Funktion " **glLoadIdentity** " ersetzt die aktuelle Matrix durch die Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="b434e-105">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b434e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b434e-106">Syntax</span></span>


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a><span data-ttu-id="b434e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b434e-107">Parameters</span></span>

<span data-ttu-id="b434e-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b434e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b434e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b434e-109">Return value</span></span>

<span data-ttu-id="b434e-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b434e-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b434e-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b434e-111">Error codes</span></span>

<span data-ttu-id="b434e-112">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b434e-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b434e-113">Name</span><span class="sxs-lookup"><span data-stu-id="b434e-113">Name</span></span>                                                                                                  | <span data-ttu-id="b434e-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b434e-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b434e-115"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b434e-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b434e-116">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b434e-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b434e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b434e-117">Remarks</span></span>

<span data-ttu-id="b434e-118">Die Funktion " **glLoadIdentity** " ersetzt die aktuelle Matrix durch die Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="b434e-118">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span> <span data-ttu-id="b434e-119">Es ist semantisch äquivalent zum Aufrufen von [**glloadmatrix**](glloadmatrix.md) mit der folgenden Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="b434e-119">It is semantically equivalent to calling [**glLoadMatrix**](glloadmatrix.md) with the following identity matrix.</span></span>

![Diagramm, das die Identitätsmatrix anzeigt, die von glLoadIdentity aufgerufen wird.](images/load01.png)

<span data-ttu-id="b434e-121">In einigen Fällen ist es jedoch effizienter.</span><span class="sxs-lookup"><span data-stu-id="b434e-121">However, in some cases, it is more efficient.</span></span>

<span data-ttu-id="b434e-122">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glLoadIdentity** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="b434e-122">The following functions retrieve information related to **glLoadIdentity**:</span></span>

<span data-ttu-id="b434e-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="b434e-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="b434e-124">**glget** mit dem Argument GL \_ Modelview \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="b434e-124">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="b434e-125">**glget** mit dem Argument GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="b434e-125">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="b434e-126">**glget** mit Argument GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="b434e-126">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="b434e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b434e-127">Requirements</span></span>



| <span data-ttu-id="b434e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b434e-128">Requirement</span></span> | <span data-ttu-id="b434e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b434e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b434e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b434e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b434e-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b434e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b434e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b434e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b434e-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b434e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b434e-134">Header</span><span class="sxs-lookup"><span data-stu-id="b434e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b434e-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b434e-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b434e-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b434e-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="b434e-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b434e-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b434e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b434e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b434e-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b434e-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b434e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b434e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b434e-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b434e-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b434e-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b434e-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b434e-143">**glloadmatrix**</span><span class="sxs-lookup"><span data-stu-id="b434e-143">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="b434e-144">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="b434e-144">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="b434e-145">**glmultmatrix**</span><span class="sxs-lookup"><span data-stu-id="b434e-145">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="b434e-146">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="b434e-146">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





