---
title: glpushclientatpub-Funktion (GL. h)
description: Die Funktionen glpushclientattab und glpopclientatpub speichern und stellen Gruppen von Client Zustandsvariablen im Client Attribut Stapel wieder her. | glpushclientatpub-Funktion (GL. h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- glpushclientatpub-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353779"
---
# <a name="glpushclientattrib-function"></a><span data-ttu-id="73ec7-105">glpushclientatpub-Funktion</span><span class="sxs-lookup"><span data-stu-id="73ec7-105">glPushClientAttrib function</span></span>

<span data-ttu-id="73ec7-106">Die Funktionen **glpushclientattab** und [**glpopclientatpub**](glpopclientattrib.md) speichern und stellen Gruppen von Client Zustandsvariablen im Client Attribut Stapel wieder her.</span><span class="sxs-lookup"><span data-stu-id="73ec7-106">The **glPushClientAttrib** and [**glPopClientAttrib**](glpopclientattrib.md) functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ec7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73ec7-107">Syntax</span></span>


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="73ec7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="73ec7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ec7-109">*mask*</span><span class="sxs-lookup"><span data-stu-id="73ec7-109">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="73ec7-110">Eine Maske, die angibt, welche Attribute gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="73ec7-110">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="73ec7-111">Im folgenden finden Sie die symbolischen Masken Konstanten und ihre zugeordneten OpenGL-Client Zustände.</span><span class="sxs-lookup"><span data-stu-id="73ec7-111">The following are the symbolic mask constants and their associated OpenGL client states.</span></span>



| <span data-ttu-id="73ec7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="73ec7-112">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="73ec7-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="73ec7-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <span data-ttu-id="73ec7-114"><dt>**GL- \_ Client \_ Pixel \_ Speicher \_ Bit**</dt></span><span class="sxs-lookup"><span data-stu-id="73ec7-114"><dt>**GL\_CLIENT\_PIXEL\_STORE\_BIT**</dt></span></span> </dl>                                             | <span data-ttu-id="73ec7-115">Pixel Speicher Modus-Attribute.</span><span class="sxs-lookup"><span data-stu-id="73ec7-115">Pixel storage mode attributes.</span></span><br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <span data-ttu-id="73ec7-116"><dt>**GL- \_ Client- \_ Vertex- \_ array \_ Bit**</dt></span><span class="sxs-lookup"><span data-stu-id="73ec7-116"><dt>**GL\_CLIENT\_VERTEX\_ARRAY\_BIT**</dt></span></span> </dl>                                          | <span data-ttu-id="73ec7-117">Vertex-Array Attribute.</span><span class="sxs-lookup"><span data-stu-id="73ec7-117">Vertex array attributes.</span></span><br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <span data-ttu-id="73ec7-118"><dt>**GL- \_ Client \_ alle \_ attrb- \_ Bits**</dt></span><span class="sxs-lookup"><span data-stu-id="73ec7-118"><dt>**GL\_CLIENT\_ALL\_ATTRIB\_BITs**</dt></span></span> </dl> | <span data-ttu-id="73ec7-119">Alle Stackable Client-State-Attribute.</span><span class="sxs-lookup"><span data-stu-id="73ec7-119">all stackable client-state attributes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ec7-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73ec7-120">Return value</span></span>

<span data-ttu-id="73ec7-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="73ec7-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73ec7-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="73ec7-122">Error codes</span></span>

<span data-ttu-id="73ec7-123">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="73ec7-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="73ec7-124">Name</span><span class="sxs-lookup"><span data-stu-id="73ec7-124">Name</span></span>                                                                                               | <span data-ttu-id="73ec7-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="73ec7-125">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73ec7-126"><dt>**GL- \_ Stapel \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="73ec7-126"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="73ec7-127">Die Funktion wurde aufgerufen, während der Client Attribut Stapel voll war.</span><span class="sxs-lookup"><span data-stu-id="73ec7-127">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="73ec7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73ec7-128">Remarks</span></span>

<span data-ttu-id="73ec7-129">Die **glpushclientatpub** -Funktion verwendet den mask-Parameter, um zu bestimmen, welche Gruppen von Client Zustandsvariablen im Client Attribut Stapel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="73ec7-129">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="73ec7-130">Sie können den bitweisen OR-Operator verwenden, um akzeptierte symbolische Konstanten zum Festlegen von Bits und zum Erstellen einer Maske zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="73ec7-130">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="73ec7-131">Die Funktion " [**glpopclientatpub**](glpopclientattrib.md) " stellt die Werte der Client Zustandsvariablen wieder her, die zuletzt mit " **glpushclientatpub**" gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="73ec7-131">The [**glPopClientAttrib**](glpopclientattrib.md) function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="73ec7-132">Nicht zuvor gespeicherte Client Zustandsvariablen bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="73ec7-132">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="73ec7-133">Durch das Übertragen von Attributen auf einen vollständigen Client Attribut Stapel oder das Pop von Attributen aus einem leeren Stapel wird ein Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="73ec7-133">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="73ec7-134">Der Client Attribut Stapel ist standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="73ec7-134">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="73ec7-135">Einige OpenGL-Client Zustands Werte können nicht auf dem Client Attribut Stapel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="73ec7-135">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="73ec7-136">Beispielsweise können Sie die SELECT-oder Feedback Zustände nicht im Client Attribut Stapel speichern.</span><span class="sxs-lookup"><span data-stu-id="73ec7-136">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="73ec7-137">Die Tiefe des Client Attribut Stapels beträgt mindestens 16.</span><span class="sxs-lookup"><span data-stu-id="73ec7-137">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="73ec7-138">Die Funktionen " **glpushclientattab** " und " **glpopclientatpub** " werden nicht in Anzeigelisten kompiliert, sondern sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73ec7-138">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="73ec7-139">Die Funktionen " **glpushclientattab** " und " **glpopclientatpub** " können nur die Pixel Speicher Modi per Push und Pop und den Scheitelpunkt Array-Client Status per Push</span><span class="sxs-lookup"><span data-stu-id="73ec7-139">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="73ec7-140">Sie müssen zum überführen von Push-und Pop-Zuständen, die auf dem Server aufbewahrt werden, [**glpushattab**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="73ec7-140">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="73ec7-141">Die Funktionen **glpushclientatpub** und **glpopclientatpub** sind nur in OpenGL, Version 1,1 oder höher, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="73ec7-141">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="73ec7-142">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glpushclientatpub** und **glpopclientatpub** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="73ec7-142">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="73ec7-143">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL- \_ Client- \_ attrb- \_ Stapel \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="73ec7-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="73ec7-144">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Max. Client Nachweis \_ \_ \_ \_ Tiefe für Client Nachweis</span><span class="sxs-lookup"><span data-stu-id="73ec7-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="73ec7-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73ec7-145">Requirements</span></span>



| <span data-ttu-id="73ec7-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73ec7-146">Requirement</span></span> | <span data-ttu-id="73ec7-147">Wert</span><span class="sxs-lookup"><span data-stu-id="73ec7-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73ec7-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73ec7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="73ec7-149">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73ec7-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="73ec7-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73ec7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="73ec7-151">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73ec7-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73ec7-152">Header</span><span class="sxs-lookup"><span data-stu-id="73ec7-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="73ec7-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="73ec7-153"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="73ec7-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73ec7-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="73ec7-155"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73ec7-155"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="73ec7-156">DLL</span><span class="sxs-lookup"><span data-stu-id="73ec7-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73ec7-157"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73ec7-157"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ec7-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73ec7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ec7-159">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="73ec7-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="73ec7-160">**gldisableclientstate**</span><span class="sxs-lookup"><span data-stu-id="73ec7-160">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="73ec7-161">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="73ec7-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="73ec7-162">**glenableclientstate**</span><span class="sxs-lookup"><span data-stu-id="73ec7-162">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="73ec7-163">**glget**</span><span class="sxs-lookup"><span data-stu-id="73ec7-163">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="73ec7-164">**glgeterror**</span><span class="sxs-lookup"><span data-stu-id="73ec7-164">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="73ec7-165">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="73ec7-165">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="73ec7-166">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="73ec7-166">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="73ec7-167">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="73ec7-167">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="73ec7-168">**glpixelstore**</span><span class="sxs-lookup"><span data-stu-id="73ec7-168">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="73ec7-169">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="73ec7-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="73ec7-170">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="73ec7-170">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="73ec7-171">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="73ec7-171">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





