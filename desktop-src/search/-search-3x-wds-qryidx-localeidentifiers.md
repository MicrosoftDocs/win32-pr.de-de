---
description: Die InputLocale-und keywordlocale-IDs helfen dem Suchmodul dabei, die richtigen Wörter Trennungen zu verwenden, indem Sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der von erweiterten Abfrage Syntax Schlüsselwörter identifizieren.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Gebiets Schema-bezeichnerargumente (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862180"
---
# <a name="locale-identifier-arguments-windows-search"></a>Gebiets Schema-bezeichnerargumente (Windows-Suche)

Die `inputlocale` `keywordlocale` Bezeichner und unterstützen das Suchmodul dabei, die richtigen Wörter Trennungen zu verwenden, indem die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der von erweiterten Abfrage Syntax Schlüsselwörter identifiziert werden. Dabei handelt es sich nicht immer um die gleichen Sprachcode Bezeichner (LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch MUI-Pakete für weitere Sprachen umfasst. InputLocale identifiziert die LCID für die Sprache, die Benutzer in Ihre Suchabfrage eingeben, während keywordlocale die LCID identifiziert, die die Suchmaschine für Schlüsselwörter verwendet.

Dieses Thema ist wie folgt organisiert:

-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="example"></a>Beispiel


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Die ersten Schritte mit Parameter-Value Argumenten](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Crumb-Argument](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Syntax Argument](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Stackedby-Argument](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Unterabfrage Argument](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



