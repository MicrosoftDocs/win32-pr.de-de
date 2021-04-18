---
title: glfinish-Funktion (GL. h)
description: Die Funktion "glfinish" wird blockiert, bis die gesamte OpenGL-Ausführung abgeschlossen ist.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- glfinish-Funktion OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731ffc91dbb8d31137a792b59d3ebc36bb4d5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519156"
---
# <a name="glfinish-function"></a><span data-ttu-id="682b0-104">glfinish-Funktion</span><span class="sxs-lookup"><span data-stu-id="682b0-104">glFinish function</span></span>

<span data-ttu-id="682b0-105">Die Funktion " **glfinish** " wird blockiert, bis die gesamte OpenGL-Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="682b0-105">The **glFinish** function blocks until all OpenGL execution is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="682b0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="682b0-106">Syntax</span></span>


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a><span data-ttu-id="682b0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="682b0-107">Parameters</span></span>

<span data-ttu-id="682b0-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="682b0-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="682b0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="682b0-109">Return value</span></span>

<span data-ttu-id="682b0-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="682b0-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="682b0-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="682b0-111">Error codes</span></span>

<span data-ttu-id="682b0-112">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="682b0-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="682b0-113">Name</span><span class="sxs-lookup"><span data-stu-id="682b0-113">Name</span></span>                                                                                                  | <span data-ttu-id="682b0-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="682b0-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="682b0-115"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="682b0-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="682b0-116">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="682b0-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="682b0-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="682b0-117">Remarks</span></span>

<span data-ttu-id="682b0-118">Die Funktion " **glfinish** " gibt erst zurück, wenn die Auswirkungen aller zuvor genannten OpenGL-Funktionen vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="682b0-118">The **glFinish** function does not return until the effects of all previously called OpenGL functions are complete.</span></span> <span data-ttu-id="682b0-119">Zu diesen Effekten gehören alle Änderungen am OpenGL-Status, alle Änderungen am Verbindungsstatus und alle Änderungen am Frame Puffer-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="682b0-119">Such effects include all changes to the OpenGL state, all changes to the connection state, and all changes to the framebuffer contents.</span></span>

<span data-ttu-id="682b0-120">Die Funktion " **glfinish** " erfordert einen Roundtrip zum Server.</span><span class="sxs-lookup"><span data-stu-id="682b0-120">The **glFinish** function requires a round trip to the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="682b0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="682b0-121">Requirements</span></span>



| <span data-ttu-id="682b0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="682b0-122">Requirement</span></span> | <span data-ttu-id="682b0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="682b0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="682b0-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="682b0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="682b0-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="682b0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="682b0-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="682b0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="682b0-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="682b0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="682b0-128">Header</span><span class="sxs-lookup"><span data-stu-id="682b0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="682b0-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="682b0-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="682b0-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="682b0-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="682b0-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="682b0-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="682b0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="682b0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="682b0-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="682b0-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="682b0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="682b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="682b0-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="682b0-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="682b0-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="682b0-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="682b0-137">**glflush**</span><span class="sxs-lookup"><span data-stu-id="682b0-137">**glFlush**</span></span>](glflush.md)
</dt> </dl>

 

 





