---
title: Funktionsweise des Echobeispiels
description: Funktionsweise des Echobeispiels
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Windows Media Player-Plug-Ins,Echo-Beispielübersicht
- Plug-Ins, Echo-Beispielübersicht
- Plug-Ins für die digitale Signalverarbeitung,Echobeispiel – Übersicht
- DSP-Plug-Ins,Echo-Beispielübersicht
- Echo DSP-Plug-In-Beispiel, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290cb56bbf1900dbcc09874213490f80cdc3af179ff243a2867bb232c3bb85c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338955"
---
# <a name="how-the-echo-sample-works"></a>Funktionsweise des Echobeispiels

Der Code erstellt den Echoeffekt, indem er einen Puffer zuteilt, der groß genug ist, um genau die Menge an Audiodaten zu enthalten, die in dem durch den Verzögerungszeitwert angegebenen Zeitrahmen gerendert werden können. Die Größe des Puffers wird mit der folgenden Formel in Bytes berechnet:

buffer size = delay time \* sample rate /1000 \* block alignment

Die Verzögerungszeit be liegt in Millisekunden. Die Werte für Die Stichprobenrate und Blockausrichtung werden in einer WAVEFORMATEX-Struktur angegeben. Die Stichprobenrate liegt in Stichproben pro Sekunde. Die Division durch 1.000 ergibt Stichproben pro Millisekunde. Die Blockausrichtung entspricht dem Produkt der Anzahl von Kanälen (1 für Mono, 2 für Stereo) und der Anzahl der Bits pro Stichprobe (8 oder 16) dividiert durch 8 (Bits pro Byte).

Zusätzlich zur Zeigervariablen, die auf den Kopf des Verzögerungspuffers zeigt, erstellt der Code einen verschiebbaren Zeiger, der die Daten im Puffer in der Synchronisierung mit der Verarbeitungsschleife in der **DoProcessOutput-Funktion** durchfingt. Wenn der verschiebbare Zeiger das Ende des Verzögerungspuffers erreicht, wird er zurück an den Kopf des Puffers bewegt. Ein auf diese Weise verwendeter Puffer wird als zirkulärer Puffer bezeichnet.

Sobald der Verzögerungspuffer vorhanden ist und Windows Media Player einen Eingabepuffer zugeordnet hat, um Audiodaten und einen Ausgabepuffer zum Empfangen verarbeiteter Audiodaten zu erhalten, wird die Echoverarbeitung wie die folgenden fortgesetzt:

1.  Geben Sie eine Schleife ein, die die Verarbeitung jedes Audiobeispiels im Eingabepuffer ermöglicht.
2.  Rufen Sie ein Beispiel aus dem Eingabepuffer ab. Bewegen Sie dann den Eingabepufferzeiger zum nächsten Beispiel, um die nächste Schleifeniteration vorzubereiten.
3.  Rufen Sie ein Beispiel aus dem Verzögerungspuffer ab.
4.  Kopieren Sie das Beispiel aus dem Eingabepuffer an die gleiche Position im Verzögerungspuffer, aus dem die letzte Verzögerungsstichprobe abgerufen wurde.
5.  Bewegen Sie den Verzögerungspufferzeiger zum nächsten Beispiel. Wenn der Zeiger über das Ende des Puffers hinaus bewegt wird, verschieben Sie ihn an den Kopf des Puffers.
6.  Kombinieren Sie das Beispiel aus dem Eingabepuffer mit dem Beispiel aus dem Verzögerungspuffer.
7.  Kopieren Sie das Ergebnis in den Ausgabepuffer. Verschieben Sie dann den Ausgabepufferzeiger zur nächsten Einheit, um sich auf die nächste Schleifeniteration vorzubereiten.
8.  Wiederholen Sie den Vorgang, bis alle Beispiele verarbeitet wurden.

Wenn ein in Schritt 2 abgerufenes Eingabebeispiel in den Verzögerungspuffer in Schritt 4 kopiert wird, bleibt es dort, bis der verschiebbare Zeiger die einzelnen Stichproben im Verzögerungspuffer durchschritt und schließlich an die gleiche Position zurückkehrt. Da die Größe des Verzögerungspuffers der Verzögerungszeit entspricht, entspricht die verstrichene Zeit zwischen dem Kopieren des Beispiels in den Verzögerungspuffer und dem erneuten Abrufen der Stichprobe der angegebenen Verzögerung (zuzüglich der Latenz, die durch die tatsächliche Verarbeitung eingeführt wird).

Wenn ein Stream gestartet wird, werden keine Verzögerungsdaten generiert, bis die Verzögerungszeit abgelaufen ist. Daher ist es wichtig, dass der Verzögerungspuffer anfänglich Stille enthält. Wenn der Verzögerungspuffer zufällige Daten enthält, wird der Benutzer ein weißes Rauschen hören, bis das Plug-In genügend Verzögerungsdaten generiert, um den gesamten Verzögerungspuffer zu überschreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echo-Beispiel – Übersicht**](echo-sample-overview.md)
</dt> </dl>

 

 




