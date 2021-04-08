---
title: glflush-Funktion (GL. h)
description: Die glflush-Funktion erzwingt die Ausführung von OpenGL-Funktionen in endlicher Zeit.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glflush-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743873"
---
# <a name="glflush-function"></a><span data-ttu-id="48d9f-104">glflush-Funktion</span><span class="sxs-lookup"><span data-stu-id="48d9f-104">glFlush function</span></span>

<span data-ttu-id="48d9f-105">Die **glflush** -Funktion erzwingt die Ausführung von OpenGL-Funktionen in endlicher Zeit.</span><span class="sxs-lookup"><span data-stu-id="48d9f-105">The **glFlush** function forces execution of OpenGL functions in finite time.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d9f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="48d9f-106">Syntax</span></span>


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a><span data-ttu-id="48d9f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="48d9f-107">Parameters</span></span>

<span data-ttu-id="48d9f-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="48d9f-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48d9f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48d9f-109">Return value</span></span>

<span data-ttu-id="48d9f-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48d9f-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48d9f-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="48d9f-111">Error codes</span></span>

<span data-ttu-id="48d9f-112">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="48d9f-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="48d9f-113">Name</span><span class="sxs-lookup"><span data-stu-id="48d9f-113">Name</span></span>                                                                                                  | <span data-ttu-id="48d9f-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="48d9f-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48d9f-115"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="48d9f-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="48d9f-116">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48d9f-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48d9f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48d9f-117">Remarks</span></span>

<span data-ttu-id="48d9f-118">Verschiedene OpenGL-Implementierungen Puffern Befehle an verschiedenen Stellen, einschließlich Netzwerkpuffern und Grafikbeschleuniger selbst.</span><span class="sxs-lookup"><span data-stu-id="48d9f-118">Different OpenGL implementations buffer commands in several different locations, including network buffers and the graphics accelerator itself.</span></span> <span data-ttu-id="48d9f-119">Die Funktion " **glflush** " Leert alle diese Puffer und bewirkt, dass alle ausgestellten Befehle so schnell ausgeführt werden, wie Sie von der tatsächlichen Renderingengine akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="48d9f-119">The **glFlush** function empties all these buffers, causing all issued commands to be executed as quickly as they are accepted by the actual rendering engine.</span></span> <span data-ttu-id="48d9f-120">Obwohl diese Ausführung möglicherweise nicht in einem bestimmten Zeitraum abgeschlossen ist, wird Sie in einer begrenzten Zeitspanne abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="48d9f-120">Though this execution may not be completed in any particular time period, it does complete in a finite amount of time.</span></span>

<span data-ttu-id="48d9f-121">Da jedes OpenGL-Programm über ein Netzwerk oder eine Zugriffstaste, die Befehle puffert, ausgeführt werden kann, müssen Sie in allen Programmen, die erfordern, dass alle zuvor ausgestellten Befehle abgeschlossen wurden, " **glflush** " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="48d9f-121">Because any OpenGL program might be executed over a network, or on an accelerator that buffers commands, be sure to call **glFlush** in any programs requiring that all of their previously issued commands have been completed.</span></span> <span data-ttu-id="48d9f-122">Nennen Sie z. b. **glflush** , bevor Sie auf Benutzereingaben warten, die vom generierten Bild abhängen.</span><span class="sxs-lookup"><span data-stu-id="48d9f-122">For example, call **glFlush** before waiting for user input that depends on the generated image.</span></span>

<span data-ttu-id="48d9f-123">Die **glflush** -Funktion kann jederzeit zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="48d9f-123">The **glFlush** function can return at any time.</span></span> <span data-ttu-id="48d9f-124">Er wartet nicht, bis die Ausführung aller zuvor ausgestellten OpenGL-Funktionen vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="48d9f-124">It does not wait until the execution of all previously issued OpenGL functions is complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="48d9f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48d9f-125">Requirements</span></span>



| <span data-ttu-id="48d9f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48d9f-126">Requirement</span></span> | <span data-ttu-id="48d9f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="48d9f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48d9f-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48d9f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="48d9f-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48d9f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="48d9f-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48d9f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="48d9f-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48d9f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48d9f-132">Header</span><span class="sxs-lookup"><span data-stu-id="48d9f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="48d9f-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="48d9f-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="48d9f-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48d9f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="48d9f-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48d9f-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="48d9f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="48d9f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48d9f-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48d9f-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48d9f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48d9f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d9f-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="48d9f-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="48d9f-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="48d9f-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="48d9f-141">**glfinish**</span><span class="sxs-lookup"><span data-stu-id="48d9f-141">**glFinish**</span></span>](glfinish.md)
</dt> </dl>

 

 





