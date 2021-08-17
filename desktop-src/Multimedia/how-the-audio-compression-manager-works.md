---
title: Funktionsweise des Audiokomprimierungs-Managers
description: Funktionsweise des Audiokomprimierungs-Managers
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- Multimediaaudio, Audiokomprimierungs-Manager (ACM)
- Audio, Audiokomprimierungs-Manager (ACM)
- Audiokomprimierungs-Manager (ACM), Informationen
- ACM (Audiokomprimierungs-Manager), Informationen
- Audiokomprimierungs-Manager (ACM), Codectreiber
- ACM (Audiokomprimierungs-Manager), Codectreiber
- Audiokomprimierungs-Manager (ACM), Formatkonvertertreiber
- ACM (Audiokomprimierungs-Manager), Formatkonvertertreiber
- Audiokomprimierungs-Manager (ACM), Filtertreiber
- ACM (Audiokomprimierungs-Manager), Filtertreiber
- Audiokomprimierungs-Manager (ACM), Komprimierungstreiber
- ACM (Audiokomprimierungs-Manager), Komprimierungstreiber
- Audiokomprimierungs-Manager (ACM), Dekomprimierungstreiber
- ACM (Audiokomprimierungs-Manager), Dekomprimierungstreiber
- Codectreiber
- Formatkonvertertreiber
- Filtertreiber
- Treiber
- Dekomprimierungstreiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb3d94feee3da290bf9c1cc90cab92f2aade083effd8a01cb17906c22e0f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140997"
---
# <a name="how-the-audio-compression-manager-works"></a>Funktionsweise des Audiokomprimierungs-Managers

Der ACM verwendet vorhandene Treiberschnittstellenhooks, um den Standardzuordnungsalgorithmus für Waveform-Audiogeräte zu überschreiben. Dies ermöglicht dem ACM das Abfangen von aufrufenden Geräten. Nachdem ein Aufruf abgefangen wurde, kann der ACM eine Vielzahl von Aufgaben ausführen, um die Audiodaten zu verarbeiten, z. B. das Einfügen einer externen Rake oder eines Dekomprimierers in die Sequenz.

Der ACM verwaltet die folgenden Typen von Treibern:

-   Zyktik- und Dekomprimierungstreiber (Codec)
-   Formatkonvertertreiber
-   Filtertreiber

Durch Komprimierungen und Dekomprimatoren wird ein Formattyp in einen anderen geändert. Beispielsweise kann ein Bzw. ein Dekomprimierer eine PCM-Datei (Pulse Code Codes) in eine ADPCM-Datei (Adaptive Differential Pulse Code Codes Codes) ändern. Formatkonverter ändern das Format, aber nicht den Datentyp. Beispielsweise kann ein Konverter 44-kHz-16-Bit-Daten in 8-Bit-Daten mit 44 kHz ändern. Filter ändern das Datenformat überhaupt nicht, aber sie ändern die Waveform-Audiodaten in irgendeiner Weise. Beispielsweise könnte ein Filter einen Datenstrom und ein Echo von sich selbst kombinieren. Ein einzelner ACM-Treiber oder ein Filtertag oder Formattag innerhalb eines Treibers unterstützt möglicherweise auch Kombinationen der vorherigen Typen.

Bei der Ausgabe von Waveform-Audio übergibt der ACM jeden Datenpuffer an den Konverter, sobald er eintrifft. Der Konverter dekomprimiert die Daten und gibt die dekomprimierten Daten in einem Schattenpuffer an den ACM zurück. Der ACM übergibt dann den dekomprimierten Schattenpuffer an den Waveform-Audiotreiber. Der ACM ordnet die Schattenpuffer zu, wenn er eine Vorbereitungsnachricht empfängt.

Für die Waveform-Audioeingabe übergibt der ACM leere Schattenpuffer an den Treiber. Sie verwendet eine Hintergrundaufgabe, um eine Benachrichtigung zu erhalten, nachdem der Treiber den Schattenpuffer gefüllt hat. Der ACM übergibt dann die Puffer zur Komprimierung an den Treiber. Nach Abschluss der Komprimierung übergibt der Treiber die Daten an die Anwendung.

 

 




