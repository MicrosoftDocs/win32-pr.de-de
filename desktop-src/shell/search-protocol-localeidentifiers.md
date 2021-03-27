---
description: Die InputLocale-und keywordlocale-IDs helfen dem Suchmodul dabei, die richtigen Wörter Trennungen zu verwenden, indem Sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der von erweiterten Abfrage Syntax Schlüsselwörter identifizieren.
title: Gebiets Schema-bezeichnerargumente (die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 403e0338b61a4dedba37a620000e3fd82c91f383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218061"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Gebiets Schema-bezeichnerargumente (die Windows-Shell)

Die `inputlocale` `keywordlocale` Bezeichner und unterstützen das Suchmodul dabei, die richtigen Wörter Trennungen zu verwenden, indem die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der von erweiterten Abfrage Syntax Schlüsselwörter identifiziert werden. Dabei handelt es sich nicht immer um die gleichen Sprachcode Bezeichner (LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch mehrsprachige Benutzeroberflächen Pakete (MUI) für weitere Sprachen enthalten. Der `inputlocale` identifiziert die LCID für die Sprache, die Benutzer in die Suchabfrage eingeben, während der die `keywordlocale` LCID identifiziert, die die Such-Engine für Schlüsselwörter verwendet.

## <a name="example"></a>Beispiel


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Argument Informationen



|                          |                                         |
|--------------------------|-----------------------------------------|
| Mindestens Betriebs System | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



