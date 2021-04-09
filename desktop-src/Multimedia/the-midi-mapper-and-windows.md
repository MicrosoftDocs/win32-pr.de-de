---
title: Der MIDI-Mapper und Windows
description: Der MIDI-Mapper und Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038923"
---
# <a name="the-midi-mapper-and-windows"></a>Der MIDI-Mapper und Windows

Der MIDI-Mapper ist Teil der Systemsoftware. In der folgenden Abbildung wird gezeigt, wie sich der MIDI-Mapper auf andere Elemente der Audiodienste bezieht.

![Beziehung des MIDI-Mappers mit anderen Elementen des audiodienstebilds](images/mmap-a01.gif)

Vom Standpunkt einer Anwendung aus sieht der MIDI-Mapper wie ein anderes MIDI-Ausgabegerät aus. Der MIDI-Mapper empfängt die an ihn gesendeten Nachrichten von den " [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) " und " [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)" auf niedriger Ebene. Der MIDI-Mapper ändert diese Nachrichten und leitet Sie entsprechend der aktuellen Registerkarte für das MIDI-Setup an ein MIDI-Ausgabegerät weiter. Die aktuelle Zuordnung von "MIDI-Setup" wird vom Benutzer mithilfe der System Steuerungs Option "MIDI" ausgewählt. Nur der Benutzer kann die aktuelle Setup Zuordnung auswählen. die aktuelle Setup Zuordnung kann von Anwendungen nicht geändert werden.

 

 