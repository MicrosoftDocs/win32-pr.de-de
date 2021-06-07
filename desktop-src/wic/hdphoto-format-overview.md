---
description: Dieses Thema enthält Informationen zum nativen HD-Fotocodec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: Übersicht über das HD-Fotoformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c526667c6bf77d340e895bdb66dc073134c33d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444871"
---
# <a name="hd-photo-format-overview"></a>Übersicht über das HD-Fotoformat

Dieses Thema enthält Informationen zum nativen HD-Fotocodec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.

> [!IMPORTANT]
>
> Das HD-Fotoformat ist eine Vorstandardimplementierungen des JPEG-XR-Formats. Das JPEG XR-Format wurde vollständig in Windows 8 implementiert. Weitere Informationen finden Sie in der [JPEG XR-Codec-Übersicht.](jpeg-xr-codec.md)

 

Dieses Thema enthält folgende Abschnitte:

-   [Codec-Identität](#codec-identity)
-   [Codieren](#encoding)
    -   [Encoderoptionen](#encoder-options)
-   [Decodierung](#decoding)
    -   [IWICBitmapSourceTransform-Unterstützung](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Informationen zur Codecidentifikation.



|   Komponente            | BESCHREIBUNG                                                                     |
|------------------------|---------------------------------------------------------------------------------|
| Formale Namen         | HD-Foto, Windows-Medienfoto                                                   |
| Dateinamenerweiterungen | Wdp                                                                             |
| MIME-Typ (MIME type)              | image/vnd.ms-photo                                                              |
| Dateisignatur(en)      | Erste vier Bytes: 0x4949bc00 (Version 0; Vorabversion), 0x4949bc01 (Version 1.0) |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen HD Photo-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatWmp | 57a37caa-367a-4540-916bf183c5093a4b |
| Decoder          | CLSID \_ WICWmpDecoder     | a26cec36-234c-4950-ae16e34aace71d0d |
| Encoder          | CLSID \_ WICWmpEncoder     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Encoderoptionen

WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene. Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen. Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes (jedoch nicht unbedingt unterstützt) oder codecspezifische Optionen verfügbar sind, die vom Bildformatcodec entworfen wurden. Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

Der HD-Fotocodec verwendet beide grundlegenden WIC-Optionen und bietet mehrere HD Photo-spezifische Codierungsoptionen. In der folgenden Tabelle sind die Encoderoptionen aufgeführt, die vom nativen HD Photo-Codec unterstützt werden.

Grundlegende WIC-Encoderoptionen

| Eigenschaftsname | VARTYPE | Wertbereich | Standardwert |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | VT \_ R4 | 0 - 1.0 | 0.9 |
| [Lossless](#lossless-option) | VT \_ BOOL | **TRUE,** **FALSE** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | VT \_ UI1 | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

HD Photo Specific Encoder Options

| Eigenschaftsname | VARTYPE | Wertbereich | Standardwert |
|---------------|---------|-------------|---------------|
| [UseCodecOptions](#usecodecoptions-option) | VT \_ BOOL | **TRUE,** **FALSE** | **FALSE** |
| [Qualität](#quality-option) | VT \_ UI1 | 1 - 255 | 10 |
| [Überlappen](#overlap-option) | VT \_ UI1 | 0 - 2 | 1 |
| [Untersampling](#subsampling-option) | VT \_ UI1 | 0 – 3 | 3, wenn ImageQuality > 0.8; andernfalls 1; |
| [HorizontalTileSlices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 | (Bildbreite – 1) >> 8 |
| [VerticalTileSlices](#horizontaltileslices-verticaltileslices-options) | VT \_ UI2 | 0 - 4095 | (Bildhöhe – 1) >> 8 |
| [FrequencyOrder](#frequencyorder-option) | VT \_ BOOL | **TRUE,** **FALSE** | **TRUE** |
| [InterleavedAlpha](#interleavedalpha-option) | VT \_ BOOL | **TRUE,** **FALSE** | **FALSE** |
| [AlphaQuality](#alphaquality-option) | VT \_ UI1 | 1 - 255 | 1 |
| [CompressedDomainTranscode](#compresseddomaintranscode-option) | VT \_ BOOL | **TRUE,** **FALSE** | **TRUE** |
| [ImageDataDiscard](#imagedatadiscard-option) | VT \_ UI1 | 0 – 3 | 0 |
| [AlphaDataDiscard](#alphadatadiscard-option) | VT \_ UI1 | 0–4 | Wird nicht verwendet. |
| [IgnoreOverlap](#ignoreoverlap-option) | VT \_ BOOL | **TRUE,** **FALSE** | **FALSE** |


Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.

### <a name="imagequality-option"></a>ImageQuality-Option

Gibt die gewünschte Bildgenauigkeit an. 0.0 gibt die geringstmögliche Genauigkeit und 1,0 die höchste Genauigkeit an. Für das HD-Fotobildformat führt ein 1,0-Wert zu einer mathematischen verlustlosen Komprimierung.

Der Standardwert ist 0,9.

### <a name="compressionquality-option"></a>CompressionQuality-Option

Gibt die gewünschte Komprimierungsqualität an. 0.0 gibt das verfügbare effiziente Komprimierungsschema an. In der Regel erzeugt dieses Schema eine schnellere Codierung, aber eine größere Ausgabe. Der Wert 1.0 gibt das effizienteste verfügbare Komprimierungsschema an, das in der Regel eine längere Codierung, aber eine kleinere Ausgabe erzeugt.

HD Photo unterstützt diese Encoderoption nicht. Dieser Wert wird ignoriert, wenn er in der [**IPropertyBag2-Parameterliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) vorhanden ist.

### <a name="lossless-option"></a>Verlustlose Option

Gibt an, ob der Verlustkomprimierungsmodus verwendet werden soll. Für das HD-Fotobildformat überschreibt dieser Wert den Wert der [Option ImageQuality.](#imagequality-option)

Der Standardwert ist **FALSE**.

### <a name="bitmaptransform-option"></a>BitmapTransform-Option

Gibt an, wie das Bild während der Bilddecodierung transformiert wird. Sie müssen diese Option auf einen der [**WICBitmapTransformOptions-Enumerationswerte**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) festlegen.

Der Standardwert ist [**WICBitmapTransformOptions::WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="usecodecoptions-option"></a>UseCodecOptions-Option

Wenn der Wert VARIANT \_ TRUE ist, werden [die Optionen Quality](#quality-option), [Overlap](#overlap-option)und [Subsampling](#subsampling-option) anstelle des Optionswerts verwendet.

Der Standardwert ist **FALSE**.

### <a name="quality-option"></a>Quality-Option

Gibt die Komprimierungsqualität für das Bild an. Der Wert 1 gibt den verlustlosen Modus an. Das Erhöhen von Werten führt zu einem höheren Komprimierungsverhältnis und einer geringeren Imagequalität.

Der Standardwert ist 10.

### <a name="overlap-option"></a>Überlappungsoption

Gibt die Ebene der Überlappungsverarbeitung an.

In der folgenden Tabelle sind die verfügbaren Überlappungsverarbeitungsebenen aufgeführt.



| Wert | BESCHREIBUNG                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Überlappungsverarbeitung ist nicht aktiviert.                                                                                                                                                           |
| 1     | Eine Ebene der Überlappungsverarbeitung ist aktiviert, bei der 4x4-blockcodierte Werte basierend auf Werten benachbarter Blöcke geändert werden.                                                                       |
| 2     | Zwei Überlappungsverarbeitungsebenen sind aktiviert. Zusätzlich zur Verarbeitung der ersten Ebene werden codierte Werte von 16x16-Makroblöcken basierend auf den Werten benachbarter Makroblöcke geändert. |



 

Der Standardwert ist 1.

### <a name="subsampling-option"></a>Subsamplingoption

Gibt zusätzliche Komprimierung im Komprimierungsraum an. Auf diese Weise können Sie die Details der Leuchtdichte auf Kosten der Farbdetails beibehalten. Diese Option gilt nur für RGB-Bilder.

In der folgenden Tabelle sind die verfügbaren Unterbeispieloptionen aufgeführt.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | Die 4:4:4-Codierung behält die vollständige Auflösung bei.                                                                                                                                                                                                                                            |
| 2     | Die 4:2:2-Codierung reduziert die Farbauflösung auf 1/2 der Leuchtdichteauflösung.                                                                                                                                                                                                                      |
| 1     | Die 4:2:0-Codierung reduziert die Auflösung der Farbauflösung auf 1/4 der Leuchtdichteauflösung.                                                                                                                                                                                                                      |
| 0     | Bei der 4:0:0-Codierung werden alle Inhalte verworfen und nur die Leuchtdichte beibehalten. Da der Codec eine leicht geänderte Definition der Leuchtdichte verwendet, um die Leistung zu verbessern, wird empfohlen, ein RGB-Bild vor der Codierung in monofarbig zu konvertieren, anstatt diesen Subsamplingmodus zu verwenden. |



 

Der Standardwert ist 3, wenn [ImageQuality](#imagequality-option) > 0,8; andernfalls 1.

### <a name="horizontaltileslices-verticaltileslices-options"></a>HorizontalTileSlices, VerticalTileSlices-Optionen

Geben Sie die horizontale und vertikale Kacheln des Bilds an, bevor Sie die Komprimierungscodierung durchführen, um die optimale Leistung der Bereichsdecodierung zu erzielen. Indem Sie das Bild während der Codierung in rechteckige Kacheln unterteilen, können Sie Bereiche des Bilds decodieren, ohne den gesamten komprimierten Datenstrom zu verarbeiten. Der Standardwert 0 gibt keine Unterteilung an, sodass das gesamte Bild als einzelne Kachel behandelt wird. Der Wert 1 für jeden Parameter erstellt eine einzelne horizontale und eine einzelne vertikale Division, die das Bild effektiv in vier gleich große Kacheln aufteilt. Der Maximalwert 4095 für jeden Parameter teilt das Bild in 4096 Kachelzeilen mit 4.096 Kacheln pro Zeile auf. Anders ausgedrückt: Die Parameterwerte sind gleich der Anzahl der horizontalen und vertikalen Kacheln (bzw. minus 1). Eine Kachel darf nie kleiner als 16 Pixel in Breite oder Höhe sein, daher kann der HD-Fotoencoder diesen Parameter anpassen, um die erforderliche minimale Kachelgröße zu erhalten. Da jeder Kachel Speicher- und Verarbeitungsaufwand zugeordnet ist, sollten Sie diese Werte sorgfältig auswählen, um das spezifische Szenario zu erfüllen.

[HorizontalTileSlices:](/windows)Der Standardwert ist (Bildbreite – 1)  >> 8.

[VerticalTileSlices:](/windows)Der Standardwert ist (Bildhöhe – 1)  >> 8.

### <a name="frequencyorder-option"></a>FrequencyOrder-Option

Gibt an, dass das Bild in der Reihenfolge der Häufigkeit codiert werden muss. Die Daten mit der niedrigsten Häufigkeit werden zuerst in der Datei angezeigt, und der Bildinhalt wird nach seiner Häufigkeit und nicht nach seiner räumlichen Ausrichtung gruppiert. Das Organisieren einer Datei nach Häufigkeits reihenfolge bietet die beste Leistung für jede häufigkeitsbasierte Decodierung und wird daher empfohlen. Geräteimplementierungen von HD-Fotoencodern können eine Datei in räumlicher Reihenfolge organisieren, um den während der Codierung erforderlichen Speicherbedarf zu reduzieren.

Der Standardwert ist **TRUE,** und es wird empfohlen, dass Anwendungen und Geräte immer die Häufigkeits reihenfolge verwenden, es sei denn, Sie haben leistungs- oder anwendungsspezifische Gründe für die Verwendung der räumlichen Reihenfolge.

### <a name="interleavedalpha-option"></a>InterleavedAlpha-Option

Wenn Sie diese Option auf **TRUE** festlegen, wird der Codec angewiesen, die Alphakanalinformationen als zusätzlichen überlappenden Kanal ohne Korrelation mit den Bildinhaltskanälen zu codieren. Dieser Modus ist nützlich, wenn Sie Alpha gleichzeitig mit dem Bild in einem Streamingszenario decodieren müssen.

Das Festlegen dieses Parameters auf **FALSE** führt zu einem planaren Alphakanal, der als separates Bild mit einem eigenen optionalen Quality-Wert codiert ist. Mithilfe eines planaren Alphakanals können Sie die Bilddaten und den Alphakanal unabhängig decodieren. Verschachtelte Alphakanäle werden nur für bestimmte RGB-Pixelformate unterstützt. Sie können einen planaren Alphakanal einem beliebigen Bildformat zuordnen, das einen Alphakanal definiert.

Der Standardwert ist **FALSE**.

### <a name="alphaquality-option"></a>AlphaQuality-Option

Gibt die Komprimierungsqualität für das planare Alphakanalbild an. Der Wert 1 legt den verlustfreien Modus fest. Steigende Werte führen zu höheren Komprimierungsverhältnissen und einer niedrigeren Imagequalität.

Der Standardwert ist 1.

### <a name="compresseddomaintranscode-option"></a>CompressedDomainTranscode-Option

Mit HD Photo können Sie eine Reihe von Dateitransformationsvorgängen ausführen, ohne die komprimierten Daten tatsächlich zu decodieren und in die Zieldatei erneut zu codieren. Komprimierte Domänenvorgänge sind sehr effizient und vermeiden zusätzliche Qualitätsverluste, die typisch sind, wenn Sie ein verlustbegrenztes, komprimiertes Bild decodieren und neu codieren.

Die folgenden komprimierten Domänenvorgänge werden unterstützt:

-   Zuschneiden eines Bildbereichs.
-   Führen Sie eine Drehungs-/Flip-Transformation aus.
-   Verwerfen von Häufigkeitsdaten (sodass eine kleinere Imagedatei erstellt werden kann)
-   Organisieren Sie das Bild zwischen der sequenziellen Reihenfolge räumlicher Und Häufigkeit neu.

Der HD-Fotoencoder führt einen komprimierten Domänentranscodierungsvorgang aus, wenn er ein HD-Fotobild codiert, indem ein HD-Fotodecoder als Bildquelle verwendet wird. Abhängig von den ausgewählten Codierungsoptionen verwendet der Codec nach Möglichkeit einen komprimierten Domänenvorgang. Wenn eine Anwendung komprimierte Domänentranscodierungsvorgänge explizit unterdrückt, sollten Sie die *Option UseCodecOptions* auf **TRUE** und die Option *CompressedDomainTranscode* auf **FALSE** festlegen.

Wenn der Codec einen komprimierten Domänenvorgang ausführt, sind nur bestimmte Encoderparameter und Eigenschafteneinstellungen zulässig.

-   Die grundlegenden Encoderoptionen [ImageQuality,](#imagequality-option) [CompressionQuality](/windows) und [Lossless](#lossless-option) werden ignoriert.
-   Die HD-Foto-spezifischen Encoderoptionen [Quality](#quality-option), [Overlap](#overlap-option), [InterleavedAlpha](#interleavedalpha-option) und [AlphaQuality](#alphaquality-option) werden ignoriert.
-   Falls vorhanden, müssen die Optionen [HorizontalTileSlices](/windows) und [VerticalTileSlices](/windows) auf 0 (null) festgelegt werden. Die Kachelgröße eines Bilds kann nicht als Teil einer komprimierten Domänentranscodierung geändert werden.
-   Sie können die Bildorganisation zwischen Häufigkeit und räumlicher Reihenfolge ändern, indem Sie den entsprechenden Wert der [FrequencyOrdering-Optionen](/windows) angeben.
-   Eine Kardinalrotation und/oder ein horizontaler/vertikaler Flip-Vorgang kann basierend auf dem in der [BitmapTransform-Encoderoption](#bitmaptransform-option) angegebenen Wert ausgeführt werden.
-   Das Bild kann zugeschnitten werden, indem der gewünschte Bereich mithilfe des [**WICRect-Parameters**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) der **WriteSource-Encodermethode** angegeben wird.
-   Bild- und/oder Alphadaten können verworfen werden, indem die entsprechenden Werte in den Optionen [ImageDataDiscard](#imagedatadiscard-option) und/oder [AlphaDataDiscard](#alphadatadiscard-option) angegeben werden, wodurch die Größe der codierten Datei reduziert und die Auflösung des neuen Bilds effektiv reduziert wird.

Der Standardwert ist **TRUE,** und es wird empfohlen, dass Anwendungen und Geräte immer die Häufigkeitsreihenfolge verwenden, es sei denn, Sie haben bestimmte Leistungs- oder Anwendungsgründe für die Verwendung der räumlichen Reihenfolge.

### <a name="imagedatadiscard-option"></a>ImageDataDiscard-Option

Dieser Parameter ist nur gültig, wenn die [CompressedDomainTranscode-Option](#compresseddomaintranscode-option) **TRUE** ist. andernfalls wird sie ignoriert. [ImageDataDiscard](#imagedatadiscard-option) gibt die Menge der Bilddaten an, die während einer komprimierten Domänentranscodierung verworfen werden sollen. Wenn das Bild einen verschachtelten Alphakanal enthält, gilt diese Datenverwerfung auch für den Alphakanal, mit den Ausnahmen, die weiter unten in diesem Abschnitt beschrieben werden.

Die folgenden Werte sind zulässig.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Es werden keine Bildfrequenzdaten verworfen.                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | Die FlexBits werden verworfen, wodurch die Qualität des transcodierten Bilds willkürlich reduziert wird, ohne die effektive Auflösung des Bilds zu ändern. Die genaue Verringerung der Dateigröße oder die spezifische Qualitätsreduzierung hängt von zahlreichen Faktoren ab und kann nicht angegeben oder vorhergesagt werden. Dieser Wert gibt einen Fehler zurück, wenn Sie ihn für einen überlappenden Alphakanal angeben.                                                    |
| 2     | Das HighPass-Frequenzdatenband wird verworfen (einschließlich flexBits), wodurch die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 4 reduziert wird. Die tatsächlichen Abmessungen des transcodierten Bilds bleiben gleich, verlieren jedoch alle Details in jedem 4x4-Pixelblock. Daher sollten Sie das transcodierte Bild bei jeder Decodierung entsprechend downsampling.                            |
| 3     | Sowohl die HighPass- als auch die LowPass-Frequenzband werden verworfen (einschließlich flexBits), wodurch die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 16 reduziert wird. Die tatsächlichen Abmessungen des transcodierten Bilds bleiben gleich, verlieren jedoch alle Details in jedem 16x16-Makroblock von Pixeln. Daher sollten Sie das transcodierte Bild bei jeder Decodierung entsprechend downsampling. |



 

Der Standardwert ist 0.

### <a name="alphadatadiscard-option"></a>AlphaDataDiscard-Option

Diese Option ist nur gültig, wenn die [CompressedDomainTranscode-Eigenschaft](#compresseddomaintranscode-option) **TRUE** ist und das Bild entweder einen planaren oder verschachtelten Alphakanal enthält. andernfalls wird sie ignoriert. Sie gibt die Menge der Alphafrequenzdaten an, die während einer komprimierten Domänentranscodierung verworfen werden sollen. Die folgenden Werte sind für einen planaren Alphakanal zulässig.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Es werden keine Bildfrequenzdaten verworfen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | Die FlexBits werden verworfen, wodurch die Qualität des planaren Alphakanals für das transcodierte Bild willkürlich reduziert wird, ohne die effektive Auflösung zu ändern. Die genaue Verringerung der Dateigröße oder die spezifische Qualitätsreduzierung hängt von zahlreichen Faktoren ab und kann nicht angegeben oder vorhergesagt werden.                                                                                                                                                                                                                                                |
| 2     | Das HighPass-Frequenzdatenband wird verworfen (einschließlich flexBits), wodurch die Auflösung des planaren Alphakanals für transcodierte Bilder in beiden Dimensionen um den Faktor 4 reduziert wird. Die tatsächlichen Abmessungen des transcodierten Bilds bleiben gleich, aber das Bild verliert alle planaren Alphakanaldetails in jedem 4x4-Pixelblock. Daher sollte das transcodierte Bild bei jeder Decodierung entsprechend heruntersamplingt werden. In der Regel sollten Sie diesen Wert nur festlegen, wenn Sie die ImageDataDiscard-Eigenschaft auf denselben Wert festlegen. |
| 3     | Sowohl die HighPass- als auch die LowPass-Frequenzband werden verworfen (einschließlich flexBits), wodurch die Auflösung des transcodierten Bilds in beiden Dimensionen um den Faktor 16 reduziert wird. Die tatsächlichen Abmessungen des transcodierten Bilds bleiben gleich, aber das Bild verliert alle Details in jedem 16x16-Makroblock von Pixeln. Daher sollte das transcodierte Bild bei jeder Decodierung entsprechend heruntersamplingt werden. In der Regel sollten Sie diesen Wert nur festlegen, wenn Sie die ImageDataDiscard-Eigenschaft auf denselben Wert festlegen.               |
| 4     | Der Alphakanal wird vollständig verworfen. Das Pixelformat des transcodierten Bilds wird geändert, um das Entfernen des Alphakanals widerzuspiegeln.                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Bei Bildern, die verschachtelte Alphakanäle enthalten, wird der Alphakanal gemäß dem Wert der ImageDataDiscard-Eigenschaft genauso wie die Bilddaten verarbeitet, sofern diese Eigenschaft nicht auf 4 festgelegt ist. Wenn diese Eigenschaft auf 4 festgelegt ist, wird der verschachtelte Alphakanal vollständig verworfen, und das Pixelformat des transcodierten Bilds wird entsprechend geändert.

Für dieses Feld gibt es keinen Standardwert.

### <a name="ignoreoverlap-option"></a>IgnoreOverlap-Option

Diese Option ist nur gültig, wenn die [CompressedDomainTranscode-Eigenschaft](#compresseddomaintranscode-option) **TRUE** ist und eine Unterbereichstranscodierung von genau einer oder mehreren Kacheln angefordert wird. Der Standardvorgang für eine Regionstranscodierung (oder -decodierung) besteht darin, den angeforderten Bereich um die umgebenden Pixel zu erweitern, die für die Überlappungsdecodierung der Bereichsränder erforderlich sind. Wenn dieser Parameter auf **TRUE** festgelegt ist, werden die umgebenden Pixel ignoriert, und nur die ausgewählten Kacheln werden extrahiert. Auch hier ist es erforderlich, dass der angeforderte Bereich genau mit den Koordinaten einer oder mehrerer Kacheln übereinstimmt. Wenn das Quellbild nicht gekachelt ist oder der angeforderte Bereich Teilkacheln angibt, wird dieser Parameter ignoriert.

Der Standardwert ist **FALSE**.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

### <a name="iwicbitmapsourcetransform-support"></a>IWICBitmapSourceTransform-Unterstützung

Zusätzlich zu den Schnittstellen, die als WIC-fähiger Codec erforderlich sind, unterstützt der native HD-Fotodecoder auch [**IWICBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) Die **IWICBitmapSourceTransform-Schnittstelle** bietet eine erweiterte Option zum Decodieren eines Bildbitstreams. Anstatt nur ein vollständiges Bild mithilfe von [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)zurückzugeben, aktiviert die **IWICBitmapSourceTransform-Schnittstelle** die folgenden Decoderoptionen.

-   Decodieren Sie einen rechteckigen Unterbereich des Bilds.
-   Decodieren in eine niedrigere Auflösung
-   Decodieren in ein anderes Pixelformat
-   Durchführen einer Transformation (Drehung/Flip) während der Decodierung

Der native HD Photo-Codec bietet die folgende Unterstützungsebene für die [**IWICBitmapSourceTransform-Schnittstelle.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)

### <a name="doessupporttransform"></a>DoesSupportTransform

Die native Implementierung unterstützt alle [**WICBitmapTransformOptions-Transformationen.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="getclosestsize"></a>GetClosestSize

Bei Anforderungen, die weniger als 1/2 der Dimension des Quellbilds in beiden Dimensionen sind, gibt HD Photo die nächstgrößerste ganzzahlige Bildgröße zurück, die durch den Faktor 2 gleichmäßig geteilt werden kann. Für alle anderen angeforderten Größen gibt HD Photo die ursprünglichen Bilddimensionen zurück.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

HD Photo gibt das Pixelformat des codierten Bilds zurück.

### <a name="copypixels"></a>Copypixels

HD Photo akzeptiert jeden vom [**WICRect-Parameter**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) angegebenen angeforderten Bereich und gibt diesen Teil des Bilds zurück.

Die Parameter *uiWidth* und *uiHeight* müssen Dimensionen angeben, die von der [**GetClosestSize-Funktion**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) zurückgegeben werden. Alle anderen Werte geben einen Fehler zurück.

Der *pguidDstFormat-Parameter* muss das von der [**GetClosestPixelFormat-Funktion**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) zurückgegebene Pixelformat angeben. Jeder andere Wert gibt einen Fehler zurück.

HD Photo akzeptiert jeden zulässigen Wert für den *dstTransform-Parameter.* Beachten Sie, dass sich die von WIC für diesen Parameter zulässigen Werte von den Werten unterscheiden, die von HD Photo für das Transformation-Metadatentag verwendet werden.

 

 
