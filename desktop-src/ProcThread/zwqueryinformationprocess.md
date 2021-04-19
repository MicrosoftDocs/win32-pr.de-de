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
# <a name="zwqueryinformationprocess-function"></a>Zwqueryinformationprocess-Funktion

\[**Zwqueryinformationprocess** kann in zukünftigen Versionen von Windows geändert werden oder nicht verfügbar sein. Anwendungen sollten die in diesem Thema aufgeführten Alternativen Funktionen verwenden.\]

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

*ProcessHandle* \[ in\]
</dt> <dd>

Ein Handle für den Prozess, für den Informationen abgerufen werden sollen.

</dd> <dt>

*Processinformationclass* \[ in\]
</dt> <dd>

Der Typ der Prozessinformationen, die abgerufen werden sollen. Dieser Parameter kann einer der folgenden Werte aus der **processinfoclass** -Enumeration sein.



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
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <dt><strong>Processbasicinformation</strong></dt> <dt>0</dt> </dl></td>
<td>Ruft einen Zeiger auf eine PEB-Struktur ab, die verwendet werden kann, um zu bestimmen, ob der angegebene Prozess gedebuggt wird, und einen eindeutigen Wert, der vom System verwendet wird, um den angegebenen Prozess zu identifizieren. <br/> Es empfiehlt sich, die Funktionen <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>checkremotedebuggerpresent</strong></a> und <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessID</strong></a> zu verwenden, um diese Informationen zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <dt><strong>Processdebugport</strong></dt> <dt>7</dt> </dl></td>
<td>Ruft einen <strong>DWORD_PTR</strong> Wert ab, der die Portnummer des Debuggers für den Prozess ist. Ein Wert ungleich 0 (null) gibt an, dass der Prozess unter der Steuerung eines Ring 3-Debuggers ausgeführt wird.<br/> Es empfiehlt sich, die <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>checkremotedebugerpresent</strong></a> -oder <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>isdebugerpresent</strong></a> -Funktion zu verwenden.<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </dl></td>
<td>Bestimmt, ob der Prozess in der WOW64-Umgebung ausgeführt wird (WOW64 ist der x86-Emulator, der die Ausführung von Win32-basierten Anwendungen auf 64-Bit-Fenstern zulässt).<br/> Es empfiehlt sich, die <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> -Funktion zu verwenden, um diese Informationen zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <dt><strong>Processimagefilename</strong></dt> <dt>27</dt> </dl></td>
<td>Ruft einen <strong>UNICODE_STRING</strong> Wert ab, der den Namen der Bilddatei für den Prozess enthält.<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <dt><strong>Processbreakonbeendigung</strong></dt> <dt>29</dt> </dl></td>
<td>Ruft einen <strong>ulong</strong> -Wert ab, der angibt, ob der Prozess als wichtig eingestuft wird.<br/>
<blockquote>
[!Note]<br />
Dieser Wert kann ab Windows XP mit SP3 verwendet werden. Ab Windows 8.1 sollte stattdessen <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>isprocesscritical</strong></a> verwendet werden.
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <dt><strong>Processprotectioninformation</strong></dt> <dt>61</dt> </dl></td>
<td>Ruft einen Bytewert ab, der den Typ des geschützten Prozesses und den Signatur Geber des geschützten Prozesses angibt.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*Processinformation* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der von der aufrufenden Anwendung bereitgestellt wird, in die die Funktion die angeforderten Informationen schreibt. Die Größe der geschriebenen Informationen variiert abhängig vom Wert des *processinformationclass* -Parameters:

<dl> <dt>

<span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>\_grundlegende \_ Informationen verarbeiten
</dt> <dd>

Wenn der *processinformationclass* -Parameter **processbasicinformation** ist, sollte der Puffer, auf den der *processinformation* -Parameter verweist, groß genug sein, um eine einzelne **Prozess \_ grundlegende \_ Informations** Struktur mit folgendem Layout zu enthalten:

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

Der **uniqueprocessid-** Member verweist auf den eindeutigen Bezeichner des Systems für diesen Prozess. Es empfiehlt sich, diese Informationen mit der [**GetProcessID-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) Funktion abzurufen.

Der Member " **Peer-BaseAddress** " verweist auf eine [**Peer**](/windows/desktop/api/Winternl/ns-winternl-peb) Struktur.

Die anderen Mitglieder dieser Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

</dd> <dt>

<span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ ptr
</dt> <dd>

Wenn der *processinformationclass* -Parameter **ProcessWow64Information** ist, sollte der Puffer, auf den der *processinformation* -Parameter verweist, groß genug sein, um ein **ulong- \_ ptr** zu speichern. Wenn dieser Wert ungleich 0 (null) ist, wird der Prozess in einer WOW64-Umgebung ausgeführt. Andernfalls wird der Prozess nicht in einer WOW64-Umgebung ausgeführt, wenn der Wert gleich 0 (null) ist.

Es empfiehlt sich, die [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) -Funktion zu verwenden, um zu bestimmen, ob ein Prozess in der WOW64-Umgebung ausgeführt wird.

</dd> <dt>

<span id="UNICODE_STRING"></span><span id="unicode_string"></span>Unicode- \_ Zeichenfolge
</dt> <dd>

Wenn der *processinformationclass* -Parameter **processimagefilename** ist, sollte der Puffer, auf den der *processinformation* -Parameter verweist, groß genug sein, um eine **Unicode- \_ Zeichen** folgen Struktur und die Zeichenfolge selbst zu speichern. Die im **Puffer** Element gespeicherte Zeichenfolge ist der Name der Bilddatei.

Wenn der Puffer zu klein ist, schlägt die Funktion mit dem \_ Fehlercode der Länge der Status Informationen \_ und dem Parameter " \_ *returnlength* " auf die erforderliche Puffergröße fest.

</dd> <dt>

<span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION
</dt> <dd>

Wenn der *processinformationclass* -Parameter **processprotectioninformation** ist, sollte der Puffer, auf den der *processinformation* -Parameter verweist, groß genug sein, um eine einzelne **PS_PROTECTION** Struktur mit folgendem Layout zu enthalten:

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

Die ersten drei Bits enthalten den Typ des geschützten Prozesses:

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

Die oberen 4 Bits enthalten den geschützten Prozess Signatur Geber:

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

*Processinformationlength* \[ in\]
</dt> <dd>

Die Größe des Puffers, auf den der *processinformation* -Parameter zeigt (in Bytes).

</dd> <dt>

*Returnlength* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, in der die Funktion die Größe der angeforderten Informationen zurückgibt. Wenn die Funktion erfolgreich war, ist dies die Größe der Informationen, die in den Puffer geschrieben werden, auf den der *processinformation* -Parameter verweist, aber wenn der Puffer zu klein war, ist dies die Mindestgröße des Puffers, der für den erfolgreichen Empfang der Informationen erforderlich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Erfolg von NTSTATUS oder einen Fehlercode zurück.

Die Formulare und die Bedeutung von NTSTATUS-Fehlercodes werden in der im DDK verfügbaren NTSTATUS. h-Header Datei aufgeführt und in der DDK-Dokumentation unter Kernel-Mode Treiberarchitektur/Entwurfs Handbuch/Treiber Programmiertechniken/Protokollierungs Fehler beschrieben.

## <a name="remarks"></a>Bemerkungen

Die **zwqueryinformationprocess** -Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden. Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen öffentliche Funktionen zu verwenden, die in der Beschreibung des *processinformationclass* -Parameters erwähnt werden.

Wenn Sie **zwqueryinformationprocess** verwenden, greifen Sie über das [dynamische Verknüpfen der Laufzeit](../dlls/using-run-time-dynamic-linking.md)auf die Funktion zu. Dadurch erhält Ihr Code die Möglichkeit, ordnungsgemäß zu reagieren, wenn die Funktion geändert oder aus dem Betriebssystem entfernt wurde. Signatur Änderungen sind jedoch möglicherweise nicht erkennbar.

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Checkremotedebugerpresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[**IsDebug-vorhanden**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
