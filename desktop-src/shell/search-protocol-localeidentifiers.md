---
description: Machen Sie sich mit den Argumenten inputlocale und keywordlocale auf der Windows Shell-Benutzeroberfläche aus, die die Suchmaschine bei der Verwendung der richtigen Wörteraufschlüsselung unterstützt.
title: Gebietsschemabezeichnerargumente (die Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b9c97f40d380acdbb26486acb248a273cb9d220588300a559275b73e41596e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677337"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Gebietsschemabezeichnerargumente (die Windows Shell)

Die `inputlocale` `keywordlocale` Bezeichner und unterstützen die Suchmaschine dabei, die richtigen Wörteraufschlüsseler zu verwenden, indem sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der Schlüsselwörter der erweiterten Abfragesyntax identifizieren. Dabei handelt es sich nicht immer um die gleichen Sprachcodebezeichner (Language Code Identifiers, LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch mehrsprachige Benutzeroberfläche Packs für weitere Sprachen enthält. identifiziert `inputlocale` die LCID für die Sprache, in der Benutzer ihre Suchabfrage eingeben, während `keywordlocale` die die LCID identifiziert, die die Suchmaschine für Schlüsselwörter verwendet.

## <a name="example"></a>Beispiel


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Argumentinformationen



|                              | Wert                                   |
|------------------------------|-----------------------------------------|
| **Mindestbetriebssystem** | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



