---
title: ResourceLocator-Objekt (WSManDisp. h)
description: Gibt den Pfad zu einer Ressource an. Sie können ein ResourceLocator-Objekt anstelle eines Ressourcen-URI in Sitzungs Objekt Vorgängen verwenden, z. b. "Session. Get", "Session. Put" oder "Session. Enumerate".
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- ResourceLocator-Objekt Windows-Remoteverwaltung
- ResourceLocator-Objekt Windows-Remoteverwaltung, beschrieben
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103078"
---
# <a name="resourcelocator-object"></a>ResourceLocator-Objekt

Ein-Objekt, das den Pfad zu einer Ressource bereitstellt. Sie können ein **ResourceLocator** -Objekt anstelle eines [*Ressourcen-URI*](windows-remote-management-glossary.md) in [**Sitzungs**](session.md) Objekt Vorgängen verwenden, z. b. " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)".

Mit diesem Objekt können Sie folgende Aktionen ausführen:

-   Fügen Sie mindestens einen [*Selektoren*](windows-remote-management-glossary.md) hinzu, der eine bestimmte Instanz einer Ressource identifiziert. Dies entspricht dem Angeben eines Schlüssel Werts im Ressourcen-URI für eine Ressource, die Schlüssel verwendet. Weitere Informationen finden Sie unter [**ResourceLocator. addselector**](resourcelocator-addselector.md). Sie können einen ähnlichen Vorgang ausführen, indem Sie den *Filter* -Parameter in einem Aufrufen von [**Session. Enumerate**](session-enumerate.md)verwenden.
-   Geben Sie einen [*Fragmentpfad*](windows-remote-management-glossary.md) und einen Dialekt an, um nur eine Eigenschaft einer Ressource zu erhalten. Sie können auch ein oder alle Elemente einer Array Eigenschaft angeben, indem Sie den Array Index bereitstellen. Weitere Informationen finden Sie unter [**ResourceLocator. fragmentpath**](resourcelocator-fragmentpath.md).
-   Fügen Sie eine oder mehrere [*Optionen*](windows-remote-management-glossary.md) hinzu, die eine Datenquelle möglicherweise benötigt, um eine Anforderung zu verarbeiten. Weitere Informationen finden Sie unter [**ResourceLocator. AddOption**](resourcelocator-addoption.md).

Weitere Informationen finden Sie unter [Abfragen für bestimmte Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md).

## <a name="members"></a>Member

Das **ResourceLocator** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **ResourceLocator** -Objekt verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddOption**](resourcelocator-addoption.md)           | Fügt zusätzliche Daten hinzu, die für die Verarbeitung der Anforderung erforderlich sind.<br/>                                                                   |
| [**Addselector**](resourcelocator-addselector.md)       | Fügt dem **ResourceLocator** -Objekt einen [*Selektor*](windows-remote-management-glossary.md) hinzu.<br/>     |
| [**Clearoptions**](resourcelocator-clearoptions.md)     | Entfernt alle [*Optionen*](windows-remote-management-glossary.md) aus dem **ResourceLocator** -Objekt.<br/> |
| [**Clearselectors**](resourcelocator-clearselectors.md) | Entfernt alle Selektoren aus einem **ResourceLocator** -Objekt.<br/>                                                            |



 

### <a name="properties"></a>Eigenschaften

Das **ResourceLocator** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                          | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fragmentdialekt**](resourcelocator-fragmentdialect.md)<br/>             | Lesen/Schreiben<br/> | Ruft den sprach Dialekt für ein [*Ressourcen*](windows-remote-management-glossary.md) [*Fragment*](windows-remote-management-glossary.md)ab oder legt ihn fest.<br/> |
| [**Fragmentpath**](resourcelocator-fragmentpath.md)<br/>                   | Lesen/Schreiben<br/> | Ruft den Pfad für ein [*Ressourcen*](windows-remote-management-glossary.md) [*Fragment*](windows-remote-management-glossary.md) oder eine Ressourcen Eigenschaft ab oder legt ihn fest.<br/> |
| [**Mustverständlicherweise-Optionen**](resourcelocator-mustunderstandoptions.md)<br/> | Lesen/Schreiben<br/> | Ruft den **mustverständlicherweise Options** -Wert für das **ResourceLocator** -Objekt ab oder legt ihn fest.<br/>                                                                                                         |
| [**ResourceURI**](resourcelocator-resourceuri.md)<br/>                     | Lesen/Schreiben<br/> | Ruft den Ressourcen- [*URI*](windows-remote-management-glossary.md) in einem **ResourceLocator** -Objekt ab oder legt ihn fest.<br/>                                                          |



 

## <a name="remarks"></a>Bemerkungen

Das **ResourceLocator** -Objekt entspricht der **iwsmanresourcelocator** -Schnittstelle.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden die Eigenschaften " **numoflogicalprocessor** " und " **numofcores** " von einer bestimmten Instanz des [**Win32- \_ Prozessors**](/windows/desktop/CIMWin32Prov/win32-processor)abgerufen.


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

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
</dt> </dl>

 

