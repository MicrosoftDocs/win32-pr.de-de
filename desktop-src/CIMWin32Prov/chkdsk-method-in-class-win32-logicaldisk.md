---
description: Ruft den CHKDSK-Vorgang auf dem Datenträger auf.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: CHKDSK-Methode der Win32_LogicalDisk-Klasse
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
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127224"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>CHKDSK-Methode der Win32 \_ LogicalDisk-Klasse

Die **chkdsk** -Instanzmethode ruft den **chkdsk** -Vorgang auf dem Datenträger auf.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

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

*Fixerrors* \[ in\]
</dt> <dd>

Gibt an, was mit den auf dem Datenträger gefundenen Fehlern geschehen soll. **True** gibt an, dass Fehler korrigiert werden. Der Standardwert ist **FALSE**.

</dd> <dt>

*VigorousIndexCheck* \[ in\]
</dt> <dd>

**True** gibt an, dass eine weniger kräftige Überprüfung der Indexeinträge ausgeführt werden soll. Der Standardwert ist **FALSE**.

</dd> <dt>

*Skipfoldercycle* \[ in\]
</dt> <dd>

**True** gibt an, dass die Überprüfung des Ordner Überlaufs ausgelassen werden soll. Der Standardwert ist **true**.

</dd> <dt>

*ForceDismount* \[ in\]
</dt> <dd>

**True** gibt an, dass das Laufwerk vor der Überprüfung gezwungen werden muss, die Einbindung aufzuheben. Der Standardwert ist **FALSE**.

</dd> <dt>

*Recoverbadsektoren* \[ in\]
</dt> <dd>

**True** gibt an, dass die fehlerhaften Sektoren gefunden und die lesbaren Informationen aus diesen Sektoren wieder hergestellt werden sollten. Der Standardwert ist **FALSE**.

</dd> <dt>

*Oktorunatbootup* \[ in\]
</dt> <dd>

**True** gibt an, dass der **chkdsk** -Vorgang beim nächsten Startzeitpunkt ausgeführt werden soll, falls der Vorgang nicht ausgeführt werden konnte, weil der Datenträger zum Zeitpunkt des Aufrufs dieser Methode gesperrt ist. Der Standardwert ist **FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung den Wert 0 (null) zurück. Andere Werte sind in der folgenden Liste aufgeführt. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg-Chkdsk abgeschlossen**
</dt> <dd>

0

Erfolg- [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) abgeschlossen

</dd> <dt>

**Erfolg: gesperrt und chkdsk geplant beim Neustart**
</dt> <dd>

1

</dd> <dt>

**Fehler-unbekanntes Dateisystem**
</dt> <dd>

2

</dd> <dt>

**Fehler-unbekannter Fehler.**
</dt> <dd>

3

</dd> <dt>

**Fehler: nicht unterstütztes Datei System**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode gilt nur für die Instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen. Sie ist nicht auf zugeordnete logische Laufwerke anwendbar.

## <a name="examples"></a>Beispiele

Das in einem Server-PowerShell-Codebeispiel festgelegte geändertes[chkdsk-Bit](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) untersucht das Remote System und gibt true oder false zurück, wenn das chkdsk/f-Flag festgelegt wurde.

Das PowerShell-Codebeispiel für die [Remote](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) Überprüfung von Datenträgern startet oder plant den Scan Datenträger

Im folgenden VBScript-Codebeispiel wird ChkDsk.exe für Laufwerk D auf einem Computer ausgeführt.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

