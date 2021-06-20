---
description: Grundlegendes zu den Argumenten inputlocale und keywordlocale in Windows Search, wodurch die Suchmaschine die richtigen Wörteraufschlüsseler verwenden kann.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Gebietsschemabezeichnerargumente (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403753"
---
# <a name="locale-identifier-arguments-windows-search"></a>Gebietsschemabezeichnerargumente (Windows Search)

Die `inputlocale` `keywordlocale` Bezeichner und unterstützen die Suchmaschine dabei, die richtigen Wörteraufschlüsseler zu verwenden, indem sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der Schlüsselwörter der erweiterten Abfragesyntax identifizieren. Dabei handelt es sich nicht immer um die gleichen Sprachcodebezeichner (Language Code Identifiers, LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch PACKS für weitere Sprachen enthält. Inputlocale identifiziert die LCID für die Sprache, in der Benutzer ihre Suchabfrage eingeben, während keywordlocale die LCID identifiziert, die die Suchmaschine für Schlüsselwörter verwendet.

Dieses Thema ist wie folgt organisiert:

-   [Beispiel](#example)
-   [Verwandte Themen](#related-topics)

## <a name="example"></a>Beispiel


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Parameter-Value Argumenten](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[ARGUMENTS-Argument](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[SYNTAX-Argument](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[STACKEDBY-Argument](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[SUBQUERY-Argument](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



