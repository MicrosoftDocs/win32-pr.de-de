---
title: Zugreifen auf die Steuerelemente Methoden, Eigenschaften und Ereignisse
description: Zugreifen auf die Steuerelemente Methoden, Eigenschaften und Ereignisse
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388240"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a>Zugreifen auf die Steuerelemente Methoden, Eigenschaften und Ereignisse

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Verwendung des Steuer Elements von Microsoft-Agent mit Visual Basic ähnelt der Verwendung des Steuer Elements mit VBScript, mit dem Unterschied, dass Ereignisse in Visual Basic den Datentyp der bestandenen Parameter einschließen müssen. Beim Hinzufügen des Microsoft-Agent-Steuer Elements zu einem Formular werden die Ereignisse des Microsoft-Agents automatisch mit den entsprechenden Parametern eingeschlossen. Außerdem wird automatisch eine Verbindung mit dem Agentserver hergestellt, wenn die Anwendung ausgeführt wird.

Möglicherweise können Sie auch die Objectes-Erstellungs Syntax Ihrer Programmiersprache verwenden, um zur Laufzeit eine Instanz des Steuer Elements zu erstellen. Wenn Sie z. b. in Visual Basic (5,0 oder höher) das Microsoft-Agent 2,0-Steuerelement in die Verweise Ihres Projekts einschließen, können Sie [**mit-Ereignissen**](https://www.bing.com/search?q=**With+Events**)verwenden. [**Neue**](https://www.bing.com/search?q=**New**) Deklaration. Wenn Sie den Verweis nicht einschließen, löst VB einen Fehler aus, der anzeigt, dass der Microsoft-Agent nicht gestartet werden konnte (Fehlercode 80042502).

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

Für Versionen von VB vor 5,0 können Sie das VB [**New**](https://www.bing.com/search?q=**New**) -Schlüsselwort ohne [**wider Vents**](https://www.bing.com/search?q=**WithEvents**) -Deklaration oder die VB-Funktion von "detarateobject" verwenden, aber diese Konventionen machen die Ereignisse des Agent-Steuer Elements nicht verfügbar. [](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) Sie müssen auch die [**verbundene**](https://www.bing.com/search?q=**Connected**) -Eigenschaft verwenden, bevor Sie auf Agent-Methoden oder-Eigenschaften verweisen können. Wenn dies nicht erfolgt, gibt VB einen Fehler aus, der anzeigt, dass der Microsoft-Agent nicht gestartet werden konnte (Fehlercode 80042502).

Ähnlich wie bei anderen Programmiersprachen müssen Sie möglicherweise die [**verbundene**](https://www.bing.com/search?q=**Connected**) -Eigenschaft verwenden, um eine Verbindung mit dem com-Server (Agent Component Object Model) herzustellen, bevor der Code eine der Methoden oder Eigenschaften des Agent-Steuer Elements abrufen kann. Außerdem können die Methoden und Eigenschaften des Agents für einige Programmiersprachen nicht direkt verfügbar gemacht werden, es sei denn, Sie deklarieren das agentsteuerelement mithilfe des Typs. Beispielsweise müssen Sie in Microsoft Access 97 das Objekt als Typ-Agent deklarieren, damit die Methoden und Eigenschaften im Dropdown Feld Member automatisch auflisten angezeigt werden, wenn Sie eingeben.

Die meisten Programmiersprachen, die ActiveX-Steuerelemente unterstützen, folgen Konventionen wie Visual Basic. Für Programmiersprachen, die keine Objekt Auflistungen unterstützen, können Sie mit der [**Zeichen**](https://www.bing.com/search?q=**Character**) Methode und der [**Befehls**](https://www.bing.com/search?q=**Command**) Methode auf Methoden und Eigenschaften von Elementen in der Auflistung zugreifen.

Programmiersprachen wie Visual Basic, die Zugriff auf die vom agentsteuerelement verfügbar gemachten Objekttypen ermöglichen, ermöglichen es Ihnen, diese in den Objekt Deklarationen zu verwenden. Anstatt ein Objekt als generischen Typ zu deklarieren, verwenden Sie z. b. Folgendes:

``` syntax
   Dim Genie as Object
```

Sie können ein Objekt als bestimmten Typ deklarieren:

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

Dies kann die Gesamtleistung der Anwendung verbessern.

Bei einigen Objekttypen finden Sie möglicherweise zwei Typen, die mit Ausnahme des Suffix "ex" identisch sind. Wenn beide vorhanden sind, verwenden Sie den Typ "ex", da dies die vollständige Funktionalität des-Agents bereitstellt. Die nicht-"ex"-Entsprechungen sind nur aus Gründen der Abwärtskompatibilität enthalten.

 

 




