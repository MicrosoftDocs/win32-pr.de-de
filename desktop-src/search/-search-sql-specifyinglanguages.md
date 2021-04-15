---
description: Sie können die Sprache angeben, die in Such Abfragen verwendet wird.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Angeben von Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525478"
---
# <a name="specifying-languages"></a>Angeben von Sprachen

Sie können die Sprache angeben, die in Such Abfragen verwendet wird. Sowohl der frei Text als auch der enthält Prädikate in der WHERE-Klausel unterstützen die Angabe einer Sprache. Sie können die Abfragesprache angeben, indem Sie einen numerischen Sprachcode Bezeichner (LCID) im enthält-oder frei Text Prädikat bereitstellen. Diese LCID gibt an, welche Wörter Trennung zum Analysieren der Abfrage Zeichenfolge verwendet werden soll. Es verwendet die folgende Syntax:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Weitere Informationen finden Sie in der Syntax für die Prädikate " [enthält](-search-sql-contains.md) " und "frei [Text](-search-sql-freetext.md) ".

 

 



