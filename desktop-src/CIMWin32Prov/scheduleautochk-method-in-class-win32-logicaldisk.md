---
description: Planen der Ausführung von Autochk auf dem Laufwerk, das vom logischen Win32-Datenträger beim nächsten Neustart dargestellt wird, wenn das \_ dirty-Bit festgelegt ist.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: ScheduleAutoChk-Methode der Win32_LogicalDisk-Klasse
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
ms.openlocfilehash: 7e4920bdded79a7f63cbe7beaf28a70837ad7a47c2b28a1e37d83208b4f4e6f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588190"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>ScheduleAutoChk-Methode der Win32 \_ LogicalDisk-Klasse

Die **ScheduleAutoChk-Klassenmethode** geplant die Ausführung von Autochk auf dem Laufwerk, das vom [**logischen \_ Win32-Datenträger**](win32-logicaldisk.md) beim nächsten Neustart dargestellt wird, wenn das dirty-Bit festgelegt ist.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LogicalDisk* \[ In\]
</dt> <dd>

Gibt die Liste der Laufwerke an, für die autochk beim nächsten Neustart geplant werden soll. Die Zeichenfolgensyntax besteht aus dem Laufwerkbuchstaben gefolgt von einem Doppelpunkt für den logischen Datenträger, z.B. "C:".

> [!Note]  
> Überprüfen Sie immer die Gültigkeit der Laufwerkbuchstaben im *LogicalDisk-Array,* wenn die Daten aus einer unbekannten Quelle oder einer Nicht vertrauenswürdigen Quelle stammen.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und bei Auftreten eines anderen Fehlers einen anderen Wert zurück. Werte sind in der folgenden Liste aufgeführt. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Kein Fehler** (0)
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

Diese Methode gilt nur für instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen. Diese Methode gilt nicht für zugeordnete logische Laufwerke.

## <a name="examples"></a>Beispiele

In den folgenden VBScript- und PowerShell-Beispielen wird Autochk.exe laufwerk C ausgeführt, wenn der Computer das nächste Mal neu gestartet wird.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> </dl>

 

