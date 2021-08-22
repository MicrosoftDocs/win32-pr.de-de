---
title: Microsoft Agent Speech Output Tags
description: Microsoft Agent Speech Output Tags
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27add35cc9be72a002cdb1a6fba60ef61d47cca61ef532a6d80fd6ed4a5794d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747888"
---
# <a name="microsoft-agent-speech-output-tags"></a>Microsoft Agent Speech Output Tags

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Die Microsoft-Agent-Dienste unterstützen das Ändern der Sprachausgabe über spezielle Tags, die in die Sprachtextzeichenfolge eingefügt werden. Mit diesen Tags können Sie die Merkmale des Ausgabeausdrucks des Zeichens ändern.

Sprachausgabetags verwenden die folgenden Syntaxregeln:

-   Alle Tags beginnen und enden mit einem umgekehrten Schrägstrich ( \\ ).
-   Der einzelne umgekehrte Schrägstrich ist innerhalb eines Tags nicht aktiviert. Um einen umgekehrten Schrägstrich in einen Textparameter eines Tags einzuschließen, verwenden Sie einen doppelten umgekehrten Schrägstrich ( \\ \\ ).
-   Bei Tags wird die Groß-/Kleinschreibung nicht beachtet. Beispielsweise \\ entspricht pit \\ dem Pit \\ \\ .
-   Tags sind leerraumabhängig. Beispielsweise \\ ist Rst \\ nicht mit \\ Rst \\ identisch.

Sofern nicht anders angegeben oder durch ein anderes Tag geändert, behält die Sprachausgabe das vom -Tag festgelegte Merkmal innerhalb des Texts bei, der in einer einzelnen [**Speak-Methode**](speak-method.md) angegeben ist. Die Sprachausgabe wird automatisch über die benutzerdefinierten Parameter zurückgesetzt, nachdem eine **Speak-Methode** abgeschlossen wurde.

Einige Tags enthalten Zeichenfolgen in Anführungszeichen. Für einige Programmiersprachen wie Visual Basic Scripting Edition (VBScript) und Visual Basic bedeutet dies, dass Sie möglicherweise zwei Anführungszeichen verwenden müssen, um den Parameter des Tags festzulegen oder ein doppeltes Anführungszeichen als Teil der Zeichenfolge zu verketten. Letzteres wird in diesem Visual Basic Beispiel gezeigt:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Bei der Programmierung von C, C++ und Java™ vorangehende umgekehrte Schrägstriche und doppelte Anführungszeichen mit einem umgekehrten Schrägstrich. Beispiel:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Für Sprachen, die DOPPEL-Byte-Zeichen (Double-Byte Character Set, DBCS) unterstützen, können Sie Doppel-Byte-Zeichen verwenden, um Zeichenfolgenparameter anzugeben. Verwenden Sie jedoch Einzel bytezeichen für alle anderen Parameter und Zeichen, die zum Definieren des Tags verwendet werden, einschließlich des Tags selbst.

Die folgenden Tags werden unterstützt:

-   [**Chr**](chr-tag.md)
-   [**Ctx**](ctx-tag.md)
-   [**Emp**](emp-tag.md)
-   [**Lst**](lst-tag.md)
-   [**Zuordnung**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**Grube**](pit-tag.md)
-   [**Ersten**](rst-tag.md)
-   [**Spd**](spd-tag.md)
-   [**Vol**](vol-tag.md)

Die Tags sind in erster Linie für die Anpassung der durch TTS (Text-to-Speech) generierten Ausgabe konzipiert. Nur die [**Tags Mrk**](mrk-tag.md) und [**Map**](map-tag.md) können mit audiodateibasierter gesprochener Ausgabe verwendet werden.

> [!Note]  
> Der Microsoft-Agent unterstützt nicht alle Tags, die im Microsoft Speech SDK dokumentiert sind. Parameter können auch je nach ausgewählter TTS-Engine variieren. Sie können eine bestimmte TTS-Engine mit [**TTSModeID**](ttsmodeid-property.md)festlegen.

 

 

 




