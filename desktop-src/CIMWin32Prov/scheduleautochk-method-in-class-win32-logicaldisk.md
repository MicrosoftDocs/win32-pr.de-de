---
description: Plant das Ausführen von AUTOCHK auf dem Laufwerk, das durch den Win32 \_ LogicalDisk beim nächsten Neustart dargestellt wird, wenn das geänderte Bit festgelegt ist.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Scheduleautochk-Methode der Win32_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958267"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Scheduleautochk-Methode der Win32 \_ LogicalDisk-Klasse

Die **scheduleautochk** -Klassenmethode plant das Ausführen von AUTOCHK auf dem Laufwerk, das beim nächsten Neustart durch den [**Win32 \_ LogicalDisk**](win32-logicaldisk.md) dargestellt wird, wenn das geänderte Bit festgelegt ist.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LogicalDisk* \[ in\]
</dt> <dd>

Gibt die Liste der Laufwerke an, die beim nächsten Neustart für Autochk geplant werden sollen. Die Zeichen folgen Syntax besteht aus dem Laufwerk Buchstaben, gefolgt von einem Doppelpunkt für den logischen Datenträger, z. b. "C:".

> [!Note]  
> Überprüfen Sie immer die Gültigkeit der Laufwerk Buchstaben im *LogicalDisk* -Array, wenn die Daten aus einer unbekannten Quelle stammen, oder aus einer nicht vertrauenswürdigen Quelle.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und einen anderen Wert zurück, wenn ein anderer Fehler auftritt. Die Werte sind in der folgenden Liste aufgeführt. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Kein Fehler** (0)
</dt> <dt>

**Fehler: Remote Laufwerk** (1)
</dt> <dt>

**Fehler-** Wechsel Datenträger (2)
</dt> <dt>

**Fehler-Laufwerk nicht Stammverzeichnis** (3)
</dt> <dt>

**Fehler-Unbekanntes Laufwerk** (4)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode gilt nur für die Instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen. Diese Methode ist nicht auf zugeordnete logische Laufwerke anwendbar.

## <a name="examples"></a>Beispiele

Die folgenden VBScript-und PowerShell-Beispiele planen Autochk.exe bei der nächsten Neustarts des Computers auf Laufwerk C ausgeführt werden.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
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
</dt> </dl>

 

