---
title: Session. Put-Methode (WSManDisp. h)
description: Aktualisieren Sie eine Ressource.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Put-Methode Windows-Remoteverwaltung
- Put-Methode Windows-Remoteverwaltung, Session-Objekt
- Session-Objekt Windows-Remoteverwaltung, Put-Methode
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
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392057"
---
# <a name="sessionput-method"></a>Session. Put-Methode

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

*resourceUri* \[ in\]
</dt> <dd>

Der Bezeichner der zu aktualisierenden Ressource.

Dieser Parameter kann eines der-Elemente enthalten, die in der folgenden Liste enthalten sind:

-   URI mit oder ohne [*Selektoren*](windows-remote-management-glossary.md). Wenn Sie die **Put** -Methode aufrufen, um eine WMI-Ressource abzurufen, verwenden Sie die Schlüsseleigenschaft oder die Eigenschaften des Objekts. Beispielsweise wird im folgenden Visual Basic Scripting Edition Codebeispiel (VBScript) der Schlüssel durch angegeben `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   [**ResourceLocator**](resourcelocator.md) -Objekt, das Selektoren, [*Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.
-   Endpunkt Verweis der [*WS-Adressierung*](windows-remote-management-glossary.md) , wie im [WS-Management-Protokoll](ws-management-protocol.md) -Standard beschrieben. Weitere Informationen zur öffentlichen Spezifikation WS-Management Protokolls finden Sie unter [Verwaltungs Spezifikationen Index page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*Ressource* \[ in\]
</dt> <dd>

Der aktualisierte Ressourcen Inhalt.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der XML-Code, der den aktualisierten Ressourcen Inhalt enthält.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden Daten in das [**Win32- \_ wmisetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) -Objekt geschrieben. Sie müssen alle nicht-Array-Eigenschaften des-Objekts in der XML-Datei des *Ressourcen* Parameters einschließen. Die Reihenfolge der Eigenschaften ist nicht signifikant.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

