---
description: Ruft Informationen zum angegebenen Prozess ab.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: Zwqueryinformationprocess-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQueryInformationProcess
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 30207c8d3d54c54f77194b542e10e9fee94e055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350218"
---
# <a name="zwqueryinformationprocess-function"></a><span data-ttu-id="9fe35-103">Zwqueryinformationprocess-Funktion</span><span class="sxs-lookup"><span data-stu-id="9fe35-103">ZwQueryInformationProcess function</span></span>

<span data-ttu-id="9fe35-104">\[**Zwqueryinformationprocess** kann in zukünftigen Versionen von Windows geändert werden oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9fe35-104">\[**ZwQueryInformationProcess** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="9fe35-105">Anwendungen sollten die in diesem Thema aufgeführten Alternativen Funktionen verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="9fe35-105">Applications should use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="9fe35-106">Ruft Informationen zum angegebenen Prozess ab.</span><span class="sxs-lookup"><span data-stu-id="9fe35-106">Retrieves information about the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe35-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fe35-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="9fe35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fe35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fe35-109">*ProcessHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fe35-109">*ProcessHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-110">Ein Handle für den Prozess, für den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9fe35-110">A handle to the process for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="9fe35-111">*Processinformationclass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fe35-111">*ProcessInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-112">Der Typ der Prozessinformationen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9fe35-112">The type of process information to be retrieved.</span></span> <span data-ttu-id="9fe35-113">Dieser Parameter kann einer der folgenden Werte aus der **processinfoclass** -Enumeration sein.</span><span class="sxs-lookup"><span data-stu-id="9fe35-113">This parameter can be one of the following values from the **PROCESSINFOCLASS** enumeration.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fe35-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9fe35-114">Value</span></span></th>
<th><span data-ttu-id="9fe35-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9fe35-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <span data-ttu-id="9fe35-116"><dt><strong>Processbasicinformation</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="9fe35-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="9fe35-117">Ruft einen Zeiger auf eine PEB-Struktur ab, die verwendet werden kann, um zu bestimmen, ob der angegebene Prozess gedebuggt wird, und einen eindeutigen Wert, der vom System verwendet wird, um den angegebenen Prozess zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9fe35-117">Retrieves a pointer to a PEB structure that can be used to determine whether the specified process is being debugged, and a unique value used by the system to identify the specified process.</span></span> <br/> <span data-ttu-id="9fe35-118">Es empfiehlt sich, die Funktionen <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>checkremotedebuggerpresent</strong></a> und <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessID</strong></a> zu verwenden, um diese Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9fe35-118">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> functions to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <span data-ttu-id="9fe35-119"><dt><strong>Processdebugport</strong></dt> <dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="9fe35-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="9fe35-120">Ruft einen <strong>DWORD_PTR</strong> Wert ab, der die Portnummer des Debuggers für den Prozess ist.</span><span class="sxs-lookup"><span data-stu-id="9fe35-120">Retrieves a <strong>DWORD_PTR</strong> value that is the port number of the debugger for the process.</span></span> <span data-ttu-id="9fe35-121">Ein Wert ungleich 0 (null) gibt an, dass der Prozess unter der Steuerung eines Ring 3-Debuggers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fe35-121">A nonzero value indicates that the process is being run under the control of a ring 3 debugger.</span></span><br/> <span data-ttu-id="9fe35-122">Es empfiehlt sich, die <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>checkremotedebugerpresent</strong></a> -oder <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>isdebugerpresent</strong></a> -Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9fe35-122">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <span data-ttu-id="9fe35-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span><span class="sxs-lookup"><span data-stu-id="9fe35-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span></span></dl></td>
<td><span data-ttu-id="9fe35-124">Bestimmt, ob der Prozess in der WOW64-Umgebung ausgeführt wird (WOW64 ist der x86-Emulator, der die Ausführung von Win32-basierten Anwendungen auf 64-Bit-Fenstern zulässt).</span><span class="sxs-lookup"><span data-stu-id="9fe35-124">Determines whether the process is running in the WOW64 environment (WOW64 is the x86 emulator that allows Win32-based applications to run on 64-bit Windows).</span></span><br/> <span data-ttu-id="9fe35-125">Es empfiehlt sich, die <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> -Funktion zu verwenden, um diese Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9fe35-125">It is best to use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> function to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <span data-ttu-id="9fe35-126"><dt><strong>Processimagefilename</strong></dt> <dt>27</dt> </span><span class="sxs-lookup"><span data-stu-id="9fe35-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span></span></dl></td>
<td><span data-ttu-id="9fe35-127">Ruft einen <strong>UNICODE_STRING</strong> Wert ab, der den Namen der Bilddatei für den Prozess enthält.</span><span class="sxs-lookup"><span data-stu-id="9fe35-127">Retrieves a <strong>UNICODE_STRING</strong> value containing the name of the image file for the process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <span data-ttu-id="9fe35-128"><dt><strong>Processbreakonbeendigung</strong></dt> <dt>29</dt> </span><span class="sxs-lookup"><span data-stu-id="9fe35-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span></span></dl></td>
<td><span data-ttu-id="9fe35-129">Ruft einen <strong>ulong</strong> -Wert ab, der angibt, ob der Prozess als wichtig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="9fe35-129">Retrieves a <strong>ULONG</strong> value indicating whether the process is considered critical.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9fe35-130">Dieser Wert kann ab Windows XP mit SP3 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fe35-130">This value can be used starting in Windows XP with SP3.</span></span> <span data-ttu-id="9fe35-131">Ab Windows 8.1 sollte stattdessen <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>isprocesscritical</strong></a> verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fe35-131">Starting in Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> should be used instead.</span></span>
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <span data-ttu-id="9fe35-132"><dt><strong>Processprotectioninformation</strong></dt> <dt>61</dt> </span><span class="sxs-lookup"><span data-stu-id="9fe35-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span></span></dl></td>
<td><span data-ttu-id="9fe35-133">Ruft einen Bytewert ab, der den Typ des geschützten Prozesses und den Signatur Geber des geschützten Prozesses angibt.</span><span class="sxs-lookup"><span data-stu-id="9fe35-133">Retrieves a BYTE value indicating the type of protected process and the protected process signer.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="9fe35-134">*Processinformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9fe35-134">*ProcessInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-135">Ein Zeiger auf einen Puffer, der von der aufrufenden Anwendung bereitgestellt wird, in die die Funktion die angeforderten Informationen schreibt.</span><span class="sxs-lookup"><span data-stu-id="9fe35-135">A pointer to a buffer supplied by the calling application into which the function writes the requested information.</span></span> <span data-ttu-id="9fe35-136">Die Größe der geschriebenen Informationen variiert abhängig vom Wert des *processinformationclass* -Parameters:</span><span class="sxs-lookup"><span data-stu-id="9fe35-136">The size of the information written varies depending on the value of the *ProcessInformationClass* parameter:</span></span>

<dl> <dt>

<span data-ttu-id="9fe35-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>\_grundlegende \_ Informationen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9fe35-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESS\_BASIC\_INFORMATION</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-138">Wenn der *processinformationclass* -Parameter **processbasicinformation** ist, sollte der Puffer, auf den der *processinformation* -Parameter verweist, groß genug sein, um eine einzelne **Prozess \_ grundlegende \_ Informations** Struktur mit folgendem Layout zu enthalten:</span><span class="sxs-lookup"><span data-stu-id="9fe35-138">When the *ProcessInformationClass* parameter is **ProcessBasicInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PROCESS\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

<span data-ttu-id="9fe35-139">Der **uniqueprocessid-** Member verweist auf den eindeutigen Bezeichner des Systems für diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="9fe35-139">The **UniqueProcessId** member points to the system's unique identifier for this process.</span></span> <span data-ttu-id="9fe35-140">Es empfiehlt sich, diese Informationen mit der [**GetProcessID-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) Funktion abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9fe35-140">It is best to use the [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) function to retrieve this information.</span></span>

<span data-ttu-id="9fe35-141">Der Member " **Peer-BaseAddress** " verweist auf eine [**Peer**](/windows/desktop/api/Winternl/ns-winternl-peb) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9fe35-141">The **PebBaseAddress** member points to a [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) structure.</span></span>

<span data-ttu-id="9fe35-142">Die anderen Mitglieder dieser Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="9fe35-142">The other members of this structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="9fe35-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ ptr</span><span class="sxs-lookup"><span data-stu-id="9fe35-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG\_PTR</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-144">Wenn der *processinformationclass* -Parameter **ProcessWow64Information** ist, sollte der Puffer, auf den der *processinformation* -Parameter verweist, groß genug sein, um ein **ulong- \_ ptr** zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9fe35-144">When the *ProcessInformationClass* parameter is **ProcessWow64Information**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **ULONG\_PTR**.</span></span> <span data-ttu-id="9fe35-145">Wenn dieser Wert ungleich 0 (null) ist, wird der Prozess in einer WOW64-Umgebung ausgeführt. Andernfalls wird der Prozess nicht in einer WOW64-Umgebung ausgeführt, wenn der Wert gleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="9fe35-145">If this value is nonzero, the process is running in a WOW64 environment; otherwise, if the value is equal to zero, the process is not running in a WOW64 environment.</span></span>

<span data-ttu-id="9fe35-146">Es empfiehlt sich, die [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) -Funktion zu verwenden, um zu bestimmen, ob ein Prozess in der WOW64-Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fe35-146">It is best to use the [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) function to determine whether a process is running in the WOW64 environment.</span></span>

</dd> <dt>

<span data-ttu-id="9fe35-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>Unicode- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9fe35-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-148">Wenn der *processinformationclass* -Parameter **processimagefilename** ist, sollte der Puffer, auf den der *processinformation* -Parameter verweist, groß genug sein, um eine **Unicode- \_ Zeichen** folgen Struktur und die Zeichenfolge selbst zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9fe35-148">When the *ProcessInformationClass* parameter is **ProcessImageFileName**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **UNICODE\_STRING** structure as well as the string itself.</span></span> <span data-ttu-id="9fe35-149">Die im **Puffer** Element gespeicherte Zeichenfolge ist der Name der Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="9fe35-149">The string stored in the **Buffer** member is the name of the image file.</span></span>

<span data-ttu-id="9fe35-150">Wenn der Puffer zu klein ist, schlägt die Funktion mit dem \_ Fehlercode der Länge der Status Informationen \_ und dem Parameter " \_ *returnlength* " auf die erforderliche Puffergröße fest.</span><span class="sxs-lookup"><span data-stu-id="9fe35-150">If the buffer is too small, the function fails with the STATUS\_INFO\_LENGTH\_MISMATCH error code and the *ReturnLength* parameter is set to the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="9fe35-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span><span class="sxs-lookup"><span data-stu-id="9fe35-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-152">Wenn der *processinformationclass* -Parameter **processprotectioninformation** ist, sollte der Puffer, auf den der *processinformation* -Parameter verweist, groß genug sein, um eine einzelne **PS_PROTECTION** Struktur mit folgendem Layout zu enthalten:</span><span class="sxs-lookup"><span data-stu-id="9fe35-152">When the *ProcessInformationClass* parameter is **ProcessProtectionInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PS_PROTECTION** structure having the following layout:</span></span>

``` syntax
typedef struct _PS_PROTECTION {
    union {
        UCHAR Level;
        struct {
            UCHAR Type   : 3;
            UCHAR Audit  : 1;                  // Reserved
            UCHAR Signer : 4;
        };
    };
} PS_PROTECTION, *PPS_PROTECTION;
```

<span data-ttu-id="9fe35-153">Die ersten drei Bits enthalten den Typ des geschützten Prozesses:</span><span class="sxs-lookup"><span data-stu-id="9fe35-153">The first 3 bits contain the type of protected process:</span></span>

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

<span data-ttu-id="9fe35-154">Die oberen 4 Bits enthalten den geschützten Prozess Signatur Geber:</span><span class="sxs-lookup"><span data-stu-id="9fe35-154">The top 4 bits contain the protected process signer:</span></span>

``` syntax
typedef enum _PS_PROTECTED_SIGNER {
    PsProtectedSignerNone = 0,
    PsProtectedSignerAuthenticode,
    PsProtectedSignerCodeGen,
    PsProtectedSignerAntimalware,
    PsProtectedSignerLsa,
    PsProtectedSignerWindows,
    PsProtectedSignerWinTcb,
    PsProtectedSignerWinSystem,
    PsProtectedSignerApp,
    PsProtectedSignerMax
} PS_PROTECTED_SIGNER, *PPS_PROTECTED_SIGNER;
```

</dd> </dl> </dd> <dt>

<span data-ttu-id="9fe35-155">*Processinformationlength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fe35-155">*ProcessInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-156">Die Größe des Puffers, auf den der *processinformation* -Parameter zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="9fe35-156">The size of the buffer pointed to by the *ProcessInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9fe35-157">*Returnlength* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="9fe35-157">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe35-158">Ein Zeiger auf eine Variable, in der die Funktion die Größe der angeforderten Informationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9fe35-158">A pointer to a variable in which the function returns the size of the requested information.</span></span> <span data-ttu-id="9fe35-159">Wenn die Funktion erfolgreich war, ist dies die Größe der Informationen, die in den Puffer geschrieben werden, auf den der *processinformation* -Parameter verweist, aber wenn der Puffer zu klein war, ist dies die Mindestgröße des Puffers, der für den erfolgreichen Empfang der Informationen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9fe35-159">If the function was successful, this is the size of the information written to the buffer pointed to by the *ProcessInformation* parameter, but if the buffer was too small, this is the minimum size of buffer needed to receive the information successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fe35-160">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fe35-160">Return value</span></span>

<span data-ttu-id="9fe35-161">Gibt einen Erfolg von NTSTATUS oder einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="9fe35-161">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="9fe35-162">Die Formulare und die Bedeutung von NTSTATUS-Fehlercodes werden in der im DDK verfügbaren NTSTATUS. h-Header Datei aufgeführt und in der DDK-Dokumentation unter Kernel-Mode Treiberarchitektur/Entwurfs Handbuch/Treiber Programmiertechniken/Protokollierungs Fehler beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9fe35-162">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation under Kernel-Mode Driver Architecture / Design Guide / Driver Programming Techniques / Logging Errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fe35-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fe35-163">Remarks</span></span>

<span data-ttu-id="9fe35-164">Die **zwqueryinformationprocess** -Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9fe35-164">The **ZwQueryInformationProcess** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="9fe35-165">Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen öffentliche Funktionen zu verwenden, die in der Beschreibung des *processinformationclass* -Parameters erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="9fe35-165">To maintain the compatibility of your application, it is better to use public functions mentioned in the description of the *ProcessInformationClass* parameter instead.</span></span>

<span data-ttu-id="9fe35-166">Wenn Sie **zwqueryinformationprocess** verwenden, greifen Sie über das [dynamische Verknüpfen der Laufzeit](../dlls/using-run-time-dynamic-linking.md)auf die Funktion zu.</span><span class="sxs-lookup"><span data-stu-id="9fe35-166">If you do use **ZwQueryInformationProcess**, access the function through [run-time dynamic linking](../dlls/using-run-time-dynamic-linking.md).</span></span> <span data-ttu-id="9fe35-167">Dadurch erhält Ihr Code die Möglichkeit, ordnungsgemäß zu reagieren, wenn die Funktion geändert oder aus dem Betriebssystem entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="9fe35-167">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="9fe35-168">Signatur Änderungen sind jedoch möglicherweise nicht erkennbar.</span><span class="sxs-lookup"><span data-stu-id="9fe35-168">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="9fe35-169">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="9fe35-169">This function has no associated import library.</span></span> <span data-ttu-id="9fe35-170">Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="9fe35-170">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe35-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fe35-171">Requirements</span></span>



| <span data-ttu-id="9fe35-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fe35-172">Requirement</span></span> | <span data-ttu-id="9fe35-173">Wert</span><span class="sxs-lookup"><span data-stu-id="9fe35-173">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe35-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fe35-174">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe35-175">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fe35-175">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9fe35-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fe35-176">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe35-177">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fe35-177">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9fe35-178">DLL</span><span class="sxs-lookup"><span data-stu-id="9fe35-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fe35-179"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe35-179"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fe35-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fe35-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe35-181">**Checkremotedebugerpresent**</span><span class="sxs-lookup"><span data-stu-id="9fe35-181">**CheckRemoteDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[<span data-ttu-id="9fe35-182">**GetProcessId**</span><span class="sxs-lookup"><span data-stu-id="9fe35-182">**GetProcessId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[<span data-ttu-id="9fe35-183">**IsDebug-vorhanden**</span><span class="sxs-lookup"><span data-stu-id="9fe35-183">**IsDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[<span data-ttu-id="9fe35-184">**IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="9fe35-184">**IsWow64Process**</span></span>](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
