---
title: Gerätetypen
description: Gerätetypen
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712966"
---
# <a name="device-types"></a>Gerätetypen

MCI erkennt einen grundlegenden Satz von *Gerätetypen*. Bei einem Gerätetyp handelt es sich um einen Satz von MCI-Treibern, die einen gemeinsamen Befehlssatz verwenden und zur Steuerung von ähnlichen Multimedia-Geräten oder Datendateien verwendet werden. Viele MCI-Befehle, wie z. b. [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), erfordern, dass Sie einen Gerätetyp angeben.

In der folgenden Tabelle sind die definierten Gerätetypen aufgeführt. Die aktuelle Implementierung von MCI enthält Befehls Sätze für eine Teilmenge dieser Geräte.



| Gerätetyp      | Konstante                      | BESCHREIBUNG                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **CDAudio**      | MCI \_ devtype \_ \_ -CD-Audiodatei       | CD-Audioplayer                                  |
| **Hütte**          | MCI \_ devtype- \_ DAT             | Digitaler audiobandplayer                        |
| **Digitalvideo** | digitales MCI \_ devtype- \_ \_ Video  | Digitales Video in einem Fenster (nicht GDI-basiert)        |
| **außer**        | MCI- \_ devtype \_ other           | Nicht definiertes MCI-Gerät                             |
| **Overlay**      | MCI \_ devtype- \_ Overlay         | Overlay-Gerät (Analog Video in einem Fenster)        |
| **scanner**      | MCI \_ devtype- \_ Scanner         | Bildscanner                                    |
| **sequencer**    | MCI \_ devtype \_ Sequencer       | MIDI-Sequencer                                   |
| **VCR**          | MCI \_ devtype \_ VCR             | Video-Kassettenrecorder oder Player                |
| **Videodisk**    | MCI \_ devtype- \_ Videodisk       | Videodisk-Player                                 |
| **waveaudiodatei**    | MCI \_ devtype \_ Waveform \_ -Audiodatei | Audiogerät, das digitalisierte Wellenform-Dateien wieder gibt |



 

In diesem Dokument sind die Namen der Gerätetypen fett formatiert. Gerätetyp Namen werden mit der Befehls Zeichenfolgen-Schnittstelle verwendet. Gerätetyp Konstanten werden mit der befehlsnachrichten Schnittstelle verwendet.

 

 




