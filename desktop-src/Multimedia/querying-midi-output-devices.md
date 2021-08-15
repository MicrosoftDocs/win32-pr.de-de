---
title: Abfragen vonENDE-Ausgabegeräten
description: Abfragen vonENDE-Ausgabegeräten
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- Instrument Digital Interface (KEYBOARD), Ausgabegeräte
- KEYBOARD (Keyboard Instrument Digital Interface), Ausgabegeräte
- Wiedergabe von WIEDERGABEDATEIEN,Ausgabegeräte
- AUDIOausgabegeräte
- InstrumentIeren der digitalen Schnittstelle (Instrument Digital Interface,ENDE), Abfragen von Ausgabegeräten
- ENDE (Keyboard Instrument Digital Interface), Abfragen von Ausgabegeräten
- Wiedergeben vonFORMAT-Dateien, Abfragen von Ausgabegeräten
- Abfragen vonENDE-Ausgabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b493c0b3554a9a60cfc349d13a5404ec4d2b27915933c14b387df29a582406e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371912"
---
# <a name="querying-midi-output-devices"></a>Abfragen vonENDE-Ausgabegeräten

Vor dem Wiedergeben einerDATEIERWEITERUNG-Datei sollten Sie mithilfe der [**Funktion "sollenOutGetDevCaps"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) die Funktionen des IMT-Ausgabegeräts bestimmen, das im System vorhanden ist. Diese Funktion nimmt eine Adresse [**einerTSOUTCAPS-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) an, die mit Informationen zu den Funktionen des angegebenen Geräts auffüllt. Zu diesen Informationen gehören die Hersteller- und Produktbezeichner, ein Produktname für das Gerät und die Versionsnummer des Gerätetreibers (angegeben in den **Membern wMid,** **wPid,** **szPname** und **vDriverVersion).**

BEI DEN OUTPUT-Geräten kann es sich entweder um interne Synthesizer oder um externe PORTS für die AUSGABE von TCP-Ausgabeanschlüssen (external). Der **wTechnology-Member** der **EIGENSCHAFTOUTCAPS-Struktur** gibt die Technologie des Geräts an.

Wenn es sich bei dem Gerät um einen internen Synthesizer handelt, sind zusätzliche Geräteinformationen in den **wVoices-,** **wNotes-** und **wChannelMask-Membern** verfügbar. Das **wVoices-Element** gibt die Anzahl der Stimmen an, die das Gerät unterstützt. Jede Stimme kann einen anderen Sound oder ein anderes Timbre haben. Stimmen sind in DEN KANÄLEn organisiert. Das **wNotes-Element** gibt die *Polyie* des Geräts an, d.&160;B. die maximale Anzahl von Notizen, die gleichzeitig abgespielt werden können. Das **wChannelMask-Member** ist eine Bitdarstellung der VOM Gerät antwortet. Wenn das Gerät beispielsweise auf die ersten acht CHANNEL-Kanäle antwortet, wird **wChannelMask** 0x00FF. Wenn das Gerät ein externer Ausgabeport ist, werden **wVoices** und **wNotes** nicht verwendet, und **wChannelMask** wird auf 0xFFFF.

Das **dwSupport-Member** der **SSDOUTCAPS-Struktur** gibt an, ob der Gerätetreiber Volumeänderungen, Patchzwischenspeicherung und Streaming unterstützt. Volumeänderungen werden nur von internen Synthesizergeräten unterstützt. Externe TCP-Ausgabeports unterstützen keine Volumeänderungen. Weitere Informationen zum Ändern des Volumes finden Sie unter [Changing Internal SYNTHESIZE Synthesizer Volume](changing-internal-midi-synthesizer-volume.md).

 

 