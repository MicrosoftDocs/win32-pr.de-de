---
title: Iresultsviewer-Schnittstelle (wdssharedidl. h)
description: Macht Methoden und Eigenschaften für die Ergebnis Ansicht verfügbar.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Iresultviewer-Oberfläche ältere Windows-Umgebungs Features
- Ältere Windows-Umgebungs Features der iresultviewer-Schnittstelle, beschrieben
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
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518125"
---
# <a name="iresultsviewer-interface"></a>Iresulensviewer-Schnittstelle

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Macht Methoden und Eigenschaften für die Ergebnis Ansicht verfügbar.

## <a name="members"></a>Member

Die **iresulensviewer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iresulzviewer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iresulzviewer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GoBack**](-search-2x-iresultsviewer-goback.md)       | Nicht implementiert.<br/>                                                            |
| [**GoForward**](-search-2x-iresultsviewer-goforward.md) | Nicht implementiert.<br/>                                                            |
| [**Aktualisieren**](-search-2x-iresultsviewer-refresh.md)     | Nicht implementiert.<br/>                                                            |
| [**Stop**](-search-2x-iresultsviewer-stop.md)           | Nicht implementiert.<br/>                                                            |
| [**Aktualisieren**](-search-2x-iresultsviewer-update.md)       | Wendet alle Abfrage Änderungen an und navigiert die Ansicht zum neuen Resultset.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **iresulensviewer** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Inhalte**](-search-2x-iresultsviewer-contents.md)<br/>                   | Lesegeschützt<br/> | Diese Eigenschaft verfolgt den Typ des Inhalts, der in der Ansicht Ergebnisse angezeigt wird. <br/>    |
| [**DisplayName**](-search-2x-iresultsviewer-displayname.md)<br/>             | Schreibgeschützt<br/>  | Lokalisierter Anzeige Name des Typs.<br/>                                                   |
| [**Enumselecteditems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Lesegeschützt<br/> | Nicht implementiert.<br/>                                                                      |
| [**Filter Type**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Lesen/Schreiben<br/> | Diese Eigenschaft legt den Namen des vorab bereitgestellten Typs fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.<br/> |
| [**HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Lesen/Schreiben<br/> | Der Header Stil, der in der Ansicht angezeigt wird.<br/>                                            |
| [**Isupdaten.**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Lesegeschützt<br/> | Dies gibt true zurück, wenn die Views-Abfrage geändert wurde und aktualisiert werden muss. <br/>           |
| [**ItemStore**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Lesen/Schreiben<br/> | Diese Eigenschaft legt den Namen des Stores fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Lesen/Schreiben<br/> | Steuert den Anzeigemodus des Vorschau Bereichs.<br/>                                             |
| [**Propertyfilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Lesegeschützt<br/> | Wenn Sie die Auflistung der Eigenschaften Filter aufrufen, wird Folgendes zurückgegeben:<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Lesen/Schreiben<br/> | Ruft den aktuellen Abfragetext ab oder legt ihn fest.<br/>                                                  |
| [**Resulstistyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Lesegeschützt<br/> | Nicht implementiert.<br/>                                                                      |
| [**Sortorienproperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Lesen/Schreiben<br/> | Diese Eigenschaft legt die Reihenfolge der Spalten fest, nach denen die Ergebnisse sortiert werden, oder gibt Sie zurück. <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Lesen/Schreiben<br/> | Diese Eigenschaft legt die indexcolumn der Eigenschaft fest, nach der die Ergebnisse sortiert werden, oder gibt Sie zurück. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methoden und Eigenschaften werden verwendet, um die angezeigten Informationen zu bearbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

