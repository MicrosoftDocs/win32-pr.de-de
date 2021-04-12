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
# <a name="javascript-object-notation-json"></a>JavaScript Object Notation (JSON)

[JavaScript Object Notation (JSON)](https://www.json.org/) ist ein einfaches und einfaches Datenaustauschformat, das auf einer Teilmenge der objektliteralnotation der JavaScript-Sprache basiert. Das JavaScript-Modul in Windows Internet Explorer 8 implementiert den [ECMAScript 3,1 JSON-Vorschlag](https://www.ecma-international.org/) für Native JSON-Behandlungs Funktionen (die die [json2.js-API von Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)verwenden).

Internet Explorer 8 enthält ein System eigenes JSON-Objekt, das mit der JSON-Unterstützung übereinstimmt, die im [Arbeitsentwurf für es 3.1-Vorschläge](https://www.ecma-international.org/)beschrieben wird. Einige Webseiten erkennen das Native JSON-Objekt und verwenden es dann auf nicht standardmäßige Weise. Diese Verwendung verursacht in der Regel einen Skript Fehler und unterbricht die Verarbeitung von AJAX-Anforderungen. Das folgende Codebeispiel zeigt die falsche Methode zum Verwenden des JSON-Objekts.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



Stattdessen wird im folgenden Codebeispiel eine gute Möglichkeit zum Verwenden des JSON-Objekts gezeigt.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer umfasst systemeigene Unterstützung für JSON durch Einführung eines globalen JSON-Objekts, das über zwei integrierte Methoden verfügt: **stringify** und **analysieren**. Das globale JSON-Objekt wird in der JavaScript-Engine definiert und während der Initialisierungsphase der Engine erstellt. Um die Abwärtskompatibilität zu gewährleisten, ist dieses Feature nur verfügbar, wenn eine Website die neueste Version der JavaScript-Features verwendet, indem Sie den Layoutmodus "Internet Explorer 8-Standard" (Dokument) verwenden. Diese Funktion kann sich auch auf das Verhalten von Webseiten auswirken, die von einer globalen JSON-Variablen abhängig sind oder [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)verwenden.

Sie können das globale JSON-Objekt überschreiben. Wenn eine Webseite jedoch den Layoutmodus "Internet Explorer 8-Standard" (Dokument) verwendet, handelt es sich nicht mehr um ein nicht definiertes Objekt. Da JSON als globaler Name von der JavaScript-Engine instanziiert wird, prüft, ob "if (! this.JSon)" zu "false" ausgewertet wird und im Benutzercode geändert werden muss.

Webseiten, die [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) verwenden, sind wahrscheinlich nicht betroffen. Mit wenigen Ausnahmen sollten diese Seiten schneller funktionieren. Die Ausnahmen sind aufgrund der Unterschiede zwischen der nativen JSON-Implementierung von Internet Explorer und json2.js. Beispielsweise erkennt die native JSON-Implementierung während der Serialisierung Zyklen und geht nicht in einer unendlichen Rekursion wie json.js. Weitere Informationen zu diesen Ausnahmen finden Sie in den [JavaScript-Blogs](/archive/blogs/jscript/).

Weitere Informationen finden Sie unter [JSON-Dokumentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) und [Versionsverwaltung sowie Unterstützung der JavaScript-Engine-Version](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
