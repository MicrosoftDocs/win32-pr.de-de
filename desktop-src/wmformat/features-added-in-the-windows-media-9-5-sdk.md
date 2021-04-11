---
title: Im Windows Media 9,5 SDK hinzugefügte Features
description: Im Windows Media 9,5 SDK hinzugefügte Features
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media-Format-SDK, Features
- Windows Media-Format-SDK, neue Funktionen
- Windows Media-Format-SDK, Schnittstelle für anwendungsspezifische Verarbeitung
- Windows Media-Format-SDK, DirectX-Video Beschleunigung (DXVA)
- Windows Media-Format-SDK, iwmplayerhook-Schnittstelle
- Iwmplayerhook
- Windows Media-Format-SDK, x64-basierte Versionen von Windows
- Windows Media-Format-SDK, Windows Media Video Bildcodec
- Windows Media-Format-SDK, Audiocodecs
- Windows Media-Format-SDK, DRM 10 für Netzwerkgeräte
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Advanced Profile Codec
- Windows Media-Format-SDK, digitales Microsoft/Philips Digital Interconnect-Format (S/PDIF)
- Windows Media-Format-SDK, Low-Delay-Formate
- Windows Media-Format-SDK, ungefähre Suchmodus
- Windows Media-Format-SDK, Brennen von Wiedergabelisten
- Windows Media-Format-SDK, Unterstützung mehrerer Sprachen
- Windows Media-Format-SDK, Windows Media Device Manager SDK
- Windows Media-Format-SDK, Codec-Schnittstellen
- Codecs, Windows Media Video Abbild
- Digital Rights Management (DRM), Netzwerkgeräte sicheres Übertragungsprotokoll
- DRM (Digital Rights Management), Netzwerkgeräte (Secure Transfer Protocol)
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Codecs, Advanced Profile Codec
- Digitales Interconnect-Format (S/PDIF) für Sony/Philips, übertragen oder übertragen mithilfe von
- S/PDIF (digitales Interconnect-Format von Sony/Philips), übertragen oder übertragen mithilfe von
- ungefähre Suchmodus
- Metadaten, Unterstützung mehrerer Sprachen
- Windows Media Device Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101302"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Im Windows Media 9,5 SDK hinzugefügte Features

Im Windows Media-Format 9,5 SDK wurden neue Funktionen eingeführt, um die Sicherheit und Flexibilität von Inhalten zu verbessern. Die folgenden Änderungen wurden seit der Veröffentlichung der 9-Serie an dem SDK vorgenommen.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Neue Schnittstelle für die anwendungsspezifische Verarbeitung während der DirectX-Video Beschleunigung

Player Anwendungen, die die DirectX-Video Beschleunigung unterstützen, können jetzt die [**iwmplayerhook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) -Schnittstelle implementieren, um die anwendungsspezifische Verarbeitung während der DirectX-VA-Decodierung Der Reader Ruft die [**iwmplayerhook::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) -Rückruf Methode auf, bevor komprimierte Videobeispiele zum Decodieren an den Videoprozessor übergeben werden.

> [!Note]  
> Um die **iwmplayerhook** -Schnittstelle und die zugehörige [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) -Schnittstelle zu verwenden, muss die Update Nummer 888656 im Windows Media-Format-SDK installiert sein. Sie können das Update von der [Microsoft-Website](https://support.microsoft.com/?id=888656)herunterladen.

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Windows Media-Format-SDK-Version für x64-basierte Versionen von Windows

Eine x64-basierte Version des SDK für Windows Media-Format ist verfügbar. Diese Dokumentation gilt sowohl für die 32-Bit-Versionen als auch für die x64-basierte Version des SDK. Allerdings wird Digital Rights Management (DRM) im x64-basierten Windows Media-Format-SDK nicht unterstützt.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>Neue Version des Windows Media Video Abbild Codecs

Mit dem Windows Media Video 9-Abbild v2-Codec werden die Beispiel Geometrie Berechnungen zum Schwenken und Zoomen vereinfacht. Der neue Codec unterstützt auch mehrere komplexe Übergänge zwischen Bildern.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>Neue Version der Windows Media Audio Codecs

Das Windows Media-Format 9,5 SDK umfasst die folgenden aktualisierten Audiocodecs:

-   Windows Media Audio 9,1
-   Windows Media Audio 9,1 Professional
-   Windows Media Audio 9,1 verlustfreie

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Unterstützung für Protokoll Unterstützung für Windows Media DRM 10 für Netzwerkgeräte

Das Windows Media-Format 9,5 SDK unterstützt das sichere Übertragungsprotokoll von Windows Media DRM 10 für Netzwerkgeräte. Dieses Protokoll kann verwendet werden, um verschlüsselte Inhalte über ein lokales Netzwerk an ein Wiedergabe Gerät zu streamen, z. b. einen Video Empfänger, der sich auf der obersten Ebene befindet.

Die meisten der Prozeduren, die zum Implementieren der Unterstützung für Windows Media DRM 10 für Netzwerkgeräte verwendet werden, müssen von der Anwendung ausgeführt werden. Sie können jedoch die Methoden des Windows Media Format SDK verwenden, um die folgenden Funktionen bereitzustellen:

-   Warten Sie eine Datenbank von Geräten, einschließlich derjenigen, die für Windows Media DRM 10 für Netzwerkgeräte aktiviert sind.
-   Überprüfen Sie die Geräte, um sicherzustellen, dass Sie ausreichend für den Client im Netzwerk für sicheres Streaming ausreichend sind.
-   Konvertieren von DRM-geschützten Dateien in Windows Media DRM 10 für Netzwerkgeräte Ströme.
-   Schreiben von Dateien mithilfe zuvor verschlüsselter Daten.

## <a name="support-for-new-drm-licenses"></a>Unterstützung für neue DRM-Lizenzen

Neue Lizenzen, die mithilfe des Windows Media Rights Manager SDK erstellt wurden, verwenden Ausgabe Schutz Ebenen (opls), um Rechte und Einschränkungen für das Abspielen und Kopieren von Inhalten anzugeben. Das SDK für den Windows Media-Format unterstützt das Lesen der opls aus einer Lizenz.

## <a name="new-video-codec"></a>Neuer Videocodec

Die Windows Media Video 9 Advanced Profile Codec basiert auf der hohen Qualität des Windows Media Video 9-Codecs und fügt gleichzeitig Unterstützung für die Zeilen Sprung Codierung hinzu.

## <a name="spdif-output"></a>S/PDIF-Ausgabe

Inhalte, die mit einem der Windows Media Audio Professional-Codecs codiert sind, können jetzt mithilfe des digitalen Interconnect-Formats (S/PDIF) von Sony/Philips übertragen oder übertragen werden.

## <a name="low-delay-audio"></a>Low-Delay Audiodaten

In den Windows Media Audio 9,1-und Windows Media Audio 9,1 Professional-Codecs werden nun jeweils mehrere Low-Delay-Formate unterstützt. Diese Formate liefern Audiostreams, die schneller gestartet werden können, wodurch die Latenz bei streamumschalungsszenarien reduziert wird. Die Gesamt Latenz bei Live Übertragungen wird auch durch die Verwendung von Low-Delay-Formaten verbessert.

## <a name="approximate-seeking-mode"></a>Ungefähre Suchmodus

Sie können jetzt eine ungefähre Zeit in einer ASF-Datei mit dem Reader suchen. Dieser Modus verbessert die Leistung bei einer unpräzisen Suche, z. b. Wenn ein Benutzer auf die Suchleiste in Windows Media Player klickt. Die ungefähre Suche gibt das Medien Beispiel für den vorherigen Cleanpoint zurück, anstatt das Beispiel für die genaue Zeit wiederherzustellen.

## <a name="playlist-burning"></a>Wiedergabelisten brennen

Windows Media DRM 10 unterstützt die Rechte zum Kopieren von Audiodateien auf Red Book CD als Teil einer Wiedergabeliste. Das Windows Media-Format-SDK stellt Methoden bereit, mit denen überprüft werden kann, ob die Dateien in einer Wiedergabeliste kopiert werden dürfen.

## <a name="improved-multiple-language-support-for-metadata"></a>Verbesserte Multiple-Language-Unterstützung für Metadaten

Im Windows Media Format 9-Reihe-SDK wurden alle zu einer Datei hinzugefügten Metadaten einer Sprachliste zugewiesen, der der sprach Bezeichner der Standardsprache zugewiesen wurde. Dies verursachte Probleme, wenn Inhalts Verteiler in verschiedenen Gebiets Schemas einige Metadaten hinzugefügt haben, da Benutzer im Gebiets Schema des Verteilers nur die wenigen Attribute sehen, die für Ihre Sprache hinzugefügt wurden. Das Windows Media-Format 9,5 SDK löst dieses Problem, indem es keine Sprachliste erstellt, bis in der Dateiattribute aus zwei Sprachen vorhanden sind. An diesem Punkt werden alle Metadaten dem Gebiets Schema der zweiten Sprache zugeordnet, das dann zum Standard wird. Auf diese Weise kann ein Inhalts Verteiler alle ursprünglichen Metadaten für eine Datei, z. b. Titel und Autor, intakt halten und gleichzeitig einige Attribute hinzufügen, die Ihrem Gebiets Schema entsprechen.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>Windows Media Device Manager SDK, das in der Installation enthalten ist

Das Installationspaket für das Windows Media-Format 9,5 SDK installiert das Windows Media Device Manager SDK. Die Dokumentation für das Windows Media Device Manager SDK finden Sie im Ordner "C: \\ wmsdk \\ WMFSDK95 \\ WMDM \\ docs" (Ihr Ordner unterscheidet sich, wenn Sie das Windows Media-Format-SDK nicht im Standardordner installieren).

## <a name="codec-interface-documentation"></a>Dokumentation zu Codec Interface

Diese Dokumentation enthält Informationen zur Verwendung der Windows Media Audio und der Video Codecs außerhalb des Windows Media SDK. Diese Dokumentation wurde ursprünglich als Teil eines Downloads aus dem Microsoft Developer Network veröffentlicht. Die Beispielanwendungen, die die Verwendung der Codec-DMOS direkt veranschaulichen, sind in der Windows Media-Format-SDK-Installation zusammen mit Headern enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media-Format-SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




