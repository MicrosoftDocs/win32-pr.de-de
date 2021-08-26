---
title: Session.Put-Methode (WSManDisp.h)
description: Aktualisieren Sie eine Ressource.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Put-Windows Remoteverwaltung
- Put-Methode Windows Remoteverwaltung, Sitzungsobjekt
- Sitzungsobjekt Windows Remoteverwaltung , Put-Methode
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c6fc6123470f6633b77a1c51234e751f3be04044c0ad100f0017849cb1ac42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898690"
---
# <a name="sessionput-method"></a>Session.Put-Methode

Aktualisieren Sie eine Ressource.

## <a name="syntax"></a>Syntax


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resourceUri* \[ In\]
</dt> <dd>

Der Bezeichner der zu aktualisierenden Ressource.

Dieser Parameter kann eines der In der folgenden Liste enthaltenen Elemente enthalten:

-   URI mit oder ohne [*Selektoren.*](windows-remote-management-glossary.md) Verwenden Sie beim **Aufrufen der Put-Methode** zum Abrufen einer WMI-Ressource die Schlüsseleigenschaft oder die Eigenschaften des Objekts. Im folgenden VBScript-Codebeispiel (Visual Basic Scripting Edition) wird der Schlüssel beispielsweise durch `Win32_Service?Name=winmgmt` angegeben.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   [**ResourceLocator-Objekt,**](resourcelocator.md) das Selektoren, [*Fragmente oder*](windows-remote-management-glossary.md)Optionen enthalten [*kann.*](windows-remote-management-glossary.md)
-   [*Referenz zum WS-Adressierungsendpunkt,*](windows-remote-management-glossary.md) wie im [WS-Management-Protokoll](ws-management-protocol.md) beschrieben. Weitere Informationen zur öffentlichen Spezifikation für das WS-Management finden Sie auf der [Indexseite für Verwaltungsspezifikationen.](/previous-versions/dotnet/articles/ms951267(v=msdn.10))

</dd> <dt>

*Ressource* \[ In\]
</dt> <dd>

Der aktualisierte Ressourceninhalt.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der XML-Code, der den aktualisierten Ressourceninhalt enthält.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden Daten in das [**Win32 \_ WMISetting-Objekt**](/windows/desktop/CIMWin32Prov/win32-wmisetting) geschrieben. Sie müssen alle Nicht-Arrayeigenschaften des -Objekts in den XML-Code des *Resource-Parameters* ein schließen. Die Reihenfolge der Eigenschaften ist nicht signifikant.


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> </dl>

 

