---
description: Die Win32Shutdown-&\# 8194; Die WMI-Klassenmethode bietet alle Optionen für das Herunterfahren, die von Win32-Betriebssystemen unterstützt werden. Hierzu gehören das Abmelden, das Herunterfahren, das Neustarten und das Erzwingen einer Abmeldung, eines herunter Fahrens oder eines Neustarts.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Win32Shutdown-Methode der Win32_OperatingSystem-Klasse
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
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861571"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a>Win32Shutdown-Methode der Win32 \_ OperatingSystem-Klasse

Die **Win32Shutdown** -   [WMI-Klassen](../wmisdk/retrieving-a-class.md) Methode bietet alle Optionen für das Herunterfahren, die von Win32-Betriebssystemen unterstützt werden. Hierzu gehören das Abmelden, das Herunterfahren, das Neustarten und das Erzwingen einer Abmeldung, eines herunter Fahrens oder eines Neustarts.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](../wmisdk/calling-a-method.md).

## <a name="syntax"></a>Syntax


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Bitzugeordneter Satz von Flags, um den Computer herunterzufahren. Fügen Sie dem Befehls Wert das Force-Flag (4) hinzu, um einen Befehl zu erzwingen. Durch die Verwendung von Force in Verbindung mit dem Herunterfahren oder Neustart auf einem Remote Computer wird sofort alles heruntergefahren (einschließlich WMI, com usw.) oder der Remote Computer neu gestartet. Dies führt zu einem unbestimmten Rückgabewert.

<dt>

0 (0x0)
</dt> <dd>

**Abmelden** : protokolliert den Benutzer vom Computer. Beim Abmelden werden alle Prozesse angehalten, die dem Sicherheitskontext des Prozesses zugeordnet sind, der die Funktion Exit aufgerufen hat, der aktuelle Benutzer wird vom System protokolliert und das Anmelde Dialogfeld angezeigt.

</dd> <dt>

4 (0x4)
</dt> <dd>

**Erzwungene Abmeldung (0 + 4)** : der Benutzer wird vom Computer sofort protokolliert, und die Anwendung wird nicht benachrichtigt, dass die Anmelde Sitzung beendet wird. Dies kann zu einem Datenverlust führen.

</dd> <dt>

1 (0x1)
</dt> <dd>

**Herunter** fahren: der Computer wird an einen Punkt heruntergefahren, an dem die Stromversorgung deaktiviert werden kann. (Alle Datei Puffer werden auf den Datenträger geleert, und alle ausgelaufenden Prozesse werden beendet.) Benutzern wird die Meldung angezeigt. `It is now safe to turn off your computer.`

Während des herunter Fahrens sendet das System eine Meldung an jede laufende Anwendung. Die Anwendungen führen bei der Verarbeitung der Nachricht alle Bereinigungs Vorgänge aus und geben true zurück, um anzugeben, dass Sie beendet werden können.

</dd> <dt>

5 (0x5)
</dt> <dd>

**Erzwungenes Herunterfahren (1 + 4)** : fährt den Computer an einen Punkt herunter, an dem die Stromversorgung deaktiviert werden kann. (Alle Datei Puffer werden auf den Datenträger geleert, und alle ausgelaufenden Prozesse werden beendet.) Benutzern wird die Meldung angezeigt.` It is now safe to turn off your computer.`

Wenn das erzwungene Herunterfahren verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren. Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remote Computer ausführen.

</dd> <dt>

2 (0x2)
</dt> <dd>

**Neustart** : der Computer wird heruntergefahren, und der Computer wird neu gestartet.

</dd> <dt>

6 (0x6)
</dt> <dd>

**Erzwungener Neustart (2 + 4)** : der Computer wird heruntergefahren, und der Computer wird neu gestartet.

Wenn der erzwungene Neustart Ansatz verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren. Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remote Computer ausführen.

</dd> <dt>

8 (0x8)
</dt> <dd>

**Ausschalten** : schaltet den Computer herunter und schaltet die Stromversorgung aus (sofern vom betreffenden Computer unterstützt).

</dd> <dt>

12 (0xc)
</dt> <dd>

**Erzwungene Stromversorgung (8 + 4)** : der Computer wird heruntergefahren, und die Leistung wird ausgeschaltet (sofern vom betreffenden Computer unterstützt).

Wenn die erzwungene Stromversorgung verwendet wird, werden alle Dienste, einschließlich WMI, sofort heruntergefahren. Aus diesem Grund können Sie keinen Rückgabewert erhalten, wenn Sie das Skript auf einem Remote Computer ausführen.

</dd> </dl> </dd> <dt>

*Reserviert* \[ in\]
</dt> <dd>

Eine Möglichkeit, **Win32Shutdown** zu erweitern. Derzeit wird der *reservierte* Parameter ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](../wmisdk/wmi-error-constants.md) oder [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](../debug/system-error-codes.md).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Sonstige** (1 – 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Zur effizienteren Verwaltung von Computern in einer Organisation benötigen Administratoren die Möglichkeit, einen Computer Remote herunterzufahren oder neu zu starten oder einen Benutzer Remote abzumelden. Durch die Möglichkeit, diese Aufgaben auszuführen, können Administratoren Software installieren, Computereinstellungen neu konfigurieren, Computer aus dem Netzwerk entfernen und andere Tasks ausführen, ohne jeden Computer manuell herunterfahren oder neu starten zu müssen.

Wenn Sie z. b. ein Netzwerk Upgrade durchführen möchten, müssen Sie möglicherweise alle Computer Herunterfahren, die in einem bestimmten Netzwerksegment ausgeführt werden. Um ein Gruppenrichtlinie Upgrade zu erzwingen, müssen Sie Benutzer auf ihren Computern protokollieren. Wenn ein Computervirus an einer beliebigen Stelle in Ihrer Organisation vorhanden ist, empfiehlt es sich, so viele Computer wie möglich herunterzufahren, bevor der Virus verteilt werden kann. Die Möglichkeit, Computer herunterzufahren und neu zu starten und Benutzerprogramm gesteuert anstelle von manuell abzumelden, kann ein enormer Zeitersparnis sein.

Der Aufrufprozess muss über die Berechtigung für das Herunterfahren des **\_ \_ namens** verfügen.

Die [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) -Methode bietet denselben Satz von Optionen für das Herunterfahren, die von der **Win32Shutdown** -Methode im [**Win32- \_ OperatingSystem**](win32-operatingsystem.md) unterstützt werden. Sie ermöglicht Ihnen aber auch das Angeben von Kommentaren, den Grund für das Herunterfahren oder ein Timeout.

Die Win32Shutdown-Methode verfügt über keinen Parameter zum Sperren einer Arbeitsstation, sodass der Benutzer angemeldet ist. Arbeitsstationen können jedoch mit dem folgenden Befehl über die Befehlszeile gesperrt werden:

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a>Beispiele

Das VBScript-Beispiel zum [Abmelden, Neustarten oder Herunterfahren von mehreren Computern](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) in der TechNet Gallery verwendet Win32Shutdown, um die im Server Array aufgeführten Computer abzumelden, herunterzufahren, neu zu starten oder auszuschalten.

Das [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell-Beispiel in der TechNet Gallery enthält eine Methode, mit der Win32Shutdown auf einem Remote Computer aufgerufen wird.

Im folgenden PowerShell-Beispiel wird die Win32Shutdown-Methode verwendet, um den angegebenen Computer herunterzufahren.


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



Im folgenden PowerShell-Codebeispiel wird das enableallprivileges-Cmdlet aus dem Get-WMIObject-Cmdlet verwendet, um die richtigen Privilegien zu erzielen.


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



Der folgende VB.NET-Beispielcode verwendet die Shutdown-Methode, um ein System neu zu starten oder abzumelden.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[**Win32- \_ OperatingSystem**](win32-operatingsystem.md)
</dt> <dt>

[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[WMI-Tasks: Desktop Verwaltung](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
