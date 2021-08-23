---
title: ResourceLocator-Objekt (WSManDisp.h)
description: Gibt den Pfad zu einer Ressource an. Sie können ein ResourceLocator-Objekt anstelle eines Ressourcen-URI in Sitzungsobjektvorgängen wie Session.Get, Session.Put oder Session.Enumerate verwenden.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- ResourceLocator-Objekt Windows Remoteverwaltung
- ResourceLocator-Objekt Windows Remoteverwaltung , beschrieben
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
ms.openlocfilehash: 26d3287c02949326b672f550271ba3472e6cb16abb6748efb4a80de425c40e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642870"
---
# <a name="resourcelocator-object"></a>ResourceLocator-Objekt

Ein -Objekt, das den Pfad zu einer Ressource liefert. Sie können ein **ResourceLocator-Objekt** anstelle eines [*Ressourcen-URI*](windows-remote-management-glossary.md) in Sitzungsobjektvorgängen wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate verwenden.**](session-enumerate.md) [](session.md)

Dieses Objekt ermöglicht Ihnen:

-   Fügen Sie einen oder mehrere [*Selektoren hinzu,*](windows-remote-management-glossary.md) die eine bestimmte Instanz einer Ressource identifizieren. Dies ist identisch mit der Bereitstellung eines Schlüsselwerts im Ressourcen-URI für eine Ressource, die Schlüssel verwendet. Weitere Informationen finden Sie unter [**ResourceLocator.AddSelector**](resourcelocator-addselector.md). Sie können einen ähnlichen Vorgang mithilfe des *Filterparameters* in einem Aufruf von [**Session.Enumerate tun.**](session-enumerate.md)
-   Geben Sie einen [*Fragmentpfad*](windows-remote-management-glossary.md) und einen Dialekt an, um nur eine Eigenschaft einer Ressource zu erhalten. Sie können auch eines oder alle Elemente einer Arrayeigenschaft angeben, indem Sie den Arrayindex angeben. Weitere Informationen finden Sie unter [**ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).
-   Fügen Sie eine oder mehrere [*Optionen hinzu,*](windows-remote-management-glossary.md) die eine Datenquelle möglicherweise benötigt, um eine Anforderung zu verarbeiten. Weitere Informationen finden Sie unter [**ResourceLocator.AddOption**](resourcelocator-addoption.md).

Weitere Informationen finden Sie unter [Abfragen für bestimmte Instanzen einer Ressource.](querying-for-specific-instances-of-a-resource.md)

## <a name="members"></a>Member

Das **ResourceLocator-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **ResourceLocator-Objekt** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddOption**](resourcelocator-addoption.md)           | Fügt zusätzliche Daten hinzu, die zum Verarbeiten der Anforderung erforderlich sind.<br/>                                                                   |
| [**AddSelector**](resourcelocator-addselector.md)       | Fügt dem **ResourceLocator-Objekt einen Selektor** hinzu. [](windows-remote-management-glossary.md)<br/>     |
| [**ClearOptions**](resourcelocator-clearoptions.md)     | Entfernt alle Optionen [*aus*](windows-remote-management-glossary.md) dem **ResourceLocator-Objekt.**<br/> |
| [**ClearSelectors**](resourcelocator-clearselectors.md) | Entfernt alle Selektoren aus einem **ResourceLocator-Objekt.**<br/>                                                            |



 

### <a name="properties"></a>Eigenschaften

Das **ResourceLocator-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                          | Zugriffstyp           | Beschreibung                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FragmentDialect**](resourcelocator-fragmentdialect.md)<br/>             | Lesen/Schreiben<br/> | Ruft den Sprachdialekt für ein Ressourcenfragment ab oder [*legt*](windows-remote-management-glossary.md) [*diese fest.*](windows-remote-management-glossary.md)<br/> |
| [**FragmentPath**](resourcelocator-fragmentpath.md)<br/>                   | Lesen/Schreiben<br/> | Ruft den Pfad für ein Ressourcenfragment oder eine Eigenschaft [*ab*](windows-remote-management-glossary.md) [*oder*](windows-remote-management-glossary.md) legt diesen fest.<br/> |
| [**MustUnderstandOptions**](resourcelocator-mustunderstandoptions.md)<br/> | Lesen/Schreiben<br/> | Ruft den **MustUnderstandOptions-Wert für das** **ResourceLocator-Objekt** ab oder legt den Wert fest.<br/>                                                                                                         |
| [**ResourceURI**](resourcelocator-resourceuri.md)<br/>                     | Lesen/Schreiben<br/> | Ruft den [*Ressourcen-URI*](windows-remote-management-glossary.md) in einem **ResourceLocator-Objekt** ab oder legt diese fest.<br/>                                                          |



 

## <a name="remarks"></a>Hinweise

Das **ResourceLocator-Objekt** entspricht der **IWSManResourceLocator-Schnittstelle.**

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden die **NumberOfLogicalProcessors-** und **NumberOfCores-Eigenschaften** von einer bestimmten Instanz des [**Win32-Prozessors \_ erhalten.**](/windows/desktop/CIMWin32Prov/win32-processor)


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinRM-Skripterstellungs-API](winrm-scripting-api.md)
</dt> </dl>

 

