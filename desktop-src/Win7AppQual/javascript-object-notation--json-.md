---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JavaScript Object Notation (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216526"
---
# <a name="javascript-object-notation-json"></a><span data-ttu-id="9c8d5-103">JavaScript Object Notation (JSON)</span><span class="sxs-lookup"><span data-stu-id="9c8d5-103">JavaScript Object Notation (JSON)</span></span>

<span data-ttu-id="9c8d5-104">[JavaScript Object Notation (JSON)](https://www.json.org/) ist ein einfaches und einfaches Datenaustauschformat, das auf einer Teilmenge der objektliteralnotation der JavaScript-Sprache basiert.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-104">[JavaScript Object Notation (JSON)](https://www.json.org/) is a simple and lightweight data-interchange format that is based on a subset of the object literal notation of the JavaScript language.</span></span> <span data-ttu-id="9c8d5-105">Das JavaScript-Modul in Windows Internet Explorer 8 implementiert den [ECMAScript 3,1 JSON-Vorschlag](https://www.ecma-international.org/) für Native JSON-Behandlungs Funktionen (die die [json2.js-API von Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)verwenden).</span><span class="sxs-lookup"><span data-stu-id="9c8d5-105">The JavaScript engine in Windows Internet Explorer 8 implements the [ECMAScript 3.1 JSON proposal](https://www.ecma-international.org/) for native JSON-handling functions (which uses [Douglas Crockford's json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span></span>

<span data-ttu-id="9c8d5-106">Internet Explorer 8 enthält ein System eigenes JSON-Objekt, das mit der JSON-Unterstützung übereinstimmt, die im [Arbeitsentwurf für es 3.1-Vorschläge](https://www.ecma-international.org/)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-106">Internet Explorer 8 includes a native JSON object that complies with the JSON support that is described in the [ES3.1 Proposal Working Draft](https://www.ecma-international.org/).</span></span> <span data-ttu-id="9c8d5-107">Einige Webseiten erkennen das Native JSON-Objekt und verwenden es dann auf nicht standardmäßige Weise.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-107">Some webpages detect the native JSON object, and then use it in a non-standard way.</span></span> <span data-ttu-id="9c8d5-108">Diese Verwendung verursacht in der Regel einen Skript Fehler und unterbricht die Verarbeitung von AJAX-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-108">This usage typically causes a script error and breaks the handling of AJAX requests.</span></span> <span data-ttu-id="9c8d5-109">Das folgende Codebeispiel zeigt die falsche Methode zum Verwenden des JSON-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-109">The following code example shows the wrong way to use the JSON object.</span></span>


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



<span data-ttu-id="9c8d5-110">Stattdessen wird im folgenden Codebeispiel eine gute Möglichkeit zum Verwenden des JSON-Objekts gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-110">Instead, the following code example shows a good way to use the JSON object.</span></span>


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



<span data-ttu-id="9c8d5-111">Windows Internet Explorer umfasst systemeigene Unterstützung für JSON durch Einführung eines globalen JSON-Objekts, das über zwei integrierte Methoden verfügt: **stringify** und **analysieren**.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-111">Windows Internet Explorer includes native supports for JSON by introducing a global JSON object that has two built-in methods: **stringify** and **parse**.</span></span> <span data-ttu-id="9c8d5-112">Das globale JSON-Objekt wird in der JavaScript-Engine definiert und während der Initialisierungsphase der Engine erstellt.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-112">The global JSON object is defined in the JavaScript engine and is created during the engine initialization phase.</span></span> <span data-ttu-id="9c8d5-113">Um die Abwärtskompatibilität zu gewährleisten, ist dieses Feature nur verfügbar, wenn eine Website die neueste Version der JavaScript-Features verwendet, indem Sie den Layoutmodus "Internet Explorer 8-Standard" (Dokument) verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-113">To maintain backward compatibility, this feature is available only when a website uses the latest version of JavaScript features by using the "Internet Explorer 8 Standards" layout (document) mode.</span></span> <span data-ttu-id="9c8d5-114">Diese Funktion kann sich auch auf das Verhalten von Webseiten auswirken, die von einer globalen JSON-Variablen abhängig sind oder [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-114">This feature also might affect the behavior of webpages that depend on a global variable JSON or use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span></span>

<span data-ttu-id="9c8d5-115">Sie können das globale JSON-Objekt überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-115">You can override the global JSON object.</span></span> <span data-ttu-id="9c8d5-116">Wenn eine Webseite jedoch den Layoutmodus "Internet Explorer 8-Standard" (Dokument) verwendet, handelt es sich nicht mehr um ein nicht definiertes Objekt.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-116">But when a webpage uses the “Internet Explorer 8 Standards” layout (document) mode, it is not an undefined object anymore.</span></span> <span data-ttu-id="9c8d5-117">Da JSON als globaler Name von der JavaScript-Engine instanziiert wird, prüft, ob "if (! this.JSon)" zu "false" ausgewertet wird und im Benutzercode geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-117">Because JSON is instantiated as a global name by the JavaScript engine, checks like "if(!this.JSON)" evaluate to False and must be changed in the user code.</span></span>

<span data-ttu-id="9c8d5-118">Webseiten, die [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) verwenden, sind wahrscheinlich nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-118">Webpages that use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) are likely not affected.</span></span> <span data-ttu-id="9c8d5-119">Mit wenigen Ausnahmen sollten diese Seiten schneller funktionieren.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-119">With few exceptions, these pages should work faster.</span></span> <span data-ttu-id="9c8d5-120">Die Ausnahmen sind aufgrund der Unterschiede zwischen der nativen JSON-Implementierung von Internet Explorer und json2.js.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-120">The exceptions are because of the differences between the Internet Explorer native JSON implementation and json2.js.</span></span> <span data-ttu-id="9c8d5-121">Beispielsweise erkennt die native JSON-Implementierung während der Serialisierung Zyklen und geht nicht in einer unendlichen Rekursion wie json.js.</span><span class="sxs-lookup"><span data-stu-id="9c8d5-121">For example, during serialization, the native JSON implementation detects cycles and does not go in infinite recursion like json.js.</span></span> <span data-ttu-id="9c8d5-122">Weitere Informationen zu diesen Ausnahmen finden Sie in den [JavaScript-Blogs](/archive/blogs/jscript/).</span><span class="sxs-lookup"><span data-stu-id="9c8d5-122">For more information about these exceptions, see the [JavaScript Blogs](/archive/blogs/jscript/).</span></span>

<span data-ttu-id="9c8d5-123">Weitere Informationen finden Sie unter [JSON-Dokumentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) und [Versionsverwaltung sowie Unterstützung der JavaScript-Engine-Version](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span><span class="sxs-lookup"><span data-stu-id="9c8d5-123">For more information, see [JSON Documentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) and [Versioning and JavaScript Engine’s Version Support](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c8d5-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c8d5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c8d5-125">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="9c8d5-125">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
