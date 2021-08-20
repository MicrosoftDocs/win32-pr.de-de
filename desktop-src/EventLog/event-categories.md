---
description: Kategorien helfen Ihnen beim Organisieren von Ereignissen, damit Ereignisanzeige sie filtern können. Jede Ereignisquelle kann eigene nummerierte Kategorien und die Textzeichenfolgen definieren, denen sie zugeordnet sind.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Ereigniskategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d68895c1043e12ab8e53e3d6db8cd385d17ccc0175c5610a487682fc1c92c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151641"
---
# <a name="event-categories"></a>Ereigniskategorien

Kategorien helfen Ihnen beim Organisieren von Ereignissen, damit Ereignisanzeige sie filtern können. Jede [Ereignisquelle](event-sources.md) kann eigene nummerierte Kategorien und die Textzeichenfolgen definieren, denen sie zugeordnet sind.

Die Kategorien müssen nacheinander nummeriert werden, beginnend mit der Zahl 1. Die Kategorien selbst werden in einer Nachrichtendatei definiert. Verwenden Sie beispielsweise die folgende Syntax, um drei Ereigniskategorien zu deklarieren. In Ereignisanzeige werden die Ereignisse, die diese Kategorien verwenden, in der Spalte **Kategorie** 1, Kategorie 2 oder Kategorie 3 angezeigt.

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

Kategorien können in einer separaten Nachrichtendatei oder in einer Datei gespeichert werden, die Nachrichten anderer Typen enthält. Wenn Sie eine einzelne Nachrichtendatei erstellen, stellen Sie sicher, dass die Kategorien die ersten Nachrichten in der Datei sind. Weitere Informationen zum Erstellen und Verwenden von Nachrichtendateien finden Sie unter [Nachrichtendateien.](message-files.md)

Die Gesamtzahl der Kategorien wird im **CategoryCount-Wert** für die Ereignisquelle gespeichert.

 

 



