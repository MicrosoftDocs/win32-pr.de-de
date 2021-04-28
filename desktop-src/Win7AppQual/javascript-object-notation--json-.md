---
description: JavaScript Object Notation (JSON)
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JavaScript Object Notation (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b5f12a2c4e3a4cd0a66a8f917c3cdf41ed17d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088188"
---
# <a name="javascript-object-notation-json"></a><span data-ttu-id="094ec-103">JavaScript Object Notation (JSON)</span><span class="sxs-lookup"><span data-stu-id="094ec-103">JavaScript Object Notation (JSON)</span></span>

<span data-ttu-id="094ec-104">[JavaScript Object Notation (JSON)](https://www.json.org/) ist ein einfaches und einfaches Datenaustauschformat, das auf einer Teilmenge der Objektliteralschreibweise der JavaScript-Sprache basiert.</span><span class="sxs-lookup"><span data-stu-id="094ec-104">[JavaScript Object Notation (JSON)](https://www.json.org/) is a simple and lightweight data-interchange format that is based on a subset of the object literal notation of the JavaScript language.</span></span> <span data-ttu-id="094ec-105">Die JavaScript-Engine in Windows Internet Explorer 8 implementiert den [ECMAScript 3.1-JSON-Vorschlag](https://www.ecma-international.org/) für native JSON-Verarbeitungsfunktionen (die [die json2.js-API von Vb Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)verwenden).</span><span class="sxs-lookup"><span data-stu-id="094ec-105">The JavaScript engine in Windows Internet Explorer 8 implements the [ECMAScript 3.1 JSON proposal](https://www.ecma-international.org/) for native JSON-handling functions (which uses [Douglas Crockford's json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span></span>

<span data-ttu-id="094ec-106">Internet Explorer 8 enthält ein natives JSON-Objekt, das der JSON-Unterstützung entspricht, die im [ES3.1 Proposal Working Draft](https://www.ecma-international.org/)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="094ec-106">Internet Explorer 8 includes a native JSON object that complies with the JSON support that is described in the [ES3.1 Proposal Working Draft](https://www.ecma-international.org/).</span></span> <span data-ttu-id="094ec-107">Einige Webseiten erkennen das native JSON-Objekt und verwenden es dann auf nicht standardmäßige Weise.</span><span class="sxs-lookup"><span data-stu-id="094ec-107">Some webpages detect the native JSON object, and then use it in a non-standard way.</span></span> <span data-ttu-id="094ec-108">Diese Verwendung verursacht in der Regel einen Skriptfehler und unterbricht die Behandlung von AJAX-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="094ec-108">This usage typically causes a script error and breaks the handling of AJAX requests.</span></span> <span data-ttu-id="094ec-109">Das folgende Codebeispiel zeigt die falsche Methode zur Verwendung des JSON-Objekts.</span><span class="sxs-lookup"><span data-stu-id="094ec-109">The following code example shows the wrong way to use the JSON object.</span></span>


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



<span data-ttu-id="094ec-110">Stattdessen zeigt das folgende Codebeispiel eine gute Möglichkeit, das JSON-Objekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="094ec-110">Instead, the following code example shows a good way to use the JSON object.</span></span>


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



<span data-ttu-id="094ec-111">Windows Internet Explorer enthält native Unterstützung für JSON, indem ein globales JSON-Objekt eingeführt wird, das über zwei integrierte Methoden verfügt: **stringify** und **parse**.</span><span class="sxs-lookup"><span data-stu-id="094ec-111">Windows Internet Explorer includes native supports for JSON by introducing a global JSON object that has two built-in methods: **stringify** and **parse**.</span></span> <span data-ttu-id="094ec-112">Das globale JSON-Objekt wird in der JavaScript-Engine definiert und während der Initialisierungsphase der Engine erstellt.</span><span class="sxs-lookup"><span data-stu-id="094ec-112">The global JSON object is defined in the JavaScript engine and is created during the engine initialization phase.</span></span> <span data-ttu-id="094ec-113">Zur Aufrechterhaltung der Abwärtskompatibilität ist dieses Feature nur verfügbar, wenn eine Website die neueste Version der JavaScript-Features mithilfe des Layoutmodus "Internet Explorer 8 Standards" (Dokument) verwendet.</span><span class="sxs-lookup"><span data-stu-id="094ec-113">To maintain backward compatibility, this feature is available only when a website uses the latest version of JavaScript features by using the "Internet Explorer 8 Standards" layout (document) mode.</span></span> <span data-ttu-id="094ec-114">Dieses Feature kann sich auch auf das Verhalten von Webseiten auswirken, die von einer globalen Variablen JSON abhängig sind oder [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)verwenden.</span><span class="sxs-lookup"><span data-stu-id="094ec-114">This feature also might affect the behavior of webpages that depend on a global variable JSON or use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span></span>

<span data-ttu-id="094ec-115">Sie können das globale JSON-Objekt überschreiben.</span><span class="sxs-lookup"><span data-stu-id="094ec-115">You can override the global JSON object.</span></span> <span data-ttu-id="094ec-116">Wenn eine Webseite jedoch den Layoutmodus "Internet Explorer 8 Standards" (Dokument) verwendet, handelt es sich nicht mehr um ein nicht definiertes Objekt.</span><span class="sxs-lookup"><span data-stu-id="094ec-116">But when a webpage uses the “Internet Explorer 8 Standards” layout (document) mode, it is not an undefined object anymore.</span></span> <span data-ttu-id="094ec-117">Da JSON von der JavaScript-Engine als globaler Name instanziiert wird, werden Überprüfungen wie "if(!this.JSON)" als False ausgewertet und müssen im Benutzercode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="094ec-117">Because JSON is instantiated as a global name by the JavaScript engine, checks like "if(!this.JSON)" evaluate to False and must be changed in the user code.</span></span>

<span data-ttu-id="094ec-118">Webseiten, die [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) verwenden, sind wahrscheinlich nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="094ec-118">Webpages that use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) are likely not affected.</span></span> <span data-ttu-id="094ec-119">Mit wenigen Ausnahmen sollten diese Seiten schneller funktionieren.</span><span class="sxs-lookup"><span data-stu-id="094ec-119">With few exceptions, these pages should work faster.</span></span> <span data-ttu-id="094ec-120">Die Ausnahmen sind auf die Unterschiede zwischen der nativen JSON-Implementierung Internet Explorer und json2.js zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="094ec-120">The exceptions are because of the differences between the Internet Explorer native JSON implementation and json2.js.</span></span> <span data-ttu-id="094ec-121">Beispielsweise erkennt die native JSON-Implementierung während der Serialisierung Zyklen und geht nicht in unendlicher Rekursion wie json.js vor.</span><span class="sxs-lookup"><span data-stu-id="094ec-121">For example, during serialization, the native JSON implementation detects cycles and does not go in infinite recursion like json.js.</span></span> <span data-ttu-id="094ec-122">Weitere Informationen zu diesen Ausnahmen finden Sie in den [JavaScript-Blogs.](/archive/blogs/jscript/)</span><span class="sxs-lookup"><span data-stu-id="094ec-122">For more information about these exceptions, see the [JavaScript Blogs](/archive/blogs/jscript/).</span></span>

<span data-ttu-id="094ec-123">Weitere Informationen finden Sie unter [JSON-Dokumentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) und [Versionierung und Versionsunterstützung der JavaScript-Engine.](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx)</span><span class="sxs-lookup"><span data-stu-id="094ec-123">For more information, see [JSON Documentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) and [Versioning and JavaScript Engine’s Version Support](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="094ec-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="094ec-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="094ec-125">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="094ec-125">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
