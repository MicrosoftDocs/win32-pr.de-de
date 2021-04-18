---
description: Mithilfe von Kategorien können Sie Ereignisse organisieren, damit Sie von Ereignisanzeige gefiltert werden können. Jede Ereignis Quelle kann eigene nummerierte Kategorien und die Text Zeichenfolgen definieren, denen Sie zugeordnet sind.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Ereigniskategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347827"
---
# <a name="event-categories"></a>Ereigniskategorien

Mithilfe von Kategorien können Sie Ereignisse organisieren, damit Sie von Ereignisanzeige gefiltert werden können. Jede [Ereignis Quelle](event-sources.md) kann eigene nummerierte Kategorien und die Text Zeichenfolgen definieren, denen Sie zugeordnet sind.

Die Kategorien müssen nacheinander nummeriert werden, beginnend mit der Zahl 1. Die Kategorien selbst werden in einer Nachrichtendatei definiert. Verwenden Sie z. b. die folgende Syntax, um drei Ereignis Kategorien zu deklarieren. In Ereignisanzeige werden die Ereignisse, in denen diese Kategorien verwendet werden, Kategorie 1, Kategorie 2 oder Kategorie 3 in der Spalte **Category** angezeigt.

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

Kategorien können in einer separaten Nachrichtendatei oder in einer Datei gespeichert werden, die Nachrichten anderer Typen enthält. Wenn Sie eine einzelne Nachrichtendatei erstellen, achten Sie darauf, dass es sich bei den Kategorien um die ersten Nachrichten in der Datei handelt. Weitere Informationen zum Erstellen und Verwenden von Nachrichten Dateien finden Sie unter [Nachrichten Dateien](message-files.md).

Die Gesamtanzahl der Kategorien wird im **CategoryCount** -Wert für die Ereignis Quelle gespeichert.

 

 



