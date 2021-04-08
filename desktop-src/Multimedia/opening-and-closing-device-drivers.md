---
title: Öffnen und Schließen von Gerätetreibern
description: Öffnen und Schließen von Gerätetreibern
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Digital Instrumentation Digital Interface (MIDI), Öffnen von Geräten
- MIDI (Digital Instrumentation Digital Interface), Öffnen von Geräten
- MIDI-Dienste, Öffnen von Geräten
- Öffnen von MIDI-Geräten
- Digital Instrumentation Digital Interface (MIDI), schließen von Geräten
- MIDI (Digital Instrumentation Digital Interface), schließen von Geräten
- MIDI-Dienste, schließen von Geräten
- Schließen von MIDI-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725080"
---
# <a name="opening-and-closing-device-drivers"></a>Öffnen und Schließen von Gerätetreibern

Sie müssen ein MIDI-Gerät öffnen, bevor Sie es verwenden können, und Sie sollten das Gerät schließen, sobald Sie es verwenden. Windows bietet die folgenden Funktionen, um unterschiedliche Arten von MIDI-Geräten zu öffnen und zu schließen.



| Wert                                | Bedeutung                                            |
|--------------------------------------|----------------------------------------------------|
| [**midiinclose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | Schließt ein angegebenes MIDI-Eingabegerät.              |
| [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | Öffnet ein angegebenes MIDI-Eingabegerät für die Aufzeichnung. |
| [**midioutclose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | Schließt ein angegebenes MIDI-Ausgabegerät.             |
| [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | Öffnet ein MIDI-Ausgabegerät für die Wiedergabe.           |



 

Jede Funktion, die ein MIDI-Gerät öffnet, benötigt als Parameter einen Geräte Bezeichner, eine Adresse eines Speicher Orts und einige Parameter, die für die Verwendung von MIDI-Geräten eindeutig sind. Der Speicherort wird mit einem Geräte handle gefüllt, das verwendet wird, um das geöffnete Audiogerät in Aufrufen von anderen Audiofunktionen zu identifizieren.

Viele MIDI-Funktionen können entweder ein Geräte handle oder einen Geräte Bezeichner akzeptieren. Obwohl Sie ein Geräte handle überall dort verwenden können, wo Sie einen Geräte Bezeichner verwenden würden, können Sie nicht immer einen Geräte Bezeichner verwenden, wenn ein Handle für aufgerufen wird.

> [!Note]  
> Bei der Erstellung von MIDI-Geräten ist es nicht zwingend möglich, dass ein bestimmtes Gerät nicht verfügbar ist, wenn ein Benutzer es anfordert. In diesem Fall sollte die Anwendung den Benutzer benachrichtigen und dem Benutzer gestatten, das Gerät erneut zu öffnen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MIDI-Dienste](midi-services.md)
</dt> </dl>

 

 