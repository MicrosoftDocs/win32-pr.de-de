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
# <a name="using-javascript-and-jscript"></a><span data-ttu-id="38fb7-103">Verwenden von JavaScript und JScript</span><span class="sxs-lookup"><span data-stu-id="38fb7-103">Using JavaScript and JScript</span></span>

<span data-ttu-id="38fb7-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="38fb7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="38fb7-105">Wenn Sie JavaScript oder Microsoft JScript für den Zugriff auf die Programmierschnittstelle des Microsoft-Agents verwenden, befolgen Sie die Konventionen für diese Sprache, um Methoden oder Eigenschaften anzugeben:</span><span class="sxs-lookup"><span data-stu-id="38fb7-105">If you use JavaScript or Microsoft JScript to access Microsoft Agent's programming interface, follow the conventions for this language for specifying methods or properties:</span></span>

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

<span data-ttu-id="38fb7-106">JavaScript verfügt derzeit nicht über eine Ereignis Syntax für nicht-HTML-Objekte.</span><span class="sxs-lookup"><span data-stu-id="38fb7-106">JavaScript does not currently have event syntax for non-HTML objects.</span></span> <span data-ttu-id="38fb7-107">Mit Internet Explorer können Sie jedoch die `<SCRIPT>` Tags **für... Ereignis** Syntax:</span><span class="sxs-lookup"><span data-stu-id="38fb7-107">However, with Internet Explorer you can use the `<SCRIPT>` tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

<span data-ttu-id="38fb7-108">Da nicht alle Browser diese Ereignis Syntax derzeit unterstützen, sollten Sie JavaScript nur für Seiten verwenden, die Microsoft Internet Explorer unterstützen, oder für Code, der keine Ereignis Behandlung erfordert.</span><span class="sxs-lookup"><span data-stu-id="38fb7-108">Because not all browsers currently support this event syntax, you may want to use JavaScript only for pages that support Microsoft Internet Explorer or for code that does not require event handling.</span></span>

<span data-ttu-id="38fb7-109">Um auf die Objekt Auflistungen des Agents zuzugreifen, verwenden Sie die JScript- [**enumeratorfunktion**](https://www.bing.com/search?q=**Enumerator**) .</span><span class="sxs-lookup"><span data-stu-id="38fb7-109">To access Agent's object collections, use the JScript [**Enumerator**](https://www.bing.com/search?q=**Enumerator**) function.</span></span> <span data-ttu-id="38fb7-110">Versionen von JScript, die vor Internet Explorer 4,0 enthalten waren, unterstützen diese Funktion jedoch nicht und unterstützen keine Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="38fb7-110">However, versions of JScript included prior to Internet Explorer 4.0 do not support this function and do not support collections.</span></span> <span data-ttu-id="38fb7-111">Um auf Methoden und Eigenschaften des [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekts zuzugreifen, verwenden Sie die- [**Zeichen**](character-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="38fb7-111">To access methods and properties of the [**Character**](/windows/desktop/lwef/the-characters-object) object, use the [**Character**](character-method.md) method.</span></span> <span data-ttu-id="38fb7-112">Wenn Sie auf die Eigenschaften eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts zugreifen möchten, verwenden Sie die- [**Befehls**](command-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="38fb7-112">Similarly, to access the properties of a [**Command**](/windows/desktop/lwef/the-command-object) object, use the [**Command**](command-method.md) method.</span></span>

 

 