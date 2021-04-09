---
title: Microsoft-Agent-Sprachausgabe Tags
description: Microsoft-Agent-Sprachausgabe Tags
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856212"
---
# <a name="microsoft-agent-speech-output-tags"></a>Microsoft-Agent-Sprachausgabe Tags

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Microsoft-Agent-Dienste unterstützen das Ändern der Sprachausgabe über spezielle Tags, die in die Zeichenfolge für die sprach Diese Tags helfen Ihnen, die Eigenschaften des Ausgabe Ausdrucks des Zeichens zu ändern.

Für Sprachausgabe Tags werden die folgenden Syntax Regeln verwendet:

-   Alle Tags beginnen und enden mit einem umgekehrten Schrägstrich ( \) .
-   Der einzelne umgekehrte Schrägstrich ist innerhalb eines Tags nicht aktiviert. Wenn Sie einen umgekehrten Schrägstrich in einen Text Parameter eines Tags einschließen möchten, verwenden Sie einen doppelten umgekehrten Schrägstrich ( \\ \) .
-   Tags Unterscheidung nach Groß-/Kleinschreibung. Beispielsweise \\ ist Pit \\ das gleiche wie \\ Pit \\ .
-   Tags sind Leerzeichen abhängig. Beispielsweise \\ ist RST \\ nicht mit \\ RST identisch \\ .

Sofern nicht anders angegeben oder von einem anderen Tag geändert, behält die Sprachausgabe das von dem-Tag festgelegte Merkmal in dem Text bei, der in einer einzelnen [**Sprech**](speak-method.md) Methode angegeben ist. Die Sprachausgabe wird automatisch durch die benutzerdefinierten Parameter zurückgesetzt, **nachdem eine Sprech** Methode abgeschlossen wurde.

Einige Tags enthalten Zeichen folgen in Anführungszeichen. Für einige Programmiersprachen, wie z. b. Visual Basic Scripting Edition (VBScript) und Visual Basic, bedeutet dies, dass Sie möglicherweise zwei Anführungszeichen verwenden müssen, um den Parameter des Tags anzugeben oder ein doppeltes Anführungszeichen als Teil der Zeichenfolge zu verketten. Letzteres wird in diesem Visual Basic Beispiel gezeigt:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Stellen Sie für C-, C++-und Java-™ Programmierung vor umgekehrten Schrägstrichen und doppelten Anführungszeichen mit einem umgekehrten Schrägstrich voran. Beispiel:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Für Fremdsprachen, die Zeichen mit Doppelbyte-Zeichensatz (Double-Byte Character Set, DBCS) unterstützen, können Sie Zeichen folgen Parameter mithilfe von Doppelbyte Zeichen angeben. Verwenden Sie jedoch Einzel Byte Zeichen für alle anderen Parameter und Zeichen, die zum Definieren des Tags verwendet werden, einschließlich des Tags selbst.

Die folgenden Tags werden unterstützt:

-   [**Chr**](chr-tag.md)
-   [**CTX**](ctx-tag.md)
-   [**EMP**](emp-tag.md)
-   [**LST**](lst-tag.md)
-   [**Bilden**](map-tag.md)
-   [**MRK**](mrk-tag.md)
-   [**Referi**](pau-tag.md)
-   [**Baum**](pit-tag.md)
-   [**RST**](rst-tag.md)
-   [**SPD**](spd-tag.md)
-   [**Volumen**](vol-tag.md)

Die Tags sind hauptsächlich für die Anpassung von von der Text-zu-Sprache (TTS) generierten Ausgaben konzipiert. Nur die [**MRK**](mrk-tag.md) -und [**map**](map-tag.md) -Tags können mit Audiodatei-basierter, gesprochener Ausgabe verwendet werden.

> [!Note]  
> Der Microsoft-Agent unterstützt nicht alle Tags, die im Microsoft Speech SDK dokumentiert sind. Parameter können auch abhängig von der ausgewählten TTS-Engine variieren. Sie können eine bestimmte TTS-Engine mit [**ttsmodeid**](ttsmodeid-property.md)festlegen.

 

 

 




