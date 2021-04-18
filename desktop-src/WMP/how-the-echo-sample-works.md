---
title: Funktionsweise des Echo-Beispiels
description: Funktionsweise des Echo-Beispiels
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Windows Media Player-Plug-ins, Übersicht über ECHO Beispiele
- Plug-ins, Echo Sample Overview
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Overview
- DSP-Plug-ins, Übersicht über ECHO Beispiele
- Echo DSP-Plug-in-Beispiel, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341242"
---
# <a name="how-the-echo-sample-works"></a>Funktionsweise des Echo-Beispiels

Der Code erstellt den Echo Effekt durch Zuordnen eines Puffers, der ausreichend groß genug ist, um genau die Menge an Audiodaten zu erhalten, die in dem durch den Verzögerungs Zeitwert angegebenen Zeitrahmen gerendert werden können. Die Größe des Puffers wird in Bytes mit der folgenden Formel berechnet:

Puffergröße = Verzögerungszeit \* Stichprobenrate/1000 \* Block Ausrichtung

Die Verzögerungszeit beträgt Millisekunden. Die Werte für die Stichprobenrate und die Block Ausrichtung werden in einer WaveFormatEx-Struktur angegeben. Die Stichprobenrate beträgt Stichproben pro Sekunde. Division durch 1000 ergibt Stichproben pro Millisekunde. Die Block Ausrichtung entspricht dem Produkt der Anzahl von Kanälen (1 für Mono, 2 für Stereo) und der Anzahl von Bits pro Stichprobe (8 oder 16) dividiert durch 8 (Bits pro Byte).

Zusätzlich zu der Zeiger Variablen, die auf den Anfang des Verzögerungs Puffers zeigt, erstellt der Code einen verschiebbaren Zeiger, der die Daten im Puffer in der Synchronisierung mit der Verarbeitungs Schleife in der **DoProcess Output** -Funktion durchläuft. Wenn der verschiebbare Zeiger das Ende des Verzögerungs Puffers erreicht, wechselt er zurück zum Anfang des Puffers. Ein auf diese Weise verwendeter Puffer wird als Zirkel Puffer bezeichnet.

Sobald der Verzögerungs Puffer vorhanden ist und Windows Media Player einen Eingabepuffer zum Bereitstellen von Audiodaten und einen Ausgabepuffer zum Empfangen der verarbeiteten Audiodaten zugeordnet hat, wird die Echo Verarbeitung wie folgt fortgesetzt:

1.  Geben Sie eine Schleife ein, die die Verarbeitung der einzelnen Audiobeispiele im Eingabepuffer zulässt.
2.  Rufen Sie ein Beispiel aus dem Eingabepuffer ab. Verschieben Sie dann den Eingabepuffer Zeiger auf das nächste Beispiel, um die nächste Schleifen Iterations Vorbereitung vorzubereiten.
3.  Rufen Sie ein Beispiel aus dem verzögerten Puffer ab.
4.  Kopieren Sie das Beispiel aus dem Eingabepuffer an den gleichen Speicherort im Verzögerungs Puffer, von dem aus die letzte Verzögerungs Stichprobe abgerufen wurde.
5.  Verschieben Sie den Verzögerungs Puffer Zeiger auf das nächste Beispiel. Wenn sich der Zeiger über das Ende des Puffers bewegt, verschieben Sie ihn an den Anfang des Puffers.
6.  Kombinieren Sie das Beispiel aus dem Eingabepuffer mit dem Beispiel aus dem verzögerten Puffer.
7.  Kopieren Sie das Ergebnis in den Ausgabepuffer. Verschieben Sie dann den Ausgabepuffer Zeiger auf die nächste Einheit, um die nächste Schleifen Iterations Vorbereitung vorzubereiten.
8.  Wiederholen Sie den Vorgang, bis alle Beispiele verarbeitet wurden.

Wenn ein Eingabe Beispiel, das in Schritt 2 abgerufen wird, in den Verzögerungs Puffer in Schritt 4 kopiert wird, bleibt es so lange, bis der verschiebbare Zeiger durch die einzelnen Beispiele im Verzögerungs Puffer geht und schließlich an dieselbe Position zurückkehrt. Da die Größe des Verzögerungs Puffers so konzipiert ist, dass Sie mit der Verzögerungszeit übereinstimmt, wird die verstrichene Zeit zwischen dem Beispiel, das in den Verzögerungs Puffer kopiert wird, und dem abgerufenen Beispiel gleich der angegebenen Verzögerung (zuzüglich der von der eigentlichen Verarbeitung eingeführten Latenzzeit) wieder hergestellt.

Wenn ein Stream gestartet wird, werden keine Verzögerungs Daten generiert, bis die Verzögerungszeit verstrichen ist. Daher ist es wichtig, dass der Verzögerungs Puffer anfänglich den Ruhe Wert enthält. Wenn der Verzögerungs Puffer zufällige Daten enthält, hört der Benutzer das weiß Rauschen, bis das Plug-in genügend Verzögerungs Daten generiert, um den gesamten Verzögerungs Puffer zu überschreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über das Echo Beispiel**](echo-sample-overview.md)
</dt> </dl>

 

 




