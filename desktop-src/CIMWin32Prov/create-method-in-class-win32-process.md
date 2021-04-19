---
description: Die CREATE&\# 8194; Die WMI-Klassenmethode erstellt einen neuen Prozess.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Create-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342761"
---
# <a name="create-method-of-the-win32_process-class"></a>Create-Methode der Win32- \_ Prozess Klasse

Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode erstellt einen neuen Prozess.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Befehlszeile* \[ in\]
</dt> <dd>

Die auszuführende Befehlszeile. Das System fügt der Befehlszeile ein NULL-Zeichen hinzu, wobei die Zeichenfolge bei Bedarf gekürzt wird, um anzugeben, welche Datei tatsächlich verwendet wurde.

</dd> <dt>

*CurrentDirectory* \[ in\]
</dt> <dd>

Aktuelles Laufwerk und Verzeichnis für den untergeordneten Prozess. Für die Zeichenfolge muss das aktuelle Verzeichnis zu einem bekannten Pfad aufgelöst werden. Ein Benutzer kann einen absoluten Pfad oder einen Pfad relativ zum aktuellen Arbeitsverzeichnis angeben. Wenn dieser Parameter **null** ist, weist der neue Prozess denselben Pfad wie der aufrufende Prozess auf. Diese Option wird in erster Linie für Shells bereitgestellt, die eine Anwendung starten müssen, und das Anfangs Laufwerk und Arbeitsverzeichnis der Anwendung angeben.

</dd> <dt>

*Processstartupinformation* \[ in\]
</dt> <dd>

Die Startkonfiguration eines Windows-Prozesses. Weitere Informationen finden Sie unter [**Win32 \_ processstartup**](win32-processstartup.md).

</dd> <dt>

*ProcessID* \[ vorgenommen\]
</dt> <dd>

Die globale Prozess-ID, die zum Identifizieren eines Prozesses verwendet werden kann. Der Wert ist ab dem Zeitpunkt gültig, zu dem der Prozess erstellt wird, bis zu dem Zeitpunkt, zu dem der Prozess beendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Prozess erfolgreich erstellt wurde, und jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss** (0)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Unzureichende Berechtigungen** (3)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

Der **Pfad wurde nicht gefunden** (9).
</dt> <dt>

**Ungültiger Parameter** (21)
</dt> <dt>

**Sonstige** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können eine Instanz der Win32-Klasse " [**\_ processstartup**](win32-processstartup.md) " erstellen, um den Prozess zu konfigurieren, bevor Sie diese Methode aufrufen.

Ein voll qualifizierter Pfad muss in Fällen angegeben werden, in denen das zu startende Programm nicht im Suchpfad Winmgmt.exe ist. Wenn der neu erstellte Prozess versucht, mit Objekten auf dem Zielsystem ohne die entsprechenden Zugriffsberechtigungen zu interagieren, wird er ohne Benachrichtigung an diese Methode beendet.

Aus Sicherheitsgründen kann die **Win32 \_ Process. Create** -Methode nicht zum Remote Starten eines interaktiven Prozesses verwendet werden.

Prozesse, die mit der **Win32 \_ Process. Create** -Methode erstellt wurden, sind durch das Auftrags Objekt beschränkt, es sei denn, das Flag **Create \_ breakoff \_ from \_ Job** ist angegeben. Weitere Informationen finden Sie unter [**Win32 \_ processstartup**](win32-processstartup.md) und [**\_ \_ providerhostquotaconfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).

## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel veranschaulicht, wie eine CIM-Methode aufgerufen wird, als ob es sich um eine Automatisierungs Methode von "errbemubject" handelt.


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



Das folgende perl-Beispiel veranschaulicht, wie Sie eine CIM-Methode aufrufen, als ob es sich um eine Automatisierungs Methode von "errbemubject" handelt.


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Im folgenden VBScript-Codebeispiel wird ein Notepad-Prozess auf dem lokalen Computer erstellt. [**Win32 \_ Processstartup**](win32-processstartup.md) wird verwendet, um die Prozesseinstellungen zu konfigurieren.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Prozess**](win32-process.md)
</dt> <dt>

[WMI-Tasks: Prozesse](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

