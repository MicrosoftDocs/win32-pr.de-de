---
title: ID3-Tagunterstützung
description: ID3-Tagunterstützung
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- Windows Medienformat-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, ID3-Tags
- ID3-Tags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fd65ffadb952e9370af609e336c08fc07c9b96f50d09d95c78492bef2163db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703025"
---
# <a name="id3-tag-support"></a>ID3-Tagunterstützung

In der folgenden Tabelle sind alle Attribute aufgeführt, die ID3-Tags entsprechen. Wenn Sie die ID3-Tags als Attribute anstelle der Standardattributnamen verwenden möchten, fügen Sie dem Tagnamen das Präfix "ID3/" hinzu. Beispielsweise entspricht "ID3/TPE2" dem **Autor**.



| attribute                      | ID3v1.x | ID3v2.2 | ID3v2.3/v2.4 |
|--------------------------------|---------|---------|--------------|
| **Author**                     | Künstler  | TP1     | TPE1         |
| **Copyright**                  |         | Tcr     | TCOP         |
| **CopyrightURL**               |         | Wcp     | WCOP         |
| **Beschreibung**                | Kommentar | COM     | COMM         |
| **Dauer**                   |         | Tle     | TLEN         |
| **FileSize**                   |         |         | TSIZ         |
| **Titel**                      | Titel   | TT2     | HIER IST DER 2.         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/AlbumTitle**              | Album   | TAL     | TALB         |
| **WM/InterpretSortOrder**         |         |         | Tsop         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/Binary**                  |         | GEOGRAFISCH     | GEOB         |
| **WM/Kommentare**                |         | COM     | COMM         |
| **WM/Composer**                |         | TCM     | TCOM         |
| **WM/Enumer**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | HIER IST DER 1.         |
| **WM/EncodedBy**               |         | Zehn     | TENC         |
| **WM/EncodingSettings**        |         | Tss     | TSSE         |
| **WM/EncodingTime**            |         |         | TDEN         |
| **WM/GenreID**                 | GenreID | Gesamtbetriebskosten     | Tcon         |
| **WM/InitialKey**              |         |         | Tkey         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/Sprache**                |         | Tla     | TLAN         |
| **WM/Synchronisierte Wm/Wm-Synchronisierung \_**    |         | Slt     | Sylt         |
| **WM/MCDI**                    |         |         | MCDI         |
| **WM/ModifiedBy**              |         |         | TPE4         |
| **WM/Stimmung**                    |         |         | TMOO         |
| **WM/Original FormatTitle**      |         | TOT     | Toal         |
| **WM/OriginalArtist**          |         | Toa     | Tope         |
| **WM/OriginalFilename**        |         | Tof     | TOFN         |
| **WM/OriginalLyricist**        |         | Tol     | TOLY         |
| **WM/OriginalReleaseYear**     |         | TOR     | Tory         |
| **WM/PartOfSet**               |         | Tpa     | Tpos         |
| **WM/Picture**                 |         | Pic     | APIC         |
| **WM/PlaylistDelay**           |         |         | TDLY         |
| **WM/Publisher**               |         | Tpb     | TPUB         |
| **WM/RadioStationName**        |         | Trn     | TRSN         |
| **WM/RadioStationOwner**       |         | Tro     | TRSO         |
| **WM/SetSubTitle**             |         |         | TSST         |
| **WM/Untertitel**                |         | TT3     | TI3         |
| **WM/Text**                    |         | TXX     | TXXX         |
| **WM/TitleSortOrder**          |         |         | TSOT         |
| **WM/TrackNumber**             | Track   | TRK     | TRCK         |
| **WM/UniqueFileIdentifier**    |         | Ufi     | UFID         |
| **WM/UserWebURL**              |         | WXX     | WXXX         |
| **WM/Writer**                  |         | TXT     | TEXT         |
| **WM/Jahr**                    | Jahr    | Tye     | TYER         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> </dl>

 

 




