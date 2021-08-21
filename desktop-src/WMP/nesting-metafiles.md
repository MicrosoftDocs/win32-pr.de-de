---
title: Schachteln von Metadateien
description: Schachteln von Metadateien
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows Medienmetadateien,Schachtelung
- Windows Medienmetadateien, die auf andere Metadateien verweisen
- Schachteln von Metadateien
- Metadateien,Schachtelung
- Metadateien, Verweisen auf andere Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29a45bf545f839e111970b31d5faddd039959b7148a331fa5e347913b67327e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574273"
---
# <a name="nesting-metafiles"></a>Schachteln von Metadateien

Eine Metadatei kann auf eine andere Metadatei verweisen. Um auf eine andere Metadatei zu verweisen, verwenden Sie **das ENTRYREF-Element.** Ein **ENTRYREF-Element** in der primären Metadatei verweist auf eine externe Metadatei.

Das Windows Media Player verarbeitet die **ENTRY-Elemente** der Metadatei, auf die verwiesen wird, so, als ob sie in der primären Metadatei an der Position des **ENTRYREF-Elements enthalten** sind. Allerdings werden alle **ENTRY-Elemente** in der Metadatei, auf die verwiesen wird, übersprungen, für die das **SKIPIFREF-Attribut** auf YES festgelegt ist.

Die Windows Media Player 7.0, 7.1 und Windows Media Player für Windows XP-Steuerelemente ignorieren **alle ENTRYREF-Elemente** in der Metadatei, auf die verwiesen wird. Daher können Metadateien mit diesen Versionen nur eine Ebene tief geschachtelt werden. Diese Versionen ignorieren auch das **ASX-Element** und seine Attribute in der Datei, auf die verwiesen wird. Windows Media Player 9-Serie oder höher unterstützt das Schachteln von Metadateien bis zu 5 Tiefe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metadateiwiedergabelisten**](creating-metafile-playlists.md)
</dt> </dl>

 

 




