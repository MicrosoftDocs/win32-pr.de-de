---
title: Zurücksetzen der OUTPUT-Ausgabe
description: Zurücksetzen der OUTPUT-Ausgabe
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Music Instrument Digital Interface (RESET), Zurücksetzen von Ausgabegeräten
- INSTRUMENTS (Music Instrument Digital Interface), Zurücksetzen von Ausgabegeräten
- Wiedergabe von WIEDERGABEDATEIEN, Zurücksetzen von Ausgabegeräten
- Zurücksetzen von Ausgabegeräten
- Instrument Digital Interface (INSTRUMENTS), Ausgabegeräte
- INSTRUMENTS (Music Instrument Digital Interface), Ausgabegeräte
- Wiedergeben von PROTOKOLLDATEIen, Ausgabegeräten
- OUTPUT-Geräte
- EOX (Ende der exklusiven Nutzung)
- Ende des exklusiven (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c0073d9fc016e21e401e4cb2e7c28b4fd1aa5e3180801975df4e334243b953
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689260"
---
# <a name="resetting-midi-output"></a>Zurücksetzen der OUTPUT-Ausgabe

Die [**funktion "bedOutReset"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) schaltet alle Notizen auf allen CHANNELS-Kanälen für ein angegebenes GERÄT aus. Anschließend markiert die Funktion alle ausstehenden systembezogenen exklusiven Puffer als erledigt und gibt sie an die Anwendung zurück. Diese Funktion kann in einer Anwendung nützlich sein, die die OUTPUT-Ausgabe verwendet, um dem Benutzer die Möglichkeit zu geben, die OUTPUT-Ausgabe zurückzusetzen.

> [!Note]  
> Das Beenden einer systembezogenen exklusiven Nachricht ohne Senden eines EOX-Byte (Ende des exklusiven Byte) kann probleme für das empfangende Gerät verursachen. Die **funktion "eqoutReset"** sendet kein EOX-Byte, wenn sie eine systemausgesperrte Nachricht beendet, da anwendungen dafür verantwortlich sind.

 

 

 