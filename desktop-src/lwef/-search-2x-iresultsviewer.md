---
title: IResultsViewer-Schnittstelle (WdsSharedIDL.h)
description: Macht Methoden und Eigenschaften für die Ergebnisansicht verfügbar.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- IResultsViewer-Schnittstelle – Legacy Windows Umgebungsfeatures
- IResultsViewer-Schnittstelle Legacy Windows Umgebungsfeatures , beschrieben
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1528f5d6da779e49836b75027845d40c76a2d948a9eb51e78b2addcefc75085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963770"
---
# <a name="iresultsviewer-interface"></a>IResultsViewer-Schnittstelle

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Macht Methoden und Eigenschaften für die Ergebnisansicht verfügbar.

## <a name="members"></a>Member

Die **IResultsViewer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultsViewer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IResultsViewer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GoBack**](-search-2x-iresultsviewer-goback.md)       | Nicht implementiert.<br/>                                                            |
| [**Goforward**](-search-2x-iresultsviewer-goforward.md) | Nicht implementiert.<br/>                                                            |
| [**Aktualisieren**](-search-2x-iresultsviewer-refresh.md)     | Nicht implementiert.<br/>                                                            |
| [**Beenden**](-search-2x-iresultsviewer-stop.md)           | Nicht implementiert.<br/>                                                            |
| [**Aktualisieren**](-search-2x-iresultsviewer-update.md)       | Wendet alle Abfrageänderungen an und navigiert in der Ansicht zum neuen Ergebnissatz.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IResultsViewer-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Inhalte**](-search-2x-iresultsviewer-contents.md)<br/>                   | Lesegeschützt<br/> | Diese Eigenschaft verfolgt den Typ des Inhalts nach, der in der Ergebnisansicht angezeigt wird. <br/>    |
| [**DisplayName**](-search-2x-iresultsviewer-displayname.md)<br/>             | Schreibgeschützt<br/>  | Lokalisierter Anzeigename des Typs.<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Lesegeschützt<br/> | Nicht implementiert.<br/>                                                                      |
| [**FilterType**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Lesen/Schreiben<br/> | Diese Eigenschaft gibt den Namen des vordefinierten Typs zum Filtern von Ergebnissen fest oder gibt diesen zurück.<br/> |
| [**Headerstyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Lesen/Schreiben<br/> | Der In der Ansicht angezeigte Headerstil.<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Lesegeschützt<br/> | Dadurch wird TRUE zurückgegeben, wenn die Sichtabfrage geändert wurde und aktualisiert werden muss. <br/>           |
| [**ItemStore**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Lesen/Schreiben<br/> | Diese Eigenschaft gibt den Namen des Speichers zum Filtern der Ergebnisse fest oder gibt diesen zurück.<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Lesen/Schreiben<br/> | Steuert den Anzeigemodus des Vorschaubereichs.<br/>                                             |
| [**PropertyFilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Lesegeschützt<br/> | Beim Aufrufen der Eigenschaftenfiltersammlung wird Folgendes zurückgerufen:<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Lesen/Schreiben<br/> | Ruft den aktuellen Abfragetext ab oder legt diese fest.<br/>                                                  |
| [**ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Lesegeschützt<br/> | Nicht implementiert.<br/>                                                                      |
| [**SortOrderProperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Lesen/Schreiben<br/> | Diese Eigenschaft wird die Reihenfolge der Spalten festlegen oder zurückgeben, nach der die Ergebnisse sortiert werden sollen. <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Lesen/Schreiben<br/> | Diese Eigenschaft wird die IndexColumn der Eigenschaft festlegen oder zurückgeben, nach der die Ergebnisse sortiert werden sollen. <br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methoden und Eigenschaften werden verwendet, um die angezeigten Informationen zu bearbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

