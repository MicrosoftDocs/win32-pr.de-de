---
title: Konfigurieren von Streams
description: Konfigurieren von Streams
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows Media-Format-SDK, Streams
- Profile, Streams
- Streams, konfigurieren
- Codecs, Konfigurieren von Streams
- Profile, iwmstreamconfig-Schnittstelle
- Streams, iwmstreamconfig-Schnittstelle
- Iwmstreamconfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc159fbd5390eb430e035db676685153d0cf174
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473132"
---
# <a name="configuring-streams"></a>Konfigurieren von Streams

Das einzige, was in einem Profil erforderlich ist, ist mindestens ein Stream. Die anderen Optionen ermöglichen den Zugriff auf Erweiterte Funktionen, aber mit mindestens einem Stream können Sie eine ASF-Datei erstellen. Es ist von grundlegender Bedeutung, dass Sie wissen, wie Datenströme vor dem Erstellen komplexer Profile konfiguriert werden.

Für Profile können Datenströme in zwei Typen unterteilt werden: solche, die mit Windows Media Codecs und beliebigen Streams komprimiert werden, die nicht mit Codecs verarbeitet werden. Audiostreams und Videostreams sind die Typen, die die Windows Media-Codecs verwenden. Natürlich können Streams Audiodaten oder Videos enthalten, die mit einem Drittanbieter-Codec komprimiert sind, aber der Prozess der Konfiguration eines solchen Datenstroms ist ein Sonderfall. Weitere Informationen finden Sie [unter So erstellen Sie ASF-Dateien mithilfe von Drittanbieter-Codecs](to-create-asf-files-using-third-party-codecs.md).

In der folgenden Liste wird der Prozess der Konfiguration eines Datenstroms zusammengefasst.

1.  Abrufen eines Datenstrom-Konfigurations Objekts für den Datenstrom.
    -   Wenn Sie einen Stream mit einem der Windows Media-Codecs erstellen, müssen Sie das Datenstrom-Konfigurationsobjekt als Codec-Format mithilfe der Methoden von [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)abrufen.
    -   Wenn der Stream ein beliebiger Typ ist, erhalten Sie ein leeres Datenstrom-Konfigurationsobjekt mithilfe von [**iwmprofile:: builddatenstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).
2.  Konfigurieren Sie den Stream entsprechend Ihren Anforderungen.
    -   Streams aller Typen sollten ein Name, ein Verbindungs Name und eine streamnummer zugewiesen werden.
    -   Streams mit Windows Media Codecs sollten nur auf vordefinierte Weise aus dem Codec-Format geändert werden. Für Audiostreams sollten nur die Einstellungen der Variablen Bitrate (VBR) für die zweistufige VBR geändert werden. Videostreams müssen mit den gewünschten Frame Eigenschaften konfiguriert werden.
    -   Beliebige Datenströme weisen abweichende Konfigurations Anforderungen nach Typ auf. Alle erfordern eine Bitrate und ein Puffer Fenster.
3.  Fügen Sie den Stream zum Profil hinzu, indem Sie [**iwmprofile:: addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)aufrufen.

Alle Streams werden mithilfe von Datenstrom-Konfigurationsobjekten definiert. Die Hauptschnittstelle für ein Datenstrom-Konfigurationsobjekt ist [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig), das Methoden zum Festlegen der grundlegenden Einstellungen eines Streams bereitstellt, z. b. die Datenstrom Nummer, die Bitrate usw. **Iwmstreamconfig** wird von den neueren Schnittstellen geerbt, [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) und [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3). Wie bei allen nummerierten Schnittstellen Revisionen sollten Sie immer die neueste Version mithilfe der **QueryInterface** -Methode abrufen.

Der Zugriff auf die meisten Einstellungen in einem Stream erfolgt über [**iwmmedia-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)Eigenschaften. Diese Einstellungen werden in einer [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur gekapselt. Für Audiodaten und Videos verweist die **WM- \_ \_ Medientyp** Struktur auf eine andere Struktur mit weiteren Informationen, die für den Medientyp spezifisch sind. Diese sekundäre Struktur ist in der Regel [**WaveFormatEx**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) für Audiodaten und [**wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) für Video. Außerdem verfügen Videostreams über eine tertiäre Struktur, **BITMAPINFOHEADER**, die die Merkmale eines einzelnen Frame eines Videos beschreibt. **BITMAPINFOHEADER** ist eine gemeinsame Struktur und befindet sich im Abschnitt Graphics Device Interface (GDI) des Platform SDK.

In den folgenden Abschnitten wird beschrieben, wie Datenströme konfiguriert werden.



| `Section`                                                                                                          | BESCHREIBUNG                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Allgemeine Konfiguration für alle Streams](configuration-common-to-all-streams.md)                                   | Beschreibt die grundlegende Datenstrom Konfiguration, die für alle Arten von Streams gemeinsam ist.                                                                                        |
| [Informationen zu streamkonfigurations Informationen von Codecs](getting-stream-configuration-information-from-codecs.md) | Beschreibt, wie Sie Datenstrom-Konfigurationsinformationen aus den Codecs erhalten, um die ordnungsgemäße Konfiguration von Streams mithilfe der Windows Media Audio und der Video Codecs sicherzustellen. |
| [Konfigurieren von Audiodatenströmen](configuring-audio-streams.md)                                                       | Beschreibt das Konfigurieren von Audiodatenströmen.                                                                                                                       |
| [Konfigurieren von Videostreams](configuring-video-streams.md)                                                       | Beschreibt, wie Videostreams konfiguriert werden.                                                                                                                       |
| [Konfigurieren von Videostreams zum Suchen der Leistung](configuring-video-streams-for-seeking-performance.md)       | Beschreibt, wie Videostreams konfiguriert werden, für die eine effiziente Suche wichtig ist.                                                                              |
| [Konfigurieren von Bildschirm Aufzeichnungsdaten strömen](configuring-screen-capture-streams.md)                                     | Beschreibt, wie Videostreams für die Bildschirmaufnahme konfiguriert werden.                                                                                                    |
| [Konfigurieren von bildstreams](configuring-image-streams.md)                                                       | Beschreibt das Konfigurieren von bildstreams.                                                                                                                       |
| [Verwenden von unkomprimierten Audiodaten und Videostreams](using-uncompressed-audio-and-video-streams.md)                     | Beschreibt, wie ein unkomprimierter Audiodatenstrom oder Videostream eingerichtet wird.                                                                                                  |
| [Konfigurieren beliebiger Streamtypen](configuring-arbitrary-stream-types.md)                                     | Beschreibt, wie Datenströme so konfiguriert werden, dass die vordefinierten willkürlichen Streamtypen verwendet werden.                                                                                |
| [Konfigurieren von VBR-Streams](configuring-vbr-streams.md)                                                           | Beschreibt, wie Datenströme für die Verwendung der variablenbitrate-Codierung (VBR) konfiguriert werden.                                                                                     |
| [Konfigurieren von Dateneinheitserweiterung en](configuring-data-unit-extensions.md)                                         | Beschreibt, wie ein Stream so konfiguriert wird, dass Dateneinheiten Erweiterungen beim Schreiben der Datei angefügt werden können.                                                      |
| [Wieder verwenden von streamkonfigurationen](reusing-stream-configurations.md)                                               | Beschreibt die Möglichkeiten, wie Sie Datenstrom-Konfigurationsobjekte aus vorhandenen Profilen zum Erstellen neuer Profile verwenden können.                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 