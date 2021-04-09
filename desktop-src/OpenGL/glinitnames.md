---
title: glinitnames-Funktion (GL. h)
description: Die Funktion "glinitnames" initialisiert den namens Stapel.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- glinitnames-Funktion OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ebdb9d19f6c88340fd53162febe694e3566408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102943"
---
# <a name="glinitnames-function"></a><span data-ttu-id="f445e-104">glinitnames-Funktion</span><span class="sxs-lookup"><span data-stu-id="f445e-104">glInitNames function</span></span>

<span data-ttu-id="f445e-105">Die Funktion " **glinitnames** " initialisiert den namens Stapel.</span><span class="sxs-lookup"><span data-stu-id="f445e-105">The **glInitNames** function initializes the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="f445e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f445e-106">Syntax</span></span>


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a><span data-ttu-id="f445e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f445e-107">Parameters</span></span>

<span data-ttu-id="f445e-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f445e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f445e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f445e-109">Return value</span></span>

<span data-ttu-id="f445e-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f445e-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f445e-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f445e-111">Error codes</span></span>

<span data-ttu-id="f445e-112">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f445e-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f445e-113">Name</span><span class="sxs-lookup"><span data-stu-id="f445e-113">Name</span></span>                                                                                                  | <span data-ttu-id="f445e-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f445e-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f445e-115"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f445e-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f445e-116">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f445e-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f445e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f445e-117">Remarks</span></span>

<span data-ttu-id="f445e-118">Die Funktion " **glinitnames** " bewirkt, dass der Namen Stapel mit seinem standardmäßigen leeren Zustand initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f445e-118">The **glInitNames** function causes the name stack to be initialized to its default empty state.</span></span> <span data-ttu-id="f445e-119">Der namens Stapel wird im Auswahlmodus verwendet, damit Sätze von renderingbefehlen eindeutig identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="f445e-119">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="f445e-120">Sie besteht aus einer geordneten Menge von Ganzzahlen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="f445e-120">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="f445e-121">Der namens Stapel ist immer leer, während der Rendermodus nicht die GL Select-Option ist \_ .</span><span class="sxs-lookup"><span data-stu-id="f445e-121">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="f445e-122">Aufrufe von **glinitnames** , während der Rendermodus nicht gl SELECT ist, \_ werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f445e-122">Calls to **glInitNames** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="f445e-123">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glinitnames** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="f445e-123">The following functions retrieve information related to **glInitNames**:</span></span>

<span data-ttu-id="f445e-124">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Name \_ Stack- \_ Tiefe"</span><span class="sxs-lookup"><span data-stu-id="f445e-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="f445e-125">**glget** mit dem Argument GL \_ Max \_ Name Stack- \_ \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="f445e-125">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="f445e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f445e-126">Requirements</span></span>



| <span data-ttu-id="f445e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f445e-127">Requirement</span></span> | <span data-ttu-id="f445e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f445e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f445e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f445e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f445e-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f445e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f445e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f445e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f445e-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f445e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f445e-133">Header</span><span class="sxs-lookup"><span data-stu-id="f445e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f445e-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f445e-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f445e-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f445e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="f445e-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f445e-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f445e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f445e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f445e-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f445e-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f445e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f445e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f445e-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f445e-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f445e-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f445e-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f445e-142">**glloadname**</span><span class="sxs-lookup"><span data-stu-id="f445e-142">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="f445e-143">**glpushname**</span><span class="sxs-lookup"><span data-stu-id="f445e-143">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="f445e-144">**glrendermode**</span><span class="sxs-lookup"><span data-stu-id="f445e-144">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="f445e-145">**glselectbuffer**</span><span class="sxs-lookup"><span data-stu-id="f445e-145">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





