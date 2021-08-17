---
description: Die IXml2Dex-Schnittstelle speichert und lädt DirectShow Editing Services-Projektdateien (DES) in Extensible Markup Language (XML). Diese Schnittstelle stellt auch Methoden zum Lesen und Schreiben von DirectShow-Graphdateien (GRF) bereit.
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: IXml2Dex-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3bc12c2305a8b92110d4aa17522184e9a3c5ee83b60ccd5a989468fa0a8c6e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952389"
---
# <a name="ixml2dex-interface"></a>IXml2Dex-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IXml2Dex` Schnittstelle speichert und lädt [DirectShow Editing](directshow-editing-services.md) Services-Projektdateien (DES) in Extensible Markup Language (XML). Diese Schnittstelle stellt auch Methoden zum Lesen und Schreiben von DirectShow-Graphdateien (GRF) bereit.

## <a name="members"></a>Member

Die **IXml2Dex-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IXml2Dex** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IXml2Dex-Schnittstelle** verfügt über diese Methoden.



| Methode                                                      | Beschreibung                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | Nicht implementiert.<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | Nicht implementiert.<br/>                                                |
| [**Löschen**](ixml2dex-delete.md)                           | Nicht implementiert.<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | Nicht implementiert.<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | Nicht implementiert.<br/>                                                |
| [**Readxml**](ixml2dex-readxml.md)                         | Nicht implementiert.<br/>                                                |
| [**ReadXMLFile**](ixml2dex-readxmlfile.md)                 | Lädt eine XML-Projektdatei.<br/>                                      |
| [**Zurücksetzen**](ixml2dex-reset.md)                             | Nicht implementiert.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Schreibt ein Filterdiagramm in eine Datei im GRF-Format.<br/>                 |
| [**Writexml**](ixml2dex-writexml.md)                       | Übersetzt eine Zeitachse in eine XML-Zeichenfolge.<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | Übersetzt eine Zeitachse in XML und schreibt die XML-Daten in eine Datei.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Nicht implementiert.<br/>                                                |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4.0 oder höher<br/>                                               |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
