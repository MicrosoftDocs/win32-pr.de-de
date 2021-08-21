---
title: Funktionsweise des Echobeispiels
description: Funktionsweise des Echobeispiels
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Windows Media Player-Plug-Ins, Echobeispiel – Übersicht
- Plug-Ins, Echo-Beispiel – Übersicht
- Digitale Signalverarbeitungs-Plug-Ins, Echobeispiel – Übersicht
- Übersicht über DSP-Plug-Ins, Echo-Beispiel
- Echo-DSP-Plug-In-Beispiel, Informationen
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

Der Code erstellt den Echoeffekt, indem ein Puffer zugewiesen wird, der groß genug ist, um genau die Menge an Audiodaten zu enthalten, die in dem durch den Verzögerungszeitwert angegebenen Zeitrahmen gerendert werden können. Die Größe des Puffers wird in Byte anhand der folgenden Formel berechnet:

Puffergröße = Verzögerungszeit \* –Abtastrate /1000 \* Blockausrichtung

Die Verzögerungszeit beträgt in Millisekunden. Die Werte für die Abtastrate und blockausrichtung werden in einer WAVEFORMATEX-Struktur angegeben. Die Abtastrate ist in Stichproben pro Sekunde enthalten. Division durch 1.000 ergibt Stichproben pro Millisekunde. Die Blockausrichtung entspricht dem Produkt der Anzahl der Kanäle (1 für Mono, 2 für Stereo) und der Anzahl der Bits pro Stichprobe (8 oder 16) geteilt durch 8 (Bits pro Byte).

Zusätzlich zur Zeigervariablen, die auf den Kopf des Verzögerungspuffers zeigt, erstellt der Code einen verschiebbaren Zeiger, der die Daten im Puffer in Synchronisierung mit der Verarbeitungsschleife in der **DoProcessOutput-Funktion** durchläuft. Wenn der verschiebbare Zeiger das Ende des Verzögerungspuffers erreicht, wird er zurück an den Kopf des Puffers verschoben. Ein auf diese Weise verwendeter Puffer wird als Kreispuffer bezeichnet.

Sobald der Verzögerungspuffer vorhanden ist und Windows Media Player einen Eingabepuffer für die Bereitstellung von Audiodaten und einen Ausgabepuffer zum Empfangen verarbeiteter Audiodaten zugeordnet hat, wird die Echoverarbeitung wie folgt fortgesetzt:

1.  Geben Sie eine Schleife ein, die die Verarbeitung jedes Audiobeispiels im Eingabepuffer ermöglicht.
2.  Rufen Sie ein Beispiel aus dem Eingabepuffer ab. Verschieben Sie dann den Eingabepufferzeiger nach vorn zum nächsten Beispiel, um sich auf die nächste Schleifeniteration vorzubereiten.
3.  Rufen Sie ein Beispiel aus dem Verzögerungspuffer ab.
4.  Kopieren Sie das Beispiel aus dem Eingabepuffer an den gleichen Speicherort im Verzögerungspuffer, von dem das letzte Verzögerungsbeispiel abgerufen wurde.
5.  Verschieben Sie den Verzögerungspufferzeiger vorwärts zum nächsten Beispiel. Wenn der Zeiger über das Ende des Puffers hinaus bewegt wird, verschieben Sie ihn an den Kopf des Puffers.
6.  Kombinieren Sie das Beispiel aus dem Eingabepuffer mit dem Beispiel aus dem Verzögerungspuffer.
7.  Kopieren Sie das Ergebnis in den Ausgabepuffer. Verschieben Sie dann den Ausgabepufferzeiger auf die nächste Einheit, um sich auf die nächste Schleifeniteration vorzubereiten.
8.  Wiederholen Sie den Vorgang, bis alle Stichproben verarbeitet wurden.

Wenn ein in Schritt 2 abgerufenes Eingabebeispiel in Schritt 4 in den Verzögerungspuffer kopiert wird, bleibt es dort, bis der verschiebbare Zeiger jedes Beispiel im Verzögerungspuffer durchschritt und schließlich an die gleiche Position zurückkehrt. Da die Größe des Verzögerungspuffers der Verzögerungszeit entspricht, entspricht die verstrichene Zeit zwischen dem Kopieren des Samplings in den Verzögerungspuffer und dem erneuten Abrufen des Beispiels der angegebenen Verzögerung (zuzüglich der Latenzzeit, die durch die tatsächliche Verarbeitung entsteht).

Wenn ein Stream gestartet wird, werden keine Verzögerungsdaten generiert, bis die Verzögerungszeit verstrichen ist. Daher ist es wichtig, dass der Verzögerungspuffer anfänglich Stille enthält. Wenn der Verzögerungspuffer zufällige Daten enthält, wird der Benutzer weiß rauschen, bis das Plug-In genügend Verzögerungsdaten generiert, um den gesamten Verzögerungspuffer zu überschreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echobeispiel – Übersicht**](echo-sample-overview.md)
</dt> </dl>

 

 




