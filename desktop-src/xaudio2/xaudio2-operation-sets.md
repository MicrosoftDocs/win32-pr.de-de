---
description: In dieser Übersicht werden mehrere XAudio2-Methoden vorgestellt, die Sie als Teil eines Vorgangssatzes aufrufen können.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: XAudio2-Vorgangssätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a7f16edfa461d9944691bc4535debc05f820150dadf746caece85cb68c9f97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089410"
---
# <a name="xaudio2-operation-sets"></a>XAudio2-Vorgangssätze

In dieser Übersicht werden mehrere XAudio2-Methoden vorgestellt, die Sie als Teil eines Vorgangssatzes aufrufen können.

Mehrere XAudio2-Methoden verwenden das *OperationSet-Argument,* mit dem sie als Teil einer verzögerten Gruppe aufgerufen werden können. Zu einem bestimmten Zeitpunkt können Sie eine ganze Gruppe von Änderungen gleichzeitig anwenden, indem Sie die Funktion [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit dem *OperationSet-Bezeichner* für diese Gruppe aufrufen. Der Bezeichner ist eine beliebige Zahl. Daher ermöglicht es separaten Teilen des Clientcodes, separate atomare Änderungen ohne Konflikte auf das Diagramm anzuwenden. Es wird empfohlen, dass der Client einen globalen Indikator erhöht,  wenn er einen eindeutigen neuen OperationSet-Bezeichner generieren muss. Eine Reihe von Änderungen am Diagramm, die atomisch angewendet werden, ist garantiert stichprobengenau. Beispielsweise werden Stimmen synchron gestartet.

Wenn Sie *OperationSet* auf XAUDIO2 \_ COMMIT NOW \_ festlegen, wird die Änderung sofort angewendet. Sie wird im ersten Audioverarbeitungsdurchlauf nach dem Methodenaufruf wirksam. Wenn Sie [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit XAUDIO2 \_ COMMIT ALL \_ aufrufen, werden Änderungen an allen ausstehenden Vorgangssätzen unabhängig von ihrem *OperationSet-Bezeichner* ausgeführt.

Bestimmte Methoden werden sofort wirksam, wenn sie von einem XAudio2-Rückruf mit einem *OperationSet* von XAUDIO2 COMMIT NOW aufgerufen \_ \_ werden. Alle anderen Methoden, die ein *OperationSet-Argument* annehmen, werden erst beim nächsten Verarbeitungsdurchlauf wirksam, nachdem die Methode aufgerufen wurde (wenn sie mit XAUDIO2 COMMIT NOW aufgerufen \_ \_ wird) oder nachdem [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit demselben *OperationSet* aufgerufen wurde. Aus diesem Grund erfolgen bestimmte Methodenaufrufe möglicherweise nicht immer in derselben Reihenfolge, in der sie aufgerufen wurden.

Alle ausstehenden Vorgänge werden atomisch ausgeführt, wenn [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) aufgerufen wird. Alle Methoden, die aufgerufen werden, während die Engine beendet wird, werden sofort wirksam, unabhängig vom bereitgestellten *OperationSet-Wert.* Wenn Sie die Engine neu starten, kehrt XAudio2 in den asynchronen Modus zurück.

Einfache Szenarien, in denen Vorgangssätze nützlich sind, sind die folgenden Beispiele.

-   Gleichzeitiges Starten mehrerer Stimmen.
-   Gleichzeitiges Übermitteln eines Puffers an eine Stimme, Festlegen der Sprachparameter und Starten der Stimme.
-   Vornehmen einer umfangreichen Änderung des Diagramms, z. B. das Verbinden aller Quellstimmen mit einer neuen Submixstimme.

Ein Beispiel für die Verwendung eines Vorgangssatzes finden Sie unter Vorgehensweise: Gruppieren von [Audiomethoden als Vorgangssatz.](how-to--group-audio-methods-as-an-operation-set.md)

## <a name="operation-set-methods"></a>Vorgangssatzmethoden

Sie können die folgenden Methoden als Teil eines Vorgangssatzes aufrufen.

-   [**IXAudio2SourceVoice::ExitLoop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice::Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Wie zuvor beschrieben, muss Clientcode letztendlich die Funktion [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) aufrufen, um die verzögerten Änderungen auszuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorgangssätze](operation-sets.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
