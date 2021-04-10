---
title: Medien Steuerungs Schnittstelle (MCI)
description: Medien Steuerungs Schnittstelle (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Windows Multimedia, Media Control Interface (MCI)
- Multimedia, Medien Steuerungs Schnittstelle (MCI)
- Multimedia-Audiodaten, Medien Steuerungs Schnittstelle (MCI)
- Audioschnittstelle, Medien Steuerungs Schnittstelle (MCI)
- Digital Instrumentation Digital Interface (MIDI), Media Control Interface (MCI)
- MIDI (Digital Instrumentation Digital Interface), Medien Steuerungs Schnittstelle (MCI)
- Media Control Interface (MCI), Digital Instrumentation Digital Interface (MIDI)
- MCI (Media Control Interface), Digital Instrumentation Digital Interface (MIDI)
- Media Control Interface (MCI), MIDI Sequencer
- MCI (Medien Steuerungs Schnittstelle), MIDI Sequencer
- MCI-MIDI-Sequencer, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036887"
---
# <a name="media-control-interface-mci"></a>Medien Steuerungs Schnittstelle (MCI)

Der MCI-c#-Sequencer ist die MCI-Systemkomponente, die die Dateien von MIDI wieder gibt Anwendungen können mithilfe von MCI die Verwendung von MIDI-Dateien problemlos wiedergeben, aber MCI erzwingt die folgenden Einschränkungen für die Funktionen von "

-   MCI unterstützt nur die MIDI-Ausgabe.
-   MCI lässt die Synchronisierung zwischen den Integritäts-und anderen Echt Zeit Ereignissen (z. b. Video) nicht zu.

Wenn Sie eine genaue MIDI-Synchronisierung benötigen, müssen Sie die Datenstrom Puffer oder die Dienst-MIDI-Dienste verwenden. Wenn Sie über die Funktionen der MIDI-Eingabe verfügen, müssen Sie die-Dienst-Dienste verwenden.

Der MCI-Dienst für die Integration von MIDI gibt standardmäßige Dateien für die Dateiformat-und ssmid-Dateien (Resource Interchange File Format) wieder. Standard-MIDI-Dateien entsprechen der Standard--Datei für die-und- [Dateien 1,0](creating-midi-files.md) Da es sich bei RMID-Dateien um standardmäßige MIDI-Dateien mit einem Riff-Header handelt, gelten die Informationen zu den standardmäßigen-Dateien für die Verwendung von Weitere Informationen zu Riff Dateien finden Sie unter [Datei Format Dienste für den Ressourcenaustausch](resource-interchange-file-format-services.md).

Obwohl derzeit drei Arten von Standard-MIDI-Dateien vorhanden sind, gibt der MCI-Sequencer nur zwei der folgenden Elemente aus: Format 0 und Format 1-MIDI-Dateien.

Weitere Informationen zum Steuern von Multimedia-Geräten (einschließlich Sequencer) mithilfe von MCI-Befehlen finden Sie unter [MCI](mci.md).

 

 




