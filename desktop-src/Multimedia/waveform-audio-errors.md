---
title: Waveform-Audio Fehler
description: Waveform-Audio Fehler
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Mcierr-Rückgabewerte, Waveform-Audiofehler
- Multimedia-Referenz, Waveform-Audiofehler
- Referenz für Multimedia-, Waveform-Audiofehler
- Media Control Interface (MCI), Waveform-Audiofehler
- MCI (Medien Steuerungs Schnittstelle), Waveform-Audiofehler
- Referenz für MCI, Waveform-Audiofehler
- MCI-Referenz, Waveform-Audiofehler
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- Waveform-Audiofehler
- MCI-Waveform-Audiofehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036557"
---
# <a name="waveform-audio-errors"></a>Waveform-Audio Fehler

Die folgenden zusätzlichen Rückgabewerte werden für MCI-Waveform-Audiogeräte definiert:



| Wert                             | Bedeutung                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mcierr \_ Wave \_ inputsinuse         | Alle Wellenform-Geräte, die Dateien im aktuellen Format aufzeichnen können, werden verwendet. Warten Sie, bis eines dieser Geräte kostenlos ist. versuchen Sie es dann erneut.                              |
| mcierr \_ Wave \_ inputsungeeig    | Kein installiertes Wellenform-Gerät kann Dateien im aktuellen Format aufzeichnen. Verwenden Sie die Option Drivers in der Systemsteuerung, um ein geeignetes Wellen Formular-Aufzeichnungsgerät zu installieren. |
| mcierr \_ Wave \_ inputunspezifiziert    | Sie können ein beliebiges kompatibles Wellen Formular-Aufzeichnungsgerät angeben.                                                                                                           |
| mcierr \_ Wave \_ outputsinuse        | Alle Wellenform-Geräte, die Dateien im aktuellen Format wiedergeben können, werden verwendet. Warten Sie, bis eines dieser Geräte kostenlos ist. versuchen Sie es dann erneut.                                |
| mcierr \_ Wave \_ outputsunpassend   | Kein installiertes Wellenform-Gerät kann Dateien im aktuellen Format wiedergeben. Verwenden Sie die Option Drivers in der Systemsteuerung, um ein geeignetes Wellenform-Gerät zu installieren.             |
| mcierr \_ Wave \_ outputunspezifiziert   | Sie können ein beliebiges kompatibles Wellenform Wiedergabe Gerät angeben.                                                                                                            |
| mcierr \_ Wave * \_ tinputinuse       | Das aktuelle Wellenform-Gerät wird verwendet. Warten Sie, bis das Gerät kostenlos ist. versuchen Sie dann erneut, das Gerät für die Aufzeichnung festzulegen.                                              |
| mcierr \_ Wave * \_ tinputungeeignet  | Das Gerät, das Sie verwenden, um eine Wellenform aufzuzeichnen, kann das Datenformat nicht erkennen.                                                                                     |
| mcierr \_ Wave \_ setoutputinuse      | Das aktuelle Wellenform-Gerät wird verwendet. Warten Sie, bis das Gerät kostenlos ist. versuchen Sie dann erneut, das Gerät für die Wiedergabe festzulegen.                                               |
| mcierr \_ Wave \_ setoutputungeeignet | Das Gerät, das Sie verwenden, um eine Wellenform wiederzugeben, kann das Datenformat nicht erkennen.                                                                                   |



 

 

 




