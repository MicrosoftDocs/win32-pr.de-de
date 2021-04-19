---
description: Die IXml2Dex-Schnittstelle speichert und lädt DirectShow-Projektdateien (Bearbeitungs Dienste) in Extensible Markup Language (XML). Diese Schnittstelle stellt auch Methoden zum Lesen und Schreiben von DirectShow Graph-Dateien (. GRF) bereit.
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: IXml2Dex-Schnittstelle (qedit. h)
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
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361476"
---
# <a name="ixml2dex-interface"></a>IXml2Dex-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `IXml2Dex` -Schnittstelle speichert und lädt [DirectShow](directshow-editing-services.md) -Projektdateien (Bearbeitungs Dienste) in Extensible Markup Language (XML). Diese Schnittstelle stellt auch Methoden zum Lesen und Schreiben von DirectShow Graph-Dateien (. GRF) bereit.

## <a name="members"></a>Member

Die **IXml2Dex** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IXml2Dex** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IXml2Dex** -Schnittstelle verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Copyxml**](ixml2dex-copyxml.md)                         | Nicht implementiert.<br/>                                                |
| [**"Kreategraphfromfile"**](ixml2dex-creategraphfromfile.md) | Nicht implementiert.<br/>                                                |
| [**Lösch**](ixml2dex-delete.md)                           | Nicht implementiert.<br/>                                                |
| [**Pastexml**](ixml2dex-pastexml.md)                       | Nicht implementiert.<br/>                                                |
| [**"Pastexmlfile"**](ixml2dex-pastexmlfile.md)               | Nicht implementiert.<br/>                                                |
| [**ReadXml**](ixml2dex-readxml.md)                         | Nicht implementiert.<br/>                                                |
| [**"Infodatei"**](ixml2dex-readxmlfile.md)                 | Lädt eine XML-Projektdatei.<br/>                                      |
| [**Zurücksetzen**](ixml2dex-reset.md)                             | Nicht implementiert.<br/>                                                |
| [**Schreibgrffile**](ixml2dex-writegrffile.md)               | Schreibt ein Filter Diagramm in eine Datei im GRF-Format.<br/>                 |
| [**WriteXml**](ixml2dex-writexml.md)                       | Übersetzt eine Zeitachse in eine XML-Zeichenfolge.<br/>                         |
| [**"Write texmlfile"**](ixml2dex-writexmlfile.md)               | Übersetzt eine Zeitachse in XML und schreibt die XML-Daten in eine Datei.<br/> |
| [**Schreib texmlpart**](ixml2dex-writexmlpart.md)               | Nicht implementiert.<br/>                                                |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4,0 oder höher<br/>                                               |
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



 

 
