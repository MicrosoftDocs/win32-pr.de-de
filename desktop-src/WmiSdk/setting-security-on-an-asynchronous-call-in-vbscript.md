---
description: Die Leistung von semisynchronen aufrufen ist in den meisten Situationen in der Regel ausreichend.
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: Festlegen der Sicherheit für einen asynchronen VBScript-Anrufe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 972947e0cb4f5d385e4d2d27b7c14298771ac4e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352336"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a>Festlegen der Sicherheit für einen asynchronen VBScript-Anrufe

Die Leistung von [*semisynchronen*](gloss-s.md) aufrufen ist in den meisten Situationen in der Regel ausreichend. Asynchrone Aufrufe sind in der Regel keine empfohlene Vorgehensweise für Skripts. Wenn jedoch asynchrone Aufrufe durchgeführt werden müssen, kann ein Registrierungs Wert festgelegt werden, um zu erzwingen, dass WMI Zugriffs Überprüfungen für asynchrone Aufrufe ausführt.


Der Registrierungs Wert " **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **unsecappaccesscontroldefault** " steuert, ob WMI bei der Rückgabe von Daten für einen asynchronen-Befehl eine akzeptable Authentifizierungs Ebene prüft. Der Rückruf kann auf einer niedrigeren Authentifizierungs Stufe zurückgegeben werden als der des ursprünglichen asynchronen Aufrufs. Standardmäßig ist dieser Wert auf 0 festgelegt, sodass Rückrufe nicht geprüft werden. Um asynchrone Aufrufe in der Skripterstellung zu sichern, müssen Sie den Registrierungsschlüssel auf 1 (eins) festlegen.

Skripts können die Methoden [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) und [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) des Registrierungs Objekts [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) verwenden, um die Einstellung des Registrierungs Werts **unsecappaccesscontroldefault** zu ändern. Weitere Informationen zu den für den Remote Zugriff erforderlichen Authentifizierungs-und Identitätswechsel Ebenen finden [Sie unter Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

## <a name="to-set-asynchronous-call-security-in-vbscript"></a>So legen Sie die Sicherheit für asynchrone Aufrufe in VBScript fest

Im folgenden VBScript-Codebeispiel wird gezeigt, wie Sie den Registrierungs Wert ändern, um die WMI-Authentifizierung von Rückrufen zu steuern.

Das Skript ändert den Wert von **unsecappaccesscontroldefault** von NULL in 1, oder wenn der Wert bereits festgelegt ist, von 1 auf 0. NULL ist die Standardeinstellung für ein neu installiertes System. Sobald das Flag festgelegt ist, wird die Einstellung über einen Neustart oder einen WMI-Neustart beibehalten.

Das Skript verwendet ein "WS [**bemmethod. InParameters**](swbemmethod-inparameters.md) "-Objekt und [**SWbemObject.Execmethod**](swbemobject-execmethod-.md) , um " [**StdRegProv. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) " und " [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)" aufzurufen. Weitere Informationen zum Festlegen der Werte in einem **InParameters** -Objekt finden Sie unter [Erstellen von inparameter-Objekten und Auswerten von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Ein Beispiel eines Registrierungs Aufrufes mithilfe von [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)finden Sie unter [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).


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



 

 
