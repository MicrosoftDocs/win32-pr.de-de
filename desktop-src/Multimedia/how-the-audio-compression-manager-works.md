---
title: Funktionsweise des Audiokomprimierungs-Managers
description: Funktionsweise des Audiokomprimierungs-Managers
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- Multimedia-Audiodatei, Audiokomprimierungs-Manager (ACM)
- Audiokomprimierung, Audiokomprimierungs-Manager (ACM)
- Audiokomprimierungs-Manager (ACM), Informationen zu
- ACM (Audiokomprimierungs-Manager), Informationen zu
- Audiokomprimierungs-Manager (ACM), Codec-Treiber
- ACM (Audiokomprimierungs-Manager), Codec-Treiber
- Audiokomprimierungs-Manager (ACM), Format Konverter-Treiber
- ACM (Audiokomprimierungs-Manager), Format Konverter-Treiber
- Audiokomprimierungs-Manager (ACM), Filtertreiber
- ACM (Audiokomprimierungs-Manager), Filtertreiber
- Audiokomprimierungs-Manager (ACM), Kompressor-Treiber
- ACM (Audiokomprimierungs-Manager), Kompressor-Treiber
- Audiokomprimierungs-Manager (ACM), Debug-Treiber
- ACM (Audiokomprimierungs-Manager), Debug-Treiber
- Codec-Treiber
- Konvertieren von konvertertreibern
- Filtertreiber
- Kompressor-Treiber
- Debug-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310340"
---
# <a name="how-the-audio-compression-manager-works"></a>Funktionsweise des Audiokomprimierungs-Managers

Der ACM verwendet vorhandene Treiber Schnittstellen Hooks, um den standardmäßigen Mapping-Algorithmus für Waveform-Audiogeräte zu überschreiben. Dadurch kann das ACM Geräte offene Aufrufe abfangen. Nachdem ein-Rückruf abgefangen wurde, kann das ACM eine Reihe von Aufgaben zum Verarbeiten der Audiodaten ausführen, z. b. das Einfügen eines externen Kompressors oder dekompressors in die Sequenz.

Das ACM verwaltet die folgenden Treiber Typen:

-   Kompressor-und Debug-Treiber (Codec)
-   Konvertieren von konvertertreibern
-   Filter Treiber

-Kompressoren und-Dekompressoren ändern einen Formattyp in einen anderen. Beispielsweise kann ein Kompressor oder Dekompressor eine PCM-Datei (Pulse Code-Modulation) in eine ADPCM-Datei (Adaptive Differential Pulse Code Modulation) ändern. Format Konverter ändern das Format, jedoch nicht den Datentyp. Ein Konverter kann z. b. 44-kHz-16-Bit-Daten in 44-kHz-, 8-Bit-Daten ändern. Filter ändern das Datenformat überhaupt nicht, aber Sie ändern die Wellenform-Audiodaten auf irgendeine Weise. Beispielsweise könnte ein Filter einen Datenstrom und ein Echo von sich selbst kombinieren. Ein einzelner ACM-Treiber oder ein Filtertag oder ein Formattag innerhalb eines Treibers unterstützt möglicherweise auch Kombinationen der vorangehenden Typen.

Bei der Waveform-Audioausgabe übergibt das ACM jeden Puffer von Daten an den Konverter, sobald er eintrifft. Der Konverter zerlegt die Daten und gibt die entkomprimierten Daten an das ACM in einem "Shadow"-Puffer zurück. Das ACM übergibt dann den entkomprimierten Schatten Puffer an den Waveform-Audiotreiber. Das ACM ordnet die Schatten Puffer an, wenn eine Vorbereitungs Nachricht empfangen wird.

Bei der Waveform-Audioeingabe übergibt das ACM leere Schatten Puffer an den Treiber. Er verwendet einen Hintergrund Task, um eine Benachrichtigung zu erhalten, nachdem der Treiber den Schatten Puffer ausgefüllt hat. Der ACM übergibt die Puffer dann zur Komprimierung an den Treiber. Nachdem die Komprimierung abgeschlossen ist, übergibt der Treiber die Daten an die Anwendung.

 

 




