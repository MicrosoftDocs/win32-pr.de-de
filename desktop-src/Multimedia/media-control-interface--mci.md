---
title: Media Control Interface (MCI)
description: Media Control Interface (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Windows Multimedia, Media Control Interface (MCI)
- multimedia, Media Control Interface (MCI)
- Multimediaaudio, Media Control Interface (MCI)
- audio, Media Control Interface (MCI)
- Music Instrument Digital Interface (SENDER), Media Control Interface (MCI)
- INSTRUMENTS (Music Instrument Digital Interface), Media Control Interface (MCI)
- Mediensteuerungsschnittstelle (Media Control Interface, MCI), Music Instrument Digital Interface (INSTRUMENTS)
- MCI (Media Control Interface), Music Instrument Digital Interface (INSTRUMENTS)
- Media Control Interface (MCI), OPC Sequencer
- MCI (Media Control Interface), OPC Sequencer
- MCI-SEQUENZER, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8d21588754d0f66dbed97c74bbaabe4c005335059dace2997012691a24c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782980"
---
# <a name="media-control-interface-mci"></a>Media Control Interface (MCI)

Der MCI-SEQUENCER IST die MCI-Systemkomponente, die CSV-Dateien abspielt. Anwendungen können DATEIEN problemlos mithilfe von MCI wiedergeben, aber MCI erzwingt die folgenden Einschränkungen für DIE FUNKTIONEN von DOSSIER:

-   MCI unterstützt nur die AUSGABE VON ONLY.
-   MCI lässt keine enge Synchronisierung zwischen EREIGNISSEN und anderen Echtzeitereignissen (z. B. Videos) zu.

Wenn Sie eine genaue SYNCHRONISIEREN-Synchronisierung benötigen, müssen Sie die Streampuffer oder die CSV-Dienste verwenden. Wenn Sie DIE INPUT-Funktionen benötigen, müssen Sie die SERVICES-Dienste verwenden.

Der MCI-CAB-Sequencer gibt STANDARDMÄßIGe CSV-Dateien und CSV-Dateien (Resource Interchange File Format, Ressourcenaustauschdateiformat) wieder, die als RMID-Dateien bezeichnet werden. STANDARDMÄßIGE DATEIEN entsprechen der [STANDARD-SPEZIFIKATION VON STANDARDS FILES 1.0.](creating-midi-files.md) Da es sich bei RMID-Dateien um STANDARDMÄßIGE DATEIEN mit einem CSV-Header handelt, gelten Informationen zu STANDARDMÄßIGEN DATEIEN auch für RMID-Dateien. Weitere Informationen zu CSV-Dateien finden Sie unter [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

Obwohl derzeit drei Arten von STANDARDMÄßIGEN DATEIEN vorhanden sind, gibt der MCI-Sequencer nur zwei davon wieder: Format 0- und Format 1 CSV-Dateien.

Weitere Informationen zum Steuern von Multimediageräten (einschließlich Sequencern) mithilfe von MCI-Befehlen finden Sie unter [MCI](mci.md).

 

 




