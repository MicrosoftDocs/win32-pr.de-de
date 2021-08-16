---
description: Sie können die Sprache angeben, die in Suchabfragen verwendet wird.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Angeben von Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ab2b5b5c5da4e9f71e49330d966895415467a671289bd4f5607e1265d22a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226815"
---
# <a name="specifying-languages"></a>Angeben von Sprachen

Sie können die Sprache angeben, die in Suchabfragen verwendet wird. Sowohl die FREETEXT- als auch die CONTAINS-Prädikate in der WHERE-Klausel unterstützen die Angabe einer Sprache. Sie können die Abfragesprache angeben, indem Sie einen numerischen Codebezeichner (LCID) im CONTAINS- oder FREETEXT-Prädikat angeben. Diese LCID gibt an, welche Wörterpause zum Analysieren der Abfragezeichenfolge verwendet werden soll. Es verwendet die folgende Syntax:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Weitere Informationen finden Sie in der Syntax für die [CONTAINS-](-search-sql-contains.md) und [FREETEXT-Prädikate.](-search-sql-freetext.md)

 

 



