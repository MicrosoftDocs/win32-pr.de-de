---
title: Waveform-Audioreferenz
description: In diesem Abschnitt werden die Funktionen, Strukturen und Nachrichten aufgelistet, die mit Wellenform-Audiodaten verknüpft sind. diese sind unter Multimedia Reference dokumentiert. Diese Elemente werden wie folgt gruppiert.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows Multimedia, Waveform-Audioreferenz
- Multimedia, Waveform-Audioreferenz
- Multimedia-Audiodatei, Waveform-Referenz
- Audiodatei, Wellenform Referenz
- Windows Multimedia, Waveform-Audiodatei
- Multimedia, Waveform-Audiodatei
- Multimedia-Audiodatei, Wellenform
- Audiodaten, Wellenform
- Wellenform-Audiodatei, Referenz
- Wellenform-Audioreferenz, Informationen zu
- Referenz für wavevoraudioinformationen, Informationen zu
- Wellenform-Audioreferenz, hilfsangeräte
- Referenz für Wellenlinien Audiogeräte, Hilfssysteme
- Wellenform-audioverweis, Wiedergabe
- Verweis für Wellen-Audiodaten, Wiedergabe
- Wellenform-Audioreferenz, Fehler
- Verweis für Wellen-Audiodaten, Fehler
- Wellenform-audioverweis, öffnen
- Verweis für Wellen-Audiodaten, öffnen
- Wellenform-audioverweis, schließen
- Verweis für Wellen-Audiodaten, schließen
- Wellenform-Audioreferenz, Tonhöhe
- Referenz für Wellen-Audiodaten, Tonhöhe
- Wellenform-Audioreferenz, Volume
- Referenz für die Wellen Vorder-Audiodaten, das Volume
- Wellenform-Audioreferenz, Meldungen
- Referenz für Wellen-Audiodaten, Meldungen
- Wellenform-audioverweis, aktuelle Position
- Verweis für wavealaudiodatei, aktuelle Position
- Wellenform-audioverweis, aufzeichnen
- Verweis für Wellen-Audiodaten, Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038900"
---
# <a name="waveform-audio-reference"></a>Waveform-Audioreferenz

In diesem Abschnitt werden die Funktionen, Strukturen und Nachrichten aufgelistet, die mit Wellenform-Audiodaten verknüpft sind. diese sind unter [Multimedia Reference](multimedia-reference.md)dokumentiert. Diese Elemente werden wie folgt gruppiert.

## <a name="auxiliary-devices"></a>Geräte mit zusätzlichen Geräten

-   [**Zugriffs enden**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**"auxgetdevcaps"**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**"auxgetnumentvs"**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**"auxgetvolume"**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**"auxoutmessage"**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**"auxsetvolume"**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Einfache Wiedergabe

-   [**PlaySound**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Errors

-   [**waveingeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveoutgeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Öffnen und schließen

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**MM \_ WIM \_ Schließen**](mm-wim-close.md)
-   [**MM \_ WIM \_ geöffnet**](mm-wim-open.md)
-   [**MM \_ WOM \_ Schließen**](mm-wom-close.md)
-   [**MM \_ WOM \_ geöffnet**](mm-wom-open.md)
-   [**Waveformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveingeclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveingeproc**](/previous-versions//dd743849(v=vs.85))
-   [**Wavin Open**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveoutclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveoutproc**](/previous-versions//dd743869(v=vs.85))
-   [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**Wim- \_ Schließen**](wim-close.md)
-   [**Wim \_ geöffnet**](wim-open.md)
-   [**WOM \_ Schließen**](wom-close.md)
-   [**WOM \_ geöffnet**](wom-open.md)

## <a name="pitch"></a>Neigung

-   [**waveoutgetpitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveoutsetpitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Wiedergabe Rate

-   [**waveoutgetplaybackrate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveoutsetplaybackrate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Wiedergabe Fortschritt

-   [**MM \_ WOM \_ abgeschlossen**](mm-wom-done.md)
-   [**waveoutbreakloop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveoutpause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveeinset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**wavestartstart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ abgeschlossen**](wom-done.md)

## <a name="playing"></a>Wiedergabe

-   [**MM \_ WOM \_ abgeschlossen**](mm-wom-done.md)
-   [**Wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveoutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveoutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ abgeschlossen**](wom-done.md)

## <a name="querying-a-device"></a>Abfragen eines Geräts

-   [**Wavin Caps**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveingegetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveingegetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**Waveoutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveoutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveoutgetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Aufzeichnung

-   [**MM- \_ WIM- \_ Daten**](mm-wim-data.md)
-   [**waveinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**wavone prepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveingereset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**wavanstart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**WaveIn-Ende**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveingeunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**Wim- \_ Daten**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Geräte Bezeichner werden abgerufen.

-   [**waveingetid**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**waveoutgetid**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>Abrufen der aktuellen Position

-   [**waveingetposition**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**waveoutgetposition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>Senden benutzerdefinierter Nachrichten

-   [**waveinmessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**waveoutmessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>Lautstärke

-   [**waveoutgetvolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**waveoutsetvolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Waveform-Audiodatei](waveform-audio.md)
</dt> </dl>

 

 