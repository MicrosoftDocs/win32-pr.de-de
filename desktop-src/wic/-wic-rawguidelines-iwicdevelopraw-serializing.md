---
description: Implementierungs Richtlinien für das Serialisieren von IWICDevelopRaw-Einstellungen
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Implementierungs Richtlinien für das Serialisieren von IWICDevelopRaw-Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48cdc78f68e6d63ee7870b9296ae4cfa4f85547a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758293"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Implementierungs Richtlinien für das Serialisieren von IWICDevelopRaw-Einstellungen

Die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle macht Einstellungen verfügbar, die von der Anwendung zum Ändern der Verarbeitung des RAW-Images verwendet werden können. Die Einstellungen sollten serialisiert werden können, damit Sie Sitzungs übergreifend beibehalten werden. Dies kann auf verschiedene Weise erfolgen, es wird jedoch empfohlen, diese Daten in einer Weise zu codieren, die mit anderen Metadaten konsistent ist.

Im folgenden sind einige allgemeine Implementierungs Richtlinien aufgeführt:

-   Alle Einstellungen, die über [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (z. b. Drehung oder weiß ausgeglichen) vorgenommen werden, sollten das Überschreiben von Kameraeinstellungen oder "als-shot"-Daten vermeiden, es sei denn, das Tag wird häufig als "aktuelle Einstellung" verwendet. Beispielsweise können mit EXIF-Ausrichtungs Tags die Drehung persistent gespeichert werden.
-   Es ist vorzuziehen, die gesamte Datei (einschließlich der Mosaik Pixeldaten) jedes Mal zu speichern, wenn die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Einstellungen zur Serialisierung aufgefordert werden.
-   Der Prozess der Serialisierung von [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Einstellungen befolgt in der Regel diese Reihenfolge von Ereignissen. Für die Anwendung gilt Folgendes:

    1.  Instanziiert einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) für eine Rohdatendatei.
    2.  Ruft [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) auf, um einen [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) für den rohframe zu erhalten.
    3.  Ruft QueryInterface für die IWICBitmapFrameDecode-Schnittstelle für die IWICDevelopRaw-Schnittstelle auf.
    4.  Ruft [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)auf, das eine IPropertyBag2-Schnittstelle mit allen in ihr gespeicherten aktuellen Eigenschaften zurückgibt.

        An dieser Stelle des Prozesses besteht das Ziel darin, die Einstellungen in der IPropertyBag2-Schnittstelle in die Rohdatendatei zu serialisieren. Hierfür müssen Sie einen Encoder einrichten usw., der in den folgenden Schritten beschrieben wird.

    5.  Erstellt ein [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) für die Rohdatendatei.
    6.  Ruft [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)auf und übergibt einen neuen (leeren) Stream, der codiert werden soll.
    7.  Ruft [**iwicbitmakcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**anmentewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) auf, um für den unformatierten Frame einen neuen IWICBitmapFrameEncode zu erstellen.
    8.  Ruft [**iwicbitmapframekocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)auf und übergibt in der IPropertyBag2-Schnittstelle aus Schritt 4.
    9.  Ruft [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Write-ource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) mit [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) aus dem Rohbild Rahmen des Decoders auf.
    10. Ruft [**iwicbitmapframekocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)auf. Der Codec serialisiert dann die Eigenschaften im IPropertyBag2 aus Schritt 8 in die Datei. Bei der gängigsten Methode zum Serialisieren der Eigenschaften wird davon ausgegangen, dass Sie in der Datei als Metadaten geschrieben werden.
    11. Ruft [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)auf.
    12. Ruft IStream:: Commit für den Stream in Schritt 6 auf.

    Die Einstellungen werden in der Datei serialisiert.

    Bei dieser Methode entstehen die Kosten für das erneute Schreiben der gesamten Rohdatendatei, wenn die Einstellungen serialisiert werden. Dies kann vermieden werden, wenn Sie [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) implementieren oder wenn das Image Dateiformat XMP oder EXIF unterstützt, da WIC [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) für beide Formate bereitstellt. Wenn Ihr Codec Änderungen am Ende der Bilddatei schreibt, werden Sie nicht mehr die gesamte Bilddatei neu schreiben.

-   Parameter Sätze werden aus dem serialisierten Zustand geladen, wenn die Anwendung die [**wicrawparameterset. wicuseradjustedparameterset**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) -Enumeration für die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) -Methode festlegt. Das Flag " [**wicrawparameterset. wicuseradjustedparameterset**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) " verweist auf den zuletzt gespeicherten Parametersatz. Daher sollte eine Auslastung mit diesem Flag dazu führen, dass Parameter im zuletzt gespeicherten Zustand wieder hergestellt werden.
-   Beim ersten Laden sollte der zuletzt gespeicherte Parametersatz geladen werden, falls verfügbar. Andernfalls sollten die "als-shot"-Einstellungen als Voreinstellungen für die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstellen Variablen verwendet werden. Diese as-shot-Einstellungen können auch mithilfe des [**wicrawparameterset. wicasshotparameterset**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) -Flags geladen werden.
-   Der Bezeichner [**wicrawparameterset. wicautoadjustedparameterset**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) soll eine "Auto"-Einstellung darstellen. Der Codec-Designer kann eine der folgenden Vorgehensweisen zum Festlegen von [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Parametern auswählen, wenn diese Einstellung vorgenommen wird:

    -   Führen Sie eine algorithmische Optimierung einiger Parameter aus, z. b. "verfügbar" oder "Farbe". Dies ist die Art und Weise, wie Auto in typischen Bild-Editoren funktioniert und hauptsächlich auf Pixeldaten Analysen basiert.
    -   Legen Sie Kameraeinstellungen ähnlich wie bei einer automatischen Einstellung fest. Dies ist hilfreich, wenn das Bild auf eine manuelle Einstellung festgelegt wurde und es dem Benutzer ermöglicht, manuelle Einstellungen zu überschreiben.
    -   Sie unternehmen nichts. Nicht alle Steuerelemente müssen festgelegt werden, wenn Auto ausgewählt ist, und es ist in Ordnung, die Einstellungen unverändert zu lassen.

Die Bearbeitungs Tools für Windows Vista Photo Gallery und Windows Live Photo Gallery und andere Bearbeitungsanwendungen verwenden die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Auto-Parameter Auslastung, wenn der Benutzer für alle normalen Codec-Steuerelement Anpassungen, wie z. b. Farbe und Verfügbarkeit, die automatische Richtigkeit auswählt, um optimale Ergebnisse zu erzielen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



