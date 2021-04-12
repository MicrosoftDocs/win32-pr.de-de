---
title: Schachteln von Metadateien
description: Schachteln von Metadateien
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows Media-Metadateien, Schachteln
- Windows Media-Metadateien, verweisen auf andere Metadateien
- Schachteln von Metadateien
- Metadatendateien, Schachteln
- Metadatendateien, verweisen auf andere Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309328"
---
# <a name="nesting-metafiles"></a>Schachteln von Metadateien

Eine Metadatei kann auf eine andere Metadatendatei verweisen. Verwenden Sie das **ENTRYREF** -Element, um auf eine andere Metadatendatei zu verweisen. Ein **ENTRYREF** -Element in der primären Metadatei verweist auf eine externe Metadatendatei.

Das Windows Media Player-Steuerelement verarbeitet die **Einstiegs** Elemente der Metadatei, auf die verwiesen wird, als ob Sie in der primären Metadatendatei an der Position des **ENTRYREF** -Elements enthalten wären. Allerdings werden alle **Eingabe** Elemente in der Metadatei, auf die verwiesen wird, ausgelassen, deren **skipifref** -Attribut auf "yes" festgelegt ist.

Die Windows Media Player 7,0-, 7,1-und Windows Media Player für Windows XP-Steuerelemente ignorieren alle **ENTRYREF** -Elemente in der Metadatei, auf die verwiesen wird. Folglich können Metadateien nur eine Ebene tief in diesen Versionen verschachtelt werden. Diese Versionen ignorieren auch das Element " **ASX** " und seine Attribute in der referenzierten Datei. Windows Media Player 9 oder höher unterstützt das Schachteln von Metadateien bis zu 5 Tiefe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> </dl>

 

 




