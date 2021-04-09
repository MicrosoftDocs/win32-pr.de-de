---
title: Rangfolge
description: Rangfolge
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows Media-Metadateien, Rangfolge
- Windows Media-Metadateien, Rangfolge
- Metadateien, Rangfolge
- Metadateien, Rangfolge
- Windows Media, Metafiles
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036615"
---
# <a name="order-of-precedence"></a>Rangfolge

Nicht alle Metadatei-Element Attribute werden gleich erstellt. Einige Metadatei-Element Attribute überschreiben andere Element Attribute. Element Attribute können von ähnlichen Element Attributen abhängig von Position und Reihenfolge überschrieben werden. Alle Attribute einer metadateiwiedergabe Liste überschreiben diejenigen, die in einer referenzierten Windows-Mediendatei enthalten sind. Ein Attribut, das eine andere überschreibt, hat eine höhere Rangfolge.

In der folgenden Tabelle wird die Hierarchie mit der höchsten Rangfolge als der niedrigste Wert angezeigt. Das Element mit der höchsten Rangfolge wird nie überschrieben.



| Bereich                    | Hierarchy                                   |
|--------------------------|---------------------------------------------|
| "Signierter DRM-Inhalt"     | Nie überschrieben.                           |
| Verweis **Element Bereich**    | Wird nur von signiertem DRM-Inhalt überschrieben.      |
| Bereich des **Einstiegs** Elements  | Überschreibt Elemente der unten aufgeführten Kategorien. |
| Bereich von **ASX**            | Überschreibt Mediendatei Elemente.              |
| Windows Media-Datei Bereich | Überschrieben von allen oben genannten.             |



 

-   "Signierter DRM-Inhalt"-digitales Signatur Objekt.

    Attribute von signiertem DRM-Inhalt überschreiben alle anderen. Beispielsweise werden die Copyright Informationen von "signiertem DRM-Inhalt" nicht überschrieben. Sie wird immer gestreamt und präsentiert.

-   Verweis **Element Bereich**

    Attribute des **ref** -Elements überschreiben andere Element Attribute, aber keinen signierten DRM-Inhalt.

-   **Einstiegs** Bereich

    Attribute des **Entry** -Elements werden durch das **ref** -Element Attribut überschrieben, überschreiben jedoch andere Element Attribute. Anstelle der Titelinformationen aus der Mediendatei werden **Titel** Metadaten aus dem **Entry** -Element angezeigt.

-   Bereich von **ASX**

    Alle Eigenschaften, die in der Metadatei eingegeben werden, überschreiben diejenigen, die in der Windows Media-Datei enthalten sind. Attribute des **Entry** -Elements überschreiben die **ASX** -Element Attribute. Während der referenzierte Medien Clip des **Eintrags** Elements abgespielt wird, werden **Titel** Metadaten aus dem **Entry** -Element anstelle von Titelinformationen **aus dem-** Element des-Elements angezeigt.

-   Windows Media-Datei Bereich

    Attribute der Windows-Mediendatei werden von allen metadateiattributen überschrieben. Die Metadaten der Mediendatei werden nur angezeigt, wenn für dieses Element in der Metadatei keine Metadaten definiert sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




