---
description: Ein Parser ist die Netzwerkmonitor, die Daten in einer verzögerten Erfassung überprüft und bestimmte Protokollinformationen an die Anwendung übergibt, die den Parser aufruft. Ein Parser ist passiv, da er nur funktioniert, Netzwerkmonitor oder ein Experte ihn aufruft.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf6f7c799782a75905d366c56157a99fd6f774f5682e302dcec4a9d6c788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555514"
---
# <a name="parser"></a>Parser

Ein Parser ist die Netzwerkmonitor, die Daten [](d.md)in einer verzögerten Erfassung überprüft und bestimmte Protokollinformationen an die Anwendung übergibt, die den Parser aufruft. Ein Parser ist passiv, da er nur funktioniert, Netzwerkmonitor oder ein Experte [*ihn*](e.md) aufruft.

Jeder Parser identifiziert ein Protokoll, und in der Regel wird ein Parser in seiner eigenen Parser-DLL implementiert. Eine Parser-DLL kann jedoch mehrere Parser enthalten, was bedeutet, dass eine DLL verwendet werden kann, um mehrere Protokolle zu erkennen.

Die an einen Parser übergebenen [](d.md)Daten werden aus einer verzögerten Erfassung übernommen und frame-für-frame-orientierte An den Parser übergeben. Eine Echtzeiterfassung kann nicht analysiert werden.

Um die Daten in einem Frame zu analysieren, muss der Parser die Protokollinstanz erkennen, die eigenschaften identifizieren, die in der Protokollinstanz vorhanden sind, und jeder Eigenschaft eine Eigenschaftendefinition anfügen. Beachten Sie, dass der Frame nur einen Datenstrom enthält. Der Frame enthält keine Daten, die angibt, welche Protokolle oder Protokolleigenschaften die Daten repräsentieren.

Die folgende Abbildung zeigt einen Frame, der eine Instanz eines Protokolls enthält.

![ein Frame, der eine Protokollinstanz enthält](images/parser1.png)

Wenn Netzwerkmonitor analysierte Daten auf der Benutzeroberfläche anzeigen, muss der Parser die Daten formatieren. Einige Experten verwenden die Parserausgabe jedoch programmgesteuert und zeigen die Ausgabe nicht in der Netzwerkmonitor an. Die angezeigten Daten enthalten sowohl vom Parser definierte Daten als auch die Daten in der Erfassung. Beispielsweise stellt der Parser in der Regel sowohl einen Namen für eine eigenschaft, die angezeigt wird, als auch die Daten in der Erfassung, die der -Eigenschaft zugeordnet sind, zur Seite.



| Informationen über                                         | Finden Sie unter                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| Welche Einstiegspunkte in der Parser-DLL implementiert werden müssen. | [Parser-DLL-Architektur](parser-dll-architecture.md)                 |
| Implementieren von Parser-DLL-Exportfunktionen.                 | [Schreiben eines Protokollparsers](writing-a-protocol-parser.md)             |
| Welche Funktionen und Strukturen Parser verwenden.                   | [Parserfunktionen und -strukturen](parser-functions-and-structures.md) |



 

 

 



