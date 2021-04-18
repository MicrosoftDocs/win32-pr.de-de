---
description: Berechnen von Parameter Werten
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Berechnen von Parameter Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341106"
---
# <a name="calculating-parameter-values"></a>Berechnen von Parameter Werten

Möglicherweise kann ein Eingabepuffer sehr groß sein. Wenn der DMO den Puffer verarbeitet, werden die Parameter im Idealfall genau auf die Kurven im gesamten Datenstapel folgen. Ein DMO hat jedoch gewisse Spielraum bei der Berechnung dieser Werte.

-   Der präzisere Ansatz besteht darin, den exakten Wert für jede atomarische Dateneinheit zu berechnen. beispielsweise jedes Audiobeispiel. Diese Vorgehensweise ist am Rechen intensivsten.
-   Ein anderer Ansatz besteht darin, die Daten in kleinere Einheiten mit fester Größe, z. b. 100-Stichproben, aufzuteilen. Bei diesem Ansatz wird ein "Stair-Step"-Effekt erzeugt. Bei einigen Parametern ist das möglicherweise akzeptabel. In Audioeffekten könnte es akustische Artefakte erstellen.
-   Eine Gefährdung besteht darin, das vorherige Verfahren zu verwenden, aber innerhalb jedes Batches eine lineare interpolung des Parameter Werts für jede Stichprobe auszuführen.

Diese Probleme sind besonders wichtig für die Audioverarbeitung. Eine Sekunde Audioinformationen können 48.000 Audiobeispiele pro Kanal enthalten. Dies ist eine Vielzahl von Berechnungen, die durchgeführt werden müssen, aber das Ohr ist für Artefakte wie Aliasing sensibel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Parameter](media-parameters.md)
</dt> </dl>

 

 



