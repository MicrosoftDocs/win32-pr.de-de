---
description: Ein Audioeffekt ist ein Objekt, das eingehende Audiodaten annimmt und vor der Übergabe einen Vorgang für die Daten ausführt. Sie können einen Effekt verwenden, um eine Vielzahl von Aufgaben auszuführen, z. B. das Hinzufügen von Hall zu einem Audiostream und das Überwachen von Spitzenlautstärken.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: XAudio2-Audioeffekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886edb81718f772f7dec31f799b1612ca701c2327468ad554fe80a17c1f69ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082854"
---
# <a name="xaudio2-audio-effects"></a>XAudio2-Audioeffekte

Ein Audioeffekt ist ein Objekt, das eingehende Audiodaten annimmt und vor der Übergabe einen Vorgang für die Daten ausführt. Sie können einen Effekt verwenden, um eine Vielzahl von Aufgaben auszuführen, z. B. das Hinzufügen von Hall zu einem Audiostream und das Überwachen von Spitzenlautstärken.

## <a name="effect-chains"></a>Effektketten

Jede XAudio2-Stimme kann eine Kette von Audioeffekten hosten. Sie können ein Array von [**XAUDIO2 \_ EFFECT \_ DESCRIPTOR-Strukturen**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) verwenden, um Effektketten anzugeben. Jeder Deskriptor enthält einen Zeiger auf ein Effektobjekt, das vom Client bereitgestellt wird. Diese Objekte müssen die APO-Schnittstellen (Audio Processing Object) implementieren. Weitere Informationen zum APO-Modell finden Sie in der [XAPO-Übersicht.](xapo-overview.md)

Effektketten können vom Client dynamisch geändert werden (während die XAudio2-Engine ausgeführt wird), Effekte können einzeln aktiviert oder deaktiviert werden, und Effektparameter können geändert werden – alles ohne Unterbrechung des Audios. Wenn sich ein Aspekt des Effektdiagramms ändert, optimiert XAudio2 das Diagramm erneut, um unnötige Verarbeitung zu vermeiden. Siehe [**IXAudio2Voice::SetEffectChain,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)und [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Nachdem ein Effekt an eine XAudio2-Stimme angefügt wurde, übernimmt XAudio2 die Kontrolle über den Effekt, und der Client sollte keine weiteren Aufrufe an ihn richten. Die einfachste Möglichkeit, dies sicherzustellen, besteht darin, alle Zeiger auf den Effekt freizugeben.

Die Effekte in der Effektkette einer bestimmten XAudio2-Stimme müssen Gleitkommaaudio mit der Verarbeitungsabtastrate dieser Stimme verarbeiten und erzeugen. Der einzige Aspekt des Audioformats, das sie ändern können, ist die Kanalanzahl (ein Halleffekt kann mono-Daten beispielsweise in 5,1 konvertieren). Der Client kann den [**XAUDIO2 \_ EFFECT \_ DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)verwenden.**OutputChannels-Feld,** um die Anzahl der Kanäle anzugeben, die jeder Effekt erzeugen soll. Die Effektkette schlägt fehl, wenn einer der Auswirkungen diese Anforderungen nicht erfüllen kann oder wenn ein Effekt eine Reihe von Kanälen erzeugt, die der nächste Effekt nicht verarbeiten kann. Alle [**IXAudio2Voice::EnableEffect-**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) oder [**IXAudio2Voice::D isableEffect-Aufrufe,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) die dazu führen, dass die Effektkette diese Anforderungen nicht mehr erfüllt, schlagen fehl.

APO-Schnittstellen, die in XAudio2 verwendet werden, müssen *destruktiv* sein. Dies bedeutet, dass sie immer alle Daten überschreiben, die sie in ihren Ausgabepuffern finden. Andernfalls kann die resultierende Audiodatei falsch sein, da XAudio2 keine Garantie dafür bietet, dass diese Puffer zuvor mit Stille initialisiert wurden.

## <a name="xaudio2-built-in-effects"></a>Integrierte XAudio2-Effekte

In der folgenden Tabelle sind die von XAudio2 bereitgestellten integrierten Audioeffekte und ihre Erstellungsmethoden aufgeführt. 

| Wirkung       | Erstellungsmethode                                              |
|--------------|--------------------------------------------------------------|
| Reverb       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Volumenzähler | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Ein Beispiel für das Erstellen und Verwenden einer Instanz eines Audioeffekts finden Sie unter [Vorgehensweise: Erstellen einer Effektkette.](how-to--create-an-effect-chain.md)

## <a name="custom-effects-in-xaudio2"></a>Benutzerdefinierte Effekte in XAudio2

Die [XAPO-API](xapo-overview.md) stellt ein Framework zum Erstellen benutzerdefinierter Audioeffekte bereit, die Sie in XAudio2 verwenden können. Ein Beispiel für das Erstellen eines benutzerdefinierten Effekts mit XAPO finden Sie unter [Vorgehensweise: Erstellen eines XAPO-Effekts.](how-to--create-an-xapo.md)

## <a name="xapo-effect-library-xapofx"></a>XAPO Effect Library (XAPOFX)

[XAPOFX](xapofx-overview.md) bietet eine zusätzliche Bibliothek mit XAPOs und einen gemeinsamen Mechanismus für deren Erstellung. Ein Beispiel für die Verwendung von XAPOFX mit XAudio2 finden Sie unter [Vorgehensweise: Verwenden von XAPOFX in XAudio2.](how-to--use-xapofx-in-xaudio2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 
