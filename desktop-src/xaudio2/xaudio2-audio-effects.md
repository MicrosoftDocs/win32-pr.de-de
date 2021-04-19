---
description: Ein Audioeffekt ist ein Objekt, das eingehende Audiodaten annimmt und vor der Übergabe einen Vorgang für die Daten ausführt. Sie können einen Effekt verwenden, um eine Vielzahl von Aufgaben auszuführen, einschließlich Hinzufügen von Hall zu einem Audiostream und Überwachen von Spitzen Volumen Ebenen.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: XAudio2-Audioeffekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8de87a65ea4321b5e8d73a837f79a3e56e8e3a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350479"
---
# <a name="xaudio2-audio-effects"></a>XAudio2-Audioeffekte

Ein Audioeffekt ist ein Objekt, das eingehende Audiodaten annimmt und vor der Übergabe einen Vorgang für die Daten ausführt. Sie können einen Effekt verwenden, um eine Vielzahl von Aufgaben auszuführen, einschließlich Hinzufügen von Hall zu einem Audiostream und Überwachen von Spitzen Volumen Ebenen.

## <a name="effect-chains"></a>Effektketten

Jede XAudio2-Stimme kann eine Kette von Audioeffekten hosten. Sie können ein Array von [**XAUDIO2 \_ Effect- \_ deskriptorstrukturen**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) verwenden, um Effektketten anzugeben. Jeder Deskriptor enthält einen Zeiger auf ein vom Client bereitgestelltes Effekt Objekt. Diese Objekte müssen die APO-Schnittstellen (Audioprocessing Object) implementieren. Weitere Informationen zum APO-Modell finden Sie in der [Übersicht über xapo](xapo-overview.md) .

Effektketten können dynamisch vom Client geändert werden (während die XAudio2-Engine ausgeführt wird), Effekte können einzeln aktiviert oder deaktiviert werden, und die Auswirkung von Parametern kann geändert werden – ohne jegliche Unterbrechung der Audiodatei. Wenn sich ein Aspekt des Effekt Diagramms ändert, optimiert XAudio2 das Diagramm erneut, um unnötige Verarbeitungsvorgänge zu vermeiden. Weitere Informationen finden Sie unter [**IXAudio2Voice:: seteffectchain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice:: enableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)und [**IXAudio2Voice:: seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Nachdem ein Effekt an eine XAudio2 Voice angefügt wurde, übernimmt XAudio2 die Kontrolle über den Effekt, und der Client sollte keine weiteren Aufrufe an ihn ausführen. Die einfachste Möglichkeit, dies sicherzustellen, besteht darin, alle Zeiger auf den Effekt freizugeben.

Die Auswirkungen in der Wirkungskette einer bestimmten XAudio2-Stimme müssen in der Verarbeitungs Stichprobenrate dieser Stimme Gleit Komma-Audiodaten verarbeiten und erzeugen. Der einzige Aspekt des Audioformats, den Sie ändern können, ist die Anzahl der Kanäle (z. b. kann ein Hall-Effekt Mono-Daten in 5,1 konvertieren). Der Client kann den [**XAUDIO2 \_ Effect- \_ Deskriptor**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)verwenden.**Outputchannels** -Feld, um die Anzahl von Kanälen anzugeben, die von den einzelnen Effekten erzeugt werden sollen. Die Effekt Kette schlägt fehl, wenn eine der Effekte diese Anforderungen nicht erfüllen kann, oder wenn ein Effekt eine Reihe von Kanälen erzeugt, die der nächste Effekt nicht verarbeiten kann. Alle [**IXAudio2Voice:: enableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) -oder [**IXAudio2Voice::D isableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) -Aufrufe, die bewirken, dass die Auswirkung-Kette diese Anforderungen nicht mehr erfüllt, schlägt fehl.

Die in XAudio2 verwendeten APO-Schnittstellen müssen *destruktiv* sein. Dies bedeutet, dass Sie immer alle Daten überschreiben, die Sie in ihren Ausgabe Puffern finden. Andernfalls ist die resultierende Audiodatei möglicherweise falsch, da XAudio2 keine Garantie dafür macht, dass diese Puffer zuvor mit dem Ruhe Wert initialisiert wurden.

## <a name="xaudio2-built-in-effects"></a>Integrierte XAudio2-Effekte

In der folgenden Tabelle sind die integrierten Audioeffekte aufgeführt, die von XAudio2 und deren Erstellungs Methoden bereitgestellt werden. 

| Wirkung       | Erstellungsmethode                                              |
|--------------|--------------------------------------------------------------|
| Hall       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Volumemeter | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Ein Beispiel für das Erstellen und Verwenden einer Instanz eines Audioeffekts finden Sie unter Gewusst [wie: Erstellen einer Wirkungskette](how-to--create-an-effect-chain.md).

## <a name="custom-effects-in-xaudio2"></a>Benutzerdefinierte Effekte in XAudio2

Die [xapo](xapo-overview.md) -API bietet ein Framework zum Erstellen von benutzerdefinierten Audioeffekten, die Sie in XAudio2 verwenden können. Ein Beispiel für das Erstellen eines benutzerdefinierten Effekts mit xapo finden [Sie unter Gewusst wie: Erstellen eines xapo](how-to--create-an-xapo.md)-Effekts.

## <a name="xapo-effect-library-xapofx"></a>Xapo-Effekt Bibliothek (xapofx)

[Xapofx](xapofx-overview.md) bietet eine zusätzliche Bibliothek von xapos und einen allgemeinen Mechanismus zum Erstellen dieser Dateien. Ein Beispiel für die Verwendung von xapofx mit XAudio2 finden Sie unter Gewusst [wie: Verwenden von xapofx in XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 
