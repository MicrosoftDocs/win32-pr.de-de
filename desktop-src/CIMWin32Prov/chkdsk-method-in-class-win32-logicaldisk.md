---
description: Ruft den chkdsk-Vorgang auf dem Datenträger auf.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Chkdsk-Methode der Win32_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24d7052cd7d36da8a9464cbbef142904a70f83767872dadf25fda2033fa66fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959109"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Chkdsk-Methode der Win32 \_ LogicalDisk-Klasse

Die **Chkdsk-Instanzmethode** ruft den **chkdsk-Vorgang** auf dem Datenträger auf.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FixErrors* \[ In\]
</dt> <dd>

Gibt an, was mit Fehlern auf dem Datenträger geschehen soll. True **gibt an,** dass Fehler behoben wurden. Der Standardwert ist **FALSE**.

</dd> <dt>

*1000000000* \[ In\]
</dt> <dd>

True **gibt an,** dass eine weniger starke Überprüfung von Indexeinträgen durchgeführt werden sollte. Der Standardwert ist **FALSE**.

</dd> <dt>

*SkipFolderCycle* \[ In\]
</dt> <dd>

True **gibt an,** dass die Überprüfung des Ordnerzyklus übersprungen werden sollte. Der Standardwert ist **true**.

</dd> <dt>

*ForceDismount* \[ In\]
</dt> <dd>

True **gibt an,** dass die Bereitstellung des Laufwerks vor der Überprüfung erzwungen werden sollte. Der Standardwert ist **FALSE**.

</dd> <dt>

*RecoverBadSectors* \[ In\]
</dt> <dd>

True **gibt an,** dass die fehlerhaften Sektoren gefunden und die lesbaren Informationen aus diesen Sektoren wiederhergestellt werden sollten. Der Standardwert ist **FALSE**.

</dd> <dt>

*OKToRunAtBootUp* \[ In\]
</dt> <dd>

True **gibt an,** dass der **chkdsk-Vorgang** beim nächsten Startvorgang ausgeführt werden sollte, falls der Vorgang nicht ausgeführt werden konnte, da der Datenträger zum Zeitpunkt des Aufrufens dieser Methode gesperrt ist. Der Standardwert ist **FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) zurück. Andere Werte sind in der folgenden Liste aufgeführt. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg– Chkdsk abgeschlossen**
</dt> <dd>

0

Erfolg – [**Chkdsk abgeschlossen**](chkdsk-method-in-class-win32-logicaldisk.md)

</dd> <dt>

**Erfolg: Gesperrt und chkdsk beim Neustart geplant**
</dt> <dd>

1

</dd> <dt>

**Fehler: Unbekanntes Dateisystem**
</dt> <dd>

2

</dd> <dt>

**Fehler: Unbekannter Fehler**
</dt> <dd>

3

</dd> <dt>

**Fehler: Nicht unterstütztes Dateisystem**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Methode gilt nur für instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen. Dies gilt nicht für zugeordnete logische Laufwerke.

## <a name="examples"></a>Beispiele

Das PowerShell-Codebeispiel Is CHKDSK Dirty Bit Set on a server (Is[CHKDSK Dirty Bit Set](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) auf einem Server) untersucht das Remotesystem und gibt true oder false zurück, wenn das Flag chkdsk /f festgelegt wurde.

Das [PowerShell-Codebeispiel](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) Remote scan disk startet oder startet scan disk (Datenträger überprüfen) remote.

Im folgenden VBScript-Codebeispiel werden ChkDsk.exe Laufwerk D auf einem Computer ausgeführt.


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

