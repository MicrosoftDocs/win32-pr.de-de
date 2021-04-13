---
title: Empfangen Time-Stamped von MIDI-Nachrichten
description: Empfangen Time-Stamped von MIDI-Nachrichten
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Digital Instrumentation Digital Interface (MIDI), Nachrichten mit Zeitstempel
- MIDI (Digital Instrumentation Digital Interface), Nachrichten mit Zeitstempel
- Aufzeichnen von MIDI-Audiodaten, Zeitstempel Meldungen
- mit Zeitstempel versehene MIDI-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314864"
---
# <a name="receiving-time-stamped-midi-messages"></a><span data-ttu-id="7c38a-107">Empfangen Time-Stamped von MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="7c38a-107">Receiving Time-Stamped MIDI Messages</span></span>

<span data-ttu-id="7c38a-108">Aufgrund der Verzögerung zwischen dem Zeitpunkt, zu dem der Gerätetreiber eine MIDI-Nachricht empfängt, und dem Zeitpunkt, zu dem die Anwendung die Nachricht empfängt, wird die MIDI-Nachricht von den MIDI-Eingabe-Gerätetreibern mit dem Zeitpunkt der Nachrichten Empfangszeit versehen.</span><span class="sxs-lookup"><span data-stu-id="7c38a-108">Because of the delay between when the device driver receives a MIDI message and the time the application receives the message, MIDI input device drivers time stamp the MIDI message with the time that the message was received.</span></span> <span data-ttu-id="7c38a-109">Die Zeitstempel von MIDI, die als Zeitpunkt definiert werden, zu dem das erste Byte der Nachricht empfangen wurde, werden in Millisekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="7c38a-109">MIDI time stamps, which are defined as the time the first byte of the message was received, are specified in milliseconds.</span></span> <span data-ttu-id="7c38a-110">Die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion setzt die Zeitstempel für ein Gerät auf 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="7c38a-110">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function resets the time stamps for a device to zero.</span></span>

<span data-ttu-id="7c38a-111">Wie bereits erwähnt, müssen Sie zum Empfangen von Zeitstempeln mit der Verwendung von MIDI eine Rückruffunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c38a-111">As stated previously, to receive time stamps with MIDI input, you must use a callback function.</span></span> <span data-ttu-id="7c38a-112">Der *dwParam2* -Parameter der Rückruffunktion gibt den Zeitstempel für die Daten an, die den [**MIM- \_ Daten**](mim-data.md) und [**MIM \_ longdata**](mim-longdata.md) -Nachrichten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7c38a-112">The *dwParam2* parameter of the callback function specifies the time stamp for data associated with the [**MIM\_DATA**](mim-data.md) and [**MIM\_LONGDATA**](mim-longdata.md) messages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c38a-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c38a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c38a-114">Aufzeichnen von MIDI-Audiodateien</span><span class="sxs-lookup"><span data-stu-id="7c38a-114">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 