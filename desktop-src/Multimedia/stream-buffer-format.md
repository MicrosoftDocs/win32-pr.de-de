---
title: Streampufferformat
description: Streampufferformat
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- Digital Instrumentation Digital Interface (MIDI), Streampuffer
- MIDI (Digital Instrumentation Digital Interface), Streampuffer
- Streampuffer, Format
- Midihdr-Struktur
- MidiEvent-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390146"
---
# <a name="stream-buffer-format"></a>Streampufferformat

Der **lpdata** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur verweist auf einen Streampuffer, und der **dwbufferlength** -Member gibt die tatsächliche Größe dieses Puffers an. Der **dwbytesrecorded** -Member von **midihdr** gibt die Anzahl der Bytes im Puffer an, die tatsächlich von den MIDI-Ereignissen verwendet werden. Dieser Wert muss kleiner oder gleich dem Wert sein, der von **dwbufferlength** angegeben wird.

Jedes der MIDI-Ereignisse im Streampuffer wird durch eine [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Struktur angegeben, die die Uhrzeit für das Ereignis, einen Datenstrom Bezeichner, einen Ereignis Code und ggf. Parameter für das Ereignis enthält. Jede dieser **MidiEvent** -Strukturen muss an einer Double Word-Grenze beginnen. Ggf. müssen Pad-Bytes am Ende der Struktur hinzugefügt werden, um sicherzustellen, dass das nächste an einer Double Word-Grenze beginnt.

 

 