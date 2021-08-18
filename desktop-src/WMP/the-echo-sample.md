---
title: Das Echobeispiel
description: Das Echobeispiel
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Windows Media Player Plug-Ins,Echo-Beispielübersicht
- Plug-Ins, Echo-Beispielübersicht
- Plug-Ins für die digitale Signalverarbeitung,Echobeispiel – Übersicht
- DSP-Plug-Ins,Echo-Beispielübersicht
- Programmierhandbuch, DSP-Plug-Ins
- Beispiele,DSP-Plug-Ins
- Echo DSP-Plug-In-Beispiel, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103054e82157d83085713937759de8aa9ed250a5491146ebe0c71559ab1ca338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762790"
---
# <a name="the-echo-sample"></a>Das Echobeispiel

Der Windows Media Player-Plug-In-Assistent kann ein DSP-Plug-In-Projekt für Microsoft Visual C++. Mit dem vom Assistenten generierten Standardcode kann der Benutzer einen Skalierungsfaktor zwischen 0 und 1 bereitstellen, der vom Programm als Multiplikator für die Audiobeispiele verwendet wird. Dies ist eine sehr einfache Implementierung, die Sie untersuchen können, um zu verstehen, wie Windows Media Player mit DSP-Plug-Ins interagiert. Die Informationen im Abschnitt About DSP Plug-ins (Informationen zu [DSP-Plug-Ins)](about-dsp-plug-ins.md) helfen Ihnen dabei, die Standardimplementierung zu verstehen.

Das in diesem Abschnitt beschriebene Beispiel ist etwas komplexer. In diesem Beispiel kann der Benutzer eine Verzögerungszeit in Millisekunden und eine Auswirkungsstufe angeben. Der Code verwendet diese Werte, um einen Echoeffekt zu generieren, wenn Dateien abspielt, die PCM-Audio (Pulse Code Codes) enthalten. Viele der Dateitypen, die Windows Media Player rendern, verwenden PCM-Audio.

Dieser Leitfaden ist in die folgenden Abschnitte unterteilt:



| `Section`                                                                                | BESCHREIBUNG                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Echo-Beispiel – Übersicht](echo-sample-overview.md)                                       | Beschreibt die allgemeinen Anforderungen und Spezifikationen für das Beispiel. Beschreibt die Funktionsweise des Plug-Ins.              |
| [Echo-Beispieleigenschaften](echo-sample-properties.md)                                   | Beschreibt, wie die Codeeigenschaft des Assistenten geändert und Methoden für die neue Eigenschaft hinzugefügt werden, die für das Echo-Beispiel erforderlich ist. |
| [Ändern der Eigenschaftenseite des Echobeispiels](modifying-the-echo-sample-property-page.md) | Zeigt, wie die vorhandene Eigenschaftenseitenimplementierung so geändert wird, dass sie mit dem Echo-Beispiel funktioniert.                         |
| [Arbeiten mit Streamingressourcen](working-with-streaming-resources.md)               | Veranschaulicht das Hinzufügen von Code zum Zuordnen und Frei geben eines Puffers, der für das Echo-Beispiel erforderlich ist.                                |
| [Implementieren von CEcho::D oProcessOutput](implementing-cecho--doprocessoutput.md)         | Beschreibt, wie der Code implementiert wird, der den Echoeffekt erstellt.                                                   |
| [Verwenden des Echo-Beispiel-DSP-Plug-Ins](using-the-echo-sample-dsp-plug-in.md)             | Beschreibt die Verwendung des abgeschlossenen Beispiels.                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch für DSP-Plug-Ins**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




