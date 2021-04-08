---
title: Metadatenerweiterungs-Richtlinien
description: Metadatenerweiterungs-Richtlinien
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Windows Media-Metadateien, Erweiterungen
- Windows Media-Metadateien, Dateinamen Erweiterungen
- Metadatendateien, Erweiterungen
- Metadateien, Dateinamen Erweiterungen
- Windows Media, Metafiles
- Dateinamen Erweiterungen für Windows Media-Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037536"
---
# <a name="metafile-extension-guidelines"></a>Metadatenerweiterungs-Richtlinien

Eine Dateinamenerweiterung bietet einen unabhängigen Softwarehersteller (Independent Software Vendor, ISV) mit Informationen zu den Renderinganforderungen einer Anwendung, die die Erweiterung verwendet, und ermöglicht Inhalts Entwicklern, allgemeine Typen von Playern als Ziel festzustellen.

Windows Media Metadatei-Erweiterungen werden verwendet, um das Format der Windows Media-Dateien zu identifizieren, auf die eine Metadatei verweist. Windows Media-Metadatendateien mit den Erweiterungen ". wax", ". wvx" oder ". asx" verweisen auf die Dateien mit den Erweiterungen. WMA,. WMV und. Alle Metadatendateien, unabhängig von der verwendeten Dateinamenerweiterung, haben das Element " **ASX** Element" am Anfang der Datei mit dem angegebenen **Versions** Attribut.

In der folgenden Tabelle werden die Medien Dateitypen angezeigt, auf die von den einzelnen Metadatendatei-Dateinamen Erweiterungen verwiesen wird. In den Spalten werden die Namen Erweiterungen für Mediendateien aufgelistet, die Metadatendatei-Erweiterungen der Zeilen Liste. Ein X in einer Spalte gibt einen Medien Dateityp an, auf den von einer bestimmten Dateinamenerweiterung für Metadatendateien verwiesen werden kann.



| Durchwahl | .asf | .wma | .wmv |
|-----------|------|------|------|
| . wvx      | X    | X    | X    |
| . Wachs      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dateinamenerweiterungen**](file-name-extensions.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




