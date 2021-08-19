---
title: Gerätetypen
description: Gerätetypen
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167eedddfc61960de35e979480c44b8f2efab5bf89738047446196b81a95a5b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497160"
---
# <a name="device-types"></a>Gerätetypen

MCI erkennt einen grundlegenden Satz von *Gerätetypen.* Ein Gerätetyp ist ein Satz von MCI-Treibern, die einen gemeinsamen Befehlssatz verwenden und zum Steuern ähnlicher Multimediageräte oder Datendateien verwendet werden. Viele MCI-Befehle, z. B. [**open**](open.md) ([**MCI \_ OPEN**](mci-open.md)), erfordern, dass Sie einen Gerätetyp angeben.

In der folgenden Tabelle sind die definierten Gerätetypen aufgeführt. Die aktuelle Implementierung von MCI enthält Befehlssätze für eine Teilmenge dieser Geräte.



| Gerätetyp      | Konstante                      | Beschreibung                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | MCI \_ DEVTYPE \_ CD \_ AUDIO       | CD-Audioplayer                                  |
| **Dat**          | MCI \_ DEVTYPE \_ DAT             | Digital-Audio-Bandplayer                        |
| **digitalvideo** | MCI \_ DEVTYPE \_ DIGITAL \_ VIDEO  | Digitales Video in einem Fenster (nicht GDI-basiert)        |
| **Andere**        | MCI \_ DEVTYPE \_ OTHER           | Nicht definiertes MCI-Gerät                             |
| **Overlay**      | MCI \_ DEVTYPE \_ OVERLAY         | Überlagerungsgerät (analoges Video in einem Fenster)        |
| **scanner**      | MCI \_ DEVTYPE \_ SCANNER         | Bildscanner                                    |
| **sequencer**    | MCI \_ DEVTYPE \_ SEQUENCER       | SEQUENCE-Sequencer                                   |
| **Vcr**          | MCI \_ DEVTYPE \_ VCR             | Video cassette recorder or player                |
| **videodisc**    | MCI \_ DEVTYPE \_ VIDEODISC       | Videodisc-Player                                 |
| **Waveaudio**    | MCI \_ DEVTYPE \_ WAVEFORM \_ AUDIO | Audiogerät, das digitalisierte Waveformdateien abspielt |



 

In diesem Dokument sind die Namen der Gerätetypen fett formatiert. Gerätetypnamen werden mit der Befehlszeichenfolgenschnittstelle verwendet. Gerätetypkonst constants werden mit der Befehlsmeldungsschnittstelle verwendet.

 

 




