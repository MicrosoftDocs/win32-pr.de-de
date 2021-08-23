---
title: Features, die im Windows Media 9.5 SDK hinzugefügt wurden
description: Features, die im Windows Media 9.5 SDK hinzugefügt wurden
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Medienformat-SDK, Features
- Windows Medienformat-SDK, neue Features
- Windows Medienformat-SDK, Schnittstelle für anwendungsspezifische Verarbeitung
- Windows Medienformat-SDK, DirectX-Videobeschleunigung (DXVA)
- Windows Medienformat-SDK, IWMPlayerHook-Schnittstelle
- IWMPlayerHook
- Windows Medienformat-SDK, x64-basierte Versionen von Windows
- Windows Medienformat-SDK,Windows Medienvideobildcodec
- Windows Medienformat-SDK, Audiocodecs
- Windows Medienformat-SDK, DRM 10 für Netzwerkgeräte
- Windows Medienformat-SDK, DRM-Lizenzen
- Windows Medienformat-SDK, Erweiterter Profilcodec
- Windows Medienformat-SDK, Digitales Verbundformat (S/PDIF)
- Windows Medienformat-SDK, Formate mit geringer Verzögerung
- Windows Medienformat-SDK, ungefährer Suchmodus
- Windows Medienformat-SDK, Wiedergabelisten-Wiedergabeliste
- Windows Medienformat-SDK, Unterstützung mehrerer Sprachen
- Windows Medienformat-SDK,Windows Media Geräte-Manager SDK
- Windows Medienformat-SDK, Codecschnittstellen
- Codecs, Windows Medienvideobild
- Digital Rights Management (DRM), Sicheres Übertragungsprotokoll für Netzwerkgeräte
- DRM (Digital Rights Management), Sicheres Übertragungsprotokoll für Netzwerkgeräte
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Codecs, Erweiterter Profilcodec
- Sende- oder Übertragungsformat (S/PDIF) mithilfe von
- S/PDIF (Sendeformat für digitale Interkonnektivierung)Übertragen oder Übertragen mithilfe von
- Ungefährer Suchmodus
- Metadaten, Unterstützung mehrerer Sprachen
- Windows Media Geräte-Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcabd2fd3ae1b1030b04c0be342bcb64678e98eef601c83570ad68a13567820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591400"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Features, die im Windows Media 9.5 SDK hinzugefügt wurden

Mit dem Windows Media Format 9.5 SDK wurden neue Features eingeführt, um die Inhaltssicherheit und -flexibilität zu erhöhen. Seit dem Release der 9er-Serie wurden die folgenden Änderungen am SDK vorgenommen.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Neue Schnittstelle für anwendungsspezifische Verarbeitung während der DirectX-Videobeschleunigung

Playeranwendungen, die die DirectX-Videobeschleunigung unterstützen, können jetzt die [**IWMPlayerHook-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) implementieren, um anwendungsspezifische Verarbeitung während der DirectX VA-Decodierung durchzuführen. Der Reader ruft die [**Rückrufmethode IWMPLayerHook::P reDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) auf, bevor komprimierte Videobeispiele zur Decodierung an den Videoprozessor übergeben werden.

> [!Note]  
> Um die **IWMPlayerHook-Schnittstelle** und die zugehörige [**IWMReaderAdvanced5-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) verwenden zu können, muss die Updatenummer 888656 im Windows Media Format SDK installiert sein. Sie können das Update von der [Microsoft-Website](https://support.microsoft.com/?id=888656)herunterladen.

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Windows Media Format SDK-Version für x64-basierte Versionen von Windows

Eine x64-basierte Version des Windows Media Format SDK ist verfügbar. Diese Dokumentation gilt sowohl für die 32-Bit-Versionen als auch für die x64-basierte Version des SDK. Die Verwaltung digitaler Rechte (Digital Rights Management, DRM) wird im x64-basierten Windows Media Format SDK jedoch nicht unterstützt.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>Neue Version des Windows Media Video Image Codec

Der Codec Windows Media Video 9 Image v2 vereinfacht die Geometrieberechnungen für das Schwenken und Zoomen. Der neue Codec unterstützt auch mehrere komplexe Übergänge zwischen Bildern.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>Neue Version der Windows Medienaudiocodecs

Das Windows Media Format 9.5 SDK enthält die folgenden aktualisierten Audiocodecs:

-   Windows Medienaudio 9.1
-   Windows Media Audio 9.1 Professional
-   Windows Medienaudio 9.1 Verlustlos

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Windows Medien-DRM 10 für Netzwerkgeräte – Protokollunterstützung

Das Windows Media Format 9.5 SDK unterstützt das neue Windows Media DRM 10 for Network Devices Secure Transfer Protocol. Dieses Protokoll kann verwendet werden, um verschlüsselte Inhalte über ein lokales Netzwerk an ein Wiedergabegerät zu streamen, z. B. an einen Videoempfänger mit set-top.net.

Die meisten Verfahren, die zum Implementieren der Unterstützung für Windows Media DRM 10 für Netzwerkgeräte verwendet werden, müssen von der Anwendung ausgeführt werden. Sie können jedoch Methoden des Windows Media Format SDK verwenden, um die folgenden Funktionen bereitzustellen:

-   Verwalten Sie eine Datenbank mit Geräten, einschließlich der Geräte, die für Windows Medien-DRM 10 für Netzwerkgeräte aktiviert sind.
-   Überprüfen Sie Geräte, um sicherzustellen, dass sie dem Client im Netzwerk "nahe" genug sind, um sicheres Streaming zu ermöglichen.
-   Konvertieren sie DRM-geschützte Dateien in Windows Medien-DRM 10 für Netzwerkgerätestreams.
-   Schreiben von Dateien mit zuvor verschlüsselten Daten.

## <a name="support-for-new-drm-licenses"></a>Unterstützung für neue DRM-Lizenzen

Neue Lizenzen, die mit dem Windows Media Rights Manager SDK erstellt wurden, verwenden Ausgabeschutzebenen (Output Protection Levels, OPLs), um Rechte und Einschränkungen für das Wiedergeben und Kopieren von Inhalten anzugeben. Das Windows Media Format SDK bietet Unterstützung für das Lesen der OPLs aus einer Lizenz.

## <a name="new-video-codec"></a>Neuer Videocodec

Der Windows Media Video 9 Advanced Profile-Codec baut auf der hohen Qualität des Windows Media Video 9-Codecs auf, während unterstützung für interlaced-Codierung hinzugefügt wird.

## <a name="spdif-output"></a>S/PDIF-Ausgabe

Inhalte, die mit einem der Windows Medienaudio-Professional Codecs codiert sind, können jetzt mithilfe des Digital Interconnect-Formats (S/PDIF) übertragen oder übertragen werden.

## <a name="low-delay-audio"></a>Low-Delay Audio

Die Windows Media Audio 9.1 und Windows Media Audio 9.1 Professional Codecs unterstützen jetzt mehrere Formate mit geringer Verzögerung. Diese Formate erzeugen Audiostreams, die schneller gestartet werden können, wodurch die Latenz in Szenarien mit Streamwechseln reduziert wird. Die Gesamtlatenz bei Liveübertragungen wird auch durch die Verwendung von Formaten mit geringer Verzögerung verbessert.

## <a name="approximate-seeking-mode"></a>Ungefährer Suchmodus

Sie können nun eine ungefähre Zeit in einer ASF-Datei mit dem Reader suchen. Dieser Modus verbessert die Leistung bei einer unpräzise Suche, z. B. wenn ein Benutzer auf die Suchleiste in Windows Media Player klickt. Ungefähre Suche gibt das Medienbeispiel für den vorherigen Cleanpoint zurück, anstatt das Beispiel für die genaue gesuchte Zeit zu rekonstruieren.

## <a name="playlist-burning"></a>Wiedergabelistenwiedergabe

Windows Media DRM 10 unterstützt Rechte zum Kopieren von Audiodateien auf Red Book CD als Teil einer Wiedergabeliste. Das Windows Media Format SDK bietet Methoden zum Überprüfen, ob die Dateien in einer Wiedergabeliste kopiert werden dürfen.

## <a name="improved-multiple-language-support-for-metadata"></a>Verbesserte Multiple-Language-Unterstützung für Metadaten

Im Windows Media Format 9 Series SDK wurden alle einer Datei hinzugefügten Metadaten einer Sprachliste zugewiesen, die den Sprachbezeichner der Standardsprache erhält. Dies führte zu Problemen, wenn Inhaltsverteiler in verschiedenen Gebietsschemas Metadaten hinzugefügt haben, da Benutzern im Gebietsschema des Verteilers nur die wenigen Attribute angezeigt werden, die für ihre Sprache hinzugefügt wurden. Das Windows Media Format 9.5 SDK löst dieses Problem, indem keine Sprachliste erstellt wird, bis Attribute aus zwei Sprachen in der Datei vorhanden sind. An diesem Punkt sind alle Metadaten dem Gebietsschema der zweiten Sprache zugeordnet, das dann zur Standardsprache wird. Auf diese Weise kann ein Inhaltsverteiler alle ursprünglichen Metadaten für eine Datei , z. B. Titel und Autor, intakt lassen und gleichzeitig einige Attribute hinzufügen, die zu ihrem Gebietsschema relevant sind.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>Windows In der Installation enthaltenes Media Geräte-Manager SDK

Das Installationspaket für das Windows Media Format 9.5 SDK installiert das Windows Media Geräte-Manager SDK. Die Dokumentation für das Windows Media Geräte-Manager SDK finden Sie im Ordner C: \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (Ihr Ordner unterscheidet sich, wenn Sie das Windows Media Format SDK nicht im Standardordner installieren).)

## <a name="codec-interface-documentation"></a>Dokumentation zur Codecschnittstelle

Diese Dokumentation enthält Informationen zur Verwendung der Windows Medienaudio- und Videocodecs außerhalb des Windows Media Format SDK. Diese Dokumentation wurde ursprünglich als Teil eines Downloads aus dem Microsoft-Entwickler Network veröffentlicht. Die Beispielanwendungen, die die direkte Verwendung der Codec-DMOs veranschaulichen, sind zusammen mit Headern in der Installation Windows Media Format SDK enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




