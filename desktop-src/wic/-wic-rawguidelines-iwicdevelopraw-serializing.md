---
description: Implementierungsrichtlinien für die Serialisierung von IWICDevelopRaw Einstellungen
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Implementierungsrichtlinien für die Serialisierung von IWICDevelopRaw Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119b6377fc8b75aa9763e8141e17ef79832a2aef5f010c2783a412cef0133788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709830"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Implementierungsrichtlinien für die Serialisierung von IWICDevelopRaw Einstellungen

Die [**IWICDevelopRaw-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) macht Einstellungen verfügbar, die die Anwendung verwenden kann, um die Verarbeitung des RAW-Images zu ändern. Die Einstellungen sollten serialisiert werden können, damit sie sitzungsübergreifend beibehalten werden. Obwohl dies auf verschiedene Weise erfolgen kann, wird empfohlen, diese Daten auf eine Weise zu codieren, die mit anderen Metadaten konsistent ist.

Es folgen einige allgemeine Implementierungsrichtlinien:

-   Alle Einstellungen, die über [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (z. B. Drehung oder Weißabgleich) vorgenommen werden, sollten das Überschreiben der Kameraeinstellung oder "as-shot"-Daten vermeiden, es sei denn, das Tag wird häufig als "aktuelle Einstellung" verwendet. Beispielsweise können EXIF-Ausrichtungstags verwendet werden, um die Rotation dauerhaft zu speichern.
-   Es empfiehlt sich, nicht jedes Mal die gesamte Datei (einschließlich der Pixeldaten) speichern zu müssen, wenn die [**IWICDevelopRaw-Einstellungen**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) zur Serialisierung aufgefordert werden.
-   Der Prozess der Serialisierung von [**IWICDevelopRaw-Einstellungen**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) folgt in der Regel dieser Reihenfolge von Ereignissen. Für die Anwendung gilt Folgendes:

    1.  Instanziiert einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) in einer RAW-Datei.
    2.  Ruft [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) auf, um einen [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) für den RAW-Frame abzurufen.
    3.  Ruft QueryInterface für die IWICBitmapFrameDecode-Schnittstelle für die IWICDevelopRaw-Schnittstelle auf.
    4.  Ruft [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)auf, das eine IPropertyBag2-Schnittstelle mit allen darin gespeicherten aktuellen Eigenschaften zurückgibt.

        An diesem Punkt des Prozesses besteht das Ziel darin, die Einstellungen in der IPropertyBag2-Schnittstelle in die RAW-Datei zu serialisieren. Hierzu müssen Sie einen Encoder einrichten usw. Dies wird in den folgenden Schritten ausführlich beschrieben.

    5.  Erstellt einen [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) für die RAW-Datei.
    6.  Ruft [**IWICBitmapEncoder auf:**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)[**Initialisieren Sie**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), und übergeben Sie einen neuen (leeren) Datenstrom zum Codieren.
    7.  Ruft [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)auf:[**CreateNewFrame,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) um einen neuen IWICBitmapFrameEncode für den RAW-Frame zu erstellen.
    8.  Ruft [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Initialisieren**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)von auf und übergibt die IPropertyBag2-Schnittstelle aus Schritt 4.
    9.  Ruft [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)auf:[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) mit [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) aus dem RAW-Bildrahmen des Decoders.
    10. Ruft [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)auf:[**Commit .**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) Der Codec serialisiert dann die Eigenschaften in IPropertyBag2 aus Schritt 8 in die Datei. Die gängigste Methode zum Serialisieren der Eigenschaften wird angenommen, indem sie als Metadaten in die Datei geschrieben werden.
    11. Ruft [**IWICBitmapEncoder auf:**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Ruft IStream::Commit für den Stream in Schritt 6 auf.

    Die Einstellungen werden in der Datei serialisiert.

    Diese Methode verursacht die Kosten für das erneute Schreiben der gesamten RAW-Datei jedes Mal, wenn die Einstellungen serialisiert werden. Dies kann vermieden werden, wenn Sie [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) implementieren oder wenn Ihr Bilddateiformat XMP oder EXIF unterstützt, da WIC [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) für beide Formate bereitstellt. Wenn Ihr Codec Änderungen am Ende der Bilddatei schreibt, werden Sie am Ende nicht die gesamte Bilddatei neu schreiben.

-   Parametersätze werden aus dem serialisierten Zustand geladen, wenn die Anwendung die [**WICRawParameterSet.WICUserAdjustedParameterSet-Enumeration**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) für die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**LoadParameterSet-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) festlegt. Das [**Flag WICRawParameterSet.WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) bezieht sich auf den zuletzt gespeicherten Parametersatz, sodass eine Last mit diesem Flag dazu führen sollte, dass Parameter im zuletzt gespeicherten Zustand wiederhergestellt werden.
-   Beim ersten Laden sollte der zuletzt gespeicherte Parametersatz geladen werden( falls verfügbar). Falls nicht, sollten die "as-shot"-Einstellungen als Voreinstellungen für die [**IWICDevelopRaw-Schnittstellenvariablen**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) verwendet werden. Diese as-shot-Einstellungen können auch mithilfe des [**WICRawParameterSet.WICAsShotParameterSet-Flags**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) geladen werden.
-   Der [**Bezeichner WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) soll eine "Auto"-Einstellung darstellen. Der Codec-Designer kann einen der folgenden Ansätze zum Festlegen von [**IWICDevelopRaw-Parametern**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) auswählen, wenn diese Einstellung vorgenommen wird:

    -   Führen Sie eine algorithmische Optimierung einiger Parameter aus, z. B. Belichtung oder Farbe. Auf diese Weise funktioniert Auto in typischen Bild-Editoren und basiert in erster Linie auf der Pixeldatenanalyse.
    -   Legen Sie Kameraeinstellungen ähnlich dem Verhalten einer Auto-Einstellung fest. Dies ist nützlich, wenn das Bild mit einer Manuell-Einstellung erstellt wurde und es dem Benutzer ermöglicht, manuelle Einstellungen außer Kraft zu setzen.
    -   Sie unternehmen nichts. Nicht alle Steuerelemente müssen festgelegt werden, wenn Auto ausgewählt ist, und es ist in Ordnung, die Einstellungen unverändert zu lassen.

Die Windows Vista Fotogalerie und Windows Live Fotogalerie Bearbeitungstools und andere Bearbeitungsanwendungen verwenden die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Auto-Parameterauslastung, wenn der Benutzer automatisch korrigieren für alle normalen Anpassungen der Codecsteuerung wie Farbe und Belichtung auswählt, um die besten Ergebnisse zu erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC Guidelines for Camera RAW Image Formats](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



