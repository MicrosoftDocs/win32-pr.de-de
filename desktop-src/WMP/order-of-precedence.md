---
title: Rangfolge
description: Rangfolge
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows Medienmetadateien,Rangfolge
- Windows Medienmetadateien,Rangfolge
- Metadateien,Rangfolge
- Metadateien,Rangfolge
- Windows Medien,Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12b55f34dd18fa6122d3f1588111aaffe374f2d87c06ef9100cbac057efd4bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467991"
---
# <a name="order-of-precedence"></a>Rangfolge

Nicht alle Metadateielementattribute werden gleich erstellt. Einige Metadateielementattribute überschreiben andere Elementattribute. Elementattribute können je nach Position und Reihenfolge durch ähnliche Elementattribute überschrieben werden. Alle Attribute einer Metadatei-Wiedergabeliste überschreiben die Attribute, die in einer Referenzdatei Windows Mediendatei enthalten sind. Ein Attribut, das ein anderes überschreibt, hat eine höhere Rangfolge.

Die Hierarchie mit der höchsten Rangfolge zu der niedrigsten ist in der folgenden Tabelle dargestellt. Das Element mit der höchsten Rangfolge wird nie überschrieben.



| `Scope`                    | Hierarchy                                   |
|--------------------------|---------------------------------------------|
| "Signierter DRM-Inhalt"     | Nie überschrieben.                           |
| **REF-Elementbereich**    | Wird nur von signierten DRM-Inhalten überschrieben.      |
| **ENTRY-Elementbereich**  | Überschreibt Elemente der folgenden Kategorien. |
| **ASX-Bereich**            | Überschreibt Mediendateielemente.              |
| Windows Mediendateibereich | Wird von allen oben genannten überschrieben.             |



 

-   "Signierter DRM-Inhalt": Digitales Signaturobjekt.

    Attribute signierter DRM-Inhalte überschreiben alle anderen. Beispielsweise werden die Copyrightinformationen von "Signierten DRM-Inhalten" nicht überschrieben. Es wird immer gestreamt und angezeigt.

-   **REF-Elementbereich**

    Attribute des **REF-Elements überschreiben** andere Elementattribute, aber keinen signierten DRM-Inhalt.

-   **ENTRY-Bereich**

    Attribute des **ENTRY-Elements** werden durch das REF-Elementattribut überschrieben, überschreiben jedoch andere Elementattribute.  **TITLE-Metadaten** **aus dem ENTRY-Element** werden anstelle der Titelinformationen aus der Mediendatei angezeigt.

-   **ASX-Bereich**

    Alle Eigenschaften, die in die Metadatei eingegeben werden, überschreiben die eigenschaften, die in der Windows Mediendatei enthalten sind. Attribute des **ENTRY-Elements** überschreiben **ASX-Elementattribute.** Während der **Medienclip** des ENTRY-Elements, auf das verwiesen wird, abspielt, werden **TITLE-Metadaten** aus dem **ENTRY-Element** anstelle von Titelinformationen aus dem **ASX-Element** angezeigt.

-   Windows Mediendateibereich

    Attribute der Windows Mediendatei werden von allen Metadateiattributen überschrieben. Metadaten der Mediendatei werden nur angezeigt, wenn in der Metadatei keine Metadaten für dieses Element definiert sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metadateiwiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




