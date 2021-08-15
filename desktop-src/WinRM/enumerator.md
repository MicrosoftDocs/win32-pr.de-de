---
title: Enumeratorobjekt (WSManDisp.h)
description: Stellt einen Datenstrom von Ergebnissen dar, die von Vorgängen zurückgegeben werden, z. B. ein Pullvorgang.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Enumeratorobjekt Windows Remoteverwaltung
- Enumeratorobjekt Windows Remoteverwaltung beschrieben
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83799c4c67ad0b0f7c1ad89c77c3abab5989f1231508757c47dfe4c1705d7e20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051828"
---
# <a name="enumerator-object"></a>Enumerator-Objekt

Stellt einen Datenstrom von Ergebnissen dar, die von Vorgängen zurückgegeben werden, z. B. ein Pullvorgang. Beispielsweise gibt die [**Session.Enumerate-Methode**](session-enumerate.md) mehrere Ergebnisse zurück.

## <a name="members"></a>Member

Das **Enumeratorobjekt** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Enumeratorobjekt** verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**Readitem**](enumerator-readitem.md) | Ruft ein Element aus der Ressource ab und gibt eine XML-Darstellung des Elements zurück.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Enumeratorobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                     | BESCHREIBUNG                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AtEndOfStream**](enumerator-atendofstream.md)<br/> | Ruft einen booleschen Wert ab, der angibt, ob mehr Elemente in der Auflistung vorhanden sind.<br/> |
| [**Fehler**](enumerator-error.md)<br/>                 | Ruft eine XML-Darstellung zusätzlicher Fehlerinformationen ab.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie [**Session.Enumerate,**](session-enumerate.md)um eine Enumeration zu starten. Verwenden Sie [**Enumerator.ReadItem,**](enumerator-readitem.md)um eine [*WS-Enumeration*](windows-remote-management-glossary.md)zu verwenden:[*Pullvorgang,*](windows-remote-management-glossary.md) der das Lesen von Elementen in der Enumeration fortsetzt.

Das **Enumeratorobjekt** entspricht der [**IWSManEnumerator-Schnittstelle.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden alle Datenträger auf einem Remotecomputer aufgeführt, die durch den vollqualifizierten Domänennamen (servername.domain.com) angegeben werden. Die DisplayOutput-Unterroutine formatiert die Datenausgabe auf die gleiche Weise wie das Tool WinRM.cmd.


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
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

[WinRM-Skript-API](winrm-scripting-api.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Skripterstellung in Windows Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





