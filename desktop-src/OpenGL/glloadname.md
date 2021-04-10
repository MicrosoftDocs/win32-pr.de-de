---
title: glloadname-Funktion (GL. h)
description: Die Funktion "glloadname" lädt einen Namen in den Namen Stapel.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- glloadname-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106412"
---
# <a name="glloadname-function"></a><span data-ttu-id="f941d-104">glloadname-Funktion</span><span class="sxs-lookup"><span data-stu-id="f941d-104">glLoadName function</span></span>

<span data-ttu-id="f941d-105">Die Funktion " **glloadname** " lädt einen Namen in den Namen Stapel.</span><span class="sxs-lookup"><span data-stu-id="f941d-105">The **glLoadName** function loads a name onto the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="f941d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f941d-106">Syntax</span></span>


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="f941d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f941d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f941d-108">*name*</span><span class="sxs-lookup"><span data-stu-id="f941d-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="f941d-109">Ein Name, der den obersten Wert des Namens Stapels ersetzt.</span><span class="sxs-lookup"><span data-stu-id="f941d-109">A name that will replace the top value on the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f941d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f941d-110">Return value</span></span>

<span data-ttu-id="f941d-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f941d-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f941d-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f941d-112">Error codes</span></span>

<span data-ttu-id="f941d-113">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f941d-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f941d-114">Name</span><span class="sxs-lookup"><span data-stu-id="f941d-114">Name</span></span>                                                                                                  | <span data-ttu-id="f941d-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f941d-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f941d-116"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f941d-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f941d-117">Die Funktion wurde aufgerufen, während der namens Stapel leer war.</span><span class="sxs-lookup"><span data-stu-id="f941d-117">The function was called while the name stack was empty.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="f941d-118"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f941d-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f941d-119">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f941d-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f941d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f941d-120">Remarks</span></span>

<span data-ttu-id="f941d-121">Die Funktion " **glloadname** " bewirkt, dass *Name* den Wert am Anfang des Namens Stapels ersetzt, der anfänglich leer ist.</span><span class="sxs-lookup"><span data-stu-id="f941d-121">The **glLoadName** function causes *name* to replace the value on the top of the name stack, which is initially empty.</span></span> <span data-ttu-id="f941d-122">Der namens Stapel wird im Auswahlmodus verwendet, damit Sätze von renderingbefehlen eindeutig identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="f941d-122">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="f941d-123">Sie besteht aus einer geordneten Menge von Ganzzahlen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="f941d-123">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="f941d-124">Der namens Stapel ist immer leer, während der Rendermodus nicht die GL Select-Option ist \_ .</span><span class="sxs-lookup"><span data-stu-id="f941d-124">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="f941d-125">Aufrufe von **glloadname** , während der Rendermodus nicht gl SELECT ist, \_ werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f941d-125">Calls to **glLoadName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="f941d-126">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit " **glloadname**" abgerufen:</span><span class="sxs-lookup"><span data-stu-id="f941d-126">The following functions retrieve information related to **glLoadName**:</span></span>

<span data-ttu-id="f941d-127">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument "GL \_ Name \_ Stack- \_ Tiefe"</span><span class="sxs-lookup"><span data-stu-id="f941d-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="f941d-128">**glget** mit dem Argument GL \_ Max \_ Name Stack- \_ \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="f941d-128">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="f941d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f941d-129">Requirements</span></span>



| <span data-ttu-id="f941d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f941d-130">Requirement</span></span> | <span data-ttu-id="f941d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f941d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f941d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f941d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f941d-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f941d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f941d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f941d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f941d-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f941d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f941d-136">Header</span><span class="sxs-lookup"><span data-stu-id="f941d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f941d-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f941d-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f941d-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f941d-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="f941d-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f941d-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f941d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f941d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f941d-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f941d-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f941d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f941d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f941d-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f941d-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f941d-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f941d-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f941d-145">**glinitnames**</span><span class="sxs-lookup"><span data-stu-id="f941d-145">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="f941d-146">**glpushname**</span><span class="sxs-lookup"><span data-stu-id="f941d-146">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="f941d-147">**glrendermode**</span><span class="sxs-lookup"><span data-stu-id="f941d-147">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="f941d-148">**glselectbuffer**</span><span class="sxs-lookup"><span data-stu-id="f941d-148">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





