---
title: glcalllists-Funktion (GL. h)
description: Die Funktion "glcalllists" führt eine Liste von Anzeigelisten aus.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glcalllists-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956606"
---
# <a name="glcalllists-function"></a><span data-ttu-id="6f488-104">glcalllists-Funktion</span><span class="sxs-lookup"><span data-stu-id="6f488-104">glCallLists function</span></span>

<span data-ttu-id="6f488-105">Die Funktion " **glcalllists** " führt eine Liste von Anzeigelisten aus.</span><span class="sxs-lookup"><span data-stu-id="6f488-105">The **glCallLists** function executes a list of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f488-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f488-106">Syntax</span></span>


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a><span data-ttu-id="6f488-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f488-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f488-108">*n*</span><span class="sxs-lookup"><span data-stu-id="6f488-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="6f488-109">Die Anzahl der auszuführenden anzeigen Listen.</span><span class="sxs-lookup"><span data-stu-id="6f488-109">The number of display lists to be executed.</span></span>

</dd> <dt>

<span data-ttu-id="6f488-110">*type*</span><span class="sxs-lookup"><span data-stu-id="6f488-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="6f488-111">Der Typ der Werte in *Listen*.</span><span class="sxs-lookup"><span data-stu-id="6f488-111">The type of values in *lists*.</span></span> <span data-ttu-id="6f488-112">Die folgenden symbolischen Konstanten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="6f488-112">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="6f488-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6f488-113">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="6f488-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6f488-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="6f488-115"><dt>**GL \_ Byte**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-115"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="6f488-116">Der *lists* -Parameter wird als Array mit signierten Bytes behandelt, jeweils im Bereich von-128 bis 127.</span><span class="sxs-lookup"><span data-stu-id="6f488-116">The *lists* parameter is treated as an array of signed bytes, each in the range -128 through 127.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="6f488-117"><dt>**GL- \_ Byte ohne Vorzeichen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-117"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="6f488-118">Der *lists* -Parameter wird als Array von Bytes ohne Vorzeichen behandelt, die jeweils im Bereich von 0 bis 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="6f488-118">The *lists* parameter is treated as an array of unsigned bytes, each in the range 0 through 255.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="6f488-119"><dt>**GL \_ Short**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-119"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="6f488-120">Der *lists* -Parameter wird als Array von ganzen Zahlen mit Vorzeichen und 2 Bytes behandelt, jeweils im Bereich von-32768 bis 32767.</span><span class="sxs-lookup"><span data-stu-id="6f488-120">The *lists* parameter is treated as an array of signed 2-byte integers, each in the range -32768 through 32767.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="6f488-121"><dt>**GL \_ unsigned \_ Short**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-121"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="6f488-122">Der *lists* -Parameter wird als Array nicht signierter 2-Byte-Ganzzahlen behandelt, wobei jede im Bereich zwischen 0 und 65535 liegt.</span><span class="sxs-lookup"><span data-stu-id="6f488-122">The *lists* parameter is treated as an array of unsigned 2-byte integers, each in the range 0 through 65535.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="6f488-123"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-123"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="6f488-124">Der *lists* -Parameter wird als Array von mit Vorzeichen enden 4-Byte-Ganzzahlen behandelt.</span><span class="sxs-lookup"><span data-stu-id="6f488-124">The *lists* parameter is treated as an array of signed 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="6f488-125"><dt>**GL \_ unsigned \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-125"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="6f488-126">Der *lists* -Parameter wird als Array nicht signierter 4-Byte-Ganzzahlen behandelt.</span><span class="sxs-lookup"><span data-stu-id="6f488-126">The *lists* parameter is treated as an array of unsigned 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="6f488-127"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-127"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="6f488-128">Der *lists* -Parameter wird als Array von 4-Byte-Gleit Komma Werten behandelt.</span><span class="sxs-lookup"><span data-stu-id="6f488-128">The *lists* parameter is treated as an array of 4-byte, floating-point values.</span></span><br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <span data-ttu-id="6f488-129"><dt>**GL \_ 2 \_ Bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-129"><dt>**GL\_2\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="6f488-130">Der *lists* -Parameter wird als Array nicht signierter Bytes behandelt.</span><span class="sxs-lookup"><span data-stu-id="6f488-130">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="6f488-131">Jedes Byte paar gibt einen einzelnen anzeigen Listennamen an.</span><span class="sxs-lookup"><span data-stu-id="6f488-131">Each pair of bytes specifies a single display-list name.</span></span> <span data-ttu-id="6f488-132">Der Wert des Paars wird als 256-fache des nicht signierten Werts des ersten Bytes zuzüglich des unsignierten Werts des zweiten Bytes berechnet.</span><span class="sxs-lookup"><span data-stu-id="6f488-132">The value of the pair is computed as 256 times the unsigned value of the first byte plus the unsigned value of the second byte.</span></span><br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <span data-ttu-id="6f488-133"><dt>**GL. \_ 3 \_ Bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-133"><dt>**GL\_3\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="6f488-134">Der *lists* -Parameter wird als Array nicht signierter Bytes behandelt.</span><span class="sxs-lookup"><span data-stu-id="6f488-134">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="6f488-135">Jede dreier Größe von Bytes gibt einen einzelnen anzeigen Listennamen an.</span><span class="sxs-lookup"><span data-stu-id="6f488-135">Each triplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="6f488-136">Der Wert der-Zeichenfolge wird als 65536-fache des unsignierten Werts des ersten Bytes zuzüglich 256 mal des unsignierten Werts des zweiten Bytes zuzüglich des Werts ohne Vorzeichen des dritten Bytes berechnet.</span><span class="sxs-lookup"><span data-stu-id="6f488-136">The value of the triplet is computed as 65536 times the unsigned value of the first byte, plus 256 times the unsigned value of the second byte, plus the unsigned value of the third byte.</span></span><br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <span data-ttu-id="6f488-137"><dt>**GL \_ 4 \_ Bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-137"><dt>**GL\_4\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="6f488-138">Der *lists* -Parameter wird als Array nicht signierter Bytes behandelt.</span><span class="sxs-lookup"><span data-stu-id="6f488-138">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="6f488-139">Jedes Vierbeiner von Bytes gibt einen einzelnen anzeigen Listennamen an.</span><span class="sxs-lookup"><span data-stu-id="6f488-139">Each quadruplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="6f488-140">Der Wert des quadrupleps wird als 16777216-fache des unsignierten Werts des ersten Bytes zuzüglich 65536 Mal des unsignierten Werts des zweiten Bytes Plus 256-mal des Werts ohne Vorzeichen des dritten Bytes und des Werts ohne Vorzeichen des vierten Bytes berechnet.</span><span class="sxs-lookup"><span data-stu-id="6f488-140">The value of the quadruplet is computed as 16777216 times the unsigned value of the first byte, plus 65536 times the unsigned value of the second byte, plus 256 times the unsigned value of the third byte, plus the unsigned value of the fourth byte.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f488-141">*aufli*</span><span class="sxs-lookup"><span data-stu-id="6f488-141">*lists*</span></span> 
</dt> <dd>

<span data-ttu-id="6f488-142">Die Adresse eines Arrays von namens Offsets in der Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="6f488-142">The address of an array of name offsets in the display list.</span></span> <span data-ttu-id="6f488-143">Der Zeigertyp ist "void", da die Offsets abhängig vom Wert des *Typs* bytes, kurze, int oder Gleit Komma Werte sein können.</span><span class="sxs-lookup"><span data-stu-id="6f488-143">The pointer type is void because the offsets can be bytes, shorts, ints, or floats, depending on the value of *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f488-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f488-144">Return value</span></span>

<span data-ttu-id="6f488-145">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6f488-145">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f488-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f488-146">Remarks</span></span>

<span data-ttu-id="6f488-147">Die Funktion **glcalllists** bewirkt, dass jede Anzeigeliste in der Liste der Namen ausgeführt wird, die als *Listen* übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6f488-147">The **glCallLists** function causes each display list in the list of names passed as *lists* to be executed.</span></span> <span data-ttu-id="6f488-148">Folglich werden die in jeder Anzeigeliste gespeicherten Funktionen in der richtigen Reihenfolge ausgeführt, als würden Sie ohne Anzeigeliste aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6f488-148">As a result, the functions saved in each display list are executed in order, just as if they were called without using a display list.</span></span> <span data-ttu-id="6f488-149">Namen von anzeigen Listen, die nicht definiert wurden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6f488-149">Names of display lists that have not been defined are ignored.</span></span>

<span data-ttu-id="6f488-150">Die Funktion **glcalllists** bietet eine effiziente Möglichkeit zum Ausführen von Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="6f488-150">The **glCallLists** function provides an efficient means for executing display lists.</span></span> <span data-ttu-id="6f488-151">Der Parameter " *n* " gibt die Anzahl der Listen mit verschiedenen namens Formaten an (angegeben durch den *Typparameter* ) " **glcalllists** " wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f488-151">The *n* parameter specifies the number of lists with various name formats (specified by the *type* parameter) **glCallLists** executes.</span></span>

<span data-ttu-id="6f488-152">Die Liste der Namen der Anzeigenliste wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="6f488-152">The list of display list names is not null-terminated.</span></span> <span data-ttu-id="6f488-153">Stattdessen gibt *n* an, wie viele Namen aus *Listen* entnommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f488-153">Rather, *n* specifies how many names are to be taken from *lists*.</span></span>

<span data-ttu-id="6f488-154">Die [**gllistbase**](gllistbase.md) -Funktion stellt eine zusätzliche dereferenzierungsstufe zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6f488-154">The [**glListBase**](gllistbase.md) function makes an additional level of indirection available.</span></span> <span data-ttu-id="6f488-155">Die **gllistbase** -Funktion gibt einen nicht signierten Offset an, der in *Listen* vor der Ausführung der Anzeigeliste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6f488-155">The **glListBase** function specifies an unsigned offset that is added to each display list name specified in *lists* before that display list is executed.</span></span>

<span data-ttu-id="6f488-156">Die Funktion " **glcalllists** " kann in einer Anzeigeliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f488-156">The **glCallLists** function can appear inside a display list.</span></span> <span data-ttu-id="6f488-157">Um die Möglichkeit der unendlichen Rekursion zu vermeiden, die sich aus Anzeigelisten ergibt, wird während der Ausführung der Anzeigeliste eine Beschränkung auf der Schachtelungs Ebene der Anzeigelisten platziert.</span><span class="sxs-lookup"><span data-stu-id="6f488-157">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display list execution.</span></span> <span data-ttu-id="6f488-158">Diese Beschränkung muss mindestens 64 betragen, und Sie hängt von der Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="6f488-158">This limit must be at least 64, and it depends on the implementation.</span></span>

<span data-ttu-id="6f488-159">Der OpenGL-Zustand wird nicht in einem Aufruf von **glcalllists** gespeichert und wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="6f488-159">The OpenGL state is not saved and restored across a call to **glCallLists**.</span></span> <span data-ttu-id="6f488-160">Folglich verbleiben Änderungen, die während der Ausführung der Anzeigelisten am OpenGL-Zustand vorgenommen werden, nach Abschluss der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="6f488-160">Thus, changes made to the OpenGL state during the execution of the display lists remain after execution is completed.</span></span> <span data-ttu-id="6f488-161">Verwenden Sie " [**glpushattab**](glpushattrib.md)", " [**glpopatpub**](glpopattrib.md)", " [**glPushMatrix**](glpushmatrix.md)" und " [**glPopMatrix**](glpopmatrix.md) ", um den OpenGL-Zustand über **glcalllists** -Aufrufe beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="6f488-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md) to preserve the OpenGL state across **glCallLists** calls.</span></span>

<span data-ttu-id="6f488-162">Sie können Anzeigelisten zwischen einem Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden " [**glEnd**](glend.md)"-Befehl ausführen, solange die Anzeigeliste nur Funktionen enthält, die in diesem Intervall zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6f488-162">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="6f488-163">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glcalllists** " ab:</span><span class="sxs-lookup"><span data-stu-id="6f488-163">The following functions retrieve information related to the **glCallLists** function:</span></span>

<span data-ttu-id="6f488-164">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument-GL- \_ Listen \_ Basis</span><span class="sxs-lookup"><span data-stu-id="6f488-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIST\_BASE</span></span>

<span data-ttu-id="6f488-165">**glget** mit dem Argument GL \_ Max. \_ Listen Schachtelung \_</span><span class="sxs-lookup"><span data-stu-id="6f488-165">**glGet** with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="6f488-166">**glislist**</span><span class="sxs-lookup"><span data-stu-id="6f488-166">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="6f488-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f488-167">Requirements</span></span>



| <span data-ttu-id="6f488-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f488-168">Requirement</span></span> | <span data-ttu-id="6f488-169">Wert</span><span class="sxs-lookup"><span data-stu-id="6f488-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f488-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f488-170">Minimum supported client</span></span><br/> | <span data-ttu-id="6f488-171">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f488-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6f488-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f488-172">Minimum supported server</span></span><br/> | <span data-ttu-id="6f488-173">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f488-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f488-174">Header</span><span class="sxs-lookup"><span data-stu-id="6f488-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f488-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6f488-176">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f488-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f488-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f488-178">DLL</span><span class="sxs-lookup"><span data-stu-id="6f488-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f488-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f488-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f488-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f488-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f488-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6f488-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6f488-182">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="6f488-182">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="6f488-183">**gldelta etelists**</span><span class="sxs-lookup"><span data-stu-id="6f488-183">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="6f488-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6f488-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6f488-185">**glgenlists**</span><span class="sxs-lookup"><span data-stu-id="6f488-185">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="6f488-186">**glget**</span><span class="sxs-lookup"><span data-stu-id="6f488-186">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6f488-187">**glislist**</span><span class="sxs-lookup"><span data-stu-id="6f488-187">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="6f488-188">**gllistbase**</span><span class="sxs-lookup"><span data-stu-id="6f488-188">**glListBase**</span></span>](gllistbase.md)
</dt> <dt>

[<span data-ttu-id="6f488-189">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="6f488-189">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="6f488-190">**glpopattenb**</span><span class="sxs-lookup"><span data-stu-id="6f488-190">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="6f488-191">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="6f488-191">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="6f488-192">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="6f488-192">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="6f488-193">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="6f488-193">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





