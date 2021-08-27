---
description: Die Leistung halbsynchroner Aufrufe ist in der Regel für die meisten Situationen ausreichend.
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: Festlegen der Sicherheit für einen asynchronen Aufruf in VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6ce457bde6e716864804d5ca62c33e31c8924ab0858bbb47f0dc345c9a3142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992360"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a>Festlegen der Sicherheit für einen asynchronen Aufruf in VBScript

Die Leistung [*halbsynchroner Aufrufe*](gloss-s.md) ist in der Regel für die meisten Situationen ausreichend. Asynchrone Aufrufe sind in der Regel keine empfohlene Vorgehensweise für Skripts. Wenn jedoch asynchrone Aufrufe ausgeführt werden müssen, kann ein Registrierungswert festgelegt werden, um WMI zu zwingen, Zugriffsüberprüfungen für asynchrone Aufrufe durchzuführen.


Der **Registrierungswert HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** steuert, ob WMI beim Zurückgeben von Daten für einen asynchronen Aufruf eine akzeptable Authentifizierungsebene überprüft. Der Rückruf kann auf einer niedrigeren Authentifizierungsebene als die des ursprünglichen asynchronen Aufrufs zurückgegeben werden. Standardmäßig ist dieser Wert auf 0 (null) festgelegt, sodass Rückrufe nicht überprüft werden. Um asynchrone Aufrufe bei der Skripterstellung zu schützen, müssen Sie den Registrierungsschlüssel auf 1 (eins) festlegen.

Skripts können die [**Methoden GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) und [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) des Registrierungsobjekts [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) verwenden, um die Einstellung des **Registrierungswerts UnsecAppAccessControlDefault** zu ändern. Weitere Informationen zu Authentifizierungs- und Identitätswechselebenen, die für den Remotezugriff erforderlich sind, finden Sie unter Herstellen einer Verbindung mit [WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

## <a name="to-set-asynchronous-call-security-in-vbscript"></a>So legen Sie die asynchrone Aufrufsicherheit in VBScript fest

Im folgenden VBScript-Codebeispiel wird gezeigt, wie Sie den Registrierungswert ändern, um die WMI-Authentifizierung von Rückrufen zu steuern.

Das Skript ändert den Wert von **UnsecAppAccessControlDefault** von 0 (null) in eins oder , wenn der Wert bereits festgelegt ist, von 1 in 0 (null). Null ist die Standardeinstellung auf einem neu installierten System. Nachdem das Flag festgelegt wurde, bleibt die Einstellung bei einem Neustart oder WMI-Neustart erhalten.

Das Skript verwendet ein [**SWbemMethod.InParameters-Objekt**](swbemmethod-inparameters.md) und [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) zum Aufrufen von [**StdRegProv.GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) und [**StdRegProv.SetStringValue.**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) Weitere Informationen zum Festlegen der Werte in einem **InParameters-Objekt** finden Sie unter [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Ein Beispiel für einen Registrierungsaufruf mit [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)finden Sie unter [**StdRegProv.SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).


```VB
' Registry key value in hex
Const hklm = &h800000002  
' Subkey string 
Const Subkey = "software\\microsoft\\wbem\\cimom" 
' Asynchronous access control
Const sValueName = "UnsecAppAccessControlDefault" 

' Obtain registry object
Set objReg = GetObject("winmgmts:root\default:StdRegProv") 

' Get the initial value of the asynchronous 
'   access control registry key
' Use an InParameters object to set up the 
'   parameters for the ExecMethod call
' For more information see Constructing InParameters Objects 
'   topic and SWbemObject.ExecMethod_ topic

Set InParams = objReg.methods_("GetStringValue").InParameters.SpawnInstance_
InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName

' Get return value from OutParameters object returned by ExecMethod. 
' For more information see Parsing OutParameters Objects topic

Set OutParams = objReg.Execmethod_("GetStringValue",InParams)

If (OutParams.ReturnValue <> 0) then
   Wscript.Echo "GetStringValue returned " & OutParams.ReturnValue
   Wscript.Quit 1
End If

Svalue = OutParams.sValue
If (sValue = 0) Then
   AccessControl = "WMI not performing asynch access control"
Else 
   AccessControl = "WMI performing asynch access control"  
End If
Wscript.Echo sValueName & " = " _
    & sValue & VBNewLine & AccessControl

' Change asynchronous access control registry key value
Set InParams = objReg.methods_("SetStringValue").InParameters.SpawnInstance_

InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName
InParams.sValue = sValue XOR 1

Set OutParams = objReg.ExecMethod_("SetStringValue",InParams)

If (OutParams.Returnvalue <> 0) Then
    Wscript.Echo "SetStringValue returned " & OutParams.Returnvalue
    Wscript.Quit 1
End If

Wscript.Echo SValueName & " changed to " & (sValue XOR 1)
```



 

 
