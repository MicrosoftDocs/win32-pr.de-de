---
description: Dieses Thema enthält Informationen zum systemeigenen HD-fotocodec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: Übersicht über das HD-Fotoformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9275abd4b74c7eb4be7673d85bb4eab5f45a163d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347374"
---
# <a name="hd-photo-format-overview"></a>Übersicht über das HD-Fotoformat

Dieses Thema enthält Informationen zum systemeigenen HD-fotocodec, der über die Windows Imaging Component (WIC) verfügbar ist.

> [!IMPORTANT]
>
> Das HD-Foto-Format ist eine vorstandard Implementierung des JPEG-XR-Formats. Das JPEG-XR-Format wurde in Windows 8 vollständig implementiert. Weitere Informationen finden Sie in der [Übersicht über JPEG XR Codec](jpeg-xr-codec.md) .

 

Dieses Thema enthält folgende Abschnitte:

-   [Codec-Identität](#codec-identity)
-   [Codieren](#encoding)
    -   [Codierungsoptionen](#encoder-options)
-   [Decodierung](#decoding)
    -   [IWICBitmapSourceTransform-Unterstützung](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                                                                                 |
|------------------------|---------------------------------------------------------------------------------|
| Formaler Name (n)         | HD-Foto, Windows Media-Foto                                                   |
| Dateinamenerweiterung (en) | WDP                                                                             |
| MIME-Typ (MIME type)              | Image/vnd. ms-Photo                                                              |
| Datei Signatur (en)      | Die ersten vier Bytes: 0x4949bc00 (Version 0; Vorabversion), 0x4949bc01 (Version 1,0) |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen HD-fotocodec-Komponenten identifiziert werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Container Format | GUID \_ containerformatwmp | 57a37caa-367a-4540-916bf 183c5093a4b |
| Decoder          | CLSID \_ wicwmpdecoder     | a26cec36-234c-4950-ae16e34aace71d0d |
| Encoder          | CLSID \_ wicwmpencoder     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Codierungsoptionen

WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene. Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen. Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle. Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

Der HD-fotocodec verwendet beide grundlegenden WIC-Optionen und bietet mehrere HD-Foto spezifische Codierungsoptionen. In der folgenden Tabelle sind die vom Native HD-fotocodec unterstützten Codierungsoptionen aufgeführt.

Grundlegende WIC-Encoder-Optionen

| Eigenschaftsname | VARTYPE | Wertbereich | Standardwert |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | VT \_ R4 | 0-1,0 | 0.9 |
| [Lossless](#lossless-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | VT \_ UI1 | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

Spezifische Codierungsoptionen für HD-Fotos

| Eigenschaftsname | VARTYPE | Wertbereich | Standardwert |
|---------------|---------|-------------|---------------|
| [Usecodecoptions](#usecodecoptions-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [Qualität](#quality-option) | VT \_ UI1 | 1 - 255 | 10 |
| [Überlappen](#overlap-option) | VT \_ UI1 | 0 - 2 | 1 |
| [Unterstichprobe](#subsampling-option) | VT \_ UI1 | 0 – 3 | 3, wenn ImageQuality > 0,8; andernfalls 1; |
| [Horizontaltileslices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 | (Bildbreite – 1)  >> 8 |
| [Verticaltileslices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 | (Bildhöhe – 1)  >> 8 |
| [Frequendcyorder](#frequencyorder-option) | VT \_ bool | **true**, **false** | **TRUE** |
| [Interleavedalpha](#interleavedalpha-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [Alphaquality](#alphaquality-option) | VT \_ UI1 | 1 - 255 | 1 |
| [Compresseddomaintranscode](#compresseddomaintranscode-option) | VT \_ bool | **true**, **false** | **TRUE** |
| [Imagedatadiscard](#imagedatadiscard-option) | VT \_ UI1 | 0 – 3 | 0 |
| [Alphadatadiscard](#alphadatadiscard-option) | VT \_ UI1 | 0–4 | Wird nicht verwendet. |
| [Ignoreüberschneidung](#ignoreoverlap-option) | VT \_ bool | **true**, **false** | **FALSE** |


Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.

### <a name="imagequality-option"></a>ImageQuality-Option

Gibt die gewünschte Bild Treue an. 0,0 gibt die niedrigste mögliche Treue an, und 1,0 gibt die höchste Genauigkeit an. Für das HD-Foto Bildformat ergibt ein 1,0-Wert eine mathematisch verlustfreie Komprimierung.

Der Standardwert ist 0,9.

### <a name="compressionquality-option"></a>CompressionQuality (Option)

Gibt die gewünschte Komprimierungs Qualität an. 0,0 gibt das effiziente verfügbare Komprimierungs Schema an. Dieses Schema erzeugt in der Regel eine schnellere Codierung, aber eine größere Ausgabe. Der Wert 1,0 gibt das effizienteste verfügbare Komprimierungs Schema an, das in der Regel eine längere Codierung, aber eine kleinere Ausgabe erzeugt.

Diese Codierungs Option wird von HD-Fotos nicht unterstützt. Dieser Wert wird ignoriert, wenn er in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Parameterliste vorhanden ist.

### <a name="lossless-option"></a>Verlustfreie Option

Gibt an, ob der Verlust Komprimierungs Modus verwendet wird. Für das HD-Foto-Bildformat überschreibt dieser Wert den Wert der [ImageQuality](#imagequality-option) -Option.

Der Standardwert ist **FALSE**.

### <a name="bitmaptransform-option"></a>BitmapTransform (Option)

Gibt an, wie das Bild während der Decodierung von Bildern transformiert wird. Sie müssen diese Option auf einen der [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) -Enumerationswerte festlegen.

Der Standardwert ist [**WICBitmapTransformOptions:: WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="usecodecoptions-option"></a>Usecodecoptions (Option)

Wenn der Wert Variant \_ true ist, werden die Optionen [Qualität](#quality-option), [Überlappung](#overlap-option)und [Unterstichprobe](#subsampling-option) anstelle des Optionswerts angezeigt.

Der Standardwert ist **FALSE**.

### <a name="quality-option"></a>Quality-Option

Gibt die Komprimierungs Qualität für das Bild an. Der Wert 1 gibt den Modus ohne Verlust an. Das Erhöhen der Werte führt zu einem höheren Komprimierungs Verhältnis und einer geringeren Bildqualität.

Der Standardwert ist 10.

### <a name="overlap-option"></a>Überlappungs Option

Gibt die Ebene der Überlappungs Verarbeitung an.

In der folgenden Tabelle sind die verfügbaren Überlappungs Verarbeitungs Ebenen aufgeführt.



| Wert | BESCHREIBUNG                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Überlappungsverarbeitung ist nicht aktiviert.                                                                                                                                                           |
| 1     | Eine Ebene der Überlappungs Verarbeitung ist aktiviert, wobei 4X4-Block codierte Werte basierend auf Werten benachbarter Blöcke geändert werden.                                                                       |
| 2     | Zwei Überlappungsverarbeitungsebenen sind aktiviert. Zusätzlich zur Verarbeitung der ersten Ebene werden codierte Werte von 16x16-Makro Blöcken basierend auf den Werten benachbarter Makroblöcke geändert. |



 

Der Standardwert ist 1.

### <a name="subsampling-option"></a>Subsampling (Option)

Gibt zusätzliche Komprimierung im Chroma-Bereich an. Auf diese Weise können Sie die Details der Leuchtkraft auf Kosten der Farbdetails beibehalten. Diese Option gilt nur für RGB-Bilder.

In der folgenden Tabelle sind die verfügbaren unter Stichproben Optionen aufgeführt.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | 4:4:4-Codierung behält vollständige Chroma-Auflösung bei.                                                                                                                                                                                                                                            |
| 2     | 4:2:2-Codierung reduziert die Chroma-Auflösung auf 1/2 der Beleuchtungs Auflösung.                                                                                                                                                                                                                      |
| 1     | 4:2:0-Codierung reduziert die Chroma-Auflösung auf 1/4 der Beleuchtungs Auflösung.                                                                                                                                                                                                                      |
| 0     | 4:0:0-Codierung verwirft alle Inhalte von Chroma und behält nur die Leuchtkraft bei. Da der Codec eine etwas geänderte Definition der Leuchtkraft verwendet, um die Leistung zu verbessern, wird empfohlen, dass Sie ein RGB-Bild vor der Codierung in monochrome konvertieren, anstatt diesen Chroma-unter Samplingmodus zu verwenden. |



 

Der Standardwert ist 3, wenn [ImageQuality](#imagequality-option) > 0,8; andernfalls 1.

### <a name="horizontaltileslices-verticaltileslices-options"></a>Horizontaltileslices, verticaltileslices (Optionen)

Geben Sie die horizontale und vertikale Ausrichtung des Bilds an, bevor Sie die Komprimierungs Codierung für die optimale Leistung der Regions Decodierung durchführen. Wenn Sie das Bild während der Codierung in rechteckige Kacheln aufteilen, können Sie die Bereiche des Bilds decodieren, ohne den gesamten komprimierten Datenstrom zu verarbeiten. Der Standardwert 0 gibt keine Unterteilung an, sodass das gesamte Bild als einzelne Kachel behandelt wird. Der Wert 1 für jeden Parameter erstellt eine einzelne horizontale und eine einzelne vertikale Division, die das Bild effektiv in vier gleichwertige Kacheln unterteilt. Der Höchstwert von 4095 für jeden Parameter dividiert das Bild in 4096 Kachel Zeilen mit 4096 Kacheln pro Zeile. Mit anderen Worten, die Parameterwerte entsprechen der Anzahl horizontaler bzw. vertikaler Kacheln minus 1. Eine Kachel kann nie kleiner als 16 Pixel Breite oder Höhe sein. Daher kann der HD-Foto-Encoder diesen Parameter anpassen, um die erforderliche minimale Kachel Größe beizubehalten. Da jeder Kachel Speicher-und Verarbeitungsaufwand zugeordnet ist, sollten Sie diese Werte sorgfältig auswählen, um das jeweilige Szenario zu erfüllen.

[Horizontaltileslices](/windows): der Standardwert ist (Bildbreite – 1)  >> 8.

[Verticaltileslices](/windows): der Standardwert ist (Bildhöhe – 1)  >> 8.

### <a name="frequencyorder-option"></a>Frequendcyorder (Option)

Gibt an, dass das Bild in Reihenfolge codiert werden muss. Die niedrigsten Häufigkeits Daten werden zuerst in der Datei angezeigt, und der Bildinhalt wird anhand seiner Häufigkeit und nicht anhand seiner räumlichen Ausrichtung gruppiert. Wenn Sie eine Datei nach Reihenfolge organisieren, wird die beste Leistung für jede Häufigkeits basierte Decodierung erzielt, weshalb wir Sie empfehlen. Geräte Implementierungen von HD-Foto Encodern können eine Datei in räumlicher Reihenfolge organisieren, um den während der Codierung erforderlichen Speicherbedarf zu reduzieren.

Der Standardwert ist **true** , und es wird empfohlen, dass Anwendungen und Geräte immer die Reihenfolge der Häufigkeit verwenden, es sei denn, Sie haben Leistungs-oder anwendungsspezifische Gründe für die räumliche Reihenfolge

### <a name="interleavedalpha-option"></a>Interleavedalpha-Option

Wenn diese Option auf **true** festgelegt wird, weist der Codec den Codec an, die Alphakanal Informationen als zusätzlichen überlappenden Kanal zu codieren, ohne dass eine Korrelation zu den Bildinhalts Kanälen besteht. Dieser Modus ist nützlich, wenn Sie Alpha gleichzeitig mit dem Bild in einem Streamingszenario decodieren müssen.

Wenn dieser Parameter auf " **false** " festgelegt wird, führt dies zu einem planaren Alphakanal, der als separates Bild mit einem eigenen optionalen Qualitäts Wert codiert ist. Mithilfe eines planaren Alphakanals können Sie die Bilddaten und den Alphakanal unabhängig decodieren. Verschachtelte Alphakanäle werden nur für bestimmte RGB-Pixel Formate unterstützt. Sie können einen planaren Alphakanal einem beliebigen Bildformat zuordnen, das einen Alphakanal definiert.

Der Standardwert ist **FALSE**.

### <a name="alphaquality-option"></a>Alphaquality-Option

Gibt die Komprimierungs Qualität für das Bild des planaren Alphakanals an. Der Wert 1 legt den Modus ohne Verlust fest. Das Erhöhen der Werte führt zu einem höheren Komprimierungs Verhältnis und einer geringeren Bildqualität.

Der Standardwert ist 1.

### <a name="compresseddomaintranscode-option"></a>Compresseddomaintranscode-Option

Mithilfe von HD-Foto können Sie eine Reihe von Datei Transformations Vorgängen ausführen, ohne die komprimierten Daten tatsächlich zu decodieren und in die Zieldatei umzucodieren. Komprimierte Domänen Vorgänge sind sehr effizient und vermeiden jeglichen zusätzlichen Qualitätsverlust, der typisch ist, wenn Sie ein Verlust behaftedes Abbilds decodieren und erneut codieren.

Folgende komprimierte Domänen Vorgänge werden unterstützt:

-   Schneiden Sie einen Bereich des Bilds ab.
-   Ausführen einer Drehung/kippen-Transformation.
-   Verwerfen von Häufigkeits Daten (ermöglicht das Erstellen einer kleineren Bilddatei.)
-   Ordnen Sie das Bild zwischen räumlicher und sequenzieller Reihenfolge neu an.

Der HD-Foto Encoder führt einen komprimierten Domänen-transcodieren-Vorgang aus, wenn er ein HD-Fotobild mithilfe eines HD-Foto-Decoders als Bildquelle codiert. Abhängig von den ausgewählten Codierungsoptionen verwendet der Codec eine komprimierte Domänen Operation, sofern möglich. Wenn sich eine Anwendung für das explizite behindern von transaktionskomprimierten Domänen Vorgängen entscheidet, sollten Sie die Option *usecodecoptions* auf **true** und die Option *compresseddomaintranscode* auf **false** festlegen.

Wenn der Codec eine komprimierte Domänen Operation ausführt, sind nur bestimmte Codierungs Parameter-und Eigenschafts Einstellungen zulässig.

-   Die grundlegenden Codierungsoptionen [ImageQuality](#imagequality-option), [CompressionQuality](/windows) und [Lossless](#lossless-option) werden ignoriert.
-   Die HD-Foto-spezifischen Codierungsoptionen [Quality](#quality-option), [überlappend](#overlap-option), [interleavedalpha](#interleavedalpha-option) und [alphaquality](#alphaquality-option) werden ignoriert.
-   Falls vorhanden, müssen die Optionen [horizontaltileslices](/windows) und [verticaltileslices](/windows) auf 0 (null) festgelegt werden. Die Kachel Größe eines Bilds kann nicht als Teil eines komprimierten Domänen Codes geändert werden.
-   Sie können die Image Organisation zwischen Häufigkeit und räumlicher Reihenfolge ändern, indem Sie den entsprechenden Wert der Optionen " [frequencyorder](/windows) " angeben.
-   Eine Haupt Drehung und/oder ein horizontaler/vertikaler Flip-Vorgang kann basierend auf dem in der [BitmapTransform](#bitmaptransform-option) -Encoder-Option angegebenen Wert ausgeführt werden.
-   Das Bild kann zugeschnitten werden, indem der gewünschte Bereich mithilfe des [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) -Parameters der " **Write tesource** "-Encoder-Methode angegeben wird.
-   Bild-und/oder Alpha Daten können verworfen werden, indem die entsprechenden Werte in den Optionen [imagedatadiscard](#imagedatadiscard-option) und/oder [alphadatadiscard](#alphadatadiscard-option) angegeben werden, sodass die codierte Dateigröße reduziert und die Auflösung des neuen Images effektiv verringert wird.

Der Standardwert ist **true** , und es wird empfohlen, dass Anwendungen und Geräte immer die Reihenfolge der Häufigkeit verwenden, es sei denn, Sie haben bestimmte Leistungs-oder Anwendungs Gründe für die räumliche Reihenfolge.

### <a name="imagedatadiscard-option"></a>Imagedatadiscard (Option)

Dieser Parameter ist nur gültig, wenn die [compresseddomaintranscode](#compresseddomaintranscode-option) -Option den Wert **true** hat. Andernfalls wird Sie ignoriert. [Imagedatadiscard](#imagedatadiscard-option) gibt die Menge der Bilddaten an, die während eines komprimierten Domänen-transcodes verworfen werden sollen. Wenn das Image einen verschachtelten Alphakanal enthält, gilt diese Daten Verwerfungs auch für den Alphakanal, mit den Ausnahmen, wie weiter unten in diesem Abschnitt beschrieben.

Die folgenden Werte sind zulässig.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Es werden keine Bildfrequenzdaten verworfen.                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | Die flexbits werden verworfen, sodass die Qualität des transcodierten Bilds beliebig reduziert wird, ohne die effektive Auflösung des Bilds zu ändern. Die genaue Verkleinerung der Dateigröße oder die spezifische Qualitäts Reduzierung hängt von zahlreichen Faktoren ab und kann nicht angegeben oder vorhergesagt werden. Durch diesen Wert wird ein Fehler festgelegt, wenn Sie ihn für einen verschachtelten Alphakanal angeben.                                                    |
| 2     | Das highpass Frequency-Daten Band wird verworfen (enthält auch die flexbits), wodurch die Auflösung des transcodierten Bilds mit dem Faktor 4 in beiden Dimensionen effektiv verringert wird. Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber es verliert alle Details in jedem 4 x 4-Block von Pixeln. Daher sollten Sie das transcodierte Bild bei der Decodierung entsprechend abgleichen.                            |
| 3     | Die Datenbänder highpass und Lowpass Frequency werden verworfen (was auch die flexbits umfasst), wodurch die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 16 verringert wird. Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber es verliert alle Details in jedem 16x16-Makroblock von Pixeln. Daher sollten Sie das transcodierte Bild bei der Decodierung entsprechend abgleichen. |



 

Der Standardwert ist 0.

### <a name="alphadatadiscard-option"></a>Alphadatadiscard (Option)

Diese Option ist nur gültig, wenn die [compresseddomaintranscode](#compresseddomaintranscode-option) -Eigenschaft auf **true** festgelegt ist und das Image entweder einen planaren oder einen verschachtelten Alphakanal enthält. Andernfalls wird Sie ignoriert. Gibt die Menge der Alpha Frequency-Daten an, die während eines komprimierten Domänen-transcodes verworfen werden sollen. Die folgenden Werte sind für einen planaren Alphakanal zulässig.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Es werden keine Bildfrequenzdaten verworfen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | Die flexbits werden verworfen, sodass die Qualität des planaren Alphakanals für das transcodierte Bild beliebig reduziert wird, ohne dass die effektive Auflösung geändert wird. Die genaue Verkleinerung der Dateigröße oder die spezifische Qualitäts Reduzierung hängt von zahlreichen Faktoren ab und kann nicht angegeben oder vorhergesagt werden.                                                                                                                                                                                                                                                |
| 2     | Das highpass Frequency Data-Band wird verworfen (enthält auch die flexbits), wodurch die Auflösung des planaren Alphakanals der transcodierten Bilder um den Faktor 4 in beiden Dimensionen verringert wird. Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle planaren Alphakanal Details in jedem 4 x 4-Block von Pixeln. Daher sollte das transcodierte Bild bei jedem decodieren entsprechend herabgesetzt werden. Normalerweise sollten Sie diesen Wert nur festlegen, wenn Sie den imagedatadiscard-Eigenschafts Wert auf denselben Wert festlegen. |
| 3     | Die Datenbänder highpass und Lowpass Frequency werden verworfen (was auch die flexbits umfasst), wodurch die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 16 verringert wird. Die tatsächlichen Dimensionen des transcodierten Bilds bleiben unverändert, aber das Bild verliert alle Details in jedem 16x16-Makroblock von Pixeln. Daher sollte das transcodierte Bild bei jedem decodieren entsprechend herabgesetzt werden. Normalerweise sollten Sie diesen Wert nur festlegen, wenn Sie die imagedatadiscard-Eigenschaft auf denselben Wert festlegen.               |
| 4     | Der Alpha Kanal wird vollständig verworfen. Das Pixel Format des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln.                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Bei Bildern, die verschachtelte Alphakanäle enthalten, wird der Alphakanal gemäß dem Wert der imagedatadiscard-Eigenschaft genauso wie die Bilddaten verarbeitet, es sei denn, diese Eigenschaft ist auf 4 festgelegt. Wenn diese Eigenschaft auf 4 festgelegt ist, wird der verschachtelte Alphakanal vollständig verworfen und das Pixel Format des transcodierten Bilds entsprechend geändert.

Für dieses Feld gibt es keinen Standardwert.

### <a name="ignoreoverlap-option"></a>Ignoreüberlappungs Option

Diese Option ist nur gültig, wenn die [compresseddomaintranscode](#compresseddomaintranscode-option) -Eigenschaft den Wert **true** hat und ein Teil Regions-transcodieren von genau einer oder mehreren Kacheln angefordert wird. Der Standard Vorgang für einen Regions-Transcodieren (oder decodieren) besteht darin, den angeforderten Bereich so zu erweitern, dass er die umgebenden Pixel einschließt, die für eine Überlappung der Bereichs Ränder erforderlich sind. Wenn dieser Parameter auf **true** festgelegt ist, werden die umgebenden Pixel ignoriert, und nur die ausgewählten Kacheln werden extrahiert. Dies erfordert wiederum, dass der angeforderte Bereich exakt mit den Koordinaten einer oder mehrerer Kacheln übereinstimmt. Wenn das Quellbild nicht gekachelt ist oder der angeforderte Bereich beliebige partielle Kacheln angibt, wird dieser Parameter ignoriert.

Der Standardwert ist **FALSE**.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

### <a name="iwicbitmapsourcetransform-support"></a>IWICBitmapSourceTransform-Unterstützung

Zusätzlich zu den Schnittstellen, die als WIC-fähiger Codec erforderlich sind, unterstützt der Native HD-Foto-Decoder auch die [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform). Die **IWICBitmapSourceTransform** -Schnittstelle stellt eine erweiterte Option zum Decodieren eines bildbit-Streams bereit. Anstatt einfach ein Abbild mithilfe von [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)zurückzugeben, aktiviert die **IWICBitmapSourceTransform** -Schnittstelle die folgenden Decoder-Optionen.

-   Decodieren eines rechteckigen unter Bereichs des Bilds.
-   Decodieren in eine niedrigere Auflösung
-   Decodieren in ein anderes Pixel Format
-   Durchführen einer Transformation (Drehung/kippen) beim Decodieren

Der Native HD-fotocodec bietet die folgende Ebene der Unterstützung für die [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) -Schnittstelle.

### <a name="doessupporttransform"></a>DoesSupportTransform

Die native Implementierung unterstützt alle [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) -Transformationen.

### <a name="getclosestsize"></a>GetClosestSize

Bei Anforderungen, die kleiner als 1/2 die Dimension des Quell Bilds in beiden Dimensionen sind, gibt HD Photo die nächst größere ganzzahlige Bildgröße zurück, die durch den Faktor zwei gleichmäßig teilbar ist. Für alle anderen angeforderten Größen gibt HD Photo die ursprünglichen Bild Dimensionen zurück.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

HD Photo gibt das Pixel Format des codierten Bilds zurück.

### <a name="copypixels"></a>CopyPixels

Das HD-Foto akzeptiert alle angeforderten Bereiche, die vom [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) -Parameter angegeben werden, und gibt den Teil des Bilds zurück.

Mit den Parametern *uiwidth* und *uiheight* müssen Dimensionen angegeben werden, die von der [**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) -Funktion zurückgegeben werden. Alle anderen Werte geben einen Fehler zurück.

Der *pguidDstFormat* -Parameter muss das von der [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) -Funktion zurückgegebene Pixel Format angeben. Jeder andere Wert gibt einen Fehler zurück.

Das HD-Foto akzeptiert jeden zulässigen Wert für den *dsttransform* -Parameter. Beachten Sie, dass die Werte, die von WIC für diesen Parameter zulässig sind, sich von den Werten unterscheiden, die für das HD-Foto für das Metadatentag

 

 
