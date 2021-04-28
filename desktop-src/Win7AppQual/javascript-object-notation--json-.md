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
# <a name="javascript-object-notation-json"></a>JavaScript Object Notation (JSON)

[JavaScript Object Notation (JSON)](https://www.json.org/) ist ein einfaches und einfaches Datenaustauschformat, das auf einer Teilmenge der Objektliteralschreibweise der JavaScript-Sprache basiert. Die JavaScript-Engine in Windows Internet Explorer 8 implementiert den [ECMAScript 3.1-JSON-Vorschlag](https://www.ecma-international.org/) für native JSON-Verarbeitungsfunktionen (die [die json2.js-API von Vb Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)verwenden).

Internet Explorer 8 enthält ein natives JSON-Objekt, das der JSON-Unterstützung entspricht, die im [ES3.1 Proposal Working Draft](https://www.ecma-international.org/)beschrieben wird. Einige Webseiten erkennen das native JSON-Objekt und verwenden es dann auf nicht standardmäßige Weise. Diese Verwendung verursacht in der Regel einen Skriptfehler und unterbricht die Behandlung von AJAX-Anforderungen. Das folgende Codebeispiel zeigt die falsche Methode zur Verwendung des JSON-Objekts.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



Stattdessen zeigt das folgende Codebeispiel eine gute Möglichkeit, das JSON-Objekt zu verwenden.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer enthält native Unterstützung für JSON, indem ein globales JSON-Objekt eingeführt wird, das über zwei integrierte Methoden verfügt: **stringify** und **parse**. Das globale JSON-Objekt wird in der JavaScript-Engine definiert und während der Initialisierungsphase der Engine erstellt. Zur Aufrechterhaltung der Abwärtskompatibilität ist dieses Feature nur verfügbar, wenn eine Website die neueste Version der JavaScript-Features mithilfe des Layoutmodus "Internet Explorer 8 Standards" (Dokument) verwendet. Dieses Feature kann sich auch auf das Verhalten von Webseiten auswirken, die von einer globalen Variablen JSON abhängig sind oder [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)verwenden.

Sie können das globale JSON-Objekt überschreiben. Wenn eine Webseite jedoch den Layoutmodus "Internet Explorer 8 Standards" (Dokument) verwendet, handelt es sich nicht mehr um ein nicht definiertes Objekt. Da JSON von der JavaScript-Engine als globaler Name instanziiert wird, werden Überprüfungen wie "if(!this.JSON)" als False ausgewertet und müssen im Benutzercode geändert werden.

Webseiten, die [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) verwenden, sind wahrscheinlich nicht betroffen. Mit wenigen Ausnahmen sollten diese Seiten schneller funktionieren. Die Ausnahmen sind auf die Unterschiede zwischen der nativen JSON-Implementierung Internet Explorer und json2.js zurückzuführen. Beispielsweise erkennt die native JSON-Implementierung während der Serialisierung Zyklen und geht nicht in unendlicher Rekursion wie json.js vor. Weitere Informationen zu diesen Ausnahmen finden Sie in den [JavaScript-Blogs.](/archive/blogs/jscript/)

Weitere Informationen finden Sie unter [JSON-Dokumentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) und [Versionierung und Versionsunterstützung der JavaScript-Engine.](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
