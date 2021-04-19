---
description: Der Native JPEG-XR-Codec ist über die Windows Imaging Component (WIC) verfügbar. Das JPEG-XR-Format, das der Codec unterstützt, ist für die digitale Fotografie von Consumer und Professional konzipiert.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: JPEG-XR-Codec-Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353877"
---
# <a name="jpeg-xr-codec-overview"></a>JPEG-XR-Codec-Übersicht

Der Native JPEG-XR-Codec ist über die Windows Imaging Component (WIC) verfügbar. Das JPEG-XR-Format, das der Codec unterstützt, ist für die digitale Fotografie von Consumer und Professional konzipiert.

Das JPEG-XR-Format kann bis zu einer doppelten Komprimierungs Effizienz des ursprünglichen JPEG-Formats mit weniger merklichen Komprimierungs Artefakten erzielen. Zu den Features von JPEG XR gehören:

-   Unterstützung für Chrome-, RGB-, CMYK-und n-Channel-Images
-   ganzzahlige Formate der Länge 8, 16 und 32 Bit
-   High Dynamic Range, Wide-Gamut-Formate, verwenden von Fixed-Punkt-oder Gleit Komma Farbwerten
-   Progressive Decodierung
-   Verlust oder Verlust lose Codierung mithilfe desselben Komprimierungs Algorithmus
-   Unterstützung für das Decodieren von Interessenbereichen in großen Bildern

Das JPEG-XR-Format wird in den folgenden Standarddokumenten definiert:

-   ITU-T t. 832: *Information Technology – JPEG XR Bild Codierungssystem – Bild Codierungs Spezifikation*
-   ISO/IEC 29199-2:2010: *Information Technology – JPEG XR Bild Codierungssystem – Teil 2: Bild Codierungs Spezifikation*

Der JPEG-XR-Standard basiert größtenteils auf dem [HD-Foto](hdphoto-format-overview.md) Format, es gibt jedoch einige Unterschiede zwischen den beiden Formaten. In Windows 8 wurde der HD-fotocodec aktualisiert, um JPEG XR zu unterstützen. Der Encoder gibt jetzt immer einen mit JPEG XR – kompatiblen Bitstream aus. Der Decoder kann sowohl JPEG XR-als auch HD-Foto Bilder decodieren.

Im Zusammenhang mit dem HD-fotocodec wurden erhebliche Leistungsverbesserungen für den JPEG-XR-Codec vorgenommen. Beispielsweise wurde die Bild Decodierung untergeordneter Auflösung, wie z. b. die Generierung von Miniaturansichten, verbessert, ebenso wie das Decodieren von Bildern mit geringer Auflösung. Es wird empfohlen, dass Sie das JPEG-XR-Format anstelle des HD-Foto Formats verwenden.

## <a name="codec-information"></a>Codec-Informationen



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| Dateinamenerweiterung | "jxr" und "WDP"                                                         |
| Container-GUID      | **GUID \_ containerformatwmp**                                            |
| Decoderguid        | **CLSID \_ wicwmpdecoder**                                                |
| Encoder-GUID        | **CLSID \_ wicwmpencoder**                                                |
| Profil Unterstützung     | Der Encoder und der Decoder unterstützen bis zu Hauptprofil und bis zu Ebene 128. |



 

## <a name="codec-features"></a>Codec-Features

### <a name="high-dynamic-range"></a>Hoher dynamischer Bereich

JPEG XR unterstützt Bilder mit hohem dynamischen Bereich unter Verwendung von Gleit Komma-oder fester Punktfarben. In diesen Farbformaten ist der numerische Bereich eines Pixels größer als der sichtbare Bereich, sodass Sie die Farben während der zwischen Verarbeitungsphasen oberhalb oder unterhalb des sichtbaren Bereichs anpassen können.

-   Fester Punkt: in einer Darstellung mit einem bestimmten Punkt steht 0 für schwarz und 1,0 für die maximale Sättigung. Der JPEG-XR-Codec unterstützt sowohl das 16-Bit-als auch das 32-Bit-Format mit fester Punkt Für 16-Bit, 1,0 = 0x2000h, das 13 Bits für den sichtbaren Bereich \[ 0... 1 ergibt \] . Der Gesamtbereich liegt zwischen – 4,0 und + 3,999 und wird linear zugeordnet. Bei 32-Bit, 1,0 = 0x01000000h beträgt der sichtbare Bereich 24 Bits, und der Gesamtbereich ist – 128 bis + 127,999.
-   Gleit Komma: in einer Gleit Komma Darstellung steht 0 für schwarz und 1,0 für die maximale Sättigung. Der JPEG-XR-Codec unterstützt sowohl das 16-Bit-als auch das 32-Bit-Gleit Komma Format.

### <a name="tiles"></a>Kacheln

Ein Frame kann in rechteckige Unterbereiche partitioniert werden, die als *Kacheln* bezeichnet werden. Eine Kachel ist ein Bereich eines Bilds, das rechteckige Arrays von Makroblocks enthält. Durch Kacheln können Bereiche des Bilds decodiert werden, ohne dass das gesamte Bild verarbeitet wird.

Wählen Sie während der Codierung die Anzahl der Kacheln aus, indem Sie die Eigenschaften " **horizontaltileslices** " und " **verticaltileslices** " festlegen. Die minimale Kachel Größe beträgt 16 × 16 Pixel. Der Encoder passt die Anzahl der Kacheln an, um diese Einschränkung aufrechtzuerhalten. Mit jeder Kachel ist Speicher-und Verarbeitungsaufwand verbunden, sodass Sie die Anzahl der Kacheln berücksichtigen sollten, die für bestimmte Szenarien erforderlich sind.

### <a name="image-stream-output"></a>Bild Datenstrom Ausgabe

Der JPEG-XR-Standard definiert zwei Teile einer JPEG-XR-Datei:

-   Der bildbit-Stream, der im Text des Standards definiert ist.
-   Der Bild Container. Die Datei enthält EXIF-und XMP-Metadaten und ist in Anhang A des Standards definiert.

Es ist möglich und durch den Standard zulässig, den Bildstream in einen anderen Typ von Datei Container einzubetten. Der Encoder unterstützt einen reinen Streammodus, der den unformatierten bildbit-Datenstrom ohne Bild Container ausgibt. Eine Anwendung kann den Bitstream in einem anderen Containerformat speichern.

Legen Sie die **streamonly** -Eigenschaft fest, um den reinen Streammodus zu aktivieren.

### <a name="image-quality-settings"></a>Bild Qualitätseinstellungen

Mehrere Codec-Eigenschaften steuern die Qualität des Ausgabe Bilds vom Encoder.

-   [ImageQuality](#imagequality) ist eine Eigenschaft, die von WIC-Codecs gemeinsam ist. Sie gibt die Bildqualität als einzelnen Gleit Komma Wert von 0,0 – 1.0 an.
-   Die Eigenschaften [Quality](#image-quality-settings), [Überlappung](#overlap)und [Subsampling](#subsampling) haben mehr Kontrolle über die Qualitätseinstellungen.

Wenn Sie die Eigenschaften [Qualität](#image-quality-settings), [Überlappung](#overlap)und [Unterstichprobe](#subsampling) verwenden möchten, legen Sie die [usecodecoptions](#usecodecoptions) -Eigenschaft auf **Variant \_ true** fest.

Wenn [usecodecoptions](#usecodecoptions) **Variant \_ false** ist (**Variant \_ false** ist die Standardeinstellung), verwendet der Encoder die [ImageQuality](#imagequality) -Eigenschaft. Der Encoder ordnet den Wert von ImageQuality auf [Qualität](#image-quality-settings), [Überlappung](#overlap)und [Unterstichprobe](#subsampling) über eine Nachschlage Tabelle zu.

Der Encoder unterstützt die **CompressionQuality** -Eigenschaft nicht.

### <a name="compressed-domain-transcode"></a>Komprimierter Domänen-transcode

Der JPEG-XR-Codec kann bestimmte Bild Transformationen ausführen, ohne die komprimierten Daten tatsächlich zu decodieren und neu zu codieren. Komprimierte Domänen Vorgänge sind sehr effizient und vermeiden jeglichen zusätzlichen Qualitätsverlust, der typisch ist, wenn Sie ein Verlust behaftedes Abbilds decodieren und erneut codieren.

Folgende komprimierte Domänen Vorgänge werden unterstützt:

-   Schneiden Sie einen Bereich des Bilds ab.
-   Drehen oder Kippen des Bilds.
-   Verwerfen von Häufigkeits Daten zum Erstellen einer kleineren Bilddatei.
-   Ordnen Sie das Bild zwischen räumlicher und Häufigkeits Reihenfolge neu an.

Der JPEG-XR-Encoder verwendet nach Möglichkeit eine komprimierte Domänen-Transcodierung, wenn das Quell Image ein JPEG-XR-Image ist. Wenn der Encoder einen komprimierten Domänen Vorgang ausführt, ignoriert er die folgenden Codec-Eigenschaften: [alphaquality](#alphaquality), [ImageQuality](#imagequality), [interleavedalpha](#interleavedalpha), [Verlust lose](#lossless)[Überlappung](#overlap)und [Qualität](#image-quality-settings). Wenn die Eigenschaften [horizontaltileslices](/windows) und [verticaltileslices](/windows) vorhanden sind, müssen Sie Sie auf 0 (null) festlegen. Die Kachel Größe eines Bilds kann nicht als Teil eines komprimierten Domänen-transcodes geändert werden.

In der folgenden Liste wird beschrieben, wie die Bild Transformationen durchgeführt werden.

-   Zum Zuschneiden des Bilds legen Sie die gewünschte Region im [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) -Parameter der " **Write tesource** "-Methode fest.
-   Um das Bild zu drehen oder zu kippen, legen Sie die Eigenschaft [BitmapTransform](#bitmaptransform) fest.
-   Um Häufigkeits Daten im Bild zu verwerfen, legen Sie die [imagedatadiscard](#imagedatadiscard) -Eigenschaft fest. Legen Sie die Eigenschaft [alphadatadiscard](#alphadatadiscard) fest, um Häufigkeits Daten im Alphakanal zu verwerfen. Das Verwerfen von Häufigkeits Daten verringert die codierte Dateigröße und kann die Auflösung verringern.
-   Um die Image Organisation zwischen Häufigkeit und räumlicher Reihenfolge zu ändern, legen Sie die Eigenschaft [frequencyorder](/windows) fest.

Wenn Sie den komprimierten Domänen Code deaktivieren und erzwingen möchten, dass der Encoder das Image erneut codieren soll, legen Sie [usecodecoptions](#usecodecoptions) auf **Variant \_ true** fest, und legen Sie [compresseddomaintranscode](#compresseddomaintranscode) auf **Variant \_ false** fest.

## <a name="encoder-options"></a>Codierungsoptionen

Um Codierungs Eigenschaften festzulegen, verwenden Sie die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle. Weitere Informationen finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

In der folgenden Liste sind die Codierungsoptionen angegeben.

-   [Alphadatadiscard](#alphadatadiscard)
-   [Alphaquality](#alphaquality)
-   [BitmapTransform](#bitmaptransform)
-   [Compresseddomaintranscode](#compresseddomaintranscode)
-   [Frequendcyorder](#frequencyorder)
-   [Horizontaltileslices](#horizontaltileslices)
-   [Ignoreüberschneidung](#ignoreoverlap)
-   [Imagedatadiscard](#imagedatadiscard)
-   [ImageQuality](#imagequality)
-   [Interleavedalpha](#interleavedalpha)
-   [Lossless](#lossless)
-   [Überlappen](#overlap)
-   [Progressivemode](#progressivemode)
-   [Qualität](#image-quality-settings)
-   [Streamonly](#streamonly)
-   [Unterstichprobe](#subsampling)
-   [Usecodecoptions](#usecodecoptions)
-   [Verticaltileslices](#verticaltileslices)

### <a name="alphadatadiscard"></a>Alphadatadiscard

Legt die Menge der Alpha Frequenzdaten fest, die während eines komprimierten Domänen-transcodes verworfen werden sollen.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0 – 4   | Keine    |



 

Diese Eigenschaft gilt nur, wenn die [compresseddomaintranscode](#compresseddomaintranscode) -Eigenschaft auf **Variant \_ true** festgelegt ist und das Bild entweder einen planaren Alphakanal oder einen verschachtelten Alphakanal enthält; andernfalls wird es ignoriert.

Bei Bildern, die einen planaren Alphakanal enthalten, sind die folgenden Werte gültig.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Es werden keine Bildfrequenzdaten verworfen.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | Die flexbits werden verworfen. Dadurch wird die Qualität des planaren Alphakanals für das transcodierte Bild willkürlich reduziert. ohne Änderung der effektiven Auflösung. Die genaue Reduzierung der Dateigröße und-Qualität hängt von zahlreichen Faktoren ab und kann nicht genau angegeben werden.                                                                                                                                                                                           |
| 2     | Das Daten Band der Hochpass Frequenz wird verworfen, einschließlich der flexbits. Dadurch wird die Auflösung des planaren Alphakanals um den Faktor 4 in beiden Dimensionen reduziert. Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 4 x 4-Block von Alpha-Channel-Pixeln. Normalerweise sollten Sie diesen Wert nur festlegen, wenn die [imagedatadiscard](#imagedatadiscard) -Eigenschaft denselben Wert aufweist.                            |
| 3     | Die Datenbänder "High-Pass" und "Low-Pass Frequency" werden verworfen, einschließlich der "flexbits". Dadurch wird die Auflösung des planaren Alphakanals um den Faktor 16 in beiden Dimensionen reduziert. Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 16x16-Makroblock von Alpha-Channel-Pixeln. Normalerweise sollten Sie diesen Wert nur festlegen, wenn die [imagedatadiscard](#imagedatadiscard) -Eigenschaft denselben Wert aufweist. |
| 4     | Der Alphakanal wird vollständig verworfen. Das Pixel Format des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln.                                                                                                                                                                                                                                                                                                                                |



 

Bei Bildern, die einen verschachtelten Alphakanal enthalten, ist der folgende Wert gültig.



| Wert | BESCHREIBUNG                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | Der Alphakanal wird vollständig verworfen. Das Pixel Format des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln. |



 

Wenn diese Eigenschaft für verschachtelte Alpha Dateien nicht auf 4 festgelegt ist, wird der Alphakanal gemäß dem Wert der [imagedatadiscard](#imagedatadiscard) -Eigenschaft genauso wie die Bilddaten verarbeitet.

### <a name="alphaquality"></a>Alphaquality

Legt die Komprimierungs Qualität für das Bild des planaren Alphakanals fest.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1 – 255 | 1       |



 

Diese Eigenschaft wird angewendet, wenn das Image einen Alpha-Kanal aufweist und die [interleavedalpha](#interleavedalpha) -Eigenschaft **Variant \_ false** ist. Der Wert 1 gibt den Modus ohne Verlust an. Das Erhöhen der Werte führt zu einem höheren Komprimierungs Verhältnis und einer geringeren Bildqualität.

### <a name="bitmaptransform"></a>BitmapTransform

Gibt an, ob das Bild beim decodierten gedreht oder geflippt wird.



| Datentyp | VARTYPE     | Range                                                                     | Standard                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **VT \_ UI1** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>Compresseddomaintranscode

Aktiviert oder deaktiviert die komprimierte Domänen übergreifende Transcodierung.



| Datentyp         | VARTYPE      | Standard           |
|-------------------|--------------|-------------------|
| **Variant \_ bool** | **VT \_ bool** | **Variant \_ true** |



 

Wenn Sie komprimierte Domänen Vorgänge deaktivieren möchten, legen Sie diese Eigenschaft auf **Variant \_ false** fest.

### <a name="frequencyorder"></a>Frequendcyorder

Aktiviert die Codierung in Reihenfolge der Häufigkeit. Geräte Implementierungen von JPEG-XR-Encodern können eine Datei in räumlicher Reihenfolge organisieren, um den während der Codierung erforderlichen Speicherplatz zu reduzieren.



| Datentyp         | VARTYPE      | Standard           |
|-------------------|--------------|-------------------|
| **Variant \_ bool** | **VT \_ bool** | **Variant \_ true** |



 

-   **Variant \_ TRUE**: Häufigkeit der Reihenfolge. Die niedrigsten Häufigkeits Daten werden zuerst in der Datei angezeigt, und der Bildinhalt wird anhand seiner Häufigkeit und nicht anhand seiner räumlichen Ausrichtung gruppiert. Das Organisieren einer Datei nach Reihenfolge der Reihenfolge bietet die beste Leistung für jede Häufigkeits basierte Decodierung.
-   **Variant \_ FALSE**: räumliche Reihenfolge. Räumliche Reihenfolge reduziert den während der Codierung erforderlichen Speicherplatz

Die Reihenfolge der Häufigkeit wird empfohlen, es sei denn, Sie haben Leistungs-oder anwendungsspezifische Gründe für die räumliche Reihenfolge

### <a name="horizontaltileslices"></a>Horizontaltileslices

Legt die Anzahl horizontaler Kacheln fest.



| Datentyp  | VARTYPE     | Range  | Standard                      |
|------------|-------------|--------|------------------------------|
| **USHORT** | **VT \_ UI2** | 0 – 4095 | (Bildbreite – 1)  >> 8 |



 

Der Wert ist die Anzahl der horizontalen Unterteilungen. Das heißt, die Anzahl horizontaler Kacheln – 1.

### <a name="ignoreoverlap"></a>Ignoreüberschneidung

Gibt an, wie der Encoder Kachel Grenzen während eines komprimierten Domänen-transcodes behandelt.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **Variant \_ bool** | **VT \_ bool** | **Variant \_ false** |



 

Diese Eigenschaft wird nur angewendet, wenn die [compresseddomaintranscode](#compresseddomaintranscode) -Eigenschaft auf **Variant \_ true** festgelegt ist und ein Teil Regions-transcodieren von genau einer oder mehreren Kacheln ausgeführt wird.

Der Standard Vorgang für einen Regions-transcodieren besteht darin, den angeforderten Bereich so zu erweitern, dass er die umgebenden Pixel einschließt, die für eine Überlappung der Bereichs Ränder erforderlich sind. Wenn diese Eigenschaft auf **Variant \_ true** festgelegt ist, ignoriert der Codec die umgebenden Pixel, und nur die ausgewählten Kacheln werden extrahiert. Wenn das Quellbild nicht gekachelt ist oder die angeforderte Region partielle Kacheln enthält, wird dieser Parameter ignoriert.

### <a name="imagedatadiscard"></a>Imagedatadiscard

Legt die Menge der Bildfrequenz Daten fest, die während eines komprimierten Domänen-transcodes verworfen werden sollen.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0 – 3   | 0       |



 

Diese Eigenschaft gilt nur, wenn die [compresseddomaintranscode](#compresseddomaintranscode) -Eigenschaft auf **Variant \_ true** festgelegt ist; andernfalls wird Sie ignoriert.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Es werden keine Bildfrequenzdaten verworfen.                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | Die flexbits werden verworfen. Dadurch wird die Qualität des transcodierten Bilds willkürlich reduziert, ohne die effektive Auflösung des Bilds zu ändern. Die genaue Reduzierung der Dateigröße und-Qualität hängt von zahlreichen Faktoren ab und kann nicht genau angegeben werden. Dieser Wert gibt einen für einen verschachtelten Alphakanal angegebenen Fehler zurück.                                                                                |
| 2     | Das Daten Band der Hochpass Frequenz wird verworfen, einschließlich der flexbits. Dadurch wird die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 4 reduziert. Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 4 x 4-Block von Pixeln. Daher sollte das transcodierte Bild bei jeder decodierte Ausführung entsprechend herabgestuft werden.                             |
| 3     | Die Datenbänder "High-Pass" und "Low-Pass Frequency" werden verworfen, einschließlich der "flexbits". Dadurch wird die Auflösung des transcodierten Bilds mit dem Faktor 16 in beiden Dimensionen reduziert. Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 16x16-Makroblock von Pixeln. Daher sollte das transcodierte Bild bei jeder decodierte Ausführung entsprechend herabgestuft werden. |



 

Wenn das Image einen verschachtelten Alphakanal enthält, wird der Wert von [imagedatadiscard](#imagedatadiscard) auf den Alphakanal angewendet, es sei denn, die [alphadatadiscard](#alphadatadiscard) -Eigenschaft ist auf 4 festgelegt. in diesem Fall wird der Alphakanal verworfen.

Bei planare Alpha werden die verworfenen Häufigkeits Daten durch die [alphadatadiscard](#alphadatadiscard) -Eigenschaft gesteuert.

### <a name="imagequality"></a>ImageQuality

Legt die Bildqualität fest.



| Datentyp | VARTYPE    | Range | Standard |
|-----------|------------|-------|---------|
| **FLOAT** | **VT \_ R4** | 0 – 1.0 | 0.9     |



 

Ebene 1,0 bietet eine mathematisch verlustfreie Komprimierung.

Ebene 0,0 ist die Einstellung für die niedrigste Qualität.

### <a name="interleavedalpha"></a>Interleavedalpha

Gibt an, ob überlappende Alpha oder planare Alpha codiert werden soll.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **Variant \_ bool** | **VT \_ bool** | **Variant \_ false** |



 

-   **Variant \_ TRUE**: Interleaved alpha. Alpha Kanalinformationen werden als zusätzlicher überlappenden Kanal codiert, ohne dass eine Korrelation zu den Bildinhalts Kanälen besteht. Dieser Modus ist nützlich für das gleichzeitige Decodieren von Alpha mit dem Bild beim Streaming des Bilds.
-   Variant \_ false: Planar alpha. Ein planarer Alphakanal wird als separates Bild codiert. Die Bilddaten und der Alphakanal werden unabhängig voneinander decodiert. Optional können Sie die Qualitätsstufe des Alphakanals festlegen, indem Sie die [alphaquality](#alphaquality) -Eigenschaft festlegen.

Das verschachtelte Alpha wird nur für bestimmte RGB-Pixel Formate unterstützt. Planar Alpha wird für jedes Bildformat unterstützt, das einen Alphakanal definiert.

### <a name="lossless"></a>Lossless

Ermöglicht die Komprimierung von Verlusten.



| Datentyp         | VARTYPE      | Standard        |
|-------------------|--------------|----------------|
| **Variant \_ bool** | **VT \_ bool** | Variant \_ false |



 

Wenn der Wert **Variant \_ true** ist, verwendet der Encoder die Verlust lose Komprimierung. Wenn diese Eigenschaft auf **Variant \_ true** festgelegt ist, überschreibt diese Eigenschaft die [ImageQuality](#imagequality) -Eigenschaft.

### <a name="overlap"></a>Überlappung

Legt die Ebene der Überlappungs Filterung fest. Mit Überlappungs Filterung werden Transformations Koeffizienten über Block-und Makroblock Grenzen hinweg angewendet. Dadurch können blockierende Artefakte reduziert werden.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0 – 4   | 1       |



 



| Wert | BESCHREIBUNG                                   |
|-------|-----------------------------------------------|
| 0     | Keine Überlappung.                                   |
| 1     | Eine Überschneidungs Ebene, weiche tiult. (Standardeinstellung) |
| 2     | Zwei überlappende Ebenen, weiche tiult.           |
| 3     | Eine Überschneidungs Ebene, harte Zeit             |
| 4     | Zwei Ebenen der Überlappung, Festplatte.           |



 

Definitionen:

-   Eine Überlappungs Ebene: die codierten Werte von 4 x 4-Blöcken werden auf der Grundlage benachbarter Blöcke geändert.
-   Zwei überlappende Ebenen: die erste Überlappungs Ebene wird angewendet. Außerdem werden die codierten Werte von 16x16-Makro Blöcken basierend auf den benachbarten Macroblocks geändert.
-   Soft tiult: überlappende Filterung wird über Kachel Grenzen hinweg angewendet.
-   Harte Zeit: überlappende Filterung wird nicht über Kachel Grenzen hinweg angewendet. Mit fest Kacheln können einige visuelle Artefakte entlang der Kachel Grenzen eingeführt werden.

Wenn Sie diese Eigenschaft festlegen, legen Sie auch [usecodecoptions](#usecodecoptions) auf **Variant \_ true** fest.

### <a name="progressivemode"></a>Progressivemode

Aktiviert oder deaktiviert die Progressive Codierung.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **Variant \_ bool** | **VT \_ bool** | **Variant \_ false** |



 



| Wert              | BESCHREIBUNG                |
|--------------------|----------------------------|
| **Variant \_ true**  | Sequenzieller Modus (Standard). |
| **Variant \_ false** | Progressiver Modus.          |



 

### <a name="quality"></a>Qualität

Legt die Komprimierungs Qualität fest.



| Datentyp | VARTYPE     | Range | Standard |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1 – 255 | 1       |



 

Der Wert 1 gibt den Modus ohne Verlust an. Das Erhöhen der Werte führt zu einem höheren Komprimierungs Verhältnis und einer geringeren Bildqualität.

Wenn Sie diese Eigenschaft festlegen, legen Sie auch [usecodecoptions](#usecodecoptions) auf **Variant \_ true** fest.

### <a name="streamonly"></a>Streamonly

Aktiviert oder deaktiviert den reinen Streammodus.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **Variant \_ bool** | **VT \_ bool** | **Variant \_ false** |



 



| Wert              | BESCHREIBUNG                                                            |
|--------------------|------------------------------------------------------------------------|
| **Variant \_ true**  | Der Encoder gibt den Rohdaten Strom ohne Metadaten aus.             |
| **Variant \_ false** | Der Encoder gibt das Containerformat (Bild Datenstrom und Metadaten) aus. |



 

### <a name="subsampling"></a>Unterstichprobe

Legt die Chroma-Unterstichprobe fest. Diese Eigenschaft gilt nur für RGB-Bilder.



| Datentyp | VARTYPE     | Range | Standard                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **VT \_ UI1** | 0 – 3   | 3, wenn [ImageQuality](#imagequality) > 0,8; andernfalls 1 |



 



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
<td>4:4:4-Codierung. Behält die vollständige Chroma-Auflösung bei.</td>
</tr>
<tr class="even">
<td>2</td>
<td>4:2:2-Codierung. Die Chroma-Auflösung ist 1/2 der Beleuchtungs Auflösung.</td>
</tr>
<tr class="odd">
<td>1</td>
<td>4:2:0-Codierung. Die Chroma-Auflösung ist 1/4 der Beleuchtungs Auflösung.</td>
</tr>
<tr class="even">
<td>0</td>
<td>4:0:0-Codierung. Verwirft alle Chroma-Werte und behält nur die Leuchtkraft bei.
<blockquote>
[!Note]<br />
Dieser Modus wird nicht empfohlen, da der Codec eine etwas geänderte Definition der Leuchtkraft verwendet, um die Leistung zu verbessern. Stattdessen ist es besser, das Bild vor der Codierung in monochrome zu konvertieren.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

4:2:2 und 4:2:0 behalten Sie die Details der Leuchtkraft auf der Kosten der Farbdetails bei.

Wenn Sie diese Eigenschaft festlegen, legen Sie auch [usecodecoptions](#usecodecoptions) auf **Variant \_ true** fest.

### <a name="usecodecoptions"></a>Usecodecoptions

Gibt an, ob die Eigenschaften [Quality](#image-quality-settings), [Überlappung](#overlap)und [Subsampling](#subsampling) anstelle der generischen [ImageQuality](#imagequality) -Eigenschaft verwendet werden sollen.



| Datentyp         | VARTYPE      | Standard            |
|-------------------|--------------|--------------------|
| **Variant \_ bool** | **VT \_ bool** | **Variant \_ false** |



 

### <a name="verticaltileslices"></a>Verticaltileslices

Legt die Anzahl horizontaler Kacheln fest.



| Datentyp  | VARTYPE     | Range  | Standard                       |
|------------|-------------|--------|-------------------------------|
| **USHORT** | **VT \_ UI2** | 0 – 4095 | (Bildhöhe – 1)  >> 8 |



 

Der Wert ist die Anzahl vertikaler Unterteilungen. Das heißt, die Anzahl vertikaler Kacheln – 1.

## <a name="supported-color-formats"></a>Unterstützte Farb Formate

Weitere Informationen zu diesen Formaten finden Sie unter [native Pixel Formats](-wic-codec-native-pixel-formats.md).

-   **Integer-RGB-Formate**
    -   GUID \_ WICPixelFormat24bppRGB
    -   GUID \_ WICPixelFormat24bppBGR
    -   GUID \_ WICPixelFormat32bppBGR
    -   GUID \_ WICPixelFormat48bppRGB
    -   GUID \_ WICPixelFormat32bppBGRA
    -   GUID \_ WICPixelFormat64bppRGBA
    -   GUID \_ WICPixelFormat32bppPBGRA
    -   GUID \_ WICPixelFormat64bppPRGBA
-   **Einstufige RGB-Formate**
    -   GUID \_ WICPixelFormat48bppRGBFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBFixedPoint
    -   GUID \_ WICPixelFormat96bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBAFixedPoint
-   **Gleit Komma-RGB-Formate**
    -   GUID \_ WICPixelFormat48bppRGBHalf
    -   GUID \_ WICPixelFormat64bppRGBHalf
    -   GUID \_ WICPixelFormat128bppRGBFloat
    -   GUID \_ WICPixelFormat64bppRGBAFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBAHalf
    -   GUID \_ WICPixelFormat128bppRGBAFloat
    -   GUID \_ WICPixelFormat128bppPRGBAFloat
-   **Graustufen Formate**
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
-   **N-Kanal Formate**
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

 

 
