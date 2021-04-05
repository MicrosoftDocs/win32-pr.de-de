---
title: Informationen zu MIDI
description: Informationen zu MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows Multimedia, Digital Instrumentation Digital Interface (MIDI)
- Multimedia, Digital Instrumentation Digital Interface (MIDI)
- Multimedia-Audiodatei, Digital Instrumentation Digital Interface (MIDI)
- Audioschnittstelle (Digital Instrumentation Digital Interface, MIDI)
- Digital Instrumentation Digital Interface (MIDI), Informationen zu
- MIDI (Digital Instrumentation Digital Interface), Informationen zu
- Digital Instrumentation Digital Interface (MIDI), Media Control Interface (MCI)
- MIDI (Digital Instrumentation Digital Interface), Medien Steuerungs Schnittstelle (MCI)
- Digital Instrumentation Digital Interface (MIDI), Streampuffer
- MIDI (Digital Instrumentation Digital Interface), Streampuffer
- Digital Instrumentation Digital Interface (MIDI), MIDI-Dienste
- MIDI (Digital Instrumentation Digital Interface), MIDI-Dienste
- Media Control Interface (MCI), Digital Instrumentation Digital Interface (MIDI)
- MCI (Media Control Interface), Digital Instrumentation Digital Interface (MIDI)
- Streampuffer, Informationen
- MIDI-Dienste, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708927"
---
# <a name="about-midi"></a>Informationen zu MIDI

Die Microsoft Win32-API (Application Programming Interface) bietet die folgenden Methoden für Anwendungen, um mit den Daten von MIDI zu arbeiten:

-   Die Media Control Interface (MCI). Die einfachste Möglichkeit zum Wiedergeben einer MIDI-Datei ist die Verwendung der mciwnd-Fenster Klasse, Sie können jedoch auch MCI-Befehle verwenden, um eine benutzerdefinierte Schnittstelle zu einem MIDI-Gerät zu erstellen. Weitere Informationen zur mciwnd-Fenster Klasse finden Sie unter [mciwnd Window Class](mciwnd-window-class.md). Weitere Informationen zu MCI finden Sie unter [MCI](mci.md)oder [Media Control Interface (MCI)](media-control-interface--mci.md).
-   [Streampuffer](stream-buffers.md). Dieses Format ermöglicht es einer Anwendung, Puffer von mit Zeitstempel versehene MIDI-Daten für die Wiedergabe zu bearbeiten. Streampuffer sind für Anwendungen nützlich, die eine präzisere Kontrolle über die Ausgabe benötigen als MCI bietet.
-   [MIDI-Dienste](midi-services.md). Anwendungen, die die präzisere Kontrolle über die Daten von MIDI benötigen, verwenden normalerweise diese Dienste auf niedriger Ebene.

In den folgenden Themen wird jede dieser Methoden beschrieben, und es wird eine Übersicht über den MIDI-Mapper bereitstellt.

-   [Der MIDI-Mapper](the-midi-mapper.md)
-   [Medien Steuerungs Schnittstelle (MCI)](media-control-interface--mci.md)
-   [Streampuffer](stream-buffers.md)
-   [MIDI-Dienste](midi-services.md)
-   [Abspielen von MIDI-Dateien](playing-midi-files.md)
-   [Aufzeichnen von MIDI-Audiodateien](recording-midi-audio.md)
-   [Verarbeiten von MIDI-Daten aus zwei MIDI-Quellen](processing-midi-data-from-two-midi-sources.md)
-   [Erstellen von MIDI-Dateien](creating-midi-files.md)

 

 




