---
description: Win32Shutdown &\# 8194; Die WMI-Klassenmethode stellt den vollständigen Satz von Optionen zum Herunterfahren zur Verfügung, die von Win32-Betriebssystemen unterstützt werden. Dazu gehören Abmelden, Herunterfahren, Neustart und Erzwingen einer Abmelde-, Herunterfahren- oder Neustartfunktion.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Win32Shutdown-Methode der Win32_OperatingSystem Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 86c09f09fe25528f5a5a8bcfbde4a0749c35577dd6928de625bc2ff3ae3f5fd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079564"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a>Win32Shutdown-Methode der Win32 \_ OperatingSystem-Klasse

Die   [WMI-Klassenmethode](../wmisdk/retrieving-a-class.md) **Win32Shutdown** bietet alle Optionen zum Herunterfahren, die von Win32-Betriebssystemen unterstützt werden. Dazu gehören Abmelden, Herunterfahren, Neustart und Erzwingen einer Abmelde-, Herunterfahren- oder Neustartfunktion.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](../wmisdk/calling-a-method.md)

## <a name="syntax"></a>Syntax


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Bitmap-Flags zum Herunterfahren des Computers. Um einen Befehl zu erzwingen, fügen Sie dem Befehlswert das Flag Erzwingen (4) hinzu. Wenn Sie "Erzwingen" in Verbindung mit dem Herunterfahren oder Neustarten auf einem Remotecomputer verwenden, wird sofort alles heruntergefahren (einschließlich WMI, COM und so weiter), oder der Remotecomputer wird neu gestartet. Dies führt zu einem unbestimmten Rückgabewert.

<dt>

0 (0x0)
</dt> <dd>

**Abmelden:** Protokolliert den Benutzer vom Computer. Die Abmeldefunktion beendet alle Prozesse, die dem Sicherheitskontext des Prozesses zugeordnet sind, der die Exitfunktion aufgerufen hat, protokolliert den aktuellen Benutzer aus dem System und zeigt das Anmeldedialogfeld an.

</dd> <dt>

4 (0x4)
</dt> <dd>

**Erzwungene Abmeldebenachrichtigung (0 + 4): Protokolliert** den Benutzer sofort vom Computer und benachrichtigt Anwendungen nicht darüber, dass die Anmeldesitzung beendet wird. Dies kann zu einem Datenverlust führen.

</dd> <dt>

1 (0x1)
</dt> <dd>

**Herunterfahren:** Der Computer wird an einem Punkt heruntergefahren, an dem das Ausschalten sicher ist. (Alle Dateipuffer werden auf den Datenträger geleert, und alle ausgeführten Prozesse werden beendet.) Benutzern wird die Meldung angezeigt. `It is now safe to turn off your computer.`

Während des Herunterfahrens sendet das System eine Meldung an jede ausgeführte Anwendung. Die Anwendungen führen alle Bereinigungen durch, während die Nachricht verarbeitet wird, und geben True zurück, um anzugeben, dass sie beendet werden können.

</dd> <dt>

5 (0x5)
</dt> <dd>

**Erzwungenes Herunterfahren (1 + 4): Herunterfahren** des Computers bis zu einem Punkt, an dem es sicher ist, die Stromversorgung ausgeschaltet zu werden. (Alle Dateipuffer werden auf den Datenträger geleert, und alle ausgeführten Prozesse werden beendet.) Benutzern wird die Meldung angezeigt.` It is now safe to turn off your computer.`

Wenn der Erzwungenes Herunterfahren verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren. Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remotecomputer ausführen.

</dd> <dt>

2 (0x2)
</dt> <dd>

**Neustart:** Wird heruntergefahren und startet den Computer dann neu.

</dd> <dt>

6 (0x6)
</dt> <dd>

**Erzwungener Neustart (2 + 4):** Wird heruntergefahren und startet den Computer dann neu.

Wenn der erzwungene Neustart verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren. Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remotecomputer ausführen.

</dd> <dt>

8 (0x8)
</dt> <dd>

**Ausschalten:** Schaltet den Computer herunter und schaltet die Stromversorgung aus (sofern dies vom genannten Computer unterstützt wird).

</dd> <dt>

12 (0xC)
</dt> <dd>

**Erzwungenes Ausschalten (8 + 4): Schaltet** den Computer herunter und schaltet die Stromversorgung aus (sofern vom genannten Computer unterstützt).

Wenn der erzwungene Ausschalten-Ansatz verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren. Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remotecomputer ausführen.

</dd> </dl> </dd> <dt>

*Reserviert* \[ In\]
</dt> <dd>

Eine Möglichkeit, **Win32Shutdown zu erweitern.** Derzeit wird der *Reserved-Parameter* ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt null (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](../wmisdk/wmi-error-constants.md) oder [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](../debug/system-error-codes.md).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Andere** (1–4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Für eine effizientere Verwaltung von Computern in einer Organisation benötigen Administratoren die Möglichkeit, einen Computer remote herunter- oder neu zu starten oder einen Benutzer remote abzumelden. Durch die Möglichkeit, diese Aufgaben auszuführen, können Administratoren Software installieren, Computereinstellungen neu konfigurieren, Computer aus dem Netzwerk entfernen und andere Aufgaben ausführen, ohne jeden Computer manuell herunterfahren oder neu starten zu müssen.

Um beispielsweise ein Netzwerkupgrade durchzuführen, müssen Sie möglicherweise alle Computer herunterfahren, die in einem bestimmten Netzwerksegment ausgeführt werden. Um ein Upgrade Gruppenrichtlinie erzwingen, müssen Sie Benutzer von ihren Computern abmelden. Wenn ein Computer virus an einer beliebigen Stelle in Ihrer Organisation vorhanden ist, sollten Sie so viele Computer wie möglich herunterfahren, bevor der Virus eine Möglichkeit hat, sich zu verteilen. Die Möglichkeit, Computer herunter- und neu zu starten und Benutzer programmgesteuert und nicht manuell abzumelden, kann ein enormer Zeitsparer sein.

Der aufrufende Prozess muss über die SE **\_ SHUTDOWN NAME \_ verfügen.**

Die [**Win32ShutdownTracker-Methode**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) bietet denselben Satz von Herunterfahrensoptionen, die von der **Win32Shutdown-Methode** in [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) unterstützt werden, ermöglicht ihnen aber auch das Angeben von Kommentaren, eines Grunds für das Herunterfahren oder eines Timeouts.

Die Win32Shutdown-Methode verfügt nicht über einen Parameter zum Sperren einer Arbeitsstation, und der Benutzer ist angemeldet. Arbeitsstationen können jedoch mithilfe des folgenden Befehls über die Befehlszeile gesperrt werden:

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a>Beispiele

Das VBScript-Beispiel Abmelden, Neustarten oder Herunterfahren mehrerer Computer im TechNet-Katalog verwendet Win32Shutdown zum Abmelden, [Herunterfahren,](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) Neustarten oder Ausschalten (je nach Auswahl) der im Serverarray aufgeführten Computer.

Das [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell-Beispiel im TechNet-Katalog enthält eine Methode, die Win32Shutdown auf einem Remotecomputer aufruft.

Im folgenden PowerShell-Beispiel wird die Win32Shutdown-Methode zum Herunterfahren des angegebenen Computers verwendet.


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



Im folgenden PowerShell-Codebeispiel wird das Cmdlet EnableAllPrivileges aus get-wmiobject verwendet, um die richtigen Ergebnisse zu erzielen.


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



Im folgenden VB.NET-Beispielcode wird die Shutdown-Methode verwendet, um ein System neu zu starten oder abzumelden.


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[**\_Win32-Betriebssystem**](win32-operatingsystem.md)
</dt> <dt>

[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[WMI-Aufgaben: Desktopverwaltung](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
