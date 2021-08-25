---
title: Verwenden von JavaScript und JScript
description: Verwenden von JavaScript und JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3b32fd3d8e2c8ce9e337f489c27dadaa32bb379d6bc90c6083d62af52bee24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960680"
---
# <a name="using-javascript-and-jscript"></a>Verwenden von JavaScript und JScript

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Wenn Sie JavaScript oder Microsoft JScript verwenden, um auf die Programmierschnittstelle des Microsoft-Agents zuzugreifen, befolgen Sie die Konventionen für diese Sprache zum Angeben von Methoden oder Eigenschaften:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

JavaScript verfügt derzeit nicht über Ereignissyntax für Nicht-HTML-Objekte. Mit Internet Explorer können Sie jedoch `<SCRIPT>` for... des Tags **verwenden. Ereignissyntax:**

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Da derzeit nicht alle Browser diese Ereignissyntax unterstützen, möchten Sie JavaScript möglicherweise nur für Seiten verwenden, die Microsoft Internet Explorer unterstützen, oder für Code, der keine Ereignisbehandlung erfordert.

Um auf objektauflistungen des -Agents zuzugreifen, verwenden Sie die JScript [**Enumeratorfunktion.**](https://www.bing.com/search?q=**Enumerator**) Versionen von JScript jedoch vor Internet Explorer 4.0 enthalten sind, unterstützen diese Funktion nicht und keine Sammlungen. Verwenden Sie die Character-Methode, um auf Methoden und Eigenschaften des [**Character-Objekts**](character-method.md) zuzugreifen. [](/windows/desktop/lwef/the-characters-object) Verwenden Sie auf ähnliche Weise die Command-Methode, um auf die Eigenschaften eines [**Command-Objekts**](command-method.md) zuzugreifen. [](/windows/desktop/lwef/the-command-object)

 

 