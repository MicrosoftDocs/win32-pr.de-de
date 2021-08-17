---
description: Ruft Informationen zum angegebenen Prozess ab.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: ZwQueryInformationProcess-Funktion
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
ms.openlocfilehash: 7972d3d2e6b98f56829680dd77c4c0a97b51679ffb2d9cfef928d4a279f6b7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792914"
---
# <a name="zwqueryinformationprocess-function"></a>ZwQueryInformationProcess-Funktion

\[**ZwQueryInformationProcess** kann in zukünftigen Versionen von geändert oder nicht mehr Windows. Anwendungen sollten die in diesem Thema aufgeführten alternativen Funktionen verwenden.\]

Ruft Informationen zum angegebenen Prozess ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProcessHandle* \[ In\]
</dt> <dd>

Ein Handle für den Prozess, für den Informationen abgerufen werden sollen.

</dd> <dt>

*ProcessInformationClass* \[ In\]
</dt> <dd>

Der Typ der abzurufenden Prozessinformationen. Dieser Parameter kann einer der folgenden Werte aus der **PROCESSINFOCLASS-Enumeration** sein.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </dl></td>
<td>Ruft einen Zeiger auf eine PEB-Struktur ab, die verwendet werden kann, um zu bestimmen, ob der angegebene Prozess debuggt wird, und einen eindeutigen Wert, der vom System zum Identifizieren des angegebenen Prozesses verwendet wird. <br/> Es ist am besten, die <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>Funktionen CheckRemoteDebuggerPresent</strong></a> und <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId zu</strong></a> verwenden, um diese Informationen zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </dl></td>
<td>Ruft einen <strong>DWORD_PTR</strong> wert ab, der die Portnummer des Debuggers für den Prozess ist. Ein Wert ungleich 0 (null) gibt an, dass der Prozess unter der Steuerung eines Ring 3-Debuggers ausgeführt wird.<br/> Es ist am besten, die <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent-</strong></a> oder <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent-Funktion zu</strong></a> verwenden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </dl></td>
<td>Bestimmt, ob der Prozess in der WOW64-Umgebung ausgeführt wird (WOW64 ist der x86-Emulator, der die Ausführung von Win32-basierten Anwendungen auf 64-Bit-Windows).<br/> Es ist am besten, die <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process-Funktion zu</strong></a> verwenden, um diese Informationen zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </dl></td>
<td>Ruft einen <strong>UNICODE_STRING</strong> wert ab, der den Namen der Bilddatei für den Prozess enthält.<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </dl></td>
<td>Ruft einen <strong>ULONG-Wert</strong> ab, der angibt, ob der Prozess als kritisch angesehen wird.<br/>
<blockquote>
[!Note]<br />
Dieser Wert kann ab Windows XP mit SP3 verwendet werden. Ab Windows 8.1 sollte <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>stattdessen IsProcessCritical</strong></a> verwendet werden.
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </dl></td>
<td>Ruft einen BYTE-Wert ab, der den Typ des geschützten Prozesses und den Signator des geschützten Prozesses angibt.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*ProcessInformation* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der von der aufrufenden Anwendung bereitgestellt wird, in den die Funktion die angeforderten Informationen schreibt. Die Größe der geschriebenen Informationen variiert je nach Wert des *ProcessInformationClass-Parameters:*

<dl> <dt>

<span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>GRUNDLEGENDE \_ INFORMATIONEN \_ VERARBEITEN
</dt> <dd>

Wenn der *ProcessInformationClass-Parameter* **ProcessBasicInformation** ist, sollte der Puffer, auf den der *ProcessInformation-Parameter* zeigt, groß genug sein, um eine einzelne **PROCESS BASIC \_ \_ INFORMATION-Struktur** mit dem folgenden Layout zu enthalten:

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

Der **UniqueProcessId-Member** verweist auf den eindeutigen Bezeichner des Systems für diesen Prozess. Es ist am besten, diese Informationen mithilfe der [**GetProcessId-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) abzurufen.

Der **PebBaseAddress-Member** verweist auf eine [**PEB-Struktur.**](/windows/desktop/api/Winternl/ns-winternl-peb)

Die anderen Member dieser Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

</dd> <dt>

<span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ PTR
</dt> <dd>

Wenn der *ProcessInformationClass-Parameter* **ProcessWow64Information** ist, sollte der Puffer, auf den der *ProcessInformation-Parameter* zeigt, groß genug sein, um einen **ULONG \_ PTR zu enthalten.** Wenn dieser Wert ungleich 0 (null) ist, wird der Prozess in einer WOW64-Umgebung ausgeführt. Andernfalls wird der Prozess nicht in einer WOW64-Umgebung ausgeführt, wenn der Wert gleich 0 (null) ist.

Es ist am besten, die [**IsWow64Process-Funktion zu**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) verwenden, um zu bestimmen, ob ein Prozess in der WOW64-Umgebung ausgeführt wird.

</dd> <dt>

<span id="UNICODE_STRING"></span><span id="unicode_string"></span>\_UNICODE-ZEICHENFOLGE
</dt> <dd>

Wenn der *ProcessInformationClass-Parameter* **ProcessImageFileName** ist, sollte der Puffer, auf den der *ProcessInformation-Parameter* zeigt, groß genug sein, um eine **UNICODE \_ STRING-Struktur** sowie die Zeichenfolge selbst zu enthalten. Die im Buffer-Member **gespeicherte Zeichenfolge** ist der Name der Bilddatei.

Wenn der Puffer zu klein ist, schlägt die Funktion mit dem Fehlercode STATUS INFO LENGTH MISMATCH fehl, und der \_ \_ \_ *ReturnLength-Parameter* wird auf die erforderliche Puffergröße festgelegt.

</dd> <dt>

<span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION
</dt> <dd>

Wenn der *ProcessInformationClass-Parameter* **ProcessProtectionInformation** ist, sollte der Puffer, auf den  der *ProcessInformation-Parameter* zeigt, groß genug sein, um eine einzelne PS_PROTECTION-Struktur mit dem folgenden Layout zu halten:

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

Die ersten 3 Bits enthalten den Typ des geschützten Prozesses:

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

Die obersten 4 Bits enthalten den Geschützten Prozess-Signator:

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

*ProcessInformationLength* \[ In\]
</dt> <dd>

Die Größe des Puffers, auf den der *ProcessInformation-Parameter* zeigt, in Bytes.

</dd> <dt>

*ReturnLength* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, in der die Funktion die Größe der angeforderten Informationen zurückgibt. Wenn die Funktion erfolgreich war, ist dies die Größe der Informationen, die in den Puffer geschrieben wurden, auf den der *ProcessInformation-Parameter* zeigt. Wenn der Puffer jedoch zu klein war, ist dies die Mindestgröße des Puffers, die zum erfolgreichen Empfangen der Informationen erforderlich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen NTSTATUS-Erfolgs- oder Fehlercode zurück.

Die Formulare und die Bedeutung von NTSTATUS-Fehlercodes sind in der im DDK verfügbaren Ntstatus.h-Headerdatei aufgeführt und werden in der DDK-Dokumentation unter Kernel-Mode Driver Architecture /Design Guide / Driver Programming Techniques / Logging Errors beschrieben.

## <a name="remarks"></a>Hinweise

Die **ZwQueryInformationProcess-Funktion** und die von ihr zurückgegebenen Strukturen sind für das Betriebssystem intern und können von einer Version von Windows in eine andere geändert werden. Um die Kompatibilität Ihrer Anwendung zu gewährleisten, ist es besser, stattdessen öffentliche Funktionen zu verwenden, die in der Beschreibung des *ProcessInformationClass-Parameters* erwähnt werden.

Wenn Sie **ZwQueryInformationProcess verwenden,** greifen Sie über dynamisches Verknüpfen zur Laufzeit [auf die Funktion zu.](../dlls/using-run-time-dynamic-linking.md) Dadurch erhält Ihr Code die Möglichkeit, ordnungsgemäß zu reagieren, wenn die Funktion geändert oder aus dem Betriebssystem entfernt wurde. Signaturänderungen sind jedoch möglicherweise nicht erkennbar.

Dieser Funktion ist keine Importbibliothek zugeordnet. Sie müssen die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Ntdll.dll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
