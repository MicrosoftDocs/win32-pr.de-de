---
title: Verwenden von JavaScript und JScript
description: Verwenden von JavaScript und JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101590"
---
# <a name="using-javascript-and-jscript"></a>Verwenden von JavaScript und JScript

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Wenn Sie JavaScript oder Microsoft JScript für den Zugriff auf die Programmierschnittstelle des Microsoft-Agents verwenden, befolgen Sie die Konventionen für diese Sprache, um Methoden oder Eigenschaften anzugeben:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

JavaScript verfügt derzeit nicht über eine Ereignis Syntax für nicht-HTML-Objekte. Mit Internet Explorer können Sie jedoch die `<SCRIPT>` Tags **für... Ereignis** Syntax:

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Da nicht alle Browser diese Ereignis Syntax derzeit unterstützen, sollten Sie JavaScript nur für Seiten verwenden, die Microsoft Internet Explorer unterstützen, oder für Code, der keine Ereignis Behandlung erfordert.

Um auf die Objekt Auflistungen des Agents zuzugreifen, verwenden Sie die JScript- [**enumeratorfunktion**](https://www.bing.com/search?q=**Enumerator**) . Versionen von JScript, die vor Internet Explorer 4,0 enthalten waren, unterstützen diese Funktion jedoch nicht und unterstützen keine Auflistungen. Um auf Methoden und Eigenschaften des [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekts zuzugreifen, verwenden Sie die- [**Zeichen**](character-method.md) Methode. Wenn Sie auf die Eigenschaften eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts zugreifen möchten, verwenden Sie die- [**Befehls**](command-method.md) Methode.

 

 