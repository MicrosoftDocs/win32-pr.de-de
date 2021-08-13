---
description: Schließt Datenträger aus dem Autochk-Vorgang aus, der beim nächsten Neustart ausgeführt werden soll.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: ExcludeFromAutochk-Methode der Win32_LogicalDisk-Klasse
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
ms.openlocfilehash: a37171c594cb3a51b131220bb604234bcae108fa025ea6343da99fdc998a7dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676128"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>ExcludeFromAutochk-Methode der Win32 \_ LogicalDisk-Klasse

Die **ExcludeFromAutochk-Methode** schließt Datenträger aus dem **autochk-Vorgang** aus, der beim nächsten Neustart ausgeführt werden soll.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LogicalDisk* \[ In\]
</dt> <dd>

Liste der Laufwerke, die beim nächsten Neustart von **autochk** ausgeschlossen werden sollen. Die Zeichenfolgensyntax besteht aus dem Laufwerkbuchstaben gefolgt von einem Doppelpunkt für den logischen Datenträger.

Beispiel: "C:"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn kein Fehler auftritt. Werte sind in der folgenden Liste aufgeführt. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Fehler: Remotelaufwerk** (1)
</dt> <dt>

**Fehler: Wechseldatenträger** (2)
</dt> <dt>

**Fehler: Laufwerk nicht Stammverzeichnis** (3)
</dt> <dt>

**Fehler: Unbekanntes Laufwerk** (4)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Wenn dies nicht ausgeschlossen ist, wird **autochk** auf dem Datenträger ausgeführt, wenn das geänderte Bit für den Datenträger festgelegt wird. Beachten Sie, dass die Aufrufe zum Ausschließen von Datenträgern nicht kumulativ sind. Wenn ein Aufruf zum Ausschließen einiger Datenträger erfolgt, wird die neue Liste nicht der Liste der Datenträger hinzugefügt, die bereits für den Ausschluss markiert sind. Die neue Liste der Datenträger überschreibt die vorherige Liste. Diese Methode gilt nur für die Instanzen eines logischen Datenträgers, die einen physischen Datenträger auf dem Computer darstellen. Sie gilt nicht für zugeordnete logische Laufwerke.

## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel stellt sicher, dass Autochk.exe nicht auf Laufwerk C ausgeführt wird, wenn der Computer das nächste Mal neu gestartet wird, auch wenn das "dirty bit" auf Laufwerk C festgelegt wurde.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

