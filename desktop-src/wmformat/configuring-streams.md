---
title: Konfigurieren Streams
description: Konfigurieren Streams
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows Medienformat-SDK,Streams
- Profile,Streams
- Streams,Konfigurieren
- Codecs,Konfigurieren von Streams
- profiles,IWMStreamConfig-Schnittstelle
- streams,IWMStreamConfig-Schnittstelle
- IWMStreamConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d55db0d02c8eae3ddd3ec780f5d6470d87628a6f7b12feceb5faa413b2e4546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199316"
---
# <a name="configuring-streams"></a>Konfigurieren Streams

In einem Profil ist nur mindestens ein Stream erforderlich. Die anderen Optionen bieten Zugriff auf erweiterte Features, aber mit mindestens einem Stream können Sie eine ASF-Datei erstellen. Es ist wichtig, dass Sie wissen, wie Datenströme konfiguriert werden, bevor Sie komplexe Profile erstellen.

Für Profile können Streams in zwei Typen unterteilt werden: Datenströme, die mit Windows Media-Codecs komprimiert sind, und beliebige Streams, die nicht mit Codecs verarbeitet werden. Audiostreams und Videostreams sind die Typen, die die Windows Mediencodecs verwenden. Natürlich können Streams Audio- oder Videodaten enthalten, die mit einem Codec eines Drittanbieters komprimiert sind, aber der Prozess der Konfiguration eines solchen Streams ist ein Sonderfall. Weitere Informationen finden Sie unter [So erstellen Sie ASF-Dateien mitHilfe von Drittanbietercodecs.](to-create-asf-files-using-third-party-codecs.md)

Die folgende Liste fasst den Prozess der Konfiguration eines Streams zusammen.

1.  Abrufen eines Streamkonfigurationsobjekts für den Stream.
    -   Wenn Sie einen Stream mit einem der Windows Media-Codecs erstellen, müssen Sie das Streamkonfigurationsobjekt mithilfe der [**Methoden von IWMCodecInfo3 als Codecformat abrufen.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)
    -   Wenn der Stream ein beliebiger Typ ist, erhalten Sie [**mitHILFE von IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)ein leeres Streamkonfigurationsobjekt.
2.  Konfigurieren Sie den Stream entsprechend Ihren Anforderungen.
    -   Streams Allen Typen sollten ein Name, ein Verbindungsname und eine Streamnummer zugewiesen werden.
    -   Streams verwendung Windows Mediencodecs sollten nur auf vordefinierte Weise aus dem Codecformat geändert werden. Bei Audiostreams sollten nur VBR-Einstellungen (Variable Bit Rate) für die VBR mit zwei Durchläufen geändert werden. Videostreams müssen mit den gewünschten Frameeigenschaften konfiguriert werden.
    -   Für beliebige Streams gelten je nach Typ unterschiedliche Konfigurationsanforderungen. Alle erfordern eine Bitrate und ein Pufferfenster.
3.  Fügen Sie den Stream dem Profil hinzu, indem [**Sie IWMProfile::AddStream aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)

Alle Streams werden mithilfe von Streamkonfigurationsobjekten definiert. Die Hauptschnittstelle für ein Streamkonfigurationsobjekt ist [**IWMStreamConfig,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)die Methoden zum Festlegen der grundlegenden Einstellungen eines Streams wie Streamnummer, Bitrate und so weiter bietet. **IWMStreamConfig** wird von den neueren [**Schnittstellen, IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) und [**IWMStreamConfig3, geerbt.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3) Wie bei allen nummerierten Schnittstellenrevisionen sollten Sie immer die neueste Version mithilfe der **QueryInterface-Methode** abrufen.

Auf die meisten Einstellungen in einem Stream wird über [**IWMMediaProps zugegriffen.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) Diese Einstellungen sind in einer [**WM \_ MEDIA \_ TYPE-Struktur gekapselt.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Für Audio und Video verweist die **WM \_ MEDIA \_ TYPE-Struktur** auf eine andere Struktur mit weiteren Spezifischen Informationen zum Medientyp. Diese sekundäre Struktur ist in der Regel [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) für Audio und [**WMVIDEOINFOHEADER für**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) Video. Darüber hinaus verfügen Videostreams über eine tertiäre Struktur, **BITMAPINFOHEADER,** die die Merkmale eines einzelnen Videoframes beschreibt. **BITMAPINFOHEADER** ist eine allgemeine Struktur und befindet sich im Abschnitt Graphics Device Interface (GDI) des Platform SDK.

In den folgenden Abschnitten wird beschrieben, wie Streams konfiguriert werden.



| `Section`                                                                                                          | BESCHREIBUNG                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuration Common to All Streams](configuration-common-to-all-streams.md)                                   | Beschreibt die grundlegende Streamkonfiguration, die allen Arten von Streams gemeinsam ist.                                                                                        |
| [Abrufen von Streamkonfigurationsinformationen aus Codecs](getting-stream-configuration-information-from-codecs.md) | Beschreibt, wie Sie Streamkonfigurationsinformationen von den Codecs erhalten, um die ordnungsgemäße Konfiguration von Streams mithilfe der Windows Medienaudio- und Videocodecs sicherzustellen. |
| [Konfigurieren von Audiodaten Streams](configuring-audio-streams.md)                                                       | Beschreibt, wie Audiostreams konfiguriert werden.                                                                                                                       |
| [Konfigurieren von Streams](configuring-video-streams.md)                                                       | Beschreibt, wie Videostreams konfiguriert werden.                                                                                                                       |
| [Konfigurieren von Video Streams for Seeking Performance](configuring-video-streams-for-seeking-performance.md)       | Beschreibt, wie Videostreams konfiguriert werden, für die eine effiziente Suche wichtig ist.                                                                              |
| [Konfigurieren von Bildschirmaufnahme-Streams](configuring-screen-capture-streams.md)                                     | Beschreibt, wie Videostreams für die Bildschirmaufnahme konfiguriert werden.                                                                                                    |
| [Konfigurieren von Streams](configuring-image-streams.md)                                                       | Beschreibt, wie Imagestreams konfiguriert werden.                                                                                                                       |
| [Verwenden von unkomprimierten Audio- und Videodateien Streams](using-uncompressed-audio-and-video-streams.md)                     | Beschreibt das Einrichten eines unkomprimierten Audio- oder Videostreams.                                                                                                  |
| [Konfigurieren beliebiger Streamtypen](configuring-arbitrary-stream-types.md)                                     | Beschreibt, wie Streams für die Verwendung der vordefinierten beliebigen Streamtypen konfiguriert werden.                                                                                |
| [Konfigurieren von VBR-Streams](configuring-vbr-streams.md)                                                           | Beschreibt, wie Datenströme für die Verwendung der Codierung mit variabler Bitrate (VBR) konfiguriert werden.                                                                                     |
| [Konfigurieren von Dateneinheitserweiterung en](configuring-data-unit-extensions.md)                                         | Beschreibt, wie ein Stream so konfiguriert wird, dass Dateneinheitserweiterungen angefügt werden können, wenn die Datei geschrieben wird.                                                      |
| [Wiederverwendung von Streamkonfigurationen](reusing-stream-configurations.md)                                               | Beschreibt die Möglichkeiten, wie Sie Streamkonfigurationsobjekte aus vorhandenen Profilen verwenden können, um neue Profile zu erstellen.                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 