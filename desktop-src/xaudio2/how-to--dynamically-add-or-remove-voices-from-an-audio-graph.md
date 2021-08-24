---
description: Sie können Audiographen jederzeit ändern, um Stimmen oder ganze Untergraphen hinzuzufügen oder zu entfernen.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: "So wird's gemacht: Dynamisches Hinzufügen und Entfernen von Stimmen zu bzw. aus einem Audiodiagramm"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a49cfc88e89884b63484b7bd58f7f5d96020cd21f8d1147794b840f00258fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082934"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a>So wird's gemacht: Dynamisches Hinzufügen und Entfernen von Stimmen zu bzw. aus einem Audiodiagramm

Sie können Audiographen jederzeit ändern, um Stimmen oder ganze Untergraphen hinzuzufügen oder zu entfernen. In diesem Thema erfahren Sie, wie Sie Untermischungsstimmen zu einem Diagramm hinzufügen oder daraus entfernen, das mit den Schritten unter [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md). Eine einzelne Stimme kann ihre Ausgabe an mehrere Stimmen oder an eine lange Stimmenkette senden. Das Entfernen oder Hinzufügen einer einzelnen Stimme kann einen großen Einfluss auf ein Audiodiagramm haben.

## <a name="to-dynamically-change-an-audio-graph"></a>So ändern Sie ein Audiodiagramm dynamisch

Das Hinzufügen und Entfernen von Stimmen aus einem Audiographen ähnelt dem Hinzufügen oder Entfernen von Knoten aus einer einzelnen verknüpften Liste oder einem diagramm.

-   So fügen Sie einem Audiodiagramm eine Stimme oder einen Untergraphen hinzu

    Legen Sie die Ausgabe einer Stimme im Diagramm( der übergeordneten Stimme) auf die Stimme fest, die mithilfe der [**SetOutputVoices-Funktion hinzugefügt werden**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) soll. Legen Sie die Ausgabe der neuen Stimme auf das ursprüngliche untergeordnete Element der übergeordneten Stimme fest.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   So entfernen Sie eine Stimme oder einen Untergraphen aus einem Audiographen

    Legen Sie die Ausgangsstimme des übergeordneten Elements der Stimme, die entfernt wird, auf das untergeordnete Element der zu entfernenden Stimme fest. Wenn sich die zu entfernende Stimme am Ende des Diagramms befindet, sollte die übergeordnete Stimme so geändert werden, dass sie auf die Masterstimme zeigt.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

Beachten Sie, dass aus Gründen der Übersichtlichkeit jedes übergeordnete Element in diesen Beispielen nur über ein untergeordnetes Element verfügt. Wenn ein übergeordneter Knoten mehrere übergeordnete Knoten hat, enthält die Sendeliste ein Array von Stimmen anstelle eines Zeigers auf nur eine Stimme.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiographen](audio-graphs.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[So wird's gemacht: Verwenden von Submixstimmen](how-to--use-submix-voices.md)
</dt> <dt>

[So wird's gemacht: Erstellen einer Effektkette](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
