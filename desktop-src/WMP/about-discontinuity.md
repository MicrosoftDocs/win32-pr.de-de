---
title: Informationen zur Diskontinuität
description: Informationen zur Diskontinuität
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Windows Media Player-Plug-Ins, Audio-DSP
- Plug-Ins, Audio-DSP
- Digitale Signalverarbeitungs-Plug-Ins, Diskontinuität von Audio
- DSP-Plug-Ins, Diskontinuität bei Audio
- Audio-DSP-Plug-Ins, Diskontinuität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40de4c75c2d17699f0c72416873d64177e47d81761b27e5ffd465d89c9ecb9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903570"
---
# <a name="about-discontinuity"></a>Informationen zur Diskontinuität

Windows Media Player können jederzeit eine Unterbrechung im Eingabestream signalisieren, indem sie die **IMediaObject::D iscontinuity-Methode** aufrufen. Dies geschieht routinemäßig am Anfang und Ende eines Streams sowie vor jedem Suchvorgang oder beim Unterbrechen von Streaminginhalten aus irgendeinem Grund. Das DSP-Beispiel-Plug-In, das vom Assistenten für Windows Media Player Plug-In generiert wird, muss aus folgenden Gründen nicht mit Diskontinuitäten umgehen:

-   PCM-Beispiele sind atomar, d.h. sie können ohne Berücksichtigung der anderen Stichproben im Stream verarbeitet werden. Einige Videoformate enthalten Daten, die von Keyframes und komprimierten Beispielen abhängen.
-   Der Beispielcode wird so geschrieben, dass der Client immer die Verarbeitung der gesamten Ausgabe erzwingen muss, bevor das Plug-In weitere Eingaben akzeptiert.

Die Standardimplementierungen von **IMediaObject::D iscontinuity** geben einfach S \_ OK zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Audio-DSP-Plug-Ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




