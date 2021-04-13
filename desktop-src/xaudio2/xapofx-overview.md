---
description: Xapofx ist eine Sammlung von Audioeffekten, die die xapo-Schnittstellen für die Verwendung in XAudio2 implementieren. Xapofx enthält mehrere Effekte und einen allgemeinen Mechanismus zum Erstellen von Effekt Instanzen.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Übersicht über xapofx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8979b5de50406d46bc472e18ca4a6479679e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526873"
---
# <a name="xapofx-overview"></a>Übersicht über xapofx

Xapofx ist eine Sammlung von Audioeffekten, die die [xapo](xapo-overview.md) -Schnittstellen für die Verwendung in XAudio2 implementieren. Xapofx enthält mehrere Effekte und einen allgemeinen Mechanismus zum Erstellen von Effekt Instanzen.

## <a name="included-effects"></a>Enthaltene Effekte

In der folgenden Tabelle werden die in xapofx enthaltenen Effekte beschrieben. 

| Auswirkung             | Beschreibung                                                                                                                                                                                           | Parameter Struktur                                                     | Parameter Konstanten                                              | Anforderungen                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Fxecho             | Ein Echo Effekt.                                                                                                                                                                                       | [**fxecho- \_ Parameter**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**Fxecho-Konstanten**](fxecho-constants.md)                     | Unterstützt nur float32-Audioformate.                                                                                      |
| F               | Ein vier-Band-Equalizer.                                                                                                                                                                                | [**f- \_ Parameter**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**Sxeq-Konstanten**](fxeq-constants.md)                         | Unterstützt nur float32-Audioformate. Die Stichprobenrate muss zwischen 22.000 Hz und 48.000 Hz liegen.                             |
| Fxmasteringlimiter | Eine volumebegrenzung.                                                                                                                                                                                     | [**fxmasteringlimiter- \_ Parameter**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**Fxmasteringlimit-Konstanten**](fxmasteringlimit-constants.md) | Unterstützt nur float32-Audioformate.                                                                                      |
| Fxreverb           | Ein einfacher einhall Effekt.<br/> XAudio2 bietet auch eine Auswirkung der Implementierung von "Princeton Digital Reverb", die mit [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)instanziiert werden kann.<br/> | [**fxreverb- \_ Parameter**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**Fxreverb-Konstanten**](fxreverb-constants.md)                 | Unterstützt nur float32-Audioformate. Außerdem unterstützt Sie nur Mono-Eingaben in Mono-Ausgabe und Stereo Eingaben für die Stereoausgabe. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Erstellen einer Instanz eines Effekts, der in xapofx enthalten ist

Xapofx stellt die Funktion " [**anatefx**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) " als allgemeinen Mechanismus zum Erstellen von Effekt Instanzen bereit. " **Kreatefx** " nimmt die CLSID eines Effekts an und gibt einen IUnknown-Schnittstellen Zeiger auf eine Instanz des Effekts zurück.

## <a name="using-xapofx-in-xaudio2"></a>Verwenden von xapofx in XAudio2

Effekte, die mit " [**kreatefx**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) " instanziiert werden, werden in XAudio2 verwendet, indem Sie an Stimmen angehängt werden. Jede XAudio2-Stimme hat eine Wirkungskette, die NULL oder mehr Audioeffekte enthält. Audiodaten, die an eine Stimme gesendet werden, werden durch jeden Effekt in der Kette geleitet, bevor Sie an die Ausgabe Ziele der Stimme gesendet werden. Die Stimme nimmt die Ausgabe jedes Effekts an und fügt Sie in den nächsten Effekt in der Kette ein, bis keine Auswirkungen mehr in der Kette vorhanden sind. Wenn Sie einen xapofx-Effekt an eine XAudio2-Stimme anfügen möchten, füllen Sie eine [**XAudio2- \_ Effekt \_ Ketten**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) Struktur mit den Informationen des Effekts aus, und übergeben Sie Sie an [**IXAudio2Voice::**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)"".

Weitere Informationen zu XAudio2 Effect-Ketten finden Sie unter [XAudio2-Audioeffekte](xaudio2-audio-effects.md).

Ein Beispiel für die Verwendung von xapofx in XAudio2 finden Sie unter Gewusst [wie: Verwenden von xapofx in XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="xaudio2-implicit-effects"></a>Implizite XAudio2-Effekte

Zusätzlich zu der Bibliothek von xapos, die von xapofx bereitgestellt wird, verfügt XAudio2 über integrierte Zuordnungs-und volumemessungseffekte. Sie können diese integrierten Effekte mit [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) und [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)erstellen. Ein Beispiel für die Verwendung einer dieser integrierten Effekte finden Sie [unter Gewusst wie: Erstellen einer Wirkungskette](how-to--create-an-effect-chain.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> </dl>

 

 
