---
title: Richtlinien für Metafileerweiterungen
description: Richtlinien für Metafileerweiterungen
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Windows Medienmetadateien, Erweiterungen
- Windows Medienmetadateien, Dateinamenerweiterungen
- Metadateien, Erweiterungen
- Metadateien, Dateinamenerweiterungen
- Windows Medien, Metadateien
- Dateinamenerweiterungen für Windows Media-Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aaa31f1364271b1b968244494586ba5006e7c292ca2d9a207cdd1c758b5e432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836967"
---
# <a name="metafile-extension-guidelines"></a>Richtlinien für Metafileerweiterungen

Eine Dateinamenerweiterung stellt einem unabhängigen Softwarehersteller (Independent Software Vendor, ISV) Informationen zu den Renderinganforderungen einer Anwendung bereit, die die Erweiterung verwendet, und ermöglicht Inhaltsautoren, allgemeine Typen von Playern als Ziel zu verwenden.

Windows Medienmetadateinamenerweiterungen werden verwendet, um das Format der Windows Mediendateien zu identifizieren, auf die eine Metadatei verweist. Windows Medienmetadateien mit Erweiterungen ".extensions", ".wvx" oder ".asx" verweisen auf Dateien mit WMA-, WMV- bzw. ASF-Erweiterungen. Alle Metadateien verfügen unabhängig von der verwendeten Dateinamenerweiterung über das **ASX-Elementtag** am Anfang der Datei mit dem angegebenen Versionsattribut. 

Die folgende Tabelle zeigt die Mediendateitypen, auf die von jedem Typ der Metadatei-Dateinamenerweiterung verwiesen wird. Die Spalten listen Erweiterungen für Mediendateinamen auf, die Zeilen listen Metadateinamenerweiterungen auf. Ein X in einer Spalte gibt einen Mediendateityp an, auf den von einer bestimmten Metadatei-Dateinamenerweiterung verwiesen werden kann.



| Erweiterung | .asf | .wma | .wmv |
|-----------|------|------|------|
| WVX      | X    | X    | X    |
| .dll      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dateinamenerweiterungen**](file-name-extensions.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Windows Media Metafile Guide**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




