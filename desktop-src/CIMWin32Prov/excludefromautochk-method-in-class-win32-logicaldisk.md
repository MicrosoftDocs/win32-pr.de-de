---
description: Schließt Datenträger aus dem Autochk-Vorgang aus, der beim nächsten Neustart ausgeführt werden soll.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Excludefromautochk-Methode der Win32_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343594"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Excludefromautochk-Methode der Win32 \_ LogicalDisk-Klasse

Die **excludefromautochk** -Methode schließt Datenträger aus dem **Autochk** -Vorgang aus, der beim nächsten Neustart ausgeführt werden soll.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LogicalDisk* \[ in\]
</dt> <dd>

Liste der Laufwerke, die beim nächsten Neustart vom **Autochk** ausgeschlossen werden sollen. Die Zeichen folgen Syntax besteht aus dem Laufwerk Buchstaben, gefolgt von einem Doppelpunkt für den logischen Datenträger.

Beispiel: "C:"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert von 0 (null) zurück, wenn kein Fehler auftritt. Die Werte sind in der folgenden Liste aufgeführt. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg** (0)
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

Wenn nicht ausgeschlossen, wird **Autochk** auf dem Datenträger ausgeführt, wenn das änderungsbit für den Datenträger festgelegt ist. Beachten Sie, dass die Aufrufe zum Ausschließen von Datenträgern nicht kumulativ sind. Wenn ein-Rückruf zum Ausschließen einiger Datenträger durchgeführt wird, wird die neue Liste nicht zur Liste der Datenträger hinzugefügt, die bereits für den Ausschluss markiert sind. Die neue Liste der Datenträger überschreibt die vorherige Liste. Diese Methode gilt nur für die Instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen. Sie ist nicht auf zugeordnete logische Laufwerke anwendbar.

## <a name="examples"></a>Beispiele

Mit dem folgenden VBScript-Codebeispiel wird sichergestellt, dass Autochk.exe nicht für Laufwerk c ausgeführt wird, wenn der Computer das nächste Mal neu gestartet wird, selbst wenn das "Dirty Bit" auf Laufwerk c festgelegt wurde.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
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

 

