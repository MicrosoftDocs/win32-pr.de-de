---
description: Machen Sie sich mit den Argumenten inputlocale und keywordlocale auf der Windows Shell-Benutzeroberfläche aus, die der Suchmaschine helfen, die richtigen Wörterschalter zu verwenden.
title: Locale Identifier Arguments (The Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 34eab39e7ed956bf68048d9ce5861c12eedbbe7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403593"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Locale Identifier Arguments (The Windows Shell)

Die Bezeichner und unterstützen die Suchmaschine dabei, die richtigen Wörterschalter zu verwenden, indem sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der `inputlocale` `keywordlocale` Schlüsselwörter für erweiterte Abfragesyntax identifiziert. Dabei handelt es sich nicht immer um dieselben Sprachcodebezeichner (Language Code Identifiers, LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch mehrsprachige Benutzeroberfläche-Pakete (COD) für weitere Sprachen enthält. Identifiziert die LCID für die Sprache, in die Benutzer ihre Suchabfrage eingeben, während die LCID identifiziert, die die `inputlocale` `keywordlocale` Suchmaschine für Schlüsselwörter verwendet.

## <a name="example"></a>Beispiel


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Argumentinformationen



|                              | Wert                                   |
|------------------------------|-----------------------------------------|
| **Mindestbetriebssystem** | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



