---
title: glpopclientattrb-Funktion (GL. h)
description: Die Funktionen glpushclientattab und glpopclientatpub speichern und stellen Gruppen von Client Zustandsvariablen im Client Attribut Stapel wieder her. | glpopclientattrb-Funktion (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- glpopclientattrb-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353349"
---
# <a name="glpopclientattrib-function"></a><span data-ttu-id="7b9be-105">glpopclientattrb-Funktion</span><span class="sxs-lookup"><span data-stu-id="7b9be-105">glPopClientAttrib function</span></span>

<span data-ttu-id="7b9be-106">Die Funktionen [**glpushclientattab**](glpushclientattrib.md) und **glpopclientatpub** speichern und stellen Gruppen von Client Zustandsvariablen im Client Attribut Stapel wieder her.</span><span class="sxs-lookup"><span data-stu-id="7b9be-106">The [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9be-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b9be-107">Syntax</span></span>


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="7b9be-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b9be-108">Parameters</span></span>

<span data-ttu-id="7b9be-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7b9be-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b9be-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b9be-110">Return value</span></span>

<span data-ttu-id="7b9be-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7b9be-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b9be-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7b9be-112">Error codes</span></span>

<span data-ttu-id="7b9be-113">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7b9be-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7b9be-114">Name</span><span class="sxs-lookup"><span data-stu-id="7b9be-114">Name</span></span>                                                                                               | <span data-ttu-id="7b9be-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7b9be-115">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b9be-116"><dt>**GL- \_ Stapel \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="7b9be-116"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="7b9be-117">Die Funktion wurde aufgerufen, während der Client Attribut Stapel voll war.</span><span class="sxs-lookup"><span data-stu-id="7b9be-117">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7b9be-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b9be-118">Remarks</span></span>

<span data-ttu-id="7b9be-119">Die **glpushclientatpub** -Funktion verwendet den mask-Parameter, um zu bestimmen, welche Gruppen von Client Zustandsvariablen im Client Attribut Stapel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7b9be-119">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="7b9be-120">Sie können den bitweisen OR-Operator verwenden, um akzeptierte symbolische Konstanten zum Festlegen von Bits und zum Erstellen einer Maske zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="7b9be-120">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="7b9be-121">Die Funktion " **glpopclientatpub** " stellt die Werte der Client Zustandsvariablen wieder her, die zuletzt mit " **glpushclientatpub**" gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="7b9be-121">The **glPopClientAttrib** function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="7b9be-122">Nicht zuvor gespeicherte Client Zustandsvariablen bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="7b9be-122">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="7b9be-123">Durch das Übertragen von Attributen auf einen vollständigen Client Attribut Stapel oder das Pop von Attributen aus einem leeren Stapel wird ein Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="7b9be-123">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="7b9be-124">Der Client Attribut Stapel ist standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="7b9be-124">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="7b9be-125">Einige OpenGL-Client Zustands Werte können nicht auf dem Client Attribut Stapel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7b9be-125">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="7b9be-126">Beispielsweise können Sie die SELECT-oder Feedback Zustände nicht im Client Attribut Stapel speichern.</span><span class="sxs-lookup"><span data-stu-id="7b9be-126">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="7b9be-127">Die Tiefe des Client Attribut Stapels beträgt mindestens 16.</span><span class="sxs-lookup"><span data-stu-id="7b9be-127">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="7b9be-128">Die Funktionen " **glpushclientattab** " und " **glpopclientatpub** " werden nicht in Anzeigelisten kompiliert, sondern sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b9be-128">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="7b9be-129">Die Funktionen " **glpushclientattab** " und " **glpopclientatpub** " können nur die Pixel Speicher Modi per Push und Pop und den Scheitelpunkt Array-Client Status per Push</span><span class="sxs-lookup"><span data-stu-id="7b9be-129">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="7b9be-130">Sie müssen zum überführen von Push-und Pop-Zuständen, die auf dem Server aufbewahrt werden, [**glpushattab**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b9be-130">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="7b9be-131">Die Funktionen **glpushclientatpub** und **glpopclientatpub** sind nur in OpenGL, Version 1,1 oder höher, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b9be-131">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="7b9be-132">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glpushclientatpub** und **glpopclientatpub** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="7b9be-132">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="7b9be-133">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Client- \_ attrb- \_ Stapel \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="7b9be-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="7b9be-134">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max. Client Nachweis \_ \_ \_ \_ Tiefe für Client Nachweis</span><span class="sxs-lookup"><span data-stu-id="7b9be-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9be-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b9be-135">Requirements</span></span>



| <span data-ttu-id="7b9be-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b9be-136">Requirement</span></span> | <span data-ttu-id="7b9be-137">Wert</span><span class="sxs-lookup"><span data-stu-id="7b9be-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9be-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b9be-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9be-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b9be-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b9be-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b9be-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9be-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b9be-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b9be-142">Header</span><span class="sxs-lookup"><span data-stu-id="7b9be-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b9be-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b9be-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7b9be-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b9be-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b9be-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b9be-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b9be-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7b9be-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b9be-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b9be-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9be-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b9be-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9be-149">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="7b9be-149">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="7b9be-150">**gldisableclientstate**</span><span class="sxs-lookup"><span data-stu-id="7b9be-150">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="7b9be-151">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="7b9be-151">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="7b9be-152">**glenableclientstate**</span><span class="sxs-lookup"><span data-stu-id="7b9be-152">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="7b9be-153">**glget**</span><span class="sxs-lookup"><span data-stu-id="7b9be-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7b9be-154">**glgeterror**</span><span class="sxs-lookup"><span data-stu-id="7b9be-154">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="7b9be-155">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="7b9be-155">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="7b9be-156">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="7b9be-156">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="7b9be-157">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="7b9be-157">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="7b9be-158">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="7b9be-158">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="7b9be-159">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="7b9be-159">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="7b9be-160">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="7b9be-160">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="7b9be-161">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="7b9be-161">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





