---
title: Übersicht über das Echo Beispiel
description: Übersicht über das Echo Beispiel
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Windows Media Player-Plug-ins, Übersicht über ECHO Beispiele
- Plug-ins, Echo Sample Overview
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Overview
- DSP-Plug-ins, Übersicht über ECHO Beispiele
- Echo DSP-Plug-in-Beispiel, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341255"
---
# <a name="echo-sample-overview"></a>Übersicht über das Echo Beispiel

Dieser Leitfaden erstellt ein Windows Media Player DSP-Plug-in, das während der Wiedergabe einen Echo Effekt in PCM-Audiodaten erstellt. Die Ziele für das Plug-in lauten wie folgt:

-   Das Plug-in verarbeitet nur 8-Bit-oder 16-Bit-PCM-Audiodaten.
-   Sie unterstützt eine Verzögerungszeit zwischen 10 Millisekunden (MS) und 2000 ms (2 Sekunden). Dies steht für die meisten Anwendungen für einen praktischen Bereich.
-   Sie unterstützt das Mischen des ursprünglichen Signals mit dem Verzögerungs Signal.
-   Sie stellt eine Implementierung der Eigenschaften Seite bereit, die es dem Benutzer ermöglicht, einen Wert für die Verzögerungszeit und einen Wert für den Prozentsatz des Verzögerungs Signals in Relation zur gesamten audiosignalstufe anzugeben.
-   Der Code wird erstellt, indem der Plug-in-Beispiel für den Windows Media Player-Plug-in-Assistent geändert wird.

Das Echo-Beispiel ist nicht im Windows Media Player SDK enthalten. Es handelt sich um ein Beispiel, das Sie erstellen. Um das Echo-Beispiel zu erstellen, müssen Sie mit dem Standard Projekt im Assistenten für Windows-Media Player-Plug-in beginnen. Sie können das Projekt beliebig benennen. in dieser Dokumentation wird davon ausgegangen, dass das Projekt Echo lautet. Ausführliche Informationen zur Verwendung des Assistenten finden Sie unter [Building a DSP Plug-in](building-a-dsp-plug-in.md).

Der folgende Abschnitt enthält eine Übersicht über die Erstellung eines ECHO Effekts durch das Beispiel:

-   [Funktionsweise des Echo-Beispiels](how-the-echo-sample-works.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Das Echo-Beispiel**](the-echo-sample.md)
</dt> </dl>

 

 




