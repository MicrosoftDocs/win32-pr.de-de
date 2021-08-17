---
title: MIDI-Referenz
description: MIDI-Referenz
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Windows Multimedia, Audio Instrument Digital Interface (INSTRUMENTS)
- multimedia,Music Instrument Digital Interface (INSTRUMENTS)
- Multimediaaudio, Music Instrument Digital Interface (INSTRUMENTS)
- audio, Music Instrument Digital Interface (INSTRUMENTS)
- Windows Multimedia, REFERENZ
- Multimedia, REFERENZ
- Multimediaaudio, REFERENZ
- Audio, REFERENZ
- Music Instrument Digital Interface (OPC), Referenz
- INSTRUMENTS (Music Instrument Digital Interface), Referenz
- Reference for PARTS,about
- REFERENZ,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da65f193bbdc6b67d317fac7546d4f5d7826d89307d1800c565febf0c7a8b6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428350"
---
# <a name="midi-reference"></a>MIDI-Referenz

In diesem Abschnitt werden die Funktionen, Makros, Nachrichten und Strukturen beschrieben, die mit der digitalen Schnittstelle des Instrumentals (INSTRUMENTS) verknüpft sind. Diese Elemente sind wie folgt gruppiert.

## <a name="allocating-and-managing-buffers"></a>Zuordnen und Verwalten von Puffern

-   [**PARTSHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [**partsInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [**partsInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [**partsInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [**partsOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [**partsOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a>Rückruffunktionen

-   [**PartsInProc**](/previous-versions//dd798460(v=vs.85))
-   [**WeichOutProc**](/previous-versions//dd798478(v=vs.85))

## <a name="device-capabilities"></a>Gerätefunktionen

-   [**WEICHEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [**partsInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [**partsInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [**partsInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [**KAPSELNOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [**partsOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [**sideOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [**partsOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [**PARTSSTRMBUFFVER**](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a>Fehlerverarbeitung

-   [**partsInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [**partsOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [**\_MIM Fehler**](mim-error.md)
-   [**\_MIM LONGERROR**](mim-longerror.md)
-   [**MM \_ MIM \_ ERROR**](mm-mim-error.md)
-   [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a>Verwalten von STREAMS

-   [**partsStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [**streamStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [**partsStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**streamStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**partsStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [**streamStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [**streamStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**partsStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a>Öffnen und Schließen von Geräten

-   [**partsInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [**partsInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [**partsOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [**partsOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [**\_MIM Schließen**](mim-close.md)
-   [**\_MIM Öffnen**](mim-open.md)
-   [**MM \_ MIM \_ CLOSE**](mm-mim-close.md)
-   [**MM \_ MIM \_ OPEN**](mm-mim-open.md)
-   [**MM \_ MOM \_ CLOSE**](mm-mom-close.md)
-   [**MM \_ MOM \_ OPEN**](mm-mom-open.md)
-   [**MOM \_ CLOSE**](mom-close.md)
-   [**MOM \_ OPEN**](mom-open.md)

## <a name="output-devices"></a>Ausgabegeräte

-   [KEYARRAY](keyarray.md)
-   [**partsOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [**cacheOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [**partsOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [**partsOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [PATCHARRAY](patcharray.md)

## <a name="playing-a-message-or-messages"></a>Wiedergeben einer Nachricht oder von Nachrichten

-   [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [**MEVT \_ EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [**WÄHREND DES EREIGNISEREIGNISSES**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [**partsOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [**partsOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [**partsOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [**partsStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**streamStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**streamStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**partsStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [**MM \_ MOM \_ DONE**](mm-mom-done.md)
-   [**MM \_ MOM \_ POSITIONCB**](mm-mom-positioncb.md)
-   [**MOM \_ DONE**](mom-done.md)
-   [**MOM \_ POSITIONCB**](mom-positioncb.md)

## <a name="recording"></a>Aufzeichnung

-   [**connectconnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [**partsDisconnect**](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [**partsInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [**partsInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [**partsInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [**TIESPROPTEMPO**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [**DIVPROPTIMEDIV**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [**\_MIM Daten**](mim-data.md)
-   [**\_MIM LONGDATA**](mim-longdata.md)
-   [**\_MIM MOREDATA**](mim-moredata.md)
-   [**MM \_ MIM \_ DATA**](mm-mim-data.md)
-   [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)
-   [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a>Senden von Nachrichten an Geräte

-   [**whatInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [**stromausfallOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Music Instrument Digital Interface (INSTRUMENTS)](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 