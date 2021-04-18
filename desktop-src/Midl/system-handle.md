---
title: system_handle-Attribut
description: Das Attribut \ system_handle \ gibt einen System definierten Handlertyp an.
keywords:
- system_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106371832"
---
# <a name="system_handle-attribute"></a><span data-ttu-id="d906d-104">system_handle-Attribut</span><span class="sxs-lookup"><span data-stu-id="d906d-104">system_handle attribute</span></span>

<span data-ttu-id="d906d-105">Das \[ **system_handle** - \] Attribut gibt einen System definierten Handlertyp an, der den Zugriff auf ein Systemobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d906d-105">The \[**system_handle**\] attribute specifies a system-defined handle type that represents access to a system object.</span></span>

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a><span data-ttu-id="d906d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d906d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d906d-107">*System Handle-Typ*</span><span class="sxs-lookup"><span data-stu-id="d906d-107">*system-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d906d-108">Gibt eine der Optionen für den systembehandlertyp an.</span><span class="sxs-lookup"><span data-stu-id="d906d-108">Specifies one of the system handle type options.</span></span>

<span data-ttu-id="d906d-109">Die gültigen Optionen sind:</span><span class="sxs-lookup"><span data-stu-id="d906d-109">The valid options are:</span></span>
* <span data-ttu-id="d906d-110">[sh_composition](sh-composition.md) : ein directcomposition-Oberflächen handle</span><span class="sxs-lookup"><span data-stu-id="d906d-110">[sh_composition](sh-composition.md) - A DirectComposition surface handle</span></span>
* <span data-ttu-id="d906d-111">[sh_event](sh-event.md) ein benanntes oder unbenanntes Ereignis Objekt</span><span class="sxs-lookup"><span data-stu-id="d906d-111">[sh_event](sh-event.md) - A named or unnamed event object</span></span>
* <span data-ttu-id="d906d-112">[sh_file](sh-file.md) : eine Datei oder ein e/a-Gerät</span><span class="sxs-lookup"><span data-stu-id="d906d-112">[sh_file](sh-file.md) - A file or I/O device</span></span>
* <span data-ttu-id="d906d-113">[sh_job](sh-job.md) : ein Auftrags Objekt</span><span class="sxs-lookup"><span data-stu-id="d906d-113">[sh_job](sh-job.md) - A job object</span></span>
* <span data-ttu-id="d906d-114">[sh_mutex](sh-mutex.md) ein benanntes oder unbenanntes Mutex-Objekt</span><span class="sxs-lookup"><span data-stu-id="d906d-114">[sh_mutex](sh-mutex.md) - A named or unnamed mutex object</span></span>
* <span data-ttu-id="d906d-115">[sh_pipe](sh-pipe.md) -ein anonymes oder Named Pipe-Objekt</span><span class="sxs-lookup"><span data-stu-id="d906d-115">[sh_pipe](sh-pipe.md) - An anonymous or named pipe object</span></span>
* <span data-ttu-id="d906d-116">[sh_process](sh-process.md) -ein Prozess Objekt</span><span class="sxs-lookup"><span data-stu-id="d906d-116">[sh_process](sh-process.md) - A process object</span></span>
* <span data-ttu-id="d906d-117">[sh_reg_key](sh-reg-key.md) -Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="d906d-117">[sh_reg_key](sh-reg-key.md) - A registry key</span></span>
* <span data-ttu-id="d906d-118">[sh_section](sh-section.md) -A Shared Memory-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d906d-118">[sh_section](sh-section.md) - A shared memory section</span></span>
* <span data-ttu-id="d906d-119">[sh_semaphore](sh-semaphore.md) ein benanntes oder unbenanntes Semaphor-Objekt</span><span class="sxs-lookup"><span data-stu-id="d906d-119">[sh_semaphore](sh-semaphore.md) - A named or unnamed semaphore object</span></span>
* <span data-ttu-id="d906d-120">[sh_socket](sh-socket.md) -ein Winsock-Socketobjekt</span><span class="sxs-lookup"><span data-stu-id="d906d-120">[sh_socket](sh-socket.md) - A WinSock socket object</span></span>
* <span data-ttu-id="d906d-121">[sh_thread](sh-thread.md) : ein Thread Objekt</span><span class="sxs-lookup"><span data-stu-id="d906d-121">[sh_thread](sh-thread.md) - A thread object</span></span>
* <span data-ttu-id="d906d-122">[sh_token](sh-token.md) : ein zugriffstokenobjekt.</span><span class="sxs-lookup"><span data-stu-id="d906d-122">[sh_token](sh-token.md) - An access token object</span></span>

</dd> <dt>

<span data-ttu-id="d906d-123">*optional-Access-Mask*</span><span class="sxs-lookup"><span data-stu-id="d906d-123">*optional-access-mask*</span></span>
</dt> <dd>

<span data-ttu-id="d906d-124">Fordert optional bestimmte Zugriffsrechte an, die auf das duplizierte handle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d906d-124">Optionally requests specific access rights applied to the duplicated handle.</span></span> <span data-ttu-id="d906d-125">Wenn dies nicht angegeben ist, wird das Handle standardmäßig mit demselben Zugriff dupliziert.</span><span class="sxs-lookup"><span data-stu-id="d906d-125">By default when this is unspecified, the handle will be duplicated with the same access.</span></span> 

<span data-ttu-id="d906d-126">Um eine andere Zugriffsebene anzugeben, verwenden Sie objektspezifische Zugriffsrechte, die dem zugrunde liegenden Systemobjekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d906d-126">To specify a different level of access, use object specific access rights corresponding to the underlying system object selected.</span></span>

<span data-ttu-id="d906d-127">Weitere Informationen zur Weitergabe von Zugriffsrechten während der Duplizierung finden Sie in der [duplikatandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="d906d-127">More information on how access rights are propagated during duplication can be found on the [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) documentation.</span></span>

<span data-ttu-id="d906d-128">Links zu Listen mit Zugriffsrechten für jeden Objekttyp finden Sie sowohl in der *dupliktandle* -Referenz als auch in den " **Siehe auch** "-Überschriften der einzelnen `sh_*` Parameter Seiten.</span><span class="sxs-lookup"><span data-stu-id="d906d-128">Links to lists of access rights for each type of object can be found in the *DuplicateHandle* reference as well as in the **See also** headings of each `sh_*` parameter page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d906d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d906d-129">Remarks</span></span>

<span data-ttu-id="d906d-130">Um dieses Attribut zu verwenden, muss das- `-target` Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d906d-130">In order to use this attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

<span data-ttu-id="d906d-131">System Handles sind Handles, die vom Betriebssystem definiert werden, um den Zugriff auf eine System Ressource bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d906d-131">System handles are handles that are defined by the operating system to provide access to a system resource.</span></span> <span data-ttu-id="d906d-132">Der spezifische Typ des Objekts hinter dem Handle muss beim Deklarieren des Attributs angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d906d-132">The specific type of the object behind the handle must be specified when declaring the attribute.</span></span>

<span data-ttu-id="d906d-133">Bei einem markierten Handle `[in]` wird das Handle in die Remote Prozedur dupliziert und bleibt für die Dauer der Prozedur gültig.</span><span class="sxs-lookup"><span data-stu-id="d906d-133">For a handle marked `[in]`, the handle will be duplicated into the remote procedure and remains valid for the duration of that procedure.</span></span> <span data-ttu-id="d906d-134">Bei der Rückgabe von der Remote Prozedur wird das doppelte Handle freigegeben.</span><span class="sxs-lookup"><span data-stu-id="d906d-134">On return from the remote procedure, the duplicated handle is freed.</span></span> <span data-ttu-id="d906d-135">Um den Zugriff auf das zugrunde liegende Objekt aufrechtzuerhalten, muss die Remote Anwendung das Handle in seinen eigenen Adressraum duplizieren.</span><span class="sxs-lookup"><span data-stu-id="d906d-135">To maintain access to the underlying object, the remote application must duplicate the handle into its own address space.</span></span>

<span data-ttu-id="d906d-136">Im Gegensatz dazu geht bei einem markierten Handle `[out]` , wenn eine Remote Prozedur ein Handle von einem-Befehl zurückgibt, der Besitz der Remote Prozedur verloren.</span><span class="sxs-lookup"><span data-stu-id="d906d-136">By contrast, for a handle marked `[out]`, when a remote procedure returns a handle from a call, the remote procedure will lose ownership of it.</span></span> <span data-ttu-id="d906d-137">Um den Zugriff auf das zugrunde liegende Objekt aufrechtzuerhalten, sollte die Remote Prozedur das Handle duplizieren und das Duplikat zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d906d-137">To maintain access to the underlying object, the remote procedure should duplicate the handle and return the duplicate.</span></span> <span data-ttu-id="d906d-138">Der zurückgegebene Handle wird dann im Besitz des Aufrufers, der die Verantwortung dafür übernimmt, ihn zu schließen, wenn der Zugriff auf das zugrunde liegende Systemobjekt nicht mehr erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d906d-138">The returned handle then becomes owned by the caller who assumes a responsibility to close it when access to the underlying system object is no longer necessary.</span></span>

<span data-ttu-id="d906d-139">Da dies ein Mechanismus zum Weiterleiten des Zugriffs auf ein Systemobjekt ist, gilt dieses Attribut nur für Aufrufe zwischen Prozeduren auf dem gleichen Computer.</span><span class="sxs-lookup"><span data-stu-id="d906d-139">As this is a mechanism for relaying access to a system object, this attribute is only applicable to calls between procedures on the same machine.</span></span>

<span data-ttu-id="d906d-140">Die Erstellungs-und Zugriffsparameter, die dem zugrunde liegenden Objekt hinter dem System Handle bei der Erstellung erteilt werden, legen vor, ob es erfolgreich in den Remote Prozedur Kontext gemarshallt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d906d-140">The creation and access parameters given to the underlying object behind the system handle on its creation will dictate whether it can be successfully marshalled to the remote procedure context.</span></span>

<span data-ttu-id="d906d-141">Ein Array von `system_handle` kann mit der Syntax, die in der [**size_is-Attribut**](size-is.md) Dokumentation gefunden wird, entweder ein-oder ausgehend werden.</span><span class="sxs-lookup"><span data-stu-id="d906d-141">An array of `system_handle` can be passed either in or out with the syntax found in the [**size_is attribute**](size-is.md) documentation.</span></span>

## <a name="examples"></a><span data-ttu-id="d906d-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d906d-142">Examples</span></span>

<span data-ttu-id="d906d-143">In den folgenden Beispielen werden verschiedene Verwendungen von verwendet `system_handle` .</span><span class="sxs-lookup"><span data-stu-id="d906d-143">The following examples several uses of `system_handle`.</span></span> <span data-ttu-id="d906d-144">Ein umfassendes Beispiel finden Sie im [System Lenker](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) -Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d906d-144">For a complete sample, see the [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) sample.</span></span>

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a><span data-ttu-id="d906d-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d906d-145">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="d906d-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d906d-146">Minimum supported client</span></span> | <span data-ttu-id="d906d-147">Windows 10 Anniversary Update (Version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="d906d-147">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="d906d-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d906d-148">Minimum supported server</span></span> | <span data-ttu-id="d906d-149">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="d906d-149">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d906d-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d906d-150">See also</span></span>

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[<span data-ttu-id="d906d-151">/target-Schalter</span><span class="sxs-lookup"><span data-stu-id="d906d-151">/target switch</span></span>](./-target.md)
</dt> <dt>

[<span data-ttu-id="d906d-152">Bindung und Handles</span><span class="sxs-lookup"><span data-stu-id="d906d-152">Binding and Handles</span></span>](../Rpc/binding-and-handles.md)
</dt> <dt>

[<span data-ttu-id="d906d-153">Handles und Objekte</span><span class="sxs-lookup"><span data-stu-id="d906d-153">Handles and Objects</span></span>](../sysinfo/handles-and-objects.md)
</dt> <dt>

[<span data-ttu-id="d906d-154">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="d906d-154">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d906d-155">**Duplialisiehandle**</span><span class="sxs-lookup"><span data-stu-id="d906d-155">**DuplicateHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="d906d-156">Sicherheitsbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="d906d-156">Security Descriptors</span></span>](../secauthz/security-descriptors.md)
</dt></dl>
