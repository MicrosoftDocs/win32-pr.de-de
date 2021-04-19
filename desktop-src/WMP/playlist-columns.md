---
title: Wiedergabeliste. Spalten
description: Das Columns-Attribut definiert die Spalten, die im Wiedergabelisten Element angezeigt werden.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- Wiedergabeliste. Spalten (Fenster) Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366939"
---
# <a name="playlistcolumns"></a>Wiedergabeliste. Spalten

Das **Columns** -Attribut definiert die Spalten, die im **Wiedergabe** Listenelement angezeigt werden.

``` syntax
        elementID.columns
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** im folgenden Format:

DB \_ Name = Anzeige \_ Name; DB \_ Name = Anzeige \_ Name;

\_Der Anzeige Name ist der Wert, der im Spaltenheader des Wiedergabelisten Elements angezeigt wird, und DB \_ Name ist ein Wert aus der folgenden Tabelle. Beachten Sie, dass ein Wiedergabelisten Element ein Medien Element aus der Bibliothek oder einer CD sein kann, oder es kann sich um eine andere **Wiedergabeliste** handeln, die entweder von einem Benutzer erstellt oder von einer CD stammt. Einige Spalten sind nur mit bestimmten Wiedergabelisten Elementen gültig, wie in der Beschreibungs Spalte angegeben.



| Wert             | BESCHREIBUNG                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| Aufzunehmen             | Der Name des Albums. Wird nur für Medienelemente verwendet.                                                                      |
| Interpret            | Der Name des Künstlers. Wird nicht mit vom Benutzer erstellten Wiedergabelisten verwendet.                                                           |
| Autor            | Der Name des Künstlers.                                                                                                 |
| Bitrate           | Die Bitrate des Inhalts. Wird nur für Medienelemente aus der Bibliothek verwendet.                                               |
| Cdtrackaktivierte    | Gibt an, ob der CD-Track aktiviert ist. Wird nur für CD-Medienelemente verwendet.                                               |
| Überprüft           | Für die zukünftige Verwendung reserviert.                                                                                                |
| Copyright         | Das Copyright der Wiedergabeliste. Wird nicht für CD-Wiedergabelisten oder Medienelemente verwendet.                                               |
| CreationDate      | Das Datum und die Uhrzeit der Erstellung des Eintrags in der Bibliothek. Wird nur mit Elementen aus der Bibliothek verwendet.                     |
| Digitallysecure   | Gibt an, ob das Element mit Windows Media Rights Manager geschützt wird. Wird nur für Medienelemente aus der Bibliothek verwendet. |
| Duration          | Die Dauer des Medien Elements.                                                                                         |
| FileType          | Für die zukünftige Verwendung reserviert.                                                                                                |
| Genre             | Das Genre der Wiedergabeliste. Wird nicht mit Wiedergabelisten von CDs verwendet.                                                            |
| MediaAttribute    | Für die zukünftige Verwendung reserviert.                                                                                                |
| MediaType         | Der Typ des Medien Elements (Audiodatei oder Video).                                                                            |
| MetadataSource    | Die Quelle der Metadaten für diesen CD-Track (AMG, WindowsMedia.com usw.). Wird nur für CD-Medienelemente verwendet.         |
| ModifiedBy        | Für die zukünftige Verwendung reserviert.                                                                                                |
| Name              | Der Name der Wiedergabeliste.                                                                                               |
| Originalindex     | Falls zutreffend, der entsprechende CD-Track-Bezeichner. Wird nur für CD-Medienelemente verwendet.                                    |
| Playcount         | Gibt an, wie oft der Inhalt bis zum Ende wiedergegeben wurde. Wird nur für Medienelemente aus der Bibliothek verwendet.        |
| Playlistatutribute | Für die zukünftige Verwendung reserviert.                                                                                                |
| Rating            | Für die zukünftige Verwendung reserviert.                                                                                                |
| SourceURL         | Der Pfad oder die URL zum Inhalt. Wird nur für Medienelemente aus der Bibliothek verwendet.                                            |
| Status            | Der Kopier Status einer CD-Spur, die kopiert wird. Wird nur für CD-Medienelemente verwendet.                                           |
| Stil             | Für die zukünftige Verwendung reserviert.                                                                                                |
| INHALTSVERZEICHNIS               | Falls zutreffend, das entsprechende CD-Inhaltsverzeichnis. Wird nicht mit vom Benutzer erstellten Wiedergabelisten verwendet.                 |



 

## <a name="remarks"></a>Bemerkungen

Wenn eine der Spalten nicht in der Bibliothek vorhanden ist, wird Sie leer gelassen.

Es können maximal 31 Spalten angegeben werden.

Wenn Sie eine doppelte Spalte angeben, werden die Daten in der ersten Spalte linksbündig ausgerichtet, aber alle anderen doppelten Spalten werden rechtsbündig ausgerichtet. Wenn Sie z. b. über zwei Duration-Spalten verfügen, werden die Daten im ersten und rechtsbündig ausgerichtet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. columnsvisible**](playlist-columnsvisible.md)
</dt> </dl>

 

 





