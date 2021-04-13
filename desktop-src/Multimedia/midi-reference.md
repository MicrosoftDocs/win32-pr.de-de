---
title: MIDI-Referenz
description: MIDI-Referenz
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Windows Multimedia, Digital Instrumentation Digital Interface (MIDI)
- Multimedia, Digital Instrumentation Digital Interface (MIDI)
- Multimedia-Audiodatei, Digital Instrumentation Digital Interface (MIDI)
- Audioschnittstelle (Digital Instrumentation Digital Interface, MIDI)
- Windows Multimedia, MIDI-Referenz
- Multimedia, MIDI-Referenz
- Multimedia-Audiodatei, MIDI-Referenz
- Audiodatei, MIDI-Referenz
- Digital Instrumentation Digital Interface (MIDI), Referenz
- MIDI (Digital Interface Digital Interface), Referenz
- Referenz für "MIDI", Informationen zu
- MIDI-Referenz, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390263"
---
# <a name="midi-reference"></a>MIDI-Referenz

In diesem Abschnitt werden die Funktionen, Makros, Meldungen und Strukturen beschrieben, die der digitalen Schnittstelle (Digital Instrumentation Digital Interface, MIDI) zugeordnet sind. Diese Elemente werden wie folgt gruppiert.

## <a name="allocating-and-managing-buffers"></a>Zuordnen und Verwalten von Puffern

-   [**Midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [**midiinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [**midiinprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [**midiinunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [**midioutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [**midioutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a>Rückruffunktionen

-   [**Midiinproc**](/previous-versions//dd798460(v=vs.85))
-   [**Midioutproc**](/previous-versions//dd798478(v=vs.85))

## <a name="device-capabilities"></a>Gerätefunktionen

-   [**Midiincaps**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [**midiingetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [**midiingetid**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [**midiingetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [**Midioutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [**midioutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [**midioutgetid**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [**midioutgetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [**Midistraumbuffver**](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a>Fehlerverarbeitung

-   [**midiingeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [**midioutgeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [**MIM- \_ Fehler**](mim-error.md)
-   [**MIM \_ longerror**](mim-longerror.md)
-   [**MM \_ MIM- \_ Fehler**](mm-mim-error.md)
-   [**MM \_ MIM \_ longerror**](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a>Verwalten von MIDI-Streams

-   [**midistreamclose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [**midistreamopen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midistreampause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midistreamposition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [**midistreamproperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [**midistreamrestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midistreamstoppt**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a>Öffnen und Schließen von Geräten

-   [**midiinclose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [**midioutclose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [**MIM \_ Close**](mim-close.md)
-   [**MIM \_ geöffnet**](mim-open.md)
-   [**MM \_ MIM \_ Schließen**](mm-mim-close.md)
-   [**MM \_ MIM \_ geöffnet**](mm-mim-open.md)
-   [**Schließen von mm \_ MOM \_**](mm-mom-close.md)
-   [**MM \_ MOM \_ geöffnet**](mm-mom-open.md)
-   [**MOM \_ Schließen**](mom-close.md)
-   [**MOM \_ geöffnet**](mom-open.md)

## <a name="output-devices"></a>Ausgabegeräte

-   [Keyarray](keyarray.md)
-   [**midioutcachedrumpatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [**midioutcachepatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [**midioutgetvolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [**midioutsetvolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [Patcharray](patcharray.md)

## <a name="playing-a-message-or-messages"></a>Wiedergeben einer Nachricht oder Nachrichten

-   [**mevt \_ EventParser**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [**mevt \_ eventType**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [**falsch einwählsatz**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midistreampause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midistreamrestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midistreamstoppt**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [**MM- \_ MOM \_ abgeschlossen**](mm-mom-done.md)
-   [**MM \_ MOM \_ positioncb**](mm-mom-positioncb.md)
-   [**MOM \_ abgeschlossen**](mom-done.md)
-   [**MOM- \_ positioncb**](mom-positioncb.md)

## <a name="recording"></a>Aufzeichnung

-   [**midiconnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [**mididisconnect**](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [**midiinreset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [**midiinstop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [**Midiproptempo**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [**Midiproptimediv**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [**MIM- \_ Daten**](mim-data.md)
-   [**MIM \_ longdata**](mim-longdata.md)
-   [**MIM \_ MoreData**](mim-moredata.md)
-   [**MM \_ MIM- \_ Daten**](mm-mim-data.md)
-   [**MM \_ MIM \_ MoreData**](mm-mim-moredata.md)
-   [**MM \_ MIM \_ longdata**](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a>Senden von Nachrichten an Geräte

-   [**midiinmessage**](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [**midioutmessage**](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digital Instrumentation Digital Interface (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 