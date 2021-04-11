---
description: Die GetOwner-&\# 8194; WMI-Klassenmethode Ruft den Benutzernamen und den Domänen Namen ab, unter dem der Prozess ausgeführt wird.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: GetOwner-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126482"
---
# <a name="getowner-method-of-the-win32_process-class"></a>GetOwner-Methode der Win32- \_ Prozess Klasse

Die **GetOwner** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode ruft den Benutzernamen und den Domänen Namen ab, unter dem der Prozess ausgeführt wird.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Benutzer* \[ vorgenommen\]
</dt> <dd>

Gibt den Benutzernamen des Besitzers dieses Prozesses zurück.

</dd> <dt>

*Domäne* \[ vorgenommen\]
</dt> <dd>

Gibt den Domänen Namen zurück, unter dem der Prozess ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

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

## <a name="examples"></a>Beispiele

[Die Monitor Prozess-CPU PCT nach Name mit Besitzer](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript-Beispiel erfasst die CPU-oder Prozessorauslastung in Prozent und sucht den Prozess Besitzer.

Das Beispiel abrufen [aller Server, auf denen eine Liste von Benutzern](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) bei PowerShell angemeldet ist WMI für den Besitzer aller explorer.exe Prozesse.

Im folgenden VBScript-Codebeispiel wird der Besitzer für jeden laufenden Prozess abgerufen.


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
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
</dt> </dl>

 

