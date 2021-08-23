---
title: Waveform-Audioreferenz
description: In diesem Abschnitt werden die Funktionen, Strukturen und Nachrichten aufgeführt, die Waveformaudio zugeordnet sind, die unter Multimediareferenz dokumentiert sind. Diese Elemente sind wie folgt gruppiert.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows Multimedia, Waveform-Audioreferenz
- Multimedia, Waveform-Audioreferenz
- Multimediaaudio, Waveformreferenz
- Audio, Waveformreferenz
- Windows Multimedia, Waveform-Audio
- Multimedia, Waveform-Audio
- Multimediaaudio, Wellenform
- Audio, Wellenform
- Waveform-Audio, Referenz
- Waveform-Audioreferenz, Informationen
- Referenz für Wavefore-Audio, Informationen
- Waveform-Audioreferenz, Hilfsgeräte
- Referenz für Wavefore-Audio, Hilfsgeräte
- Waveform-Audioreferenz, Wiedergabe
- Referenz für Wavefore-Audio, Wiedergabe
- Waveform-Audioreferenz, Fehler
- Referenz für Wavefore-Audio, Fehler
- Waveform-Audioreferenz, öffnen
- Referenz für Wavefore-Audio, Öffnen
- Waveform-Audioreferenz, Schließen
- Referenz für Wavefore-Audio, Schließen
- Waveform-Audioreferenz, Tonhöhe
- Referenz für Wavefore-Audio, Tonhöhe
- Waveform-Audioreferenz, Lautstärke
- Referenz für Wavefore-Audio, Lautstärke
- Waveform-Audioreferenz, Meldungen
- Referenz für Wavefore-Audio, Nachrichten
- Waveform-Audioreferenz, aktuelle Position
- Referenz für Wavefore-Audio, aktuelle Position
- Waveform-Audioreferenz,Aufzeichnung
- Referenz für Wavefore-Audio, Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd83f843de130d247749acfc87a67c60948871bb8cd878f9aa180fcd385fb13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687420"
---
# <a name="waveform-audio-reference"></a>Waveform-Audioreferenz

In diesem Abschnitt werden die Funktionen, Strukturen und Nachrichten aufgelistet, die Waveformaudio zugeordnet sind, die unter [Multimediareferenz](multimedia-reference.md)dokumentiert sind. Diese Elemente sind wie folgt gruppiert.

## <a name="auxiliary-devices"></a>Hilfsgeräte

-   [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**auxOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Einfache Wiedergabe

-   [**PlaySound**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Fehler

-   [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Öffnen und Schließen

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**MM \_ WIM \_ CLOSE**](mm-wim-close.md)
-   [**MM \_ WIM \_ OPEN**](mm-wim-open.md)
-   [**MM \_ WOM \_ CLOSE**](mm-wom-close.md)
-   [**MM \_ WOM \_ OPEN**](mm-wom-open.md)
-   [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveInProc**](/previous-versions//dd743849(v=vs.85))
-   [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveOutProc**](/previous-versions//dd743869(v=vs.85))
-   [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**WIM \_ CLOSE**](wim-close.md)
-   [**WIM \_ OPEN**](wim-open.md)
-   [**WOM \_ CLOSE**](wom-close.md)
-   [**WOM \_ OPEN**](wom-open.md)

## <a name="pitch"></a>Neigung

-   [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Wiedergaberate

-   [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Wiedergabefortschritt

-   [**MM \_ WOM \_ DONE**](mm-wom-done.md)
-   [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ DONE**](wom-done.md)

## <a name="playing"></a>Wiedergabe

-   [**MM \_ WOM \_ DONE**](mm-wom-done.md)
-   [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ DONE**](wom-done.md)

## <a name="querying-a-device"></a>Abfragen eines Geräts

-   [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Aufzeichnung

-   [**MM \_ WIM \_ DATA**](mm-wim-data.md)
-   [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**WIM \_ DATA**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Abrufen von Gerätebezeichnern

-   [**waveInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**waveOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>Abrufen der aktuellen Position

-   [**waveInGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>Senden von benutzerdefinierten Nachrichten

-   [**waveInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>Volume

-   [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Waveform-Audio](waveform-audio.md)
</dt> </dl>

 

 