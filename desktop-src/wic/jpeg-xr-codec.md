---
description: Der native JPEG XR-Codec ist über den Windows-Bilderstellungskomponente (WIC) verfügbar. Das JPEG-XR-Format, das vom Codec unterstützt wird, ist für digitale Consumer und professionelle digitale Komprimierung konzipiert.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: ÜBERSICHT ÜBER DEN JPEG XR-Codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d39608535f9be09821d8db3615641a84fd95a6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444462"
---
# <a name="jpeg-xr-codec-overview"></a>ÜBERSICHT ÜBER DEN JPEG XR-Codec

Der native JPEG XR-Codec ist über den Windows-Bilderstellungskomponente (WIC) verfügbar. Das JPEG-XR-Format, das vom Codec unterstützt wird, ist für digitale Consumer und professionelle digitale Komprimierung konzipiert.

Das JPEG-XR-Format kann bis zu doppelt so viele Komprimierungseffizienzen wie das ursprüngliche JPEG-Format erreichen, mit weniger spürbaren Komprimierungsartefakten. Zu den Features von JPEG XR gehören:

-   Unterstützung für monofarbige, RGB-, CGAM- und n-kanalbasierte Bilder
-   8-, 16- und 32-Bit-Ganzzahlformate
-   Hoher dynamischer Bereich, Breitformatformat mit Festkomma- oder Gleitkommafarbwerten
-   Progressive Decodierung
-   Verlustfreie oder verlustfreie Codierung mit demselben Komprimierungsalgorithmus
-   Unterstützung für die Decodierung von für große Bilder von Interesseden Regionen

Das JPEG-XR-Format wird in den folgenden Standarddokumenten definiert:

-   ITU-T T.832: *Informationstechnologie – JPEG XR-Bildcodierungssystem – Spezifikation der Bildcodierung*
-   ISO/IEC 29199-2:2010: *Informationstechnologie – JPEG XR-Bildcodierungssystem – Teil 2: Spezifikation* der Bildcodierung

Der JPEG-XR-Standard basiert größtenteils auf dem [HD-Fotoformat,](hdphoto-format-overview.md) es gibt jedoch einige Unterschiede zwischen den beiden Formaten. In Windows 8 wurde der HD-Fotocodec aktualisiert, um JPEG XR zu unterstützen. Der Encoder gibt jetzt immer einen JPEG XR-kompatiblen Bitstream aus. Der Decoder kann sowohl JPEG-XR- als auch HD-Fotobilder decodieren.

Im Zusammenhang mit dem HD-Fotocodec wurden erhebliche Leistungsverbesserungen am JPEG-XR-Codec vorgenommen. Beispielsweise wurde die Bilddecodierung mit unterer Auflösung, z. B. die Miniaturansichtsgenerierung, sowie die Bilddecodierung mit niedriger Auflösung verbessert. Es wird empfohlen, anstelle des HD-Fotoformats das JPEG-XR-Format zu verwenden.

## <a name="codec-information"></a>Codec-Informationen



|      Komponente      |    BESCHREIBUNG                                                          |
|---------------------|-------------------------------------------------------------------------|
| Dateinamenerweiterung | "jxr" und "wdp"                                                         |
| Container-GUID      | **GUID \_ ContainerFormatWmp**                                            |
| Decoder-GUID        | **CLSID \_ WICWmpDecoder**                                                |
| Encoder-GUID        | **CLSID \_ WICWmpEncoder**                                                |
| Profilunterstützung     | Encoder und Decoder unterstützen bis zu Hauptprofil und bis Ebene 128. |



 

## <a name="codec-features"></a>Codecfunktionen

### <a name="high-dynamic-range"></a>High Dynamic Range

JPEG XR unterstützt Bilder mit hohem dynamischem Bereich, die Gleitkomma- oder Festkommafarben verwenden. In diesen Farbformaten ist der numerische Bereich eines Pixels größer als der sichtbare Bereich, sodass Sie Farben über oder unterhalb des sichtbaren Bereichs während zwischengeschalteter Verarbeitungsphasen anpassen können.

-   Fester Punkt: In einer Festpunktdarstellung steht 0 für Schwarz und 1,0 für die maximale Sättigung. Der JPEG XR-Codec unterstützt sowohl 16-Bit- als auch 32-Bit-Festpunktformate. Für 16-Bit, 1,0 = 0x2000h, was 13 Bits für den sichtbaren Bereich \[ 0...1 \] ergibt. Der Gesamtbereich ist –4,0 bis +3,999 und wird linear zugeordnet. Für 32-Bit, 1,0 = 0x01000000h beträgt der sichtbare Bereich 24 Bits und der Gesamtbereich –128 bis +127,999.
-   Gleitkomma: In einer Gleitkommadarstellung steht 0 für Schwarz und 1,0 für die maximale Sättigung. Der JPEG XR-Codec unterstützt sowohl 16-Bit- als auch 32-Bit-Gleitkommaformate.

### <a name="tiles"></a>Kacheln

Ein Frame kann in rechteckige Unterregionen partitioniert werden, die als Kacheln *bezeichnet werden.* Eine Kachel ist ein Bereich eines Bilds, das rechteckige Arrays von Makroblocks enthält. Mit Kacheln können Bereiche des Bilds decodiert werden, ohne das gesamte Bild zu verarbeiten.

Wählen Sie während der Codierung die Anzahl der Kacheln aus, indem Sie die **Eigenschaften HorizontalTileSlices** und **VerticalTileSlices** festlegen. Die minimale Kachelgröße beträgt 16 × 16 Pixel. Der Encoder passt die Anzahl der Kacheln an, um diese Einschränkung zu erhalten. Da jeder Kachel Speicher- und Verarbeitungsaufwand zugeordnet ist, sollten Sie die Anzahl der Kacheln berücksichtigen, die für bestimmte Szenarien erforderlich sind.

### <a name="image-stream-output"></a>Imagestreamausgabe

Der JPEG-XR-Standard definiert zwei Teile einer JPEG-XR-Datei:

-   Der Bildbitstream, der im Textkörper des Standards definiert ist.
-   Der Imagecontainer. Die Datei enthält Exif- und XMP-Metadaten und ist in Anhang A des Standards definiert.

Es ist möglich und wird vom Standard zugelassen, den Imagestream in einen anderen Typ von Dateicontainer einbetten. Der Encoder unterstützt einen Nur-Stream-Modus, der den Unformatiertbild-Bitstream ohne Imagecontainer aus gibt. Eine Anwendung kann den Bitstream in einem anderen Containerformat speichern.

Legen Sie die **StreamOnly-Eigenschaft** fest, um den modus only stream zu aktivieren.

### <a name="image-quality-settings"></a>Einstellungen für die Imagequalität

Mehrere Codeceigenschaften steuern die Qualität des Ausgabebilds vom Encoder.

-   [ImageQuality ist](#imagequality) eine Eigenschaft, die von WIC-Codecs gemeinsam verwendet wird. Sie gibt die Bildqualität als einzelnen Gleitkommawert von 0,0 bis 1,0 an.
-   Die [Eigenschaften Quality](#image-quality-settings), [Overlap](#overlap)und [Subsampling](#subsampling) bieten mehr Kontrolle über die Qualitätseinstellungen.

Um die [Eigenschaften Quality](#image-quality-settings), [Overlap](#overlap)und [Subsampling](#subsampling) zu verwenden, legen Sie die [UseCodecOptions-Eigenschaft](#usecodecoptions) auf **VARIANT TRUE \_ fest.**

Wenn [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ FALSE** festgelegt ist **(standardmäßig VARIANT \_ FALSE),** verwendet der Encoder die [ImageQuality-Eigenschaft.](#imagequality) Der Encoder ordnet den Wert von ImageQuality [quality](#image-quality-settings), [Overlap](#overlap)und [Subsampling](#subsampling) über eine Nachschlagetabelle zu.

Der Encoder unterstützt die **CompressionQuality-Eigenschaft** nicht.

### <a name="compressed-domain-transcode"></a>Transcodierung komprimierter Domänen

Der JPEG XR-Codec kann bestimmte Bildtransformationen durchführen, ohne die komprimierten Daten tatsächlich zu decodieren und neu zu codieren. Vorgänge für komprimierte Domänen sind sehr effizient und vermeiden zusätzliche Qualitätsverluste, die typisch sind, wenn Sie ein verlustverknrücktes Bild decodieren und erneut codieren.

Die folgenden Vorgänge für komprimierte Domänen werden unterstützt:

-   Zuschneiden eines Bildbereichs.
-   Drehen oder kippen Sie das Bild.
-   Verwerfen Sie Häufigkeitsdaten, um eine kleinere Bilddatei zu erstellen.
-   Organisieren Sie das Bild zwischen räumlicher reihenfolge und Häufigkeits reihenfolge neu.

Der JPEG XR-Encoder verwendet nach Möglichkeit eine komprimierte Domänentranscodierung, wenn das Quellbild ein JPEG XR-Bild ist. Wenn der Encoder einen komprimierten Domänenvorgang ausführt, ignoriert er die folgenden Codeceigenschaften: [AlphaQuality,](#alphaquality) [ImageQuality,](#imagequality) [InterleavedAlpha,](#interleavedalpha) [Lossless](#lossless)[Overlap](#overlap)und [Quality](#image-quality-settings). Wenn die [Eigenschaften HorizontalTileSlices](/windows) und [VerticalTileSlices](/windows) vorhanden sind, müssen Sie sie auf 0 (null) festlegen. Sie können die Kachelgröße eines Bilds nicht im Rahmen einer komprimierten Domänentranscodierung ändern.

In der folgenden Liste wird beschrieben, wie die Bildtransformationen durchzuführen sind.

-   Legen Sie zum Zuschneiden des Bilds den gewünschten Bereich im [**WICRect-Parameter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) der **WriteSource-Methode** fest.
-   Legen Sie die [BitmapTransform-Eigenschaft](#bitmaptransform) fest, um das Bild zu drehen oder zu kippen.
-   Legen Sie die [ImageDataDiscard-Eigenschaft](#imagedatadiscard) fest, um Häufigkeitsdaten im Bild zu verwerfen. Legen Sie die AlphaDataDiscard-Eigenschaft fest, um Häufigkeitsdaten im [Alphakanal zu verwerfen.](#alphadatadiscard) Durch das Verwerfen von Häufigkeitsdaten wird die codierte Dateigröße reduziert, und die Auflösung kann reduziert werden.
-   Um die Bildorganisation zwischen Häufigkeit und räumlicher Reihenfolge zu ändern, legen Sie die [FrequencyOrdering-Eigenschaft](/windows) fest.

Legen Sie [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ TRUE** und [CompressedDomainTranscode](#compresseddomaintranscode) auf VARIANT FALSE fest, um die Transcodierung komprimierter Domänen zu deaktivieren und die erneute Codierung des Bilds durch den Encoder zu **\_ erzwingen.**

## <a name="encoder-options"></a>Encoderoptionen

Verwenden Sie zum Festlegen von Codierungseigenschaften die [**IPropertyBag2-Schnittstelle.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) Weitere Informationen finden Sie unter Übersicht über [die Codierung.](-wic-creating-encoder.md)

In der folgenden Liste sind die Encoderoptionen angegeben.

-   [AlphaDataDiscard](#alphadatadiscard)
-   [AlphaQuality](#alphaquality)
-   [BitmapTransform](#bitmaptransform)
-   [CompressedDomainTranscode](#compresseddomaintranscode)
-   [FrequencyOrder](#frequencyorder)
-   [HorizontalTileSlices](#horizontaltileslices)
-   [IgnoreOverlap](#ignoreoverlap)
-   [ImageDataDiscard](#imagedatadiscard)
-   [ImageQuality](#imagequality)
-   [InterleavedAlpha](#interleavedalpha)
-   [Lossless](#lossless)
-   [Überlappen](#overlap)
-   [ProgressiveMode](#progressivemode)
-   [Qualität](#image-quality-settings)
-   [StreamOnly](#streamonly)
-   [Untersampling](#subsampling)
-   [UseCodecOptions](#usecodecoptions)
-   [VerticalTileSlices](#verticaltileslices)

### <a name="alphadatadiscard"></a>AlphaDataDiscard

Legt die Menge der Alphafrequenzdaten fest, die während einer komprimierten Domänentranscodierung verworfen werden sollen.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–4   | Keine    |



 

Diese Eigenschaft gilt nur, wenn die [CompressedDomainTranscode-Eigenschaft](#compresseddomaintranscode) auf **VARIANT \_ TRUE** festgelegt ist und das Bild entweder einen planaren Alphakanal oder einen verschachtelten Alphakanal enthält. Andernfalls wird sie ignoriert.

Für Bilder, die einen planaren Alphakanal enthalten, sind die folgenden Werte gültig.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Es werden keine Bildfrequenzdaten verworfen.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | Die Flexbits werden verworfen. Dadurch wird die Qualität des planaren Alphakanals für das transcodierte Bild willkürlich reduziert. , ohne eine Änderung der effektiven Auflösung. Die genaue Verringerung der Dateigröße und -qualität hängt von zahlreichen Faktoren ab und kann nicht genau angegeben werden.                                                                                                                                                                                           |
| 2     | Das Datenband mit hoher Durchlauffrequenz wird verworfen, einschließlich der Flexbits. Dadurch wird die Auflösung des planaren Alphakanals in beiden Dimensionen um den Faktor 4 reduziert. Die tatsächlichen Abmessungen des transcodierten Bilds bleiben gleich, aber das Bild verliert alle Details in jedem 4x4-Block von Alphakanalpixeln. In der Regel sollten Sie diesen Wert nur festlegen, wenn die [ImageDataDiscard-Eigenschaft](#imagedatadiscard) denselben Wert hat.                            |
| 3     | Sowohl die Datenbänder mit hoher als auch der niedriger Durchlauffrequenz werden verworfen, einschließlich der Flexbits. Dadurch wird die Auflösung des planaren Alphakanals in beiden Dimensionen um den Faktor 16 reduziert. Die tatsächlichen Abmessungen des transcodierten Bilds bleiben gleich, aber das Bild verliert alle Details in jedem 16x16-Makroblock von Alphakanalpixeln. In der Regel sollten Sie diesen Wert nur festlegen, wenn die [ImageDataDiscard-Eigenschaft](#imagedatadiscard) denselben Wert hat. |
| 4     | Der Alphakanal wird vollständig verworfen. Das Pixelformat des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln.                                                                                                                                                                                                                                                                                                                                |



 

Für Bilder, die einen verschachtelten Alphakanal enthalten, ist der folgende Wert gültig.



| Wert | BESCHREIBUNG                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | Der Alphakanal wird vollständig verworfen. Das Pixelformat des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln. |



 

Wenn diese Eigenschaft für verschachtelte Alphas nicht auf 4 festgelegt ist, wird der Alphakanal gemäß dem Wert der [ImageDataDiscard-Eigenschaft](#imagedatadiscard) mit den Bilddaten verarbeitet.

### <a name="alphaquality"></a>AlphaQuality

Legt die Komprimierungsqualität für das planare Alphakanalbild fest.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1–255 | 1       |



 

Diese Eigenschaft gilt, wenn das Bild über einen Alphakanal verfügt und die [InterleavedAlpha-Eigenschaft](#interleavedalpha) **VARIANT \_ FALSE** ist. Der Wert 1 gibt den verlustfreien Modus an. Steigende Werte führen zu höheren Komprimierungsverhältnissen und einer niedrigeren Imagequalität.

### <a name="bitmaptransform"></a>BitmapTransform

Gibt an, ob das Bild beim Decodieren gedreht oder gekippt wird.



| Datentyp | VARTYPE     | Range                                                                     | Standard                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **VT \_ UI1** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>CompressedDomainTranscode

Aktiviert oder deaktiviert die komprimierte Domänentranscodierung.



| Datentyp         | VARTYPE      | Standard           |
|-------------------|--------------|-------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ TRUE** |



 

Legen Sie diese Eigenschaft auf **VARIANT \_ FALSE** fest, um komprimierte Domänenvorgänge zu deaktivieren.

### <a name="frequencyorder"></a>FrequencyOrder

Aktiviert die Codierung in der Häufigkeitsreihenfolge. Geräteimplementierungen von JPEG XR-Encodern können eine Datei in räumlicher Reihenfolge organisieren, um den während der Codierung erforderlichen Arbeitsspeicher zu reduzieren.



| Datentyp         | VARTYPE      | Standard           |
|-------------------|--------------|-------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ TRUE** |



 

-   **VARIANT \_ TRUE:** Häufigkeitsreihenfolge. Die Daten mit der niedrigsten Häufigkeit werden zuerst in der Datei angezeigt, und der Bildinhalt wird nach der Häufigkeit und nicht nach der räumlichen Ausrichtung gruppiert. Das Organisieren einer Datei nach Häufigkeits reihenfolge bietet die beste Leistung für jede häufigkeitsbasierte Decodierung.
-   **VARIANT \_ FALSE:** Räumliche Reihenfolge. Die räumliche Reihenfolge reduziert den während der Codierung erforderlichen Arbeitsspeicher.

Die Häufigkeits reihenfolge wird empfohlen, es sei denn, Sie haben leistungs- oder anwendungsspezifische Gründe für die Verwendung der räumlichen Reihenfolge.

### <a name="horizontaltileslices"></a>HorizontalTileSlices

Legt die Anzahl horizontaler Kacheln fest.



| Datentyp  | VARTYPE     | Range  | Standard                      |
|------------|-------------|--------|------------------------------|
| **Ushort** | **VT \_ UI2** | 0–4095 | (Bildbreite – 1) >> 8 |



 

Der Wert ist die Anzahl horizontaler Unterteilungen. das heißt, die Anzahl der horizontalen Kacheln – 1.

### <a name="ignoreoverlap"></a>IgnoreOverlap

Gibt an, wie der Encoder Kachelgrenzen während einer komprimierten Domänentranscodierung behandelt.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

Diese Eigenschaft wird nur angewendet, wenn die [CompressedDomainTranscode-Eigenschaft](#compresseddomaintranscode) auf **VARIANT \_ TRUE** festgelegt ist und eine Unterbereichstranscodierung mit genau einer oder mehreren Kacheln ausgeführt wird.

Der Standardvorgang für eine Region-Transcodierung besteht im Erweitern des angeforderten Bereich um die umgebenden Pixel, die für die Überlappung der Bereichsränder erforderlich sind. Wenn diese Eigenschaft auf **VARIANT \_ TRUE festgelegt** ist, ignoriert der Codec die umgebenden Pixel, und nur die ausgewählten Kacheln werden extrahiert. Wenn das Quellbild nicht gekachelt ist oder der angeforderte Bereich Teilkacheln enthält, wird dieser Parameter ignoriert.

### <a name="imagedatadiscard"></a>ImageDataDiscard

Legt die Menge der Bildfrequenzdaten fest, die während einer komprimierten Domänentranscodierung verworfen werden.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–3   | 0       |



 

Diese Eigenschaft gilt nur, wenn [die CompressedDomainTranscode-Eigenschaft](#compresseddomaintranscode) auf **VARIANT \_ TRUE** festgelegt ist. Andernfalls wird sie ignoriert.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Es werden keine Bildfrequenzdaten verworfen.                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | Die Flexbits werden verworfen. Dadurch wird die Qualität des transcodierten Bilds willkürlich reduziert, ohne die effektive Auflösung des Bilds zu ändern. Die genaue Verringerung der Dateigröße und -qualität hängt von zahlreichen Faktoren ab und kann nicht genau angegeben werden. Dieser Wert gibt einen Fehler zurück, der für einen überlappten Alphakanal angegeben ist.                                                                                |
| 2     | Das Datenband mit hoher Durchgangshäufigkeit wird verworfen, einschließlich der Flexbits. Dadurch wird die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 4 reduziert. Die tatsächlichen Abmessungen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 4x4-Pixelblock. Daher sollte das transcodierte Bild bei jeder Decodierung entsprechend herabsampelt werden.                             |
| 3     | Sowohl die Datenbänder mit hoher als auch niedriger Durchgangshäufigkeit werden verworfen, einschließlich der Flexbits. Dadurch wird die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 16 reduziert. Die tatsächlichen Abmessungen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 16 x 16-Makroblock von Pixeln. Daher sollte das transcodierte Bild bei jeder Decodierung entsprechend herabsampelt werden. |



 

Wenn das Bild einen überlappten Alphakanal enthält, wird der Wert von [ImageDataDiscard](#imagedatadiscard) auf den Alphakanal angewendet, es sei denn, die [AlphaDataDiscard-Eigenschaft](#alphadatadiscard) ist auf 4 festgelegt. In diesem Fall wird der Alphakanal verworfen.

Bei planaren Alphas werden die verworfenen Häufigkeitsdaten durch die [AlphaDataDiscard-Eigenschaft](#alphadatadiscard) gesteuert.

### <a name="imagequality"></a>ImageQuality

Legt die Imagequalität fest.



| Datentyp | VARTYPE    | Range | Standard |
|-----------|------------|-------|---------|
| **FLOAT** | **VT \_ R4** | 0–1.0 | 0.9     |



 

Ebene 1.0 bietet eine mathematische verlustfreie Komprimierung.

Ebene 0.0 ist die Einstellung mit der niedrigsten Qualität.

### <a name="interleavedalpha"></a>InterleavedAlpha

Gibt an, ob verleerte alpha- oder planare Alphas codiert werden sollen.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

-   **VARIANT \_ TRUE:** Überlappter Alphawert. Alphakanalinformationen werden als zusätzlicher verwebter Kanal ohne Korrelation mit den Bildinhaltskanälen codiert. Dieser Modus ist nützlich, um alpha gleichzeitig mit dem Bild zu decodieren, wenn das Bild gestreamt wird.
-   VARIANT \_ FALSE: Planares Alpha. Ein planarer Alphakanal wird als separates Bild codiert. Die Bilddaten und der Alphakanal werden unabhängig decodiert. Optional können Sie die Qualitätsstufe des Alphakanals festlegen, indem Sie die [AlphaQuality-Eigenschaft](#alphaquality) festlegen.

Überlappte Alphas werden nur für bestimmte RGB-Pixelformate unterstützt. Planares Alpha wird für jedes Bildformat unterstützt, das einen Alphakanal definiert.

### <a name="lossless"></a>Lossless

Aktiviert die Verlustkomprimierung.



| Datentyp         | VARTYPE      | Standard        |
|-------------------|--------------|----------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | VARIANT \_ FALSE |



 

Wenn der Wert **VARIANT \_ TRUE ist,** verwendet der Encoder eine verlustfreie Komprimierung. Wenn diese Eigenschaft **auf VARIANT \_ TRUE festgelegt** ist, überschreibt diese Eigenschaft die [ImageQuality-Eigenschaft.](#imagequality)

### <a name="overlap"></a>Überlappung

Legt die Ebene der Überlappungsfilterung fest. Bei der Überlappungsfilterung werden Transformationskoeffizienten über Block- und Makroblockgrenzen hinweg angewendet. Dadurch können blockierende Artefakte reduziert werden.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–4   | 1       |



 



| Wert | BESCHREIBUNG                                   |
|-------|-----------------------------------------------|
| 0     | Keine Überlappung.                                   |
| 1     | Eine Ebene der Überlappung, soft tiling. (Standardeinstellung) |
| 2     | Zwei Ebenen der Überlappung, soft tiling.           |
| 3     | Eine Ebene der Überlappung, harter Tiling             |
| 4     | Zwei Ebenen von Überlappungen, harte Kacheln.           |



 

Definitionen:

-   Eine Überlappungsebene: Die codierten Werte von 4x4-Blöcken werden basierend auf benachbarten Blöcken geändert.
-   Zwei Überlappungsebenen: Die erste Überlappungsebene wird angewendet. Darüber hinaus werden die codierten Werte von 16 x 16 Makroblocks basierend auf den benachbarten Makroblocks geändert.
-   Weiche Kacheln: Überlappende Filterung wird über Kachelgrenzen hinweg angewendet.
-   Harte Kacheln: Die Filterung von Überlappungen wird nicht über Kachelgrenzen hinweg angewendet. Harte Kacheln können einige visuelle Artefakte entlang der Kachelgrenzen einführen.

Wenn Sie diese Eigenschaft festlegen, legen Sie auch [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ TRUE** fest.

### <a name="progressivemode"></a>ProgressiveMode

Aktiviert oder deaktiviert die progressive Codierung.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 



| Wert              | BESCHREIBUNG                |
|--------------------|----------------------------|
| **VARIANT \_ TRUE**  | Sequenzieller Modus (Standard). |
| **VARIANT \_ FALSE** | Progressiver Modus.          |



 

### <a name="quality"></a>Qualität

Legt die Komprimierungsqualität fest.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1–255 | 1       |



 

Der Wert 1 gibt den verlustfreien Modus an. Steigende Werte führen zu höheren Komprimierungsverhältnissen und einer niedrigeren Imagequalität.

Wenn Sie diese Eigenschaft festlegen, legen Sie auch [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ TRUE** fest.

### <a name="streamonly"></a>StreamOnly

Aktiviert oder deaktiviert den reinen Streammodus.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 



| Wert              | BESCHREIBUNG                                                            |
|--------------------|------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | Der Encoder gibt den unformatierten Bilddatenstrom ohne Metadaten aus.             |
| **VARIANT \_ FALSE** | Der Encoder gibt das Containerformat (Bilddatenstrom plus Metadaten) aus. |



 

### <a name="subsampling"></a>Untersampling

Legt die Subsampling für die -Subsampling fest. Diese Eigenschaft gilt nur für RGB-Bilder.



| Datentyp | VARTYPE     | Range | Standard                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **VT \_ UI1** | 0–3   | 3, wenn [ImageQuality](#imagequality) 0.8 >; andernfalls 1 |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3</td>
<td>4:4:4-Codierung. Behält die vollständige Auflösung bei.</td>
</tr>
<tr class="even">
<td>2</td>
<td>4:2:2-Codierung. Die Auflösung von 1/2 der Leuchtdichte beträgt 1/2.</td>
</tr>
<tr class="odd">
<td>1</td>
<td>4:2:0-Codierung. Die Auflösung von 1/4 der Leuchtdichte beträgt 1/4.</td>
</tr>
<tr class="even">
<td>0</td>
<td>4:0:0-Codierung. Verwirft alle Werte und behält nur die Leuchtdichte bei.
<blockquote>
[!Note]<br />
Dieser Modus wird nicht empfohlen, da der Codec eine leicht geänderte Definition der Leuchtdichte verwendet, um die Leistung zu verbessern. Stattdessen ist es besser, das Bild vor der Codierung in monocolore zu konvertieren.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

4:2:2 und 4:2:0 behalten die Leuchtdichtedetails auf Kosten der Farbdetails bei.

Wenn Sie diese Eigenschaft festlegen, legen Sie auch [UseCodecOptions](#usecodecoptions) auf **VARIANT \_ TRUE** fest.

### <a name="usecodecoptions"></a>UseCodecOptions

Gibt an, ob die Eigenschaften [Quality,](#image-quality-settings) [Overlap](#overlap)und [Subsampling](#subsampling) anstelle der generischen [ImageQuality-Eigenschaft](#imagequality) verwendet werden sollen.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

### <a name="verticaltileslices"></a>VerticalTileSlices

Legt die Anzahl horizontaler Kacheln fest.



| Datentyp  | VARTYPE     | Range  | Standard                       |
|------------|-------------|--------|-------------------------------|
| **Ushort** | **VT \_ UI2** | 0–4095 | (Bildhöhe – 1) >> 8 |



 

Der Wert ist die Anzahl der vertikalen Unterteilungen. Das heißt, die Anzahl der vertikalen Kacheln – 1.

## <a name="supported-color-formats"></a>Unterstützte Farbformate

Weitere Informationen zu diesen Formaten finden Sie unter [Native PixelFormate.](-wic-codec-native-pixel-formats.md)

-   **Ganzzahlige RGB-Formate**
    -   GUID \_ WICPixelFormat24bppRGB
    -   GUID \_ WICPixelFormat24bppBGR
    -   GUID \_ WICPixelFormat32bppBGR
    -   GUID \_ WICPixelFormat48bppRGB
    -   GUID \_ WICPixelFormat32bppBGRA
    -   GUID \_ WICPixelFormat64bppRGBA
    -   GUID \_ WICPixelFormat32bppPBGRA
    -   GUID \_ WICPixelFormat64bppPRGBA
-   **RGB-Formate mit festem Punkt**
    -   GUID \_ WICPixelFormat48bppRGBFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBFixedPoint
    -   GUID \_ WICPixelFormat96bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBAFixedPoint
-   **RGB-Gleitkommaformate**
    -   GUID \_ WICPixelFormat48bppRGBHalf
    -   GUID \_ WICPixelFormat64bppRGBHalf
    -   GUID \_ WICPixelFormat128bppRGBFloat
    -   GUID \_ WICPixelFormat64bppRGBAFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBAHalf
    -   GUID \_ WICPixelFormat128bppRGBAFloat
    -   GUID \_ WICPixelFormat128bppPRGBAFloat
-   **Graustufenformate**
    -   GUID \_ WICPixelFormat8bppGray
    -   GUID \_ WICPixelFormat16bppGray
    -   GUID \_ WICPixelFormat16bppGrayFixedPoint
    -   GUID \_ WICPixelFormat16bppGrayHalf
    -   GUID \_ WICPixelFormat32bppGrayFixedPoint
    -   GUID \_ WICPixelFormat32bppGrayFloat
-   **Gepackte Formate**
    -   GUID \_ WICPixelFormat16bppBGR555
    -   GUID \_ WICPixelFormat16bppBGR565
    -   GUID \_ WICPixelFormat32bppBGR101010
    -   GUID \_ WICPixelFormat32bppRGBE
-   **CMYK-Formate**
    -   GUID \_ WICPixelFormat40bppCMYKAlpha
    -   GUID \_ WICPixelFormat64bppCMYK
    -   GUID \_ WICPixelFormat80bppCMYKAlpha
-   **N-Kanal-Formate**
    -   GUID \_ WICPixelFormat32bpp4Channels
    -   GUID \_ WICPixelFormat40bpp5Channels
    -   GUID \_ WICPixelFormat48bpp6Channels
    -   GUID \_ WICPixelFormat56bpp7Channels
    -   GUID \_ WICPixelFormat64bpp8Channels
    -   GUID \_ WICPixelFormat32bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat40bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat56bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat64bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat72bpp8ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp3Channels
    -   GUID \_ WICPixelFormat64bpp4Channels
    -   GUID \_ WICPixelFormat80bpp5Channels
    -   GUID \_ WICPixelFormat96bpp6Channels
    -   GUID \_ WICPixelFormat128bpp8Channels
    -   GUID \_ WICPixelFormat64bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat80bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat96bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat112bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat128bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat144bpp8ChannelsAlpha

 

 
