---
description: Alphabetische Liste der DirectShow-Schnittstellen
ms.assetid: 9c7f56f4-92af-40c6-8124-f2715ac3f6d7
title: Alphabetische Liste der DirectShow-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd37ad1d6b510f61964eb9f210ab9481560b2d3e2f522b8fc38da10b7582a991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074824"
---
# <a name="alphabetical-list-of-directshow-interfaces"></a>Alphabetische Liste der DirectShow-Schnittstellen

Es folgt eine alphabetische Liste der DirectShow-Schnittstellen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Schnittstelle</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder"><strong>IAMAnalogVideoDecoder</strong></a></td>
<td>Legt Informationen zum Analog-Digital-Konvertierungsprozess in einem Videoaufzeichnungsfilter fest und ruft sie ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer"><strong>IAMAudioInputMixer</strong></a></td>
<td>Steuert Audioaufnahmeeigenschaften.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></td>
<td>Ruft statistische Leistungsinformationen aus einem Audiorendererfilter ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation"><strong>IAMBufferNegotiation</strong></a></td>
<td>Fordert die Anzahl der Puffer für einen Filter an, um die Größe und die Größe jedes Puffers zu erstellen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol"><strong>IAMCameraControl</strong></a></td>
<td>Steuert Kameraeinstellungen wie Zoom, Schwenk, Öffnungsanpassung oder Beschleunigung.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></td>
<td>Sendet COPP-Nachrichten (Certified Output Protection Protocol) an den Grafiktreiber.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/qnetwork/nn-qnetwork-iamchannelinfo"><strong>IAMChannelInfo</strong></a></td>
<td>Ruft Kanalinformationen für Windows Media Station-Dateien (.nsc) ab und legt sie fest.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockadjust"><strong>IAMClockAdjust</strong></a></td>
<td>Passt die Referenzuhr an.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></td>
<td>Steuert die Toleranz eines Audiorenderers, wenn er Raten mit einer anderen Uhr abgleicht.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress"><strong>IAMCopyCaptureFileProgress</strong></a></td>
<td>Rückrufschnittstelle für die <a href="/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-copycapturefile"><strong>ICaptureGraphBuilder2::CopyCaptureFile-Methode.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamcrossbar"><strong>IAMCrossbar</strong></a></td>
<td>Leitet Signale von einer analogen oder digitalen Quelle an einen Videoaufnahmefilter weiter.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps"><strong>IAMDecoderCaps</strong></a></td>
<td>Gibt Funktioneninformationen aus einem MPEG-Decoderfilter zurück.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamdeviceremoval"><strong>IAMDeviceRemoval</strong></a></td>
<td>Bietet dem Filter Graph Manager die Möglichkeit, sich für Ereignisse zum Entfernen von Geräten für ein Erfassungsgerät zu registrieren.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></td>
<td>Gibt an, welches Fenster den Fokus für die Steuerung der DirectSound-Audiowiedergabe hat.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes"><strong>IAMDroppedFrames</strong></a></td>
<td>Ruft Leistungsinformationen aus einem Videoaufnahmefilter ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamextdevice"><strong>IAMExtDevice</strong></a></td>
<td>Steuert ein externes Gerät, z. B. eine DV-Kamera oder einen Videoband-Recoder (VTR).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamexttransport"><strong>IAMExtTransport</strong></a></td>
<td>Steuert den Transport auf einem VTR oder Einem -Dennder.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/qnetwork/nn-qnetwork-iamextendedseeking"><strong>IAMExtendedSeeking</strong></a></td>
<td>Sucht nach einem Marker in einem Windows Medienstream oder ändert die Wiedergaberate für eine Windows Mediendatei.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback"><strong>IAMFilterGraphCallback</strong></a></td>
<td>Rückrufschnittstelle für die Grapherstellung.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></td>
<td>Fragt ab, ob ein Filter ein Quellfilter oder ein Renderer ist.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback"><strong>IAMGraphBuilderCallback</strong></a></td>
<td>Rückrufschnittstelle für die Grapherstellung.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams"><strong>IAMGraphStreams</strong></a></td>
<td>Steuert ein Filterdiagramm, das eine Livequelle rendert.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamlatency"><strong>IAMLatency</strong></a></td>
<td>Meldet die Latenz, die ein Filter in das Diagramm einführt.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></td>
<td>Legt Informationen zu Untertiteln fest und ruft sie ab.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a></td>
<td>Ruft Metadaten aus einem Stream ab.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig"><strong>IAMNetShowConfig</strong></a></td>
<td>Konfiguriert den Legacy-Windows Media Player 6.4-Quellfilter.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops"><strong>IAMNetShowExProps</strong></a></td>
<td>Konfiguriert den Legacy-Windows Media Player 6.4-Quellfilter.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowpreroll"><strong>IAMNetShowPreroll</strong></a></td>
<td>Legt die Prerolleinstellungen für den Legacy-Windows Media Player 6.4-Quellfilter fest und ruft sie ab.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/qnetwork/nn-qnetwork-iamnetworkstatus"><strong>IAMNetworkStatus</strong></a></td>
<td>Meldet die Qualität der Netzwerkverbindung für den Legacy-Windows Media Player 6.4-Quellfilter.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamopenprogress"><strong>IAMOpenProgress</strong></a></td>
<td>Meldet den Fortschritt eines Dateiöffnungsvorgangs.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></td>
<td>Steuert, wie die Videoüberlagerung auf dem Bildschirm des Benutzers angezeigt wird.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a></td>
<td>Legt die Analysezeit für einen MPEG-2-Stream fest und ruft sie ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a></td>
<td>Synchronisiert ein Filterdiagramm, das eine Livequelle rendert.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></td>
<td>Öffnet eine Audiogeräteressource und enthält sie.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-iamstats"><strong>IAMStats</strong></a></td>
<td>Ruft Leistungsdaten aus dem Filter Graph Manager ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a></td>
<td>Legt das Ausgabeformat für bestimmte Erfassungs- und Komprimierungsfilter fest.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a></td>
<td>Steuert einzelne Datenströme in einem Filter.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></td>
<td>wählt aus den verfügbaren Streams in einem Parserfilter aus.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader"><strong>IAMTimecodeReader</strong></a></td>
<td>Liest SMPTE- oder CODE-Zeitcode von einem externen Gerät.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamtuner"><strong>IAMTuner</strong></a></td>
<td>Steuert einen TV-Tuner.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamtvaudio"><strong>IAMTVAudio</strong></a></td>
<td>Steuert Audiodaten aus einer Fernsehquelle.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamtvtuner"><strong>IAMTVTuner</strong></a></td>
<td>Steuert einen TV-Tuner.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs"><strong>IAMVfwCaptureDialogs</strong></a></td>
<td>Zeigt ein Dialogfeld an, das von einem Video for Windows(VFW)-Erfassungstreiber bereitgestellt wird.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs"><strong>IAMVfwCompressDialogs</strong></a></td>
<td>Zeigt ein Dialogfeld an, das von einem Video for Windows-Codec (VFW) bereitgestellt wird.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></td>
<td>Ermöglicht einem Videodecoderfilter den Zugriff auf directX Video Acceleration (DXVA) 1.0-Funktionen.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify"><strong>IAMVideoAcceleratorNotify</strong></a></td>
<td>Rückrufschnittstelle für DXVA 1.0.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a></td>
<td>Legt Videokomprimierungseigenschaften fest und ruft sie ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol"><strong>IAMVideoControl</strong></a></td>
<td>Steuert bestimmte Videoaufnahmevorgänge, z. B. das Aufzählen verfügbarer Bildraten und bildausrichtung.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></td>
<td>Steuert, wie das Overlay-Mixer Videodezimation ausführt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp"><strong>IAMVideoProcAmp</strong></a></td>
<td>Passt die Qualitäten eines eingehenden Videosignals an.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass"><strong>IAMWMBufferPass</strong></a></td>
<td>Ruft Eigenschaften für einzelne Beispiele in einem ASF-Stream ab oder legt sie fest.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback"><strong>IAMWMBufferPassCallback</strong></a></td>
<td>Rückrufschnittstelle, die mit der <a href="/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass"><strong>IAMWMBufferPass-Schnittstelle verwendet</strong></a> wird.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder"><strong>IAMWstDecoder</strong></a></td>
<td>Legt Informationen zu World Standard Teletext (WST) fest und ruft sie ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iasyncreader"><strong>IAsyncReader</strong></a></td>
<td>Führt eine asynchrone Datenanforderung für einen Filter aus.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
<td>Wird von Filtern verfügbar gemacht. Dies ist die primäre Schnittstelle für alle DirectShow-Filter.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></td>
<td>Steuert die Lautstärke und das Gleichgewicht des Audiostreams.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></td>
<td>Legt Videoeigenschaften fest, z. B. das Ziel- und Quellrechteck.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vidcap/nn-vidcap-icameracontrol"><strong>ICameraControl</strong></a></td>
<td>Steuert die Kameraeinstellungen auf einem Aufnahmegerät.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2"><strong>ICaptureGraphBuilder2</strong></a></td>
<td>Erstellt Erfassungsdiagramme und andere benutzerdefinierte Filterdiagramme.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a></td>
<td>Konfiguriert einen Encoder oder Decoder.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter"><strong>IConfigAsfWriter</strong></a></td>
<td>Konfiguriert den <a href="wm-asf-writer-filter.md">WM ASF Writer-Filter.</a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2"><strong>IConfigAsfWriter2</strong></a></td>
<td>Erweitert die <a href="/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter"><strong>IConfigAsfWriter-Schnittstelle.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a></td>
<td>Konfiguriert den <a href="avi-mux-filter.md">AVI Mux-Filter.</a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a></td>
<td>Steuert, wie der AVI Mux Audio- und Videobeispiele überlagert.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-icreatedevenum"><strong>ICreateDevEnum</strong></a></td>
<td>Erstellt einen Enumerator für eine Kategorie von Filtern.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></td>
<td>Aktiviert die Videowiedergabe im exklusiven DirectDraw-Vollbildmodus.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></td>
<td>Rückrufschnittstelle für die <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idecimatevideoimage"><strong>IDecimateVideoImage</strong></a></td>
<td>Gibt die Dezimierung für einen Decoderfilter an.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-ideferredcommand"><strong>IDeferredCommand</strong></a></td>
<td>Bricht Graphsteuerbefehle ab, die mithilfe der <a href="/windows/desktop/api/Control/nn-control-iqueuecommand"><strong>IQueueCommand-Schnittstelle</strong></a> in die Warteschlange gestellt wurden, oder ändert sie.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></td>
<td>Fragt den <a href="video-renderer-filter.md">Videorendererfilter</a> zu DirectDraw-Oberflächen und Hardwarefunktionen ab.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></td>
<td>Ermöglicht den Zugriff auf DirectDraw-Oberflächen, die vom <a href="overlay-mixer-filter.md">Overlay-Mixer</a> werden.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasampleallocator"><strong>IDirectDrawMediaSampleAllocator</strong></a></td>
<td>Ordnet Beispiele zu, die DirectDraw-Oberflächen enthalten.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idistributornotify"><strong>IDistributorNotify</strong></a></td>
<td>Ermöglicht es einem Plug-In-Verteiler, benachrichtigt zu werden, wenn sich das Filterdiagramm ändert.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter"><strong>IDMOWrapperFilter</strong></a></td>
<td>Ermöglicht einer Anwendung die Verwendung eines DirectX Media Object (DMO) in einem Filterdiagramm.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/qnetwork/nn-qnetwork-idshowplugin"><strong>IDShowPlugin</strong></a></td>
<td>Ermöglicht dem Windows Medienquellenfilter die Kommunikation mit dem Windows Media Player 6.4-Plug-In für Netscape Navigator.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idvdcmd"><strong>IDvdCmd</strong></a></td>
<td>Wartet, bis DVD-Befehle gestartet oder beendet werden.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a></td>
<td>Navigiert und gibt DVD-Video wieder.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder"><strong>IDvdGraphBuilder</strong></a></td>
<td>Erstellt ein Filterdiagramm für die DVD-Video Wiedergabe.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a></td>
<td>Meldet Attribute eines DVD-Datenträgers oder den aktuellen Status des DVD Navigator-Filters.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idvdstate"><strong>IDvdState</strong></a></td>
<td>Speichert den aktuellen DVD-Wiedergabespeicherort und -status.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a></td>
<td>Legt Eigenschaften für den <a href="dv-video-encoder-filter.md">DV Video Encoder-Filter</a> fest und ruft sie ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a></td>
<td>Steuert den dynamischen Bereich in den Filtern DV Video Encoder und <a href="dv-video-decoder-filter.md">DV Video Decoder.</a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-idvsplitter"><strong>IDVSplitter</strong></a></td>
<td>Herabstufung der Bildfrequenz für einen DV-Stream (Digital Video).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ienumfilters"><strong>IEnumFilters</strong></a></td>
<td>Listet die Filter in einem Filterdiagramm auf.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ienummediatypes"><strong>IEnumMediaTypes</strong></a></td>
<td>Aufzählen der bevorzugten Medientypen eines Pins</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/bdaiface/nn-bdaiface-ienumpidmap"><strong>IEnumPIDMap</strong></a></td>
<td>Listet die Zuordnungen von Paket-IDs (PID) zu Ausgabepins im <a href="mpeg-2-demultiplexer.md">MPEG-2-Demultiplexerfilter</a> auf.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ienumpins"><strong>IEnumPins</strong></a></td>
<td>Listet Stecknadeln in einem Filter auf.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ienumstreamidmap"><strong>IEnumStreamIdMap</strong></a></td>
<td>Listet die Zuordnungen von Stream-IDs zu Ausgabepins im MPEG-2-Demultiplexerfilter auf.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter"><strong>IFileSinkFilter</strong></a></td>
<td>Wird von Filtern verfügbar gemacht, die Daten in eine Datei schreiben.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2"><strong>IFileSinkFilter2</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter"><strong>IFileSinkFilter-Schnittstelle.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a></td>
<td>Wird von Quellfiltern verfügbar gemacht.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifilterchain"><strong>IFilterChain</strong></a></td>
<td>Startet, beendet oder entfernt Filterketten in einem Filterdiagramm.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifiltergraph"><strong>IFilterGraph</strong></a></td>
<td>Erstellt ein Filterdiagramm.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2"><strong>IFilterGraph2</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Strmif/nn-strmif-igraphbuilder"><strong>IGraphBuilder-Schnittstelle.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3"><strong>IFilterGraph3</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2"><strong>IFilterGraph2-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2"><strong>IFilterMapper2</strong></a></td>
<td>Registriert filter und entfernt die Registrierung und sucht filter in der Registrierung.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ifiltermapper3"><strong>IFilterMapper3</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2"><strong>IFilterMapper2-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex"><strong>IFullScreenVideoEx</strong></a></td>
<td>Wird vom <a href="full-screen-renderer-filter.md">Vollbild-Rendererfilter</a> verfügbar gemacht.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey"><strong>IGetCapabilitiesKey</strong></a></td>
<td>Ruft die Funktionen eines Software- oder Hardwareencoders aus der Registrierung ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-igraphbuilder"><strong>IGraphBuilder</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Strmif/nn-strmif-ifiltergraph"><strong>IFilterGraph-Schnittstelle.</strong></a> Dies ist die primäre Schnittstelle des Filter Graph-Managers.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-igraphconfig"><strong>IGraphConfig</strong></a></td>
<td>Konfiguriert das Filterdiagramm neu, während das Diagramm ausgeführt wird.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback"><strong>IGraphConfigCallback</strong></a></td>
<td>Rückrufschnittstelle für die <a href="/windows/desktop/api/Strmif/nn-strmif-igraphconfig"><strong>IGraphConfig-Schnittstelle.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-igraphversion"><strong>IGraphVersion</strong></a></td>
<td>Ruft die aktuelle Versionsnummer des Filterdiagramms ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a></td>
<td>Konfiguriert den <a href="dv-video-decoder-filter.md">FILTER DV-Videodecoder.</a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vidcap/nn-vidcap-iksnodecontrol"><strong>IKsNodeControl</strong></a></td>
<td>Verfügbar gemacht durch USB Video Class (UVC)-Erweiterungseinheiten.</td>
</tr>
<tr class="odd">
<td><a href="ikspin.md"><strong>IKsPin</strong></a></td>
<td>Ruft die von einem Kernelmodus-Pin unterstützten Medien ab.</td>
</tr>
<tr class="even">
<td><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></td>
<td>Legt Eigenschaften für einen Kernelmodusfilter fest.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vidcap/nn-vidcap-ikstopologyinfo"><strong>IKsTopologyInfo</strong></a></td>
<td>Listet die Knoten in einem Streamklassentreiber auf.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-imediacontrol"><strong>IMediaControl</strong></a></td>
<td>Steuert den Datenfluss durch das Filterdiagramm.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-imediaevent"><strong>IMediaEvent</strong></a></td>
<td>Ruft Ereignisbenachrichtigungen aus dem Filterdiagramm ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-imediaeventex"><strong>IMediaEventEx</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Control/nn-control-imediaevent"><strong>IMediaEvent-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></td>
<td>Benachrichtigt den Filter Graph Manager über Ereignisse, die im Filterdiagramm auftreten.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imediafilter"><strong>IMediaFilter</strong></a></td>
<td>Steuert den Streamingstatus eines Filters.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></td>
<td>Steuerelemente, die im Filterdiagramm gesucht werden.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imediapropertybag"><strong>IMediaPropertyBag</strong></a></td>
<td>Legt INFO- und DISP-Blöcke in Audio-Video AVI-Dateien (Interleaved) fest und ruft sie ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></td>
<td>Legt Eigenschaften für Medienbeispiele fest und ruft sie ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2config"><strong>IMediaSample2Config</strong></a></td>
<td>Gibt einen Zeiger auf eine Direct3D-Oberfläche zurück, die einen VRAM-Erfassungspuffer darstellt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></td>
<td>Steuerelemente, die im Filterdiagramm gesucht werden.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imemallocator"><strong>IMemAllocator</strong></a></td>
<td>Ordnet Medienbeispiele zu.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp"><strong>IMemAllocatorCallbackTemp</strong></a></td>
<td>Aktiviert einen Filter, um eine Rückrufbenachrichtigung von einer Zuweisung zu empfangen.
<blockquote>
[!Note]<br />
Veraltet.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp"><strong>IMemAllocatorNotifyCallbackTemp</strong></a></td>
<td>Rückrufschnittstelle für die <a href="/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp"><strong>IMemAllocatorCallbackTemp-Schnittstelle.</strong></a>
<blockquote>
[!Note]<br />
Veraltet.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></td>
<td>Übermittelt Mediendaten an einen Eingabepin.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></td>
<td>Wird vom Filter Overlay Mixer verfügbar gemacht.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></td>
<td>Rückrufschnittstelle für die <a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a></td>
<td>Bearbeitet Videostreams auf dem Filter Overlay Mixer.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></td>
<td>Erweitert die <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></td>
<td>Konfiguriert den MPEG-2-Demultiplexerfilter.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a></td>
<td>Ordnet dem MPEG-2-Demultiplexer-Filter mindestens eine Paket-IDs (PIDs) zu.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></td>
<td>Ordnet einen Ausgabepin für den MPEG-2-Demultiplexerfilter einer oder mehreren Stream-IDs zu.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/mpegtype/nn-mpegtype-impegaudiodecoder"><strong>IMpegAudioDecoder</strong></a></td>
<td>Konfiguriert den MPEG-1-Audiodecoder.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a></td>
<td>Ermöglicht es einem Filter, direkt in den Videospeicher zu schreiben.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a></td>
<td>Rückrufschnittstelle für die <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify2"><strong>IOverlayNotify2</strong></a></td>
<td>Rückrufschnittstelle für die <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay-Schnittstelle.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></td>
<td>Legt INFO- und DISP-Blöcke in Audio-Video Interleaved-Streams (AVI) fest und ruft sie ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></td>
<td>Wird von allen Filterpins verfügbar gemacht.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></td>
<td>Stellt erneut eine Verbindung mit einem Eingabepin her, während der Filter noch ausgeführt wird.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol"><strong>IPinFlowControl</strong></a></td>
<td>Blockiert den Datenfluss von einem aktiven Ausgabepin.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
<td>Bietet Unterstützung für die Qualitätssteuerung im Filterdiagramm.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></td>
<td>Ruft Leistungsinformationen von Videorenderern ab.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-iqueuecommand"><strong>IQueueCommand</strong></a></td>
<td>Reiht einen Befehl im Filterdiagramm zur Verarbeitung zu einem bestimmten Zeitpunkt in die Warteschlange ein.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></td>
<td>Stellt die Referenzzeit für das Filterdiagramm bereit.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol"><strong>IReferenceClockTimerControl</strong></a></td>
<td>Ändert den von einer Verweisuhr verwendeten Timerzeitraum.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider"><strong>IRegisterServiceProvider</strong></a></td>
<td>Registriert ein Objekt als Dienst beim Filter Graph-Manager.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iresourceconsumer"><strong>IResourceConsumer</strong></a></td>
<td>Rückrufschnittstelle für die <a href="/windows/desktop/api/Strmif/nn-strmif-iresourcemanager"><strong>IResourceManager-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iresourcemanager"><strong>IResourceManager</strong></a></td>
<td>Löst Konflikte für Systemressourcen auf.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru"><strong>ISeekingPassThru</strong></a></td>
<td>Implementiert die Suche nach One-Input-Filtern.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vidcap/nn-vidcap-iselector"><strong>ISelector</strong></a></td>
<td>Wählt Quellknoten in einem Streamklassentreiber aus.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></td>
<td>Aktiviert einen Ausgabepin, um den Downstreamabschnitt des Filterdiagramms zu erstellen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivideoframestep"><strong>IVideoFrameStep</strong></a></td>
<td>Schritte durch einen Videostream.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp"><strong>IVideoProcAmp</strong></a></td>
<td>Steuert die Einstellungen für die Bildanpassung (ProcAmp) auf einem Erfassungsgerät.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></td>
<td>Legt Eigenschaften im Videofenster fest.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></td>
<td>steuert, ob der Filter 7 (VMR-7) des <a href="video-mixing-renderer-filter-7.md">Videomischungsrenderers</a> das Seitenverhältnis des Quellvideos beibehaltung.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></td>
<td>Steuert, ob der <a href="video-mixing-renderer-filter-9.md">Video Mixing Renderer Filter 9</a> (VMR-9) das Seitenverhältnis des Quellvideos beibehaltung.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></td>
<td>Unterstützt hardwarebeschleunigtes Deinterlacing mit vmr-7.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></td>
<td>Unterstützt hardwarebeschleunigtes Deinterlacing mithilfe von VMR-9.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></td>
<td>Konfiguriert VMR-7.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></td>
<td>Konfiguriert VMR-9.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></td>
<td>Wird von VMR-7-Compositoren verfügbar gemacht.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></td>
<td>Verfügbar gemacht durch VMR-9-Compositoren.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></td>
<td>Verfügbar gemacht von VMR-7 allocator-presenters.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></td>
<td>Verfügbar gemacht von VMR-9 allocator-presenters.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></td>
<td>Legt die Renderereinstellungen für die image presenter fest, die von VMR-7 verwendet wird.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></td>
<td>Legt die Renderereinstellungen für die image presenter fest, die von VMR-9 verwendet wird.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterexclmodeconfig"><strong>IVMRImagePresenterExclModeConfig</strong></a></td>
<td>Festlegen und Abrufen der Renderereinstellungen für den exklusiven Modus Allocator-Presenter für VMR-7</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></td>
<td>Fügt bei Verwendung von VMR-7 ein statisches Image in den Videostream ein.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></td>
<td>Fügt bei Verwendung von VMR-9 ein statisches Image in den Videostream ein.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></td>
<td>Bearbeitet die eingehenden Videostreams auf der VMR-7.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></td>
<td>Bearbeitet die eingehenden Videodatenströme auf der VMR-9.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></td>
<td>Steuert die Überwachung der Nutzung durch die VMR-7.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></td>
<td>Steuert die Überwachung der Nutzung durch VMR-9.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurface"><strong>IVMRSurface</strong></a></td>
<td>Verfügbar gemacht durch Medienbeispiele von VMR-7.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></td>
<td>Verfügbar gemacht durch Medienbeispiele von VMR-9.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></td>
<td>Ordnet die DirectDraw-Oberflächen zu, die vom ALLOCATOR-Presenter VMR-7 verwendet werden.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></td>
<td>Ordnet die direct3D-Oberflächen zu, die vom Allocator-Presenter VMR-9 verwendet werden.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></td>
<td>Erweitert die <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9-Schnittstelle.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></td>
<td>Ermöglicht dem Allocator-Presenter, vmR-7 zu benachrichtigen.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></td>
<td>Ermöglicht dem allocator-presenter das Benachrichtigen von VMR-9.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></td>
<td>Steuert Eingabepins auf der VMR-7.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></td>
<td>Steuert Eingabepins auf der VMR-9.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></td>
<td>Steuert, wie die VMR-7 einen Videostream rendert.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></td>
<td>Steuert, wie die VMR-9 einen Videostream rendert.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig"><strong>IVPBaseConfig</strong></a></td>
<td>Basisschnittstelle für die <a href="/previous-versions/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig"><strong>IVPConfig-Schnittstelle.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpbasenotify"><strong>IVPBaseNotify</strong></a></td>
<td>Basisschnittstelle für die <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify-Schnittstelle.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig"><strong>IVPConfig</strong></a></td>
<td>Ermöglicht einem Videoport die Kommunikation mit dem Filter Overlay Mixer.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ivpmanager"><strong>IVPManager</strong></a></td>
<td>Wird vom Videoport-Manager-Filter verfügbar gemacht.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a></td>
<td>Aktiviert die Überlagerungs-Mixer, um die Eigenschaften eines Hardwaregeräts zu steuern, das einen Videoport verwendet.</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
<td>Erweitert die <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify-Schnittstelle.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/amxmlgraphbuilder/nn-amxmlgraphbuilder-ixmlgraphbuilder"><strong>IXMLGraphBuilder</strong></a></td>
<td>Persistentes Speichern eines DirectShow-Filterdiagramms mithilfe eines XML-Dateiformats.
<blockquote>
[!Note]<br />
Veraltet.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veraltete Schnittstellen](deprecated-interfaces.md)
</dt> </dl>

 

 




