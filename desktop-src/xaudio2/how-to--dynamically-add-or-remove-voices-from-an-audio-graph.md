---
description: Sie können audiodiagramme jederzeit ändern, um Stimmen oder gesamte unter Diagramme hinzuzufügen oder zu entfernen.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: "So wird's gemacht: Dynamisches Hinzufügen und Entfernen von Stimmen zu bzw. aus einem Audiodiagramm"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129768"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a>So wird's gemacht: Dynamisches Hinzufügen und Entfernen von Stimmen zu bzw. aus einem Audiodiagramm

Sie können audiodiagramme jederzeit ändern, um Stimmen oder gesamte unter Diagramme hinzuzufügen oder zu entfernen. In diesem Thema wird gezeigt, wie Sie Teilmengen Stimmen aus einem Diagramm hinzufügen oder entfernen, das nach den Schritten in Gewusst [wie: Erstellen eines einfachen audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)erstellt wurde. Eine einzelne Stimme kann Ihre Ausgabe an mehrere Stimmen oder an eine lange Reihe von Stimmen senden. Das Entfernen oder Hinzufügen einer einzelnen Stimme kann eine große Auswirkung auf ein audiodiagramm haben.

## <a name="to-dynamically-change-an-audio-graph"></a>So ändern Sie ein audiodiagramm dynamisch

Das Hinzufügen und Entfernen von Stimmen aus einem audiodiagramm ähnelt dem Hinzufügen oder Entfernen von Knoten aus einer einzelnen verknüpften Liste oder einem einzelnen verknüpften Diagramm.

-   So fügen Sie einem audiodiagramm eine Stimme oder ein unter Diagramm hinzu

    Legen Sie die Ausgabe einer Stimme im Diagramm, der übergeordneten Stimme, auf die Stimme fest, die mit der [**setoutputvoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) -Funktion hinzugefügt werden soll. Legen Sie die Ausgabe der neuen Stimme auf das ursprüngliche untergeordnete Element der übergeordneten Stimme fest.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   So entfernen Sie eine Stimme oder ein unter Diagramm aus einem audiodiagramm

    Legen Sie die Ausgabesprache des übergeordneten Elements der zu entfernenden Stimme auf das untergeordnete Element der zu entfernenden Stimme fest. Wenn sich die zu entfernende Stimme am Ende des Diagramms befindet, sollte die übergeordnete Stimme so geändert werden, dass Sie auf die Master Stimme verweist.

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

Beachten Sie, dass für die Übersichtlichkeit jedes übergeordnete Element in diesen Beispielen nur ein untergeordnetes Wenn ein übergeordneter Knoten über mehrere untergeordnete Knoten verfügt, enthält seine sendlist anstelle eines Zeigers nur eine Stimme ein Array von Stimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiodiagramme](audio-graphs.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[So wird's gemacht: Verwenden von Submixstimmen](how-to--use-submix-voices.md)
</dt> <dt>

[So wird's gemacht: Erstellen einer Effektkette](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
