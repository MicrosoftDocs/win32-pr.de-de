---
title: MIDI-Ereignis Typen
description: MIDI-Ereignis Typen
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- Digital Instrumentation Digital Interface (MIDI), Ereignis Typen
- MIDI (Digital Instrumentation Digital Interface), Ereignis Typen
- MidiEvent-Struktur
- Streampuffer, MIDI-Ereignis Typen
- MIDI-Ereignis Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038969"
---
# <a name="midi-event-types"></a>MIDI-Ereignis Typen

Der **dwevent** -Member der [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Struktur beschreibt das zu durch zuwählenden MIDI-Ereignis. Kurze Ereignisse sind vollständig in diesen Member integriert. Lange Ereignisse erfordern zusätzlich zum **dwevent** -Member einen oder mehrere Double Word-Werte, um die Ereignis Beschreibungen zu speichern.

Das hohe Byte des **dwevent** -Members enthält Informationen darüber, ob das Ereignis lang oder kurz ist, und ob ein Rückruf zusammen mit dem Ereignis generiert wird. Außerdem wird dieses Byte verwendet, um den Ereignistyp zu beschreiben. Die verbleibenden 24 Bits des **dwevent** -Members werden entweder verwendet, um die Ereignis Parameter (für kurze Nachrichten) oder die Länge der Ereignis Parameter (für lange Nachrichten) zu enthalten. Um Informationen aus dem **dwevent** -Member zu extrahieren, verwenden Sie den [**mevt \_ eventType**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) -und [**mevt \_ eventarm**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) -Makros.

Eine Beschreibung der vordefinierten Ereignis Typen finden Sie im Referenzmaterial für die **MidiEvent** -Struktur.

 

 