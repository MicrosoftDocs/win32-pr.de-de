---
description: Die Win32ShutdownTracker-Methode bietet den gleichen Satz von Herunterfahroptionen, die von der Win32Shutdown-Methode in Win32 OperatingSystem unterstützt \_ werden. Sie können aber auch Kommentare, einen Grund für das Herunterfahren oder ein Timeout angeben.
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
ms.openlocfilehash: 58c83e90f5256b2b2abb681048678b7c3bb4df3e9c4f4cdade16cb9ea00c4e48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079524"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Win32ShutdownTracker-Methode der Win32 \_ OperatingSystem-Klasse

Die **Win32ShutdownTracker-Methode** stellt den gleichen Satz von Herunterfahroptionen bereit, die von der [**Win32Shutdown-Methode**](win32shutdown-method-in-class-win32-operatingsystem.md) im [**Win32-Betriebssystem \_**](win32-operatingsystem.md)unterstützt werden. Sie können aber auch Kommentare, einen Grund für das Herunterfahren oder ein Timeout angeben.

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

*Timeout* \[ In\]
</dt> <dd>

Zeit in Sekunden, bevor das Herunterfahren erfolgt. Der Standardwert ist 0 (null).

</dd> <dt>

*Kommentar* \[ In\]
</dt> <dd>

Meldung, die im Dialogfeld zum Herunterfahren angezeigt wird, das auch als Kommentar im Ereignisprotokolleintrag gespeichert wird.

</dd> <dt>

*ReasonCode* \[ In\]
</dt> <dd>

Grund für das Initiieren des Herunterfahrens.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Ein Bitmapsatz von Flags zum Herunterfahren des Computers. Um einen Befehl zu erzwingen, fügen Sie dem Befehlswert das Flag Force (4) hinzu. Wenn Sie Force in Verbindung mit Herunterfahren oder Neustart auf einem Remotecomputer verwenden, wird sofort alles heruntergefahren (einschließlich WMI, COM usw.), oder der Remotecomputer wird neu gestartet. Dies führt zu einem unbestimmten Rückgabewert.

<dt>

0 (0x0)
</dt> <dd>

Abmelden

</dd> <dt>

4 (0x4)
</dt> <dd>

Erzwungene Abmeldung (0 + 4)

</dd> <dt>

1 (0x1)
</dt> <dd>

Herunterfahren

</dd> <dt>

5 (0x5)
</dt> <dd>

Erzwungenes Herunterfahren (1 + 4)

</dd> <dt>

2 (0x2)
</dt> <dd>

Neustart

</dd> <dt>

6 (0x6)
</dt> <dd>

Erzwungener Neustart (2 + 4)

</dd> <dt>

8 (0x8)
</dt> <dd>

Ausschalten

</dd> <dt>

12 (0xC)
</dt> <dd>

Erzwungenes Ausschalten (8 + 4)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](../wmisdk/wmi-error-constants.md) oder [**WbemErrorEnum.**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](../debug/system-error-codes.md)

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Sonstiges** (1–4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Der aufrufende Prozess muss über die **berechtigung SE \_ SHUTDOWN \_ NAME** verfügen.

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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[**Win32 \_ OperatingSystem**](win32-operatingsystem.md)
</dt> <dt>

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
