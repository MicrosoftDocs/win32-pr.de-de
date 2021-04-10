---
description: Media Foundation Schnittstellen
ms.assetid: 3e367190-4c88-430e-adbf-9837e1bf0d2b
title: Media Foundation Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12379dc83287b2a03ae0223a5a9a7d945d8fa77
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961109"
---
# <a name="media-foundation-interfaces"></a>Media Foundation Schnittstellen

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapture"><strong>Iadvancedmediacapture</strong></a><br/></td>
<td>Aktiviert die erweiterte Medien Erfassung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediacapture/nn-mfmediacapture-iadvancedmediacaptureinitializationsettings"><strong>Iadvancedmediacaptureinitializationsettings</strong></a><br/></td>
<td>Stellt Initialisierungs Einstellungen für die erweiterte Medien Erfassung bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapturesettings"><strong>Iadvancedmediacapturesettings</strong></a><br/></td>
<td>Stellt Einstellungen für die erweiterte Medien Erfassung bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9"><strong>IDirect3DDeviceManager9</strong></a><br/></td>
<td>Ermöglicht zwei Threads das Freigeben desselben Direct3D 9-Geräts und ermöglicht den Zugriff auf die Features der DirectX-Video Beschleunigung (DXVA) des Geräts.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice"><strong>Idirectxvideoaccelerationservice</strong></a><br/></td>
<td>Stellt DXVA-Dienste (DirectX Video Acceleration) von einem Direct3D-Gerät bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder"><strong>Idirectxvideodecoder</strong></a><br/></td>
<td>Stellt ein DXVA-Video-Decodergerät (DirectX Video Acceleration) dar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice"><strong>Idirectxvideodecoderservice</strong></a><br/></td>
<td>Bietet Zugriff auf die DXVA-decoderdienste (DirectX Video Acceleration).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>Idirectxvideomemoryconfiguration</strong></a><br/></td>
<td>Legt den Typ des Video Speichers für nicht komprimierte Video Oberflächen fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor"><strong>Idirectxvideoprocessor</strong></a><br/></td>
<td>Stellt ein DXVA-Videoprozessor Gerät (DirectX Video Acceleration) dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice"><strong>Idirectxvideoprocess-Service</strong></a><br/></td>
<td>Bietet Zugriff auf die Video Verarbeitungsdienste von DirectX Video Acceleration (DXVA).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>Ievrfilterconfig</strong></a><br/></td>
<td>Legt die Anzahl der Eingabe Pins für den von DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>Enhanced Video Renderer</strong></a> (EVR)-Filter fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfigex"><strong>Ievrfilterconfigex</strong></a><br/></td>
<td>Konfiguriert den "DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>Enhanced Video Renderer</strong></a> "-Filter (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin"><strong>Ievrtreuhändvideoplugin</strong></a><br/></td>
<td>Aktiviert eine Plug-in-Komponente für den erweiterten Videorenderer (EVR), um mit geschützten Medien zu arbeiten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>Ievrvideostreamcontrol</strong></a><br/></td>
<td>Diese Schnittstelle wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer"><strong>IMF2DBuffer</strong></a><br/></td>
<td>Stellt einen Puffer dar, der eine zweidimensionale Oberfläche (z. b. einen Videoframe) enthält. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2"><strong>IMF2DBuffer2</strong></a><br/></td>
<td>Stellt einen Puffer dar, der eine zweidimensionale Oberfläche (z. b. einen Videoframe) enthält.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate"><strong>Imfaktivate</strong></a><br/></td>
<td>Ermöglicht der Anwendung, die Erstellung eines Objekts zurückzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo"><strong>Imfasf ContentInfo</strong></a><br/></td>
<td>Stellt Methoden bereit, um mit dem Header Abschnitt von Dateien zu arbeiten, die der ASF-Spezifikation (Advanced Systems Format) entsprechen. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer"><strong>Imfasfindexer</strong></a><br/></td>
<td>Stellt Methoden zum Arbeiten mit Indizes in ASF-Dateien (Systems Format) bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer"><strong>Imfasf Multiplexer</strong></a><br/></td>
<td>Stellt Methoden zum Erstellen von Datenpaketen für das Advanced Systems Format (ASF) bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion"><strong>Imfassmutualexclusion</strong></a><br/></td>
<td>Konfiguriert ein gegenseitiges zwischen Abgleich-Ausschluss Objekt von Advanced Systems Format (ASF), das Informationen über eine Gruppe von Datenströmen in einem ASF-Profil verwaltet, die sich gegenseitig ausschließen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile"><strong>Imfasf profile</strong></a><br/></td>
<td>Verwaltet ein ASF-Profil (Advanced Systems Format).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter"><strong>Imfasfäsplitter</strong></a><br/></td>
<td>Stellt Methoden zum Lesen von Daten aus einer ASF-Datei (Advanced Systems Format) bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig"><strong>Imfasf streamconfig</strong></a><br/></td>
<td>Konfiguriert die Einstellungen eines Datenstroms in einer ASF-Datei.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization"><strong>Imfasf streampriorisierung</strong></a><br/></td>
<td>Nicht implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector"><strong>Imfasfästreamselector</strong></a><br/></td>
<td>Wählt Streams in einer ASF-Datei (Advanced Systems Format) basierend auf den gegenseitigen Ausschluss Informationen im ASF-Header aus.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback"><strong>Imfasynccallback</strong></a><br/></td>
<td>Rückruf Schnittstelle, um die Anwendung zu benachrichtigen, wenn eine asynchrone Methode abgeschlossen ist. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mfobjects/nn-mfobjects-imfasynccallbacklogging"><strong>Imfasynccallbacklogging</strong></a><br/></td>
<td>Stellt Protokollierungs Informationen zu dem übergeordneten Objekt bereit, dem der Async-Rückruf zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>Imfasynkresult</strong></a><br/></td>
<td>Stellt Informationen über das Ergebnis eines asynchronen Vorgangs bereit. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>Imfattributes</strong></a><br/></td>
<td>Stellt eine generische Möglichkeit zum Speichern von Schlüssel-Wert-Paaren für ein-Objekt bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMF audiomediatype</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>Imsaudiomediatype</strong></a> steht nicht mehr zur Verwendung ab Windows 7 zur Verfügung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy"><strong>IMF audiopolicy</strong></a><br/></td>
<td>Konfiguriert die Audiositzung, die dem Streaming-audiorenderer (SAR) zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume"><strong>IMF audiostreamvolume</strong></a><br/></td>
<td>Steuert die volumeebenen einzelner Audiokanäle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfbufferlistnotify"><strong>IMF bufferlistnotify</strong></a><br/></td>
<td>Aktiviert das <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>imfsourcebufferlist</strong></a> -Objekt, um seine Clients über wichtige Zustandsänderungen zu benachrichtigen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream"><strong>IMFByteStream</strong></a><br/></td>
<td>Stellt einen Bytestream aus einer Datenquelle dar, bei der es sich möglicherweise um eine lokale Datei, eine Netzwerkdatei oder eine andere Quelle handelt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering"><strong>IMF bytestreambufferung</strong></a><br/></td>
<td>Steuert, wie ein Bytestream Daten aus einem Netzwerk puffert. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol"><strong>IMF bytestreamcachecontrol</strong></a><br/></td>
<td>Steuert, wie ein netzwerkbytestream Daten in einen lokalen Cache überträgt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol2"><strong>IMFByteStreamCacheControl2</strong></a><br/></td>
<td>Steuert, wie ein netzwerkbytestream Daten in einen lokalen Cache überträgt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler"><strong>IMF bytestreamhandler</strong></a><br/></td>
<td>Erstellt eine Medienquelle aus einem Bytestream. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestreamproxyclassfactory"><strong>IMF bytestreamproxyclassfactory</strong></a><br/></td>
<td>Erstellt einen Proxy für einen Byte Datenstrom.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamtimeseek"><strong>IMF bytestreamtimeseek</strong></a><br/></td>
<td>Sucht einen Bytestream nach Zeit Position.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine"><strong>IMF-Engine</strong></a><br/></td>
<td>Steuert ein oder mehrere Aufzeichnungsgeräte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineclassfactory"><strong>IMF captureengineclassfactory</strong></a><br/></td>
<td>Erstellt eine Instanz der Erfassungs-Engine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineoneventcallback"><strong>IMF captureengineoneventcallback</strong></a><br/></td>
<td>Rückruf Schnittstelle für das Empfangen von Ereignissen von der Erfassungs-Engine.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMF captureengineonsamplecallback</strong></a><br/></td>
<td>Rückruf Schnittstelle zum Empfangen von Daten von der Erfassungs-Engine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback2"><strong>IMFCaptureEngineOnSampleCallback2</strong></a><br/></td>
<td>Erweiterungen für die <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>imfcaptureengineonsamplecallback</strong></a> -Rückruf Schnittstelle, die zum Empfangen von Daten aus der Aufzeichnungs-Engine verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink"><strong>IMF capturephotosink</strong></a><br/></td>
<td>Steuert die Photo-Senke.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink"><strong>IMF capturepreviewsink</strong></a><br/></td>
<td>Steuert die Vorschau Senke.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink"><strong>IMF capturerecordsink</strong></a><br/></td>
<td>Steuert die Aufzeichnungs Senke.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMF capturesink</strong></a><br/></td>
<td>Steuert eine Aufzeichnungs Senke, bei der es sich um ein Objekt handelt, das einen oder mehrere Streams von einem Erfassungsgerät empfängt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink2"><strong>IMFCaptureSink2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>imfcapturesink</strong></a> -Schnittstelle, um Funktionen für das dynamische Festlegen des Ausgabemedien Typs der Daten Satz-Senke oder der Vorschaufenster bereitzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource"><strong>IMF capturesource</strong></a><br/></td>
<td>Steuert das Erfassungs Quell Objekt. Die Erfassungs Quelle verwaltet die Audiogeräte und Video Erfassungsgeräte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify"><strong>IMF cdmsuspendnotify</strong></a><br/></td>
<td>Wird verwendet, um dem Client das Benachrichtigen des Inhalts Entschlüsselungs Moduls (CDM) zu ermöglichen, wenn globale Ressourcen vor dem Anhalten in einen konsistenten Zustand versetzt werden sollten. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock"><strong>IMF</strong></a><br/></td>
<td>Stellt Zeit Steuerungsinformationen von einer Uhr in Microsoft Media Foundation bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockconsumer"><strong>IMF-Consumer</strong></a><br/></td>
<td>Wird von einer APP implementiert, um Zugriff auf <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>imfpresentationclock</strong></a>zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink"><strong>IMF-staatink</strong></a><br/></td>
<td>Empfängt Zustands Änderungs Benachrichtigungen von der Präsentations Uhr. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection"><strong>Imbercollection</strong></a><br/></td>
<td>Stellt eine generische Auflistung von <strong>IUnknown</strong> -Zeigern dar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext"><strong>IMF contentdecryptor Context</strong></a><br/></td>
<td>Ermöglicht einem Entschlüsselungen das Verwalten von Hardware Schlüsseln und das Entschlüsseln von Hardware Beispielen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler"><strong>IMF contentenabler</strong></a><br/></td>
<td>Implementiert einen Schritt, der für den Benutzer ausgeführt werden muss, um auf Medieninhalte zuzugreifen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice"><strong>IMF contentschutzdevice</strong></a><br/></td>
<td>Ermöglicht es einem Entschlüsselungs Dienst, mit dem Sicherheits Prozessor zu kommunizieren, der die Hardware Entschlüsselung für ein Schutzsystem implementiert. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager"><strong>IMF contentprotection Manager</strong></a><br/></td>
<td>Ermöglicht die Wiedergabe geschützter Inhalte durch Bereitstellen eines Zeigers eines inhaltsenabler-Objekts für die Anwendung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample"><strong>IMF-redsample</strong></a><br/></td>
<td>Ermöglicht dem Presenter für den erweiterten Videorenderer (EVR), einen bestimmten Frame vom Video-Mixer anzufordern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmp2dlna/nn-mfmp2dlna-imfdlnasinkinit"><strong>IMF-nasinkinit</strong></a><br/></td>
<td>Initialisiert die Media-Senke der Digital Living Network Alliance (DLNA). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfdrmnethelper"><strong>Imbdrmnetthelper</strong></a><br/></td>
<td>Konfiguriert Windows Media Digital Rights Management (DRM) für Netzwerkgeräte in einer Netzwerk Senke.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer"><strong>IMF dxgibuffer</strong></a><br/></td>
<td>Stellt einen Puffer dar, der eine DXGI-Oberfläche (Microsoft DirectX Graphics Infrastructure) enthält.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMF dxgidebug Manager</strong></a><br/></td>
<td>Ermöglicht zwei Threads das Freigeben desselben Microsoft Direct3D 11-Geräts.<br/></td>
</tr>
<tr class="odd">
<td><a href="imfdxgidevicemanagersource.md"><strong>IMF-xgide vicemanagersource</strong></a><br/></td>
<td>Stellt Funktionen zum erhalten von <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>imsdxgidevicemanager</strong></a> aus der Media Foundation Video Rendering-Senke bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock"><strong>Imffieldofusemftunlock</strong></a><br/></td>
<td>Ermöglicht es einer Anwendung, eine Media Foundation Transformation (MFT) zu verwenden, deren Verwendung Einschränkungen hat.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink"><strong>Imffinalizablemediasink</strong></a><br/></td>
<td>Optional von Medien senken unterstützt, um erforderliche Aufgaben vor dem Herunterfahren auszuführen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMF-Dienst</strong></a><br/></td>
<td>Fragt ein Objekt für eine angegebene Dienst Schnittstelle ab. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest"><strong>IMF httpdownloadrequest</strong></a><br/></td>
<td>Anwendungen implementieren diese Schnittstelle, um die Standard Implementierung der von Microsoft Media Foundation verwendeten HTTP-und HTTPS-Protokolle zu überschreiben. Anwendungen stellen die <strong>imfhttpdownloadrequest</strong> -Schnittstelle bereit, um Sie über die Methode "Methode" <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest"><strong>in der "</strong></a> <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>imfhttpdownloadsession</strong></a> "-Schnittstelle zu Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMF httpdownloadsession</strong></a><br/></td>
<td>Anwendungen implementieren diese Schnittstelle, um die Standard Implementierung der von Microsoft Media Foundation verwendeten HTTP-und HTTPS-Protokolle zu überschreiben. Anwendungen stellen die <strong>imfhttpdownloadsession</strong> -Schnittstelle für Media Foundation über <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>die Methode "" der Methode</strong></a> " <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>imfhttpdownloadsessionprovider</strong></a> " bereit. Microsoft Media Foundation verwendet diese Schnittstelle, um einen "Streaming"-oder "progressiv"-Download einer Ressource durchzuführen, die durch eine HTTP-oder HTTPS-URL identifiziert wird. Zum Herunterladen der Ressource können mehrere HTTP-Anforderungen gesendet werden. Die <strong>imfhttpdownloadsession</strong> -Schnittstelle wird verwendet, um diese einzelnen HTTP-Anforderungen zu erstellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMF httpdownloadsessionprovider</strong></a><br/></td>
<td>Anwendungen implementieren diese Schnittstelle, um benutzerdefinierte HTTP-oder https-Download Implementierungen bereitzustellen. Verwenden Sie die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>imfsourceresolver</strong></a> -Schnittstelle, um den Anbieter zu registrieren. Weitere Informationen finden Sie unter <a href="using-the-source-resolver.md">using the Source Resolver</a>. Nachdem die Microsoft Media Foundation registriert wurde, ruft die-die Methode " <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>samatehttpdownloadsession</strong></a> " der Anbieter Implementierung auf, um http-oder HTTPS-URLs zu öffnen, anstatt die Standard Implementierung zu verwenden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>Imfmagesharingengine</strong></a><br/></td>
<td>Aktiviert die Bildfreigabe.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengineclassfactory"><strong>Imfmagesharingengineclassfactory</strong></a><br/></td>
<td>Erstellt eine Instanz von <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>imfmagesharingengine</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority"><strong>Imfinputtrustauthority</strong></a><br/></td>
<td>Ermöglicht anderen Komponenten im geschützten Medien Pfad (PMP), das von einer Eingabe Vertrauensstelle (ITA) bereitgestellte Eingabe Schutzsystem zu verwenden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imflocalmftregistration"><strong>Imflocalmautregistration</strong></a><br/></td>
<td>Registriert Media Foundation Transformationen (MFTs) im Prozess des Aufrufers.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer"><strong>Imfmediabuffer</strong></a><br/></td>
<td>Stellt einen Speicherblock dar, der Mediendaten enthält.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMF Media Engine</strong></a><br/></td>
<td>Ermöglicht es einer Anwendung, Audiodateien oder Videodateien wiederzugeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMF mediaengineclassfactory</strong></a><br/></td>
<td>Erstellt eine Instanz der Medien-Engine.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory2"><strong>IMFMediaEngineClassFactory2</strong></a><br/></td>
<td>Erstellt eine Instanz des <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMF MediaKeys</strong></a> -Objekts.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex"><strong>IMF mediaengineclassfacrenyex</strong></a><br/></td>
<td>Erweiterung für die <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMF mediaengineclassfactory</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme"><strong>IMF mediaengineeme</strong></a><br/></td>
<td>Wird von der Medien-Engine implementiert, um verschlüsselte Medien Erweiterungs Methoden hinzuzufügen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex"><strong>IMF mediaengineex</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMF Media Engine</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension"><strong>IMF mediaengineextension</strong></a><br/></td>
<td>Ermöglicht es einer Anwendung, Medienressourcen in der Medien-Engine zu laden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify"><strong>IMF mediaengineneedkeynotify</strong></a><br/></td>
<td>Stellt einen Rückruf an die Medien-Engine dar, um wichtige Anforderungs Daten zu benachrichtigen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify"><strong>IMF Media enginenotify</strong></a><br/></td>
<td>Rückruf Schnittstelle für die <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMF Media Engine</strong></a> -Schnittstelle. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineopminfo"><strong>IMF mediaengineopminfo</strong></a><br/></td>
<td>Stellt Methoden bereit, mit denen Informationen zum <a href="output-protection-manager.md">Output Protection Manager</a> (OPM) erhalten werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent"><strong>IMF mediaengineprotectedcontent</strong></a><br/></td>
<td>Ermöglicht der Medien-Engine das Abspielen geschützter Videoinhalte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>Imfmediaenginesrcelements</strong></a><br/></td>
<td>Stellt der Medien-Engine eine Liste mit Medienressourcen bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelementsex"><strong>IMF mediaenginesrcelementsex</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>imfmediaenginesrcelements</strong></a> -Schnittstelle, um zusätzliche Funktionen bereitzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesupportssourcetransfer"><strong>IMF mediaenginesupportssourcetransfer</strong></a><br/></td>
<td>Ermöglicht die Übertragung der Medienquelle zwischen der Medien-Engine und der Freigabe-Engine für die Wiedergabe in.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginewebsupport"><strong>IMF mediaenginewebsupport</strong></a><br/></td>
<td>Ermöglicht die Wiedergabe von webaudiodaten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror"><strong>IMF MediaError</strong></a><br/></td>
<td>Gibt den aktuellen Fehlerstatus für die Medien-Engine an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent"><strong>IMF Media Event</strong></a><br/></td>
<td>Stellt ein Ereignis dar, das von einem Media Foundation-Objekt generiert wird. Verwenden Sie diese Schnittstelle, um Informationen zum Ereignis zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMF Media Event Generator</strong></a><br/></td>
<td>Ruft Ereignisse von einem beliebigen Media Foundation Objekt ab, das Ereignisse generiert. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue"><strong>IMF mediaeventqueue</strong></a><br/></td>
<td>Stellt eine Ereignis Warteschlange für Anwendungen bereit, die die <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>imfmediaeventgenerator</strong></a> -Schnittstelle implementieren müssen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMF Media Keys</strong></a><br/></td>
<td>Stellt einen Medien Schlüssel dar, mit dem Mediendaten mithilfe eines DRM-Schlüssel Systems (Digital Rights Management) entschlüsselt werden. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession"><strong>IMF mediakeysession</strong></a><br/></td>
<td>Stellt eine Sitzung mit dem DRM-Schlüsselsystem (Digital Rights Management) dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysessionnotify"><strong>IMF mediakeysessionnotify</strong></a><br/></td>
<td>Bietet einen Mechanismus zum Benachrichtigen der APP über Informationen zur Medien schlüsselsitzung. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession"><strong>Imfmediasession</strong></a><br/></td>
<td>Stellt Wiedergabe Steuerelemente für geschützten und ungeschützten Inhalt bereit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>Imfmediasharingengine</strong></a><br/></td>
<td>Ermöglicht die Medien Freigabe.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengineclassfactory"><strong>Imfmediasharingengineclassfactory</strong></a><br/></td>
<td>Erstellt eine Instanz von <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>imfmediasharingengine</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink"><strong>Imfmediasink</strong></a><br/></td>
<td>Wird von Medien Senk Objekten implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll"><strong>Imfmediasinkpreroll</strong></a><br/></td>
<td>Ermöglicht, dass eine Medien Senke Stichproben empfängt, bevor die Präsentations Uhr gestartet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>Imfmediasource</strong></a><br/></td>
<td>Wird von Medienquellen Objekten implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex"><strong>Imfmediasourceex</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>imfmediasource</strong></a> -Schnittstelle, um zusätzliche Funktionen für eine Medienquelle bereitzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>Imfmediasourceextension</strong></a><br/></td>
<td>Stellt Funktionen für die Medienquellen Erweiterung (MSE) bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextensionnotify"><strong>Imfmediasourceextensionnotify</strong></a><br/></td>
<td>Stellt Funktionen zum anwecken von Ereignissen bereit, die <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>imfmediasourceextension</strong></a>zugeordnet sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider"><strong>Imfmediasourcepresentationprovider</strong></a><br/></td>
<td>Stellt Benachrichtigungen für die Sequencer-Quelle bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider"><strong>Imfmediasourcetopologyprovider</strong></a><br/></td>
<td>Ermöglicht es einer Anwendung, eine Topologie aus der Sequencer-Quelle zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream"><strong>IMF Media Stream</strong></a><br/></td>
<td>Stellt einen Stream in einer Medienquelle dar. <br/></td>
</tr>
<tr class="odd">
<td><a href="imfmediastreamsourcesamplerequest.md"><strong>Imfmediastreamsourcesamplerequest</strong></a><br/></td>
<td>Stellt eine Anforderung für ein Beispiel aus einem MediaStreamSource-Element dar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange"><strong>IMF mediatimerange</strong></a><br/></td>
<td>Stellt eine Liste von Zeit Bereichen dar, in denen jeder Bereich durch einen Start-und Endzeit Wert definiert wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype"><strong>IMF MediaType</strong></a><br/></td>
<td>Stellt eine Beschreibung eines Medien Formats dar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler"><strong>IMF mediatypeer Handler</strong></a><br/></td>
<td>Dient zum Abrufen und Festlegen von Medientypen für ein Objekt, z. b. eine Medienquelle oder eine Medien Senke. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata"><strong>IMF-Metadaten</strong></a><br/></td>
<td>Verwaltet die Metadaten für ein-Objekt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a><br/></td>
<td>Ruft Metadaten aus einer Medienquelle oder einem anderen Objekt ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager"><strong>IMF muxstreamattributesmanager</strong></a><br/></td>
<td>Bietet Zugriff auf die <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>unfattributes</strong></a> der untergeordneten Datenströme einer Multiplex Medienquelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager"><strong>IMF muxstreamsamplemanager</strong></a><br/></td>
<td>Bietet die Möglichkeit, <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>imfsample</strong></a> -Objekte für einzelne untergeordnete Datenströme innerhalb der Ausgabe einer multiplext-Medienquelle abzurufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager"><strong>IMF muxstreammediatypemanager</strong></a><br/></td>
<td>Ermöglicht die Verwaltung von streamkonfigurationen für eine Multiplex Medienquelle. Eine Datenstrom Konfiguration definiert eine Gruppe von unter strömen, die in die multiplext-Ausgabe eingeschlossen werden können.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential"><strong>IMF Network Credential</strong></a><br/></td>
<td>Legt Informationen zu Benutzername und Kennwort für Authentifizierungszwecke fest und ruft diese ab. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache"><strong>IMF netkredentialcache</strong></a><br/></td>
<td>Ruft Anmelde Informationen aus dem Cache für Anmelde Informationen ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager"><strong>IMF netkredentialmanager</strong></a><br/></td>
<td>Wird von Anwendungen implementiert, um Benutzer Anmelde Informationen für eine Netzwerkquelle bereitzustellen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcrossoriginsupport"><strong>IMF netcrossoriginsupport</strong></a><br/></td>
<td>Wird von Clients implementiert, die eine Ursprungs übergreifende Richtlinie für HTML5-Medien Downloads erzwingen möchten. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator"><strong>IMF netproxylocator</strong></a><br/></td>
<td>Bestimmt den Proxy, der beim Herstellen einer Verbindung mit einem Server verwendet werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory"><strong>IMF netproxyloerfactory</strong></a><br/></td>
<td>Erstellt ein proxylocatorobjekt, das den zu verwendenden Proxy bestimmt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter"><strong>Imbernetztresourcefilter</strong></a><br/></td>
<td>Benachrichtigt die Anwendung, wenn ein Bytestream eine URL anfordert, und ermöglicht der Anwendung das Blockieren der URL-Umleitung.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig"><strong>IMF netschemehandlerconfig</strong></a><br/></td>
<td>Konfiguriert ein Netzwerk Schema-Plug-in. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream"><strong>Imfobjectreferencestream</strong></a><br/></td>
<td>Marshunkt einen Schnittstellen Zeiger auf einen und aus einem Stream. <br/> Streamobjekte, die <strong>IStream</strong> unterstützen, können diese Schnittstelle zur Bereitstellung eines benutzerdefinierten Marshalling für Schnittstellen Zeiger verfügbar machen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy"><strong>IMF outputpolicy</strong></a><br/></td>
<td>Kapselt eine Verwendungs Richtlinie von einer eingabevertrauensstellungs-Autorität (ITA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema"><strong>IMF OutputSchema</strong></a><br/></td>
<td>Kapselt Informationen zu einem Ausgabe Schutzsystem und den entsprechenden Konfigurationsdaten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority"><strong>IMF outputtrustauthority</strong></a><br/></td>
<td>Kapselt die Funktionalität eines oder mehrerer Ausgabe Schutzsysteme, die von einer vertrauenswürdigen Ausgabe unterstützt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol"><strong>IMF-Steuerelement</strong></a><br/></td>
<td>Steuert, wie Medienquellen und Transformationen in Media Foundation aufgelistet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol2"><strong>IMFPluginControl2</strong></a><br/></td>
<td>Steuert, wie Medienquellen und Transformationen in Media Foundation aufgelistet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem"><strong>Imfpmediaitem</strong></a><br/></td>
<td>Stellt ein Medien Element dar. (Veraltet.)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>Imfpmediaplayer</strong></a><br/></td>
<td>Enthält Methoden zum Wiedergeben von Mediendateien. (Veraltet.)<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback"><strong>Imfpmediaplayercallback</strong></a><br/></td>
<td>Rückruf Schnittstelle für die <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>imfpmediaplayer</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient"><strong>Imfpmpclient</strong></a><br/></td>
<td>Ermöglicht es einer Medienquelle, einen Zeiger auf die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>imfpmphost</strong></a> -Schnittstelle zu erhalten. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclientapp"><strong>Imfpmpclientapp</strong></a><br/></td>
<td>Bietet einen Mechanismus, mit dem eine Medienquelle inhaltsschutzfunktionen in Windows Store-Apps implementieren können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>Imfpmphost</strong></a><br/></td>
<td>Ermöglicht es einer Medienquelle im Anwendungsprozess, Objekte im PMP-Prozess (Protected Media Path) zu erstellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp"><strong>Imfpmphostapp</strong></a><br/></td>
<td>Ermöglicht es einer Medienquelle, ein <a href="/windows/desktop/WinRT/reference">Windows-Runtime</a> Objekt im PMP-Prozess ( <a href="protected-media-path.md">Protected Media Path</a> ) zu erstellen. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver"><strong>Imfpmpserver</strong></a><br/></td>
<td>Ermöglicht zwei Instanzen der <a href="media-session.md">Medien Sitzung</a> , den gleichen PMP-Prozess (Protected Media Path) gemeinsam zu nutzen. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMF presentationclock</strong></a><br/></td>
<td>Stellt eine Präsentations Uhr dar, die verwendet wird, um zu planen, wann Samples gerendert werden und wie mehrere Streams synchronisiert werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor"><strong>IMF presentationdescriptor</strong></a><br/></td>
<td>Beschreibt die Details einer Präsentation. Eine <em>Präsentation</em> ist ein Satz verwandter Mediendaten Ströme, die eine gemeinsame Präsentationszeit haben. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource"><strong>IMF presentationtimesource</strong></a><br/></td>
<td>Gibt die Uhrzeiten für die Präsentations Uhr an. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfprotectedenvironmentaccess"><strong>IMF protectedenvironmentaccess</strong></a><br/></td>
<td>Bietet eine Methode, mit der Inhalts Schutzsysteme einen Handshake mit der geschützten Umgebung ausführen können. Dies ist erforderlich, da die APIs " <strong>appatefile</strong> " und " <strong>DeviceIoControl</strong> " für Windows Store-Apps nicht verfügbar sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMF-Empfehlung</strong></a><br/></td>
<td>Ermöglicht es dem Quality Manager, die Audio-oder Videoqualität einer Komponente in der Pipeline anzupassen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a><br/></td>
<td>Ermöglicht einem Pipeline Objekt, seine eigene Audio-oder Videoqualität als Reaktion auf Qualitäts Meldungen anzupassen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadviselimits"><strong>Immaqualityadviselimits</strong></a><br/></td>
<td>Fragt ein Objekt nach der Anzahl der unterstützten <em>Qualitäts Modi</em> ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager"><strong>IMF-Manager</strong></a><br/></td>
<td>Passt die Wiedergabequalität an. Diese Schnittstelle wird vom Quality Manager verfügbar gemacht. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>Imfratecontrol</strong></a><br/></td>
<td>Ruft die Wiedergabe Rate ab oder legt Sie fest. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>Imfratesupport</strong></a><br/></td>
<td>Fragt den Bereich der unterstützten Wiedergabe Raten ab, einschließlich der umgekehrten Wiedergabe.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory"><strong>Imfreadschreiteclassfactory</strong></a><br/></td>
<td>Erstellt eine Instanz des Senke Writers oder des Quell Readers.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>Imfrealtimeclient</strong></a><br/></td>
<td>Benachrichtigt ein Pipeline Objekt, sich selbst beim Multimedia Class Scheduler Service (MMCSS) zu registrieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex"><strong>Imfrealtimecliumtex</strong></a><br/></td>
<td>Benachrichtigt ein Pipeline Objekt, sich selbst beim Multimedia Class Scheduler Service (MMCSS) zu registrieren. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfremoteasynccallback"><strong>Imfremoteasynccallback</strong></a><br/></td>
<td>Wird von der Media Foundation Proxy/Stub-DLL verwendet, um bestimmte asynchrone Methodenaufrufe über Prozess Grenzen hinweg zu Mars Hallen.<br/> Diese Schnittstelle wird von Anwendungen nicht verwendet oder implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremotedesktopplugin"><strong>Imfremotedesktopplugin</strong></a><br/></td>
<td>Ändert eine Topologie für die Verwendung in einer Terminaldiensteumgebung. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy"><strong>Imfremoteproxy</strong></a><br/></td>
<td>Verfügbar gemacht von Objekten, die als Proxy für ein Remote Objekt fungieren.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle"><strong>Imsasamistyle</strong></a><br/></td>
<td>Legt die in der <a href="sami-media-source.md">Sami-Medienquelle</a>verfügbaren Sami-Stile fest und ruft diese ab. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMF Sample</strong></a><br/></td>
<td>Stellt ein Medien Beispiel dar, bei dem es sich um ein Container Objekt für Mediendaten handelt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>Imbersamplegrabbersinkcallback</strong></a><br/></td>
<td>Rückruf Schnittstelle zum erhalten von Mediendaten aus der Sample-Grabber-Senke. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback2"><strong>IMFSampleGrabberSinkCallback2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMF samplegrabbersink Callback</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsampleoutputstream"><strong>IMF Sample OutputStream</strong></a><br/></td>
<td>Schreibt Medien Beispiele in einen Bytestream.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsampleprotection"><strong>IMF Sample Protection</strong></a><br/></td>
<td>Ermöglicht die Verschlüsselung von Mediendaten im geschützten Medien Pfad (PMP). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsavejob"><strong>Imsasavejob</strong></a><br/></td>
<td>Speichert Mediendaten aus einem Quell Byte Datenstrom in einem von der Anwendung bereitgestellten Bytestream.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler"><strong>IMF Schema Handler</strong></a><br/></td>
<td>Erstellt eine Medienquelle oder einen Bytestream aus einer URL. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsecurechannel"><strong>IMF-Kanal</strong></a><br/></td>
<td>Einrichten eines unidirektionalen sicheren Kanals zwischen zwei-Objekten. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfseekinfo"><strong>IMF seekinfo</strong></a><br/></td>
<td>Für eine bestimmte Suchposition Ruft die zwei nächsten Keyframes ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport"><strong>Imssensoractivitiesreport</strong></a><br/></td>
<td>Bietet Zugriff auf <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>imfsensoractivityreport</strong></a> -Objekte, die die aktuelle Aktivität eines Sensors beschreiben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback"><strong>IMF sensoractivitiesreportcallback</strong></a><br/></td>
<td>Schnittstelle, die vom Client implementiert wird, um Rückrufe zu empfangen, wenn Sensor Aktivitätsberichte verfügbar sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitymonitor"><strong>IMF sensoractivitymonitor</strong></a><br/></td>
<td>Stellt Methoden zum Steuern eines Sensor Aktivitäts Monitors bereit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>Imssensoractivityreport</strong></a><br/></td>
<td>Stellt einen Aktivitäts Bericht für einen Sensor dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice"><strong>IMF-Gerät</strong></a><br/></td>
<td>Stellt ein Sensorgerät dar, das zu einer Sensor Gruppe gehören kann, die durch die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>imfsensorgroup</strong></a> -Schnittstelle dargestellt wird. Der Begriff " &quot; Gerät" &quot; in diesem Kontext kann sich auf ein physisches Gerät, eine benutzerdefinierte Medienquelle oder einen Frame Anbieter beziehen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>Immasensorgroup</strong></a><br/></td>
<td>Stellt eine Gruppe von Sensorgeräten dar, von denen eine <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>imfmediasource</strong></a> erstellt werden kann. Der Begriff " &quot; Gerät" &quot; in diesem Kontext kann sich auf ein physisches Gerät, eine benutzerdefinierte Medienquelle oder einen Frame Anbieter beziehen. Eine Sensor Gruppe kann tatsächlich mehrere Sensorgeräte enthalten, oder Sie kann nur ein einzelnes Gerät enthalten, aber Sie verhält sich immer noch als Sensor Gruppe.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity"><strong>Imssensorprocessactivity</strong></a><br/></td>
<td>Stellt die Aktivität eines einem Sensor zugeordneten Prozesses dar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection"><strong>Imbersensorprofilecollection</strong></a><br/></td>
<td>Enthält eine Auflistung von Media Foundation Sensor profile-Objekten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile"><strong>Immasensorprofile</strong></a><br/></td>
<td>Beschreibt ein Media Foundation-Sensor Profil.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream"><strong>IMF sensorstream</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory"><strong>IMF sensortransformfactory</strong></a><br/></td>
<td>Die von Sensor implementierte Schnittstelle, mit der die Medien Pipeline Anforderungen der Sensor Transformation Abfragen und eine Lauf Zeit Instanz der Sensor Transformation erstellen kann.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource"><strong>IMF sequencersource</strong></a><br/></td>
<td>Wird von der <a href="sequencer-source.md">Sequencer-Quelle</a>implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfsharingengineclassfactory"><strong>IMF sharingengineclassfactory</strong></a><br/></td>
<td>Erstellt eine Instanz der Medien Freigabe-Engine.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown"><strong>Nicht Herunterfahren</strong></a><br/></td>
<td>Wird von einigen Media Foundation Objekten verfügbar gemacht, die explizit heruntergefahren werden müssen. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary"><strong>IMF signedlibrary</strong></a><br/></td>
<td>Stellt eine Methode bereit, die es Inhalts Schutzsystemen ermöglicht, die Prozedur Adresse einer Funktion in der signierten Bibliothek zu erhalten. Diese Methode bietet die gleiche Funktionalität wie <strong>GetProcAddress</strong> , die für Windows Store-Apps nicht verfügbar ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume"><strong>Imbersimpleaudiovolume</strong></a><br/></td>
<td>Steuert die Master Volume-Ebene der Audiositzung, die dem streamingaudiorenderer (SAR) und der audioerfassungs Quelle zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>Imbersink Writer</strong></a><br/></td>
<td>Wird vom Media Foundation Sink Writer-Objekt implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>Imbsinkschreiterrückruf</strong></a><br/></td>
<td>Rückruf Schnittstelle für den Media Foundation Sink-Writer. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback2"><strong>IMFSinkWriterCallback2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMF Sink Write-Rückruf</strong></a> Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterencoderconfig"><strong>Imbsinkschreiterencoderconfig</strong></a><br/></td>
<td>Stellt zusätzliche Funktionen für den senkwriter bereit, um den Medientyp und die Encoderkonfiguration dynamisch zu ändern. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex"><strong>Imbsinkschreiterex</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMF Sink Writer</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMF sourceBuffer</strong></a><br/></td>
<td>Stellt einen Puffer dar, der Mediendaten für eine <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>imfmediasourceextension</strong></a>enthält. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMF sourcebufferlist</strong></a><br/></td>
<td>Stellt eine Auflistung von <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMF sourceBuffer</strong></a> -Objekten dar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify"><strong>IMF sourcebuffernotify</strong></a><br/></td>
<td>Stellt Funktionen zum Aufrufen von Ereignissen bereit, die <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMF sourceBuffer</strong></a>zugeordnet sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor"><strong>IMF sourceopenmonitor</strong></a><br/></td>
<td>Rückruf Schnittstelle zum Empfangen von Benachrichtigungen von einer Netzwerkquelle beim Fortschritt eines asynchronen Öffnungs Vorgangs.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a><br/></td>
<td>Wird vom Media Foundation Quell Lese Objekt implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMF sourcereadercallback</strong></a><br/></td>
<td>Rückruf Schnittstelle für den Media Foundation Quellen Reader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback2"><strong>IMFSourceReaderCallback2</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMF sourcereadercallback</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex"><strong>IMF sourcereaderex</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMF sourcereader</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMF sourceresolver</strong></a><br/></td>
<td>Erstellt eine Medienquelle aus einer URL oder einem Bytestream.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMF spatialaudioobjectbuffer</strong></a><br/></td>
<td>Stellt einen Abschnitt von Audiodaten mit zugeordneten positionellen und renderingmetadaten dar. Räumliche Audioobjekte werden in <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>imbspatialaudiosample</strong></a> -Instanzen gespeichert und ermöglichen das übergeben räumlicher Audioinformationen zwischen Media Foundation-Komponenten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMF spatialaudiosample</strong></a><br/></td>
<td>Stellt ein multimediateibeispiel mit räumlichen Audioinformationen dar. Jedes <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMF spatialaudiosample</strong></a> -Objekt enthält ein oder mehrere <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMF spatialaudioobjectbuffer</strong></a> -Objekte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager"><strong>Imssslcertifieremanager</strong></a><br/></td>
<td>Wird von einem Client implementiert und von Media Foundation aufgerufen, um das vom Server angeforderte Client Secure Sockets Layer (SSL)-Zertifikat zu erhalten. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor"><strong>IMF-Deskriptor</strong></a><br/></td>
<td>Ruft Informationen zu einem Stream in einer Medienquelle ab. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamingsinkconfig"><strong>IMF streamingsink config</strong></a><br/></td>
<td>Übergibt Konfigurationsinformationen an die Medien senken, die zum Streamen der Inhalte verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink"><strong>IMF-Senke</strong></a><br/></td>
<td>Stellt einen Stream für ein Medien Senk Objekt dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsystemid"><strong>IMF System Mid</strong></a><br/></td>
<td>Stellt eine Methode bereit, mit der System-ID-Daten retisiert werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate"><strong>IMF timecodetranslation</strong></a><br/></td>
<td>Konvertiert zwischen den Zeit Codes von Motion Picture und TV Engineers (SMPTE) und 100-Nanosecond-Zeiteinheiten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext"><strong>Unverändertext</strong></a><br/></td>
<td>Ein Zeit gesteuerter Text-Objekt stellt eine Komponente des zeitgesteuerten Texts dar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextbinary"><strong>Imstimedtextbinary</strong></a><br/></td>
<td>Stellt den Dateninhalt eines zeitgesteuerten Text Objekts dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue"><strong>IMF timedtextcue</strong></a><br/></td>
<td>Stellt das zeitgesteuerte Text-Hinweis Objekt dar. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext"><strong>IMF timedtextformattedtext</strong></a><br/></td>
<td>Stellt einen Block mit formatiertem zeitgesteuerten Text dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify"><strong>IMF timedtextnotify</strong></a><br/></td>
<td>Schnittstelle, die Rückrufe für Media Foundation zeitgesteuerte Text Benachrichtigungen definiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion"><strong>IMF timedtextregion</strong></a><br/></td>
<td>Stellt den Anzeigebereich eines zeitgesteuerten Text Objekts dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle"><strong>IMF timedtextstyle</strong></a><br/></td>
<td>Stellt den Stil für einen zeitgesteuerten Text dar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack"><strong>Imstimedtexttrack</strong></a><br/></td>
<td>Stellt einen Titel für einen zeitgesteuerten Text dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist"><strong>IMF timedtexttracklist</strong></a><br/></td>
<td>Stellt eine Liste mit zeitgesteuerten Text Spuren dar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimer"><strong>IMF-Timer</strong></a><br/></td>
<td>Stellt einen Timer bereit, der einen Rückruf zu einem angegebenen Zeitpunkt aufruft.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopoloader"><strong>Imftopoloader</strong></a><br/></td>
<td>Konvertiert eine partielle Topologie in eine vollständige Topologie.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology"><strong>Imftopology</strong></a><br/></td>
<td>Stellt eine Topologie dar. Eine <em>Topologie</em> beschreibt eine Sammlung von Medienquellen, senken und Transformationen, die in einer bestimmten Reihenfolge verbunden sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode"><strong>Imftopologynode</strong></a><br/></td>
<td>Stellt einen Knoten in einer Topologie dar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor"><strong>Imftopologynoentattributeeditor</strong></a><br/></td>
<td>Aktualisiert die Attribute von einem oder mehreren Knoten in der aktuellen Topologie der Medien Sitzung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup"><strong>IMFTopologyServiceLookup</strong></a><br/></td>
<td>Ermöglicht einem benutzerdefinierten Video-Mixer oder Video Presenter das erhalten von Schnittstellen Zeigern aus dem <a href="enhanced-video-renderer.md">erweiterten Videorenderer</a> (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient"><strong>Imftopologyservicelookupclient</strong></a><br/></td>
<td>Initialisiert einen Video-Mixer oder einen Presenter.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample"><strong>IMF trackedsample</strong></a><br/></td>
<td>Verfolgt die Verweis Zähler für ein Video Medien Beispiel.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile"><strong>IMF transcodeprofile</strong></a><br/></td>
<td>Wird vom transcodieren-Profil Objekt implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider"><strong>Imotranscodesinkinooprovider</strong></a><br/></td>
<td>Wird vom transcodieren Sink-Aktivierungs Objekt implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMF-Transformation</strong></a><br/></td>
<td>Wird von allen <a href="media-foundation-transforms.md">Media Foundation Transformationen</a> (MFTs) implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput"><strong>Imbtreudinput</strong></a><br/></td>
<td>Wird von Komponenten implementiert, die Input Trust Autoritäten (ITAs) bereitstellen. Diese Schnittstelle wird verwendet, um die ITA für jeden der Datenströme der Komponente zu erhalten. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput"><strong>IMF-Treuhänder Ausgabe</strong></a><br/></td>
<td>Wird von Komponenten implementiert, die Output Trust Autoritäten (OTAS) bereitstellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodeviceid"><strong>IMF videoabviceid</strong></a><br/></td>
<td>Gibt den von einer videorendererkomponente unterstützten Geräte Bezeichner zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol"><strong>IMF videodisplaycontrol</strong></a><br/></td>
<td>Steuert, wie der <a href="enhanced-video-renderer.md">Erweiterte Videorenderer</a> (EVR) Video anzeigt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype"><strong>IMF videomediatype</strong></a><br/></td>
<td>Stellt eine Beschreibung eines Video Formats dar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap"><strong>IMF videomixerbitmap</strong></a><br/></td>
<td>Alpha: kombiniert ein statisches Bitmap-Bild mit dem Video, das vom <a href="enhanced-video-renderer.md">erweiterten Videorenderer</a> (EVR) angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol"><strong>IMF videomixercontrol</strong></a><br/></td>
<td>Steuert, wie der <a href="enhanced-video-renderer.md">Erweiterte Videorenderer</a> (EVR) Video-unter Ströme mischt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2"><strong>IMFVideoMixerControl2</strong></a><br/></td>
<td>Steuert die Einstellungen für Video Deinterlacing.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMF videopositionmapper</strong></a><br/></td>
<td>Ordnet eine Position in einem Eingabe-Videodaten Strom der entsprechenden Position in einem ausgabevideostream zu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter"><strong>IMF videopresenter</strong></a><br/></td>
<td>Stellt einen Video Presenter dar. Ein <em>Video Presenter</em> ist ein Objekt, das Video Frames empfängt (in der Regel von einem Video-Mixer) und Sie in irgendeiner Form präsentiert, in der Regel durch Rendering in der Anzeige.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor"><strong>IMF videoprocessor</strong></a><br/></td>
<td>Steuert die Videoverarbeitung im <a href="enhanced-video-renderer.md">erweiterten Videorenderer</a> (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol"><strong>IMF videoprocess Control</strong></a><br/></td>
<td>Konfiguriert die <a href="video-processor-mft.md"><strong>MFT des Video Prozessors</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol2"><strong>IMFVideoProcessorControl2</strong></a><br/></td>
<td>Konfiguriert die <a href="video-processor-mft.md"><strong>MFT des Video Prozessors</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>Imsvideorenderer</strong></a><br/></td>
<td>Legt einen neuen Mixer oder Presenter für den <a href="enhanced-video-renderer.md">erweiterten Videorenderer</a> (EVR) fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator"><strong>IMF videosamplezuordcator</strong></a><br/></td>
<td>Weist Videobeispiele für eine Video Medien-Senke zu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMF videosamplezuordnungs-Rückruf</strong></a><br/></td>
<td>Ermöglicht es einer Anwendung, Videobeispiele zu verfolgen, die vom erweiterten Videorenderer (EVR) zugeordnet wurden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex"><strong>IMF videosamplezuweisungen</strong></a><br/></td>
<td>Weist Videobeispiele zu, die Direct3D 11-Textur Oberflächen enthalten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify"><strong>IMF videosamplezupornotify</strong></a><br/></td>
<td>Der Rückruf für die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMF videosamplezustellercallback</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotifyex"><strong>IMF videosamplezustansorornotifyex</strong></a><br/></td>
<td>Der Rückruf für die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMF videosamplezustellercallback</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMF workqueueservices</strong></a><br/></td>
<td>Steuert die von der <a href="media-session.md">Medien Sitzung</a>erstellten Arbeits Warteschlangen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex"><strong>IMF workqueueservicesex</strong></a><br/></td>
<td>Erweitert die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMF workqueueservices</strong></a> -Schnittstelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrol"><strong>Iplayto Control</strong></a><br/></td>
<td>Aktiviert das <strong>playdeconnection</strong> -Objekt, um eine Verbindung mit einem Medien Element herzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrolwithcapabilities"><strong>Iplaydecontrolwith-Funktionen</strong></a><br/></td>
<td>Stellt Funktionen für <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>iplayysource</strong></a> bereit, um die Funktionen des Inhalts zu ermitteln.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>Iplaytosourceclassfactory</strong></a><br/></td>
<td>Erstellt eine Instanz des <a href="/uwp/api/Windows.Media.PlayTo.PlayToSource"><strong>playysource</strong></a> -Objekts.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket"><strong>Iwmcodecleakybucket</strong></a><br/></td>
<td>Konfiguriert die &quot; Parameter für den Leaky-Bucket &quot; in einem Video Encoder.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecoutputtimestamp"><strong>Iwmcodecoutputtimestamp</strong></a><br/></td>
<td>Ruft den Zeitstempel des nächsten Video Rahmens ab, der decodiert werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata"><strong>Iwmcodecprivatedata</strong></a><br/></td>
<td>Ruft die privaten Codec-Daten ab, die an den Ausgabe Medientyp angehängt werden müssen. Diese Codec-Daten sind erforderlich, um Windows Media Video Inhalt ordnungsgemäß zu decodieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprops"><strong>Iwmcodec-Eigenschaften</strong></a><br/></td>
<td>Stellt Methoden bereit, die Format spezifische Codec-Eigenschaften abrufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecstrings"><strong>Iwmcodecstrings</strong></a><br/></td>
<td>Ruft Namen und beschreibende Zeichen folgen für Codecs und Formate ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops"><strong>Iwmcolor-Eigenschaften</strong></a><br/></td>
<td>Legt Eigenschaften für den Farb Konverter DSP fest. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops"><strong>Iwmresamplerproperties</strong></a><br/></td>
<td>Legt Eigenschaften für den audioresampler-DSP fest. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops"><strong>Iwmresizer-Eigenschaften</strong></a><br/></td>
<td>Legt Eigenschaften für den Video Resizer DSP fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmsampleextensionsupport"><strong>Iwmsampleextensionsupport</strong></a><br/></td>
<td>Konfiguriert die Codec-Unterstützung für Beispiel Erweiterungen. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup"><strong>Iwmvideodecoderhurryup</strong></a><br/></td>
<td>Steuert die Geschwindigkeit des Video-Decoders.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderreconbuffer"><strong>Iwmvideodecoderreconbuffer</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Schnittstelle ist veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> Verwaltet rekonstruierte Video Frames.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideoforcekeyframe"><strong>Iwmvideoforcekeyframe</strong></a><br/></td>
<td>Erzwingt das Codieren des aktuellen Frames als Keyframe durch den Encoder. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierreferenz](media-foundation-programming-reference.md)
</dt> </dl>

 

 
