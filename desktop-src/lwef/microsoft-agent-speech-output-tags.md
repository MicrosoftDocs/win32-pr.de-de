---
title: Microsoft Agent Speech-Ausgabetags
description: Microsoft Agent Speech-Ausgabetags
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e712285b8160cf12817890ac42c4d49e95d72a2b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386799"
---
# <a name="microsoft-agent-speech-output-tags"></a>Microsoft Agent Speech-Ausgabetags

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Die Microsoft Agent-Dienste unterstützen das Ändern der Sprachausgabe über spezielle Tags, die in die Sprachtextzeichenfolge eingefügt werden. Mit diesen Tags können Sie die Merkmale des Ausgabeausdrucks des Zeichens ändern.

Sprachausgabetags verwenden die folgenden Syntaxregeln:

-   Alle Tags beginnen und enden mit einem schrägen Schrägstrich ( \\ ).
-   Der einzelne schräge Schrägstrich ist innerhalb eines Tags nicht aktiviert. Verwenden Sie einen doppelten schrägen Schrägstrich ( ), um einen schrägen Schrägstrich in einen Textparameter eines Tags ein-/aus. \\ \\
-   Bei Tags wird die Groß-/Kleinschreibung nicht beachtet. Pit ist \\ \\ z. B. identisch mit \\ PIT \\ .
-   Tags sind leerraumabhängig. Beispielsweise ist \\ Rst \\ nicht mit \\ Rst \\ identisch.

Sofern nicht anders angegeben oder durch ein anderes Tag geändert, behält die Sprachausgabe das Merkmal bei, das durch das -Tag innerhalb des in einer einzelnen Speak-Methode angegebenen [**Texts festgelegt**](speak-method.md) wird. Die Sprachausgabe wird automatisch über die benutzerdefinierten Parameter zurückgesetzt, nachdem eine **Speak-Methode** abgeschlossen wurde.

Einige Tags enthalten Zeichenfolgen in Anführungswörtern. Für einige Programmiersprachen wie Visual Basic Scripting Edition (VBScript) und Visual Basic bedeutet dies, dass Sie möglicherweise zwei Anführungszeichen verwenden müssen, um den Parameter des Tags zu kennzeichnen oder ein doppeltes Anführungszeichen als Teil der Zeichenfolge zu verketten. Letzteres wird in diesem Beispiel Visual Basic gezeigt:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Bei C-, C++- und Java™-Programmierung vor den zurücken Schrägstrichen und doppelten Anführungszeichen mit einem zurücken Schrägstrich. Zum Beispiel:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Für Sprachen, die Doppel-Byte-Zeichensatzzeichen (Double-Byte Character Set, DBCS) unterstützen, können Sie Doppel bytezeichen verwenden, um Zeichenfolgenparameter anzugeben. Verwenden Sie jedoch Einzel bytezeichen für alle anderen Parameter und Zeichen, die zum Definieren des Tags verwendet werden, einschließlich des Tags selbst.

Die folgenden Tags werden unterstützt:

-   [**Chr**](chr-tag.md)
-   [**Ctx**](ctx-tag.md)
-   [**Emp**](emp-tag.md)
-   [**Lst**](lst-tag.md)
-   [**Karte**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**Grube**](pit-tag.md)
-   [**Ersten**](rst-tag.md)
-   [**Spd**](spd-tag.md)
-   [**Vol**](vol-tag.md)

Die Tags sind in erster Linie für die Anpassung der von TTS (Text-to-Speech) generierten Ausgabe konzipiert. Nur die [**Mrk-**](mrk-tag.md) und [**Map-Tags**](map-tag.md) können mit audiodateibasierter gesprochener Ausgabe verwendet werden.

> [!Note]  
> Microsoft Agent unterstützt nicht alle Tags, die im Microsoft Speech SDK dokumentiert sind. Die Parameter können auch abhängig von der ausgewählten TTS-Engine variieren. Sie können eine bestimmte TTS-Engine mit [**TTSModeID festlegen.**](ttsmodeid-property.md)

 

 

 




