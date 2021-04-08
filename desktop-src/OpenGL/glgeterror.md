---
title: glgeterror-Funktion (GL. h)
description: Die glgeterror-Funktion gibt Fehlerinformationen zurück.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glgeterror-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957023"
---
# <a name="glgeterror-function"></a><span data-ttu-id="39a7b-104">glgeterror-Funktion</span><span class="sxs-lookup"><span data-stu-id="39a7b-104">glGetError function</span></span>

<span data-ttu-id="39a7b-105">Die **glgeterror** -Funktion gibt Fehlerinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="39a7b-105">The **glGetError** function returns error information.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a7b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="39a7b-106">Syntax</span></span>


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a><span data-ttu-id="39a7b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="39a7b-107">Parameters</span></span>

<span data-ttu-id="39a7b-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="39a7b-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39a7b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39a7b-109">Return value</span></span>

<span data-ttu-id="39a7b-110">Die **glgeterror** -Funktion gibt einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="39a7b-110">The **glGetError** function returns one of the following error codes.</span></span>



| <span data-ttu-id="39a7b-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="39a7b-111">Return code</span></span>                                                                                           | <span data-ttu-id="39a7b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39a7b-112">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39a7b-113"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-113"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="39a7b-114">Für ein Enumerationsobjekt ist ein unzulässiger Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="39a7b-114">An unacceptable value is specified for an enumerated argument.</span></span> <span data-ttu-id="39a7b-115">Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="39a7b-115">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>         |
| <dl> <span data-ttu-id="39a7b-116"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-116"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="39a7b-117">Ein numerisches Argument liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="39a7b-117">A numeric argument is out of range.</span></span> <span data-ttu-id="39a7b-118">Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="39a7b-118">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                                    |
| <dl> <span data-ttu-id="39a7b-119"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="39a7b-120">Der angegebene Vorgang ist im aktuellen Zustand nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="39a7b-120">The specified operation is not allowed in the current state.</span></span> <span data-ttu-id="39a7b-121">Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="39a7b-121">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>           |
| <dl> <span data-ttu-id="39a7b-122"><dt>**GL \_ - \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-122"><dt>**GL\_NO\_ERROR**</dt></span></span> </dl>          | <span data-ttu-id="39a7b-123">Es wurde kein Fehler aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39a7b-123">No error has been recorded.</span></span> <span data-ttu-id="39a7b-124">Der Wert dieser symbolischen Konstante ist garantiert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="39a7b-124">The value of this symbolic constant is guaranteed to be zero.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="39a7b-125"><dt>**GL- \_ Stapel \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-125"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="39a7b-126">Diese Funktion würde zu einem Stapelüberlauf führen.</span><span class="sxs-lookup"><span data-stu-id="39a7b-126">This function would cause a stack overflow.</span></span> <span data-ttu-id="39a7b-127">Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="39a7b-127">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                            |
| <dl> <span data-ttu-id="39a7b-128"><dt>**GL. \_ Stapel \_ Unterlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-128"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="39a7b-129">Diese Funktion würde einen Stapel Unterlauf verursachen.</span><span class="sxs-lookup"><span data-stu-id="39a7b-129">This function would cause a stack underflow.</span></span> <span data-ttu-id="39a7b-130">Die problematische Funktion wird ignoriert, ohne dass Nebeneffekte festgelegt wird, um das Fehlerflag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="39a7b-130">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                           |
| <dl> <span data-ttu-id="39a7b-131"><dt>**\_nicht genügend \_ Arbeits \_ Speicher für GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-131"><dt>**GL\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="39a7b-132">Es ist nicht genügend Arbeitsspeicher zum Ausführen der Funktion vorhanden.</span><span class="sxs-lookup"><span data-stu-id="39a7b-132">There is not enough memory left to execute the function.</span></span> <span data-ttu-id="39a7b-133">Der Status OpenGL ist nicht definiert, außer dem Zustand der Fehlerflags, nachdem dieser Fehler aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="39a7b-133">The state of OpenGL is undefined, except for the state of the error flags, after this error is recorded.</span></span><br/> |



 

<span data-ttu-id="39a7b-134">Beachten Sie, dass " **glgeterror** " den Vorgang "GL invalid" zurückgibt, \_ \_ Wenn er zwischen einem Aufruf von [**glBegin**](glbegin.md) und seinem entsprechenden Aufruf von " [**glEnd**](glend.md)" aufgerufen</span><span class="sxs-lookup"><span data-stu-id="39a7b-134">Note that **glGetError** returns GL\_INVALID\_OPERATION if it is called between a call to [**glBegin**](glbegin.md) and its corresponding call to [**glEnd**](glend.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="39a7b-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39a7b-135">Remarks</span></span>

<span data-ttu-id="39a7b-136">Jedem erkennbaren Fehler wird ein numerischer Code und ein symbolischer Name zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="39a7b-136">Each detectable error is assigned a numeric code and symbolic name.</span></span> <span data-ttu-id="39a7b-137">Wenn ein Fehler auftritt, wird das Fehlerflag auf den entsprechenden Fehler Codewert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="39a7b-137">When an error occurs, the error flag is set to the appropriate error code value.</span></span> <span data-ttu-id="39a7b-138">Es werden keine weiteren Fehler aufgezeichnet, bis " **glgeterror** " aufgerufen wird. der Fehlercode wird zurückgegeben, und das Flag wird auf "GL No error" zurückgesetzt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="39a7b-138">No other errors are recorded until **glGetError** is called, the error code is returned, and the flag is reset to GL\_NO\_ERROR.</span></span> <span data-ttu-id="39a7b-139">Wenn bei einem Aufrufen von **glgeterror** der Befehl "GL \_ no error" zurück \_ gegeben wird, ist seit dem letzten Aufrufen von " **glgeterror**" bzw. seit dem Initialisieren von OpenGL ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="39a7b-139">If a call to **glGetError** returns GL\_NO\_ERROR, there has been no detectable error since the last call to **glGetError**, or since OpenGL was initialized.</span></span>

<span data-ttu-id="39a7b-140">Um verteilte Implementierungen zu ermöglichen, gibt es möglicherweise mehrere Fehlerflags.</span><span class="sxs-lookup"><span data-stu-id="39a7b-140">To allow for distributed implementations, there may be several error flags.</span></span> <span data-ttu-id="39a7b-141">Wenn ein einzelnes Fehlerflag einen Fehler aufgezeichnet hat, wird der Wert dieses Flags zurückgegeben, und dieses Flag wird auf "GL No error" zurückgesetzt, \_ \_ Wenn " **glgeterror** " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="39a7b-141">If any single error flag has recorded an error, the value of that flag is returned and that flag is reset to GL\_NO\_ERROR when **glGetError** is called.</span></span> <span data-ttu-id="39a7b-142">Wenn mehr als ein Flag einen Fehler aufgezeichnet hat, gibt **glgeterror** einen beliebigen Fehlerflag-Wert zurück und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="39a7b-142">If more than one flag has recorded an error, **glGetError** returns and clears an arbitrary error flag value.</span></span> <span data-ttu-id="39a7b-143">Wenn alle Fehlerflags zurückgesetzt werden sollen, sollten Sie in einer Schleife immer " **glgeterror** " aufrufen, bis "GL No error" zurückgegeben wird \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="39a7b-143">If all error flags are to be reset, you should always call **glGetError** in a loop until it returns GL\_NO\_ERROR.</span></span>

<span data-ttu-id="39a7b-144">Anfänglich werden alle Fehlerflags auf "GL \_ no error" festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="39a7b-144">Initially, all error flags are set to GL\_NO\_ERROR.</span></span>

<span data-ttu-id="39a7b-145">Wenn ein Fehlerflag festgelegt ist, sind die Ergebnisse eines OpenGL-Vorgangs nur dann definiert, wenn nicht genügend Arbeitsspeicher verfügbar ist \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="39a7b-145">When an error flag is set, results of an OpenGL operation are undefined only if GL\_OUT\_OF\_MEMORY has occurred.</span></span> <span data-ttu-id="39a7b-146">In allen anderen Fällen wird die Funktion, die den Fehler erzeugt, ignoriert und hat keine Auswirkung auf den OpenGL-Zustand oder Frame Puffer-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="39a7b-146">In all other cases, the function generating the error is ignored and has no effect on the OpenGL state or framebuffer contents.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a7b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39a7b-147">Requirements</span></span>



| <span data-ttu-id="39a7b-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39a7b-148">Requirement</span></span> | <span data-ttu-id="39a7b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="39a7b-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39a7b-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39a7b-150">Minimum supported client</span></span><br/> | <span data-ttu-id="39a7b-151">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39a7b-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="39a7b-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39a7b-152">Minimum supported server</span></span><br/> | <span data-ttu-id="39a7b-153">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39a7b-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39a7b-154">Header</span><span class="sxs-lookup"><span data-stu-id="39a7b-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a7b-155"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-155"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="39a7b-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39a7b-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="39a7b-157"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-157"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="39a7b-158">DLL</span><span class="sxs-lookup"><span data-stu-id="39a7b-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39a7b-159"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-159"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a7b-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39a7b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a7b-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="39a7b-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="39a7b-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="39a7b-162">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





