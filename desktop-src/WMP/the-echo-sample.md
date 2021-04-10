---
title: Das Echo-Beispiel
description: Das Echo-Beispiel
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Windows Media Player-Plug-ins, Übersicht über ECHO Beispiele
- Plug-ins, Echo Sample Overview
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Overview
- DSP-Plug-ins, Übersicht über ECHO Beispiele
- Programmier Handbuch, DSP-Plug-ins
- Beispiele, DSP-Plug-ins
- Echo DSP-Plug-in-Beispiel, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f2dfe6a59257b8a16dc31a5b4cb751d649cd6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947805"
---
# <a name="the-echo-sample"></a>Das Echo-Beispiel

Mit dem Assistenten für Windows-Media Player-Plug-in kann ein DSP-Plug-in-Projekt für Microsoft Visual C++ erstellt werden. Der vom Assistenten generierte Standard Code ermöglicht dem Benutzer die Angabe eines Skalierungsfaktors zwischen 0 und 1, der vom Programm als Multiplikator für die Audiobeispiele verwendet wird. Dies ist eine sehr einfache Implementierung, die Sie untersuchen können, um zu verstehen, wie Windows Media Player mit DSP-Plug-ins interagiert. Die Informationen im Abschnitt [zu DSP-Plug-ins](about-dsp-plug-ins.md) können Ihnen helfen, die Standard Implementierung zu verstehen.

Das in diesem Abschnitt beschriebene Beispiel ist etwas komplexer. In diesem Beispiel kann der Benutzer eine Verzögerungszeit in Millisekunden und eine Wirkungs Stufe angeben. Der Code verwendet diese Werte zum Generieren eines ECHO Effekts bei der Wiedergabe von Dateien, die PCM-Audiodaten (Pulse Code Modulation) enthalten. Viele der Dateitypen, die von Windows Media Player gerendert werden, verwenden PCM-Audiodaten

Dieses Handbuch ist in die folgenden Abschnitte unterteilt:



| `Section`                                                                                | BESCHREIBUNG                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Übersicht über das Echo Beispiel](echo-sample-overview.md)                                       | Beschreibt die allgemeinen Anforderungen und Spezifikationen für das Beispiel. Beschreibt, wie das Plug-in funktioniert.              |
| [Echo-Beispiel Eigenschaften](echo-sample-properties.md)                                   | Beschreibt, wie Sie die Eigenschaft des Assistenten Codes ändern und Methoden für die neue Eigenschaft hinzufügen, die für das Echo-Beispiel erforderlich ist. |
| [Ändern der Eigenschaften Seite Echo Sample](modifying-the-echo-sample-property-page.md) | Zeigt, wie die vorhandene Implementierung der Eigenschaften Seite geändert wird, um mit dem Echo-Beispiel zu arbeiten.                         |
| [Arbeiten mit Streamingressourcen](working-with-streaming-resources.md)               | Veranschaulicht das Hinzufügen von Code zum Zuordnen und Freigeben eines Puffers, der für das Echo Beispiel erforderlich ist.                                |
| [Implementieren von Cecho::D oprocess Output](implementing-cecho--doprocessoutput.md)         | Beschreibt, wie der Code implementiert wird, der den Echo Effekt erstellt.                                                   |
| [Verwenden des Echo Sample DSP-Plug-ins](using-the-echo-sample-dsp-plug-in.md)             | Beschreibt, wie das abgeschlossene Beispiel verwendet wird.                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für DSP-Plug-ins**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




