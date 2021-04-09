---
title: Enumeratorobjekt (WSManDisp. h)
description: Stellt einen Stream von Ergebnissen dar, die von Vorgängen zurückgegeben werden, z. b. ein Pull
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- EnumeratorobjektWindows-Remoteverwaltung
- EnumeratorobjektWindows-Remoteverwaltung, beschrieben
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
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040926"
---
# <a name="enumerator-object"></a>Enumerator-Objekt

Stellt einen Stream von Ergebnissen dar, die von Vorgängen zurückgegeben werden, z. b. ein Pull Beispielsweise gibt die [**Session. Enumerate**](session-enumerate.md) -Methode mehrere Ergebnisse zurück.

## <a name="members"></a>Member

Das **Enumeratorobjekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Enumeratorobjekt** verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**"ReadItem"**](enumerator-readitem.md) | Ruft ein Element aus der Ressource ab und gibt eine XML-Darstellung des Elements zurück.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Enumeratorobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                     | BESCHREIBUNG                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Atendof-Stream**](enumerator-atendofstream.md)<br/> | Ruft einen booleschen Wert ab, der angibt, ob in der Auflistung weitere Elemente vorhanden sind.<br/> |
| [**Fehler**](enumerator-error.md)<br/>                 | Ruft eine XML-Darstellung zusätzlicher Fehlerinformationen ab.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum Starten einer Enumeration [**Session. Enumerate**](session-enumerate.md). Verwenden Sie zum Ausführen eines [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) -Vorgangs, der weiterhin Elemente in der-Enumeration liest, [**Enumerator. ReadItem**](enumerator-readitem.md).

Das **Enumeratorobjekt** entspricht der [**iwsmanenumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) -Schnittstelle.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden alle Datenträger auf einem Remote Computer aufgelistet, die durch den voll qualifizierten Domänen Namen (Servername.Domain.com) angegeben werden. Die DisplayOutput-Unterroutine formatiert die Datenausgabe auf die gleiche Weise wie das WinRM. cmd-Tool.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinRM-Skript-API](winrm-scripting-api.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Skripterstellung in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





