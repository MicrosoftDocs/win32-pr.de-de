---
description: Ein Parser ist die Netzwerkmonitor Komponente, die Daten in einer verzögerten Erfassung überprüft und bestimmte Protokollinformationen an die Anwendung übergibt, die den Parser aufruft. Ein Parser ist passiv, da er nur funktioniert, wenn Netzwerkmonitor oder ein Experte ihn aufruft.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861991"
---
# <a name="parser"></a>Parser

Ein Parser ist die Netzwerkmonitor Komponente, die Daten in einer [*verzögerten Erfassung*](d.md)überprüft und bestimmte Protokollinformationen an die Anwendung übergibt, die den Parser aufruft. Ein Parser ist passiv, da er nur funktioniert, wenn Netzwerkmonitor oder ein [*Experte*](e.md) ihn aufruft.

Jeder Parser identifiziert ein Protokoll, und in der Regel wird ein Parser in seiner eigenen Parser-DLL implementiert. Eine Parser-DLL kann jedoch mehrere Parser enthalten. Dies bedeutet, dass eine DLL verwendet werden kann, um mehr als ein Protokoll zu erkennen.

Die an einen Parser weiter gegebenen Daten werden aus einer [*verzögerten Erfassung*](d.md)entnommen und auf Frame-für-Frame-Basis an den Parser übergeben. Sie können eine echt Zeiterfassung nicht analysieren.

Um die Daten in einem Frame zu analysieren, muss der Parser die Protokoll Instanz erkennen, die Eigenschaften identifizieren, die in der Protokoll Instanz vorhanden sind, und jede Eigenschaft eine Eigenschafts Definition anfügen. Beachten Sie, dass der Frame nur einen Datenstrom enthält. Der Frame enthält keine Daten, die angeben, welche Protokolle oder Protokoll Eigenschaften die Daten darstellen.

Die folgende Abbildung zeigt einen Frame, der eine Instanz eines Protokolls enthält.

![ein Frame, der eine Protokoll Instanz enthält.](images/parser1.png)

Wenn Netzwerkmonitor Analysierte Daten in der Benutzeroberfläche anzeigt, muss der Parser die Daten formatieren. Einige Experten verwenden die parserausgabe jedoch Programm gesteuert und zeigen die Ausgabe nicht in der Netzwerkmonitor-Benutzeroberfläche an. Die angezeigten Daten umfassen sowohl Parser-definierte Daten als auch die Daten in der Erfassung. Der Parser stellt z. b. in der Regel einen Namen für eine angezeigte Eigenschaft und die Daten in der Erfassung bereit, die der-Eigenschaft zugeordnet ist.



| Informationen über                                         | Finden Sie unter                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| Welche Einstiegspunkte in der Parser-DLL implementiert werden müssen. | [Architektur der Parser-DLL](parser-dll-architecture.md)                 |
| Gewusst wie: Implementieren von parserdll-Exportfunktionen                 | [Schreiben eines Protokoll Parsers](writing-a-protocol-parser.md)             |
| Welche Funktionen und Struktur Parser verwenden.                   | [Parser-Funktionen und-Strukturen](parser-functions-and-structures.md) |



 

 

 



