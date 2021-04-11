---
description: Die Win32ShutdownTracker-Methode bietet die gleichen Optionen für das Herunterfahren, die von der Win32Shutdown-Methode im Win32- \_ OperatingSystem unterstützt werden, Sie ermöglicht Ihnen aber auch das Angeben von Kommentaren, den Grund für das Herunterfahren oder ein Timeout.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Win32ShutdownTracker-Methode der Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126073"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Win32ShutdownTracker-Methode der Win32 \_ OperatingSystem-Klasse

Die **Win32ShutdownTracker** -Methode bietet die gleichen Optionen für das Herunterfahren, die von der [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) -Methode im [**Win32- \_ OperatingSystem**](win32-operatingsystem.md)unterstützt werden, Sie ermöglicht Ihnen aber auch das Angeben von Kommentaren, den Grund für das Herunterfahren oder ein Timeout.

## <a name="syntax"></a>Syntax


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Timeout* \[ in\]
</dt> <dd>

Zeit in Sekunden, bevor das Herunterfahren stattfindet. Der Standardwert ist 0 (null).

</dd> <dt>

*Kommentar* \[ in\]
</dt> <dd>

Die Meldung, die im Dialogfeld zum Herunterfahren angezeigt wird, das auch als Kommentar im Ereignisprotokoll Eintrag gespeichert wird.

</dd> <dt>

*Reasoncode* \[ in\]
</dt> <dd>

Grund für das Initiieren des herunter Fahrens.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Bitzugeordneter Satz von Flags, um den Computer herunterzufahren. Fügen Sie dem Befehls Wert das Force-Flag (4) hinzu, um einen Befehl zu erzwingen. Durch die Verwendung von Force in Verbindung mit dem Herunterfahren oder Neustart auf einem Remote Computer wird sofort alles heruntergefahren (einschließlich WMI, com usw.) oder der Remote Computer neu gestartet. Dies führt zu einem unbestimmten Rückgabewert.

<dt>

0 (0x0)
</dt> <dd>

Abmelden

</dd> <dt>

4 (0x4)
</dt> <dd>

Erzwungene Protokollierung (0 + 4)

</dd> <dt>

1 (0x1)
</dt> <dd>

Shutdown

</dd> <dt>

5 (0x5)
</dt> <dd>

Erzwungenes Herunterfahren (1 + 4)

</dd> <dt>

2 (0x2)
</dt> <dd>

Reboot

</dd> <dt>

6 (0x6)
</dt> <dd>

Erzwungener Neustart (2 + 4)

</dd> <dt>

8 (0x8)
</dt> <dd>

Ausschalten

</dd> <dt>

12 (0xc)
</dt> <dd>

Erzwungene Stromversorgung (8 + 4)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](../wmisdk/wmi-error-constants.md) oder [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](../debug/system-error-codes.md).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Sonstige** (1 – 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Der Aufrufprozess muss über die Berechtigung für das Herunterfahren des **\_ \_ namens** verfügen.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird beschrieben, wie **Win32ShutdownTracker** aufgerufen wird.


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
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

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
