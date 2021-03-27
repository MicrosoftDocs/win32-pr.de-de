---
description: Die folgende Liste enthält Beschreibungen der Eigenschaften Elemente, die von Windows GDI+ unterstützt werden.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Eigenschaften Element Beschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636122"
---
# <a name="property-item-descriptions"></a>Eigenschaften Element Beschreibungen

Die folgende Liste enthält Beschreibungen der Eigenschaften Elemente, die von Windows GDI+ unterstützt werden. Die Beschreibungen sind kurz und allgemein, sodass Sie auf eine Vielzahl von Bild Dateiformaten angewendet werden. Eine ausführliche Beschreibung der Verwendung eines Eigenschafts Elements in einem bestimmten Dateiformat finden Sie in der Spezifikation für dieses Dateiformat. Links zu mehreren Datei Spezifikationen und anderen Dokumenten, in denen Metadaten ausführlich beschrieben werden, finden Sie unter [Spezifikation von Image Dateiformaten](-gdiplus-constant-image-file-format-specifications.md).

Das EXIF-Format (austauschbar Image File) ist ein JEIDA-Standard (Electronic Electronic Industry Development Association), der vom Juni 1998 als Version 2,1 überarbeitet wurde. Teile der EXIF-Spezifikation werden mit der Berechtigung JEIDA verwendet.

## <a name="propertytaggpsver"></a>Propertytaggpsver

Version der Global Positionierungs Systems (GPS) IFD, die als 2.0.0.0 angegeben ist. Dieses Tag ist obligatorisch, wenn das propertytaggpsifd-Tag vorhanden ist. Wenn die Version 2.0.0.0 ist, ist der Tagwert 0x02000000.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x0000              |
| type  | Propertytagtypebyte |
| Anzahl | 4                   |



 

## <a name="propertytaggpslatituderef"></a>Propertytaggpslatituderef

Mit NULL beendete Zeichenfolge, die angibt, ob der Breitengrad "North" oder "South" ist. `N` Gibt die nördliche Breite an und `S` gibt den südlichen Breitengrad an.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x0001                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpslatitude"></a>Propertytaggpslatitude

Die Breitenkoordinate. Der Breitengrad wird als drei rationale Werte ausgedrückt, die den Grad, die Minuten und die Sekunden geben. Wenn Grad, Minuten und Sekunden ausgedrückt werden, ist das Format dd/1, mm/1, SS/1. Wenn Grad und Minuten verwendet werden und z. b. ein Bruchteil von Minuten bis zu zwei Dezimalstellen erhalten, ist das Format dd/1, MMMM/100, 0/1.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0002                  |
| type  | Propertytagtyperational |
| Anzahl | 3                       |



 

## <a name="propertytaggpslongituderef"></a>Propertytaggpslängs

Eine mit NULL endend beendete Zeichenfolge, die angibt, ob der Längengrad Ost-oder West-Längengrad ist. `E` Gibt den Ost-Längengrad an und `W` gibt den West Längengrad an.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x0003                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpslongitude"></a>Propertytaggpslängen Grad

Die Längenkoordinate. Der Längengrad wird als drei rationale Werte ausgedrückt, die den Grad, die Minuten und die Sekunden geben. Wenn Grad, Minuten und Sekunden ausgedrückt werden, lautet das Format DDD/1, mm/1, SS/1. Wenn Grad und Minuten verwendet werden und z. b. Bruchteile von Minuten bis zu zwei Dezimalstellen angegeben werden, lautet das Format DDD/1, MMMM/100, 0/1.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0004                  |
| type  | Propertytagtyperational |
| Anzahl | 3                       |



 

## <a name="propertytaggpsaltituderef"></a>Propertytaggpsaltituderef

Bezugs Höhe in Meter.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x0005              |
| type  | Propertytagtypebyte |
| Anzahl | 1                   |



 

## <a name="propertytaggpsaltitude"></a>Propertytaggpsaltitude

Die Höhe in Meter basierend auf der durch propertytaggpsaltituderef angegebenen Bezugs Höhe.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0006                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytaggpsgpstime"></a>Propertytaggpsgpstime

Zeit als koordinierte Weltzeit (UTC). Der Wert wird als drei rationale Zahlen ausgedrückt, die Stunde, Minute und Sekunde.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0007                  |
| type  | Propertytagtyperational |
| Anzahl | 3                       |



 

## <a name="propertytaggpsgpssatellites"></a>Propertytaggpsgpssatellites

Eine auf NULL endende Zeichenfolge, die die für Messungen verwendeten GPS-Satelliten angibt. Dieses Tag kann verwendet werden, um die ID-Nummer, den Winkel der Höhe, die Azimuth, SNR und weitere Informationen zu den einzelnen Satelliten anzugeben. Das Format ist nicht angegeben. Wenn der GPS-Empfänger nicht in der Lage ist, Messungen durchzusetzen, muss der Wert des Tags auf **null** festgelegt werden.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x0008                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytaggpsgpsstatus"></a>Propertytaggpsgpsstatus

Mit NULL beendete Zeichenfolge, die den Status des GPS-Empfängers angibt, wenn das Bild aufgezeichnet wird. `A` bedeutet, dass die Messung ausgeführt wird, und bedeutet, dass `V` die Messung Interoperabilität ist.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x0009                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpsgpsmeasuremode"></a>Propertytaggpsgpsmessremode

Mit NULL beendete Zeichenfolge, die den GPS-Mess Modus angibt. `2` Gibt die 2D-Messung an und `3` legt die 3D-Messung fest.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x000A                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpsgpsdop"></a>Propertytaggpsgpsdop

GPS-DOP (Daten Genauigkeits Grad). Während der 2D-Messung wird ein HDOP-Wert geschrieben, und bei der 3D-Messung wird ein PDOP-Wert geschrieben.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x000B                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytaggpsspeedref"></a>Propertytaggpsspeedref

Mit NULL endende Zeichenfolge, die die Einheit angibt, die zum Ausdrücken der Geschwindigkeit der Geschwindigkeit des GPS-Empfängers verwendet wird. `K`, `M` und `N` stellen Kilometer pro Stunde, Meilen pro Stunde bzw. Knoten dar.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x000C                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpsspeed"></a>Propertytaggpsspeed

Geschwindigkeit der GPS-Empfänger Bewegung.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x000D                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytaggpstrackref"></a>Propertytaggpstrackref

Mit NULL endende Zeichenfolge, die den Verweis zum Angeben der Richtung der GPS-Empfänger Bewegung angibt. `T` Gibt die tatsächliche Richtung an und `M` gibt die Magnet Richtung an.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x000e                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpstrack"></a>Propertytaggpstrack

Richtung der GPS-Empfänger Bewegung. Der Wertebereich liegt zwischen 0,00 und 359,99.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x000F                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytaggpsimgdirref"></a>Propertytaggpsimgdirref

Mit NULL beendete Zeichenfolge, die den Verweis auf die Richtung des Bilds angibt, wenn es aufgezeichnet wird. `T` Gibt die tatsächliche Richtung an und `M` gibt die Magnet Richtung an.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x0010                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpsimgdir"></a>Propertytaggpsimgdir

Richtung des Bilds, wenn es aufgezeichnet wurde. Der Wertebereich liegt zwischen 0,00 und 359,99.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0011                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytaggpsmapdatum"></a>Propertytaggpsmapdatum

Auf NULL endende Zeichenfolge, die geodätische Umfragedaten angibt, die vom GPS-Empfänger verwendet werden. Wenn die Umfragedaten auf Japan beschränkt sind, ist der Wert dieses Tags `TOKYO` oder `WGS-84` .



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x0012                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytaggpsdestlatref"></a>Propertytaggpsdestlatref

Eine mit NULL endend beendete Zeichenfolge, die angibt, ob der Breitengrad des Ziel Punkts Nord-oder Südbreite ist. `N` Gibt die nördliche Breite an und `S` gibt den südlichen Breitengrad an.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x0013                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpsdestlat"></a>Propertytaggpsdestlat

Der Breitengrad des Ziel Punkts. Der Breitengrad wird als drei rationale Werte ausgedrückt, die den Grad, die Minuten und die Sekunden geben. Wenn Grad, Minuten und Sekunden ausgedrückt werden, ist das Format dd/1, mm/1, SS/1. Wenn Grad und Minuten verwendet werden und z. b. ein Bruchteil von Minuten bis zu zwei Dezimalstellen erhalten, ist das Format dd/1, MMMM/100, 0/1.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0014                  |
| type  | Propertytagtyperational |
| Anzahl | 3                       |



 

## <a name="propertytaggpsdestlongref"></a>Propertytaggpsdestlongref

Eine mit NULL endend beendete Zeichenfolge, die angibt, ob der Längengrad des Zielpunkts Ost-oder West-Längengrad ist. `E` Gibt den Ost-Längengrad an und `W` gibt den West Längengrad an.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x0015                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpsdestlong"></a>Propertytaggpsdestlong

Längengrad des Ziel Punkts. Der Längengrad wird als drei rationale Werte ausgedrückt, die den Grad, die Minuten und die Sekunden geben. Wenn Grad, Minuten und Sekunden ausgedrückt werden, lautet das Format DDD/1, mm/1, SS/1. Wenn Grad und Minuten verwendet werden und z. b. Bruchteile von Minuten bis zu zwei Dezimalstellen angegeben werden, lautet das Format DDD/1, MMMM/100, 0/1.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0016                  |
| type  | Propertytagtyperational |
| Anzahl | 3                       |



 

## <a name="propertytaggpsdestbearref"></a>Propertytaggpsdestbearref

Mit NULL endende Zeichenfolge, die den Verweis angibt, mit dem das-Verhalten an den Zielpunkt übertragen wird. `T` Gibt die tatsächliche Richtung an und `M` gibt die Magnet Richtung an.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x0017                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpsdestbear"></a>Propertytaggpsdestbear

Die auf den Zielpunkt zu übertragen. Der Wertebereich liegt zwischen 0,00 und 359,99.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0018                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytaggpsdestdistref"></a>Propertytaggpsdestdistref

Mit NULL endende Zeichenfolge, die die Einheit angibt, mit der die Entfernung zum Zielpunkt ausgedrückt wird. "K", "M" und "N" stellen jeweils die Kilometer, Meilen und Knoten dar.



| Eigenschafts Informationen | Wert |
|-------|--------------------------------------------|
| Tag   | 0x0019                                     |
| type  | Propertytagtybäuercii                       |
| Anzahl | 2 (ein Zeichen plus das NULL-Terminator) |



 

## <a name="propertytaggpsdestdist"></a>Propertytaggpsdestdist

Entfernung zum Zielpunkt.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x001a                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagnewsubfiletype"></a>Propertytagnewsubfiletype

Der Typ der Daten in einer unter Datei.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x00fe              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagsubfiletype"></a>Propertytagsubfiletype

Der Typ der Daten in einer unter Datei.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x00FF               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagimagewidth"></a>PropertyTagImageWidth

Anzahl der Pixel pro Zeile.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0100                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagimageheight"></a>Propertytagimageheight

Anzahl der Pixel Zeilen.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0101                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagbitspersample"></a>Propertytagbitspersample

Anzahl der Bits pro Farbkomponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0102                                   |
| type  | Propertytagtypeshort                     |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagcompression"></a>Propertytagcompression

Das für die Bilddaten verwendete Komprimierungs Schema.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0103               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagphotometricinterp"></a>Propertytagphotomepackcinterp

Wie Pixeldaten interpretiert werden.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0106               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthreshholding"></a>Propertytagschwelle

Technik, die verwendet wird, um von grauen Pixeln in schwarze und weiße Pixel zu konvertieren.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0107               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagcellwidth"></a>Propertytagcellwidth

Breite der Dithering-oder Halftoning-Matrix.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0108               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagcellheight"></a>Propertytagcellheight

Höhe der Dithering-oder Halftoning-Matrix.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0109               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagfillorder"></a>Propertytagfillorder

Logische Reihenfolge von Bits in einem Byte.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x010a               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagdocumentname"></a>Propertytagdocumentname

Mit NULL beendete Zeichenfolge, die den Namen des Dokuments angibt, aus dem das Bild gescannt wurde.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x010d                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagimagedescription"></a>Propertytagimagedescription

Mit NULL beendete Zeichenfolge, die den Titel des Bilds angibt.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x010e                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagequipmake"></a>Propertytagequipmake

Mit NULL endende Zeichenfolge, die den Hersteller der Ausrüstung angibt, die zum Aufzeichnen des Bilds verwendet wird.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x010F                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagequipmodel"></a>Propertytagequipmodel

Mit NULL endende Zeichenfolge, die den Modellnamen oder die Modellnummer der Ausrüstung angibt, die zum Aufzeichnen des Bilds verwendet wird.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x0110                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagstripoffsets"></a>Propertytagstripoffsets

Für jeden Strip den Byte Offset dieses Streifens. Siehe auch [propertytagrowsperstrip](#propertytagrowsperstrip) und [propertytagstripbytescount](#propertytagstripbytescount).



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0111                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | Anzahl von Bändern                            |



 

## <a name="propertytagorientation"></a>Propertytagorientation

Bild Ausrichtung wird in Form von Zeilen und Spalten angezeigt.



Tag

0x0112

type

Propertytagtypeshort

Anzahl

1

1: die Zeile nullten befindet sich am oberen Rand des visuellen Bilds, und die Spalte nullten ist das visuelle Element auf der linken Seite. 2: die Zeile nullten befindet sich am visuellen oberen Rand des Bilds, und die Spalte nullten ist die visuelle Rechte Seite. 3: die Zeile nullten befindet sich am visuellen Rand des Bilds, und die nullten-Spalte ist die visuelle Rechte Seite. 4-die Zeile nullten befindet sich am visuellen Rand des Bilds, und die nullten-Spalte ist die visuelle Darstellung Links. 5-die Zeile nullten ist das visuelle Element auf der linken Seite des Bilds, und die Spalte nullten ist der visuelle obere Rand. 6-die Zeile nullten ist die visuelle Rechte Seite des Bilds, und die nullten-Spalte ist der visuelle obere Rand. 7-die Zeile nullten ist die visuelle Rechte Seite des Bilds, und die Spalte nullten ist das visuelle Element unten. 8: die Zeile nullten ist das visuelle Element auf der linken Seite des Bilds, und die Spalte nullten ist das visuelle Element unten.



 

## <a name="propertytagsamplesperpixel"></a>Propertytagsamplesperpixel

Anzahl der Farbkomponenten pro Pixel.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0115               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagrowsperstrip"></a>Propertytagrowsperstrip

Anzahl der Zeilen pro Strip. Siehe auch [propertytagstripbytescount](#propertytagstripbytescount) und [propertytagstripoffsets](#propertytagstripoffsets).



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0116                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagstripbytescount"></a>Propertytagstripbytescount

Für jeden Strip die Gesamtzahl der Bytes in diesem Strip.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0117                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | Anzahl von Bändern                            |



 

## <a name="propertytagminsamplevalue"></a>Propertytagminsamplevalue

Für jede Farbkomponente der minimale Wert, der dieser Komponente zugewiesen ist. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0118                                   |
| type  | Propertytagtypeshort                     |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagmaxsamplevalue"></a>Propertytagmaxsamplevalue

Für jede Farbkomponente der Maximalwert, der dieser Komponente zugewiesen ist. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0119                                   |
| type  | Propertytagtypeshort                     |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagxresolution"></a>Propertytagxresolution

Die Anzahl der Pixel pro Einheit in der Bild breiten Richtung (x). Die Einheit wird durch [propertytagresolutionunit](#propertytagresolutionunit)angegeben.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x011a                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagyresolution"></a>Propertytagyresolution

Anzahl der Pixel pro Einheit in der Bildhöhe (y). Die Einheit wird durch [propertytagresolutionunit](#propertytagresolutionunit)angegeben.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x011b                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagplanarconfig"></a>Propertytagplanarconfig

Gibt an, ob Pixel Komponenten im segmentierten oder planaren Format aufgezeichnet werden.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x011c               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagpagename"></a>Propertytagpagename

Mit NULL beendete Zeichenfolge, die den Namen der Seite angibt, von der das Bild gescannt wurde.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x011d                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagxposition"></a>Propertytagxposition

Offset von der linken Seite der Seite auf die linke Seite des Bilds. Die Maßeinheit wird durch [propertytagresolutionunit](#propertytagresolutionunit)angegeben.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x011e                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagyposition"></a>Propertytagyposition

Offset vom oberen Rand der Seite bis zum oberen Rand des Bilds. Die Maßeinheit wird durch [propertytagresolutionunit](#propertytagresolutionunit)angegeben.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x011f                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagfreeoffset"></a>Propertytagfreoffset

Für jede Zeichenfolge von zusammenhängenden nicht verwendeten Bytes der Byte Offset dieser Zeichenfolge.



| Eigenschafts Informationen | Wert |
|------|---------------------|
| Tag  | 0x0120              |
| type | Propertytagtypelong |



 

## <a name="propertytagfreebytecounts"></a>Propertytagfrebytecounts

Die Anzahl von Bytes in dieser Zeichenfolge für jede Zeichenfolge von zusammenhängenden nicht verwendeten Bytes.



| Eigenschafts Informationen | Wert |
|-------|-----------------------------------------------|
| Tag   | 0x0121                                        |
| type  | Propertytagtypelong                           |
| Anzahl | Anzahl von Zeichen folgen aus zusammenhängenden nicht verwendeten Bytes. |



 

## <a name="propertytaggrayresponseunit"></a>Propertytaggrayresponseunit

Genauigkeit der Zahl, die durch propertytaggrayresponsecurve angegeben wird. 1 gibt Zehntel an, 2 gibt Hundertstel an, 3 gibt Tausendstel usw. an.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0122               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytaggrayresponsecurve"></a>Propertytaggrayresponsecurve

Die optische Dichte dieses Pixel Werts für jeden möglichen Pixelwert in einem Graustufenbild.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------|
| Tag   | 0x0123                          |
| type  | Propertytagtypeshort            |
| Anzahl | Anzahl möglicher Pixelwerte |



 

## <a name="propertytagt4option"></a>PropertyTagT4Option

Ein Satz von Flags, die sich auf die T4-Codierung beziehen.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x0124              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagt6option"></a>PropertyTagT6Option

Ein Satz von Flags, die sich auf die T6-Codierung beziehen.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x0125              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagresolutionunit"></a>Propertytagresolutionunit

Maßeinheit für die horizontale Auflösung und die vertikale Auflösung.



Tag

0x0128

type

Propertytagtypeshort

Anzahl

1

2 Zoll, 3 Zentimeter



 

## <a name="propertytagpagenumber"></a>Propertytagpagenumber

Die Seitenzahl der Seite, von der das Bild gescannt wurde.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0129               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagtransferfunction"></a>Propertytagtransferfunction

Tabellen, die Übertragungsfunktionen für das Image angeben.



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------------------|
| Tag   | 0x012d                                               |
| type  | Propertytagtypeshort                                 |
| Anzahl | Die Gesamtanzahl der für die Tabellen erforderlichen 16-Bit-Wörter. |



 

## <a name="propertytagsoftwareused"></a>Propertytagsoftwareused

Mit NULL endende Zeichenfolge, die den Namen und die Version der Software oder Firmware des Geräts angibt, das zum Generieren des Images verwendet wurde.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x0131                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagdatetime"></a>Propertytagdatetime

Datum und Uhrzeit der Erstellung des Bilds.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0132               |
| type  | Propertytagtybäuercii |
| Anzahl | 20                   |



 

## <a name="propertytagartist"></a>Propertytagartist

Mit NULL beendete Zeichenfolge, die den Namen der Person angibt, die das Image erstellt hat.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x013b                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytaghostcomputer"></a>Propertytaghostcomputer

Mit NULL endende Zeichenfolge, die den Computer und/oder das Betriebssystem angibt, mit dem das Image erstellt wird.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x013c                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagpredictor"></a>Propertytagvorhertor

Der Typ des Vorhersage Schemas, das auf die Bilddaten angewendet wurde, bevor das Codierungsschema angewendet wurde.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x013d               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagwhitepoint"></a>Propertytagwhitepoint

Die Chromatizität des weißen Punkts des Bilds.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x013e                  |
| type  | Propertytagtyperational |
| Anzahl | 2                       |



 

## <a name="propertytagprimarychromaticities"></a>Propertytagprimarychromaticities

Für jede der drei Primärfarben im Bild die Chromatizität dieser Farbe.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x013f                  |
| type  | Propertytagtyperational |
| Anzahl | 6                       |



 

## <a name="propertytagcolormap"></a>Propertytagcolormap

Farbpalette (Nachschlage Tabelle) für ein palettenindiziertes Bild.



| Eigenschafts Informationen | Wert |
|-------|-------------------------------------------------|
| Tag   | 0x0140                                          |
| type  | Propertytagtypeshort                            |
| Anzahl | Die Anzahl der für die Palette erforderlichen 16-Bit-Wörter. |



 

## <a name="propertytaghalftonehints"></a>Propertytaghalftonehints

Von der Funktion "Halbton" verwendete Informationen



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0141               |
| type  | Propertytagtypeshort |
| Anzahl | 2                    |



 

## <a name="propertytagtilewidth"></a>Propertytagtilewidth

Anzahl der Pixel Spalten in den einzelnen Kacheln.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0142                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagtilelength"></a>Propertytagtilelength

Anzahl der Pixel Zeilen in jeder Kachel.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0143                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagtileoffset"></a>Propertytagtileoffset

Für jede Kachel der Byte Offset der Kachel.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x0144              |
| type  | Propertytagtypelong |
| Anzahl | Anzahl von Kacheln     |



 

## <a name="propertytagtilebytecounts"></a>Propertytagtilebytecounts

Für jede Kachel die Anzahl der Bytes in der Kachel.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0145                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | Anzahl von Kacheln                             |



 

## <a name="propertytaginkset"></a>Propertytaginkset

Eine Reihe von Farben, die in einem getrennten Bild verwendet werden.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x014c               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytaginknames"></a>Propertytaginknames

Sequenz von verketteten, auf NULL endenden Zeichen folgen, die die Namen der in einem getrennten Bild verwendeten Farben angeben.



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------------------------------------|
| Tag   | 0x014d                                                                 |
| type  | Propertytagtybäuercii                                                   |
| Anzahl | Gesamtlänge der Sequenz von Zeichen folgen einschließlich der NULL-Abschluss Zeichen |



 

## <a name="propertytagnumberofinks"></a>Propertytagnumofinert

Anzahl der Farben.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x014e               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagdotrange"></a>Propertytagdotrange

Farbkomponenten Werte, die einem Punkt von 0 Prozent und einem Punkt von 100 Prozent entsprechen.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x0150                                      |
| type  | Propertytagtypebyte oder propertytagtypeshort |
| Anzahl | 2 oder 2 × propertytagsamplesperpixel           |



 

## <a name="propertytagtargetprinter"></a>Propertytagtargetprinter

Mit NULL beendete Zeichenfolge, die die vorgesehene Druckumgebung beschreibt.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x0151                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagextrasamples"></a>Propertytagextrasamples

Anzahl der zusätzlichen Farbkomponenten. Beispielsweise kann eine zusätzliche Komponente einen Alpha-Wert enthalten.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0152               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagsampleformat"></a>Propertytagsampleformat

Für jede Farbkomponente das numerische Format (unsigned, signed, Floating Point) dieser Komponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0153                                   |
| type  | Propertytagtypeshort                     |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagsminsamplevalue"></a>Propertytagsminsamplevalue

Für jede Farbkomponente der minimale Wert dieser Komponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|-----------------------------------------------------|
| Tag   | 0x0154                                              |
| type  | Der Typ, der am besten mit den Pixel Komponenten Daten übereinstimmt. |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel            |



 

## <a name="propertytagsmaxsamplevalue"></a>Propertytagsmaxsamplevalue

Der maximale Wert dieser Komponente für jede Farbkomponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|-----------------------------------------------------|
| Tag   | 0x0155                                              |
| type  | Der Typ, der am besten mit den Pixel Komponenten Daten übereinstimmt. |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel            |



 

## <a name="propertytagtransferrange"></a>Propertytagtransferrange

Tabelle mit Werten, die den Bereich der Übertragungsfunktion erweitern.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0156               |
| type  | Propertytagtypeshort |
| Anzahl | 6                    |



 

## <a name="propertytagjpegproc"></a>Propertytagjpgproc

JPEG-Komprimierungs Vorgang.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0200               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagjpeginterformat"></a>Propertytagjpeer ginterformat

Offset bis zum Anfang eines JPEG-Bitstreams.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x0201              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagjpeginterlength"></a>Propertytagjpeer-interlength

Länge des JPEG-Bitstreams in Bytes.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x0202              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagjpegrestartinterval"></a>Propertytagjggrestartinterval

Länge des Neustart Intervalls.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0203               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagjpeglosslesspredictors"></a>Propertytagjpeer glosslesendiktoren

Für jede Farbkomponente ein verlustfreier Wert für die Vorhersage der Komponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0205                                   |
| type  | Propertytagtypeshort                     |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagjpegpointtransforms"></a>Propertytagjpgpointtransformationen

Für jede Farbkomponente ein Wert für die Punkt Transformation für diese Komponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0206                                   |
| type  | Propertytagtypeshort                     |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagjpegqtables"></a>Propertytagjpgqtables

Für jede Farbkomponente der Offset zur quantifizierungstabelle für diese Komponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0207                                   |
| type  | Propertytagtypelong                      |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagjpegdctables"></a>Propertytagjpeer dsctables

Für jede Farbkomponente der Offset zur DC-Huffman-Tabelle (oder Verlust lose Huffman-Tabelle) für diese Komponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0208                                   |
| type  | Propertytagtypelong                      |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagjpegactables"></a>Propertytagjpeer-Tabellen

Für jede Farbkomponente der Offset zur AC-Huffman-Tabelle für diese Komponente. Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------|
| Tag   | 0x0209                                   |
| type  | Propertytagtypelong                      |
| Anzahl | Anzahl von Stichproben (Komponenten) pro Pixel |



 

## <a name="propertytagycbcrcoefficients"></a>Propertytagycbcrkoefficients

Koeffizienten für die Transformation von RGB zu YCbCr-Bilddaten.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0211                  |
| type  | Propertytagtyperational |
| Anzahl | 3                       |



 

## <a name="propertytagycbcrsubsampling"></a>Propertytagycbcrsubsampling

Das Stichproben Verhältnis von Chrominanz-Komponenten im Verhältnis zur Leuchtkraft Komponente.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0212               |
| type  | Propertytagtypeshort |
| Anzahl | 2                    |



 

## <a name="propertytagycbcrpositioning"></a>Propertytagycbcrpositionierung

Die Position von Chrominanz-Komponenten im Verhältnis zur Leuchtkraft Komponente.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x0213               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagrefblackwhite"></a>Propertytagref BlackWhite

Verweis-Schwarzpunkt Wert und Referenz-weiß Punkt Wert.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0214                  |
| type  | Propertytagtyperational |
| Anzahl | 6                       |



 

## <a name="propertytaggamma"></a>Propertytaggamma

An das Bild angefügter Gamma Wert. Der Gamma Wert wird als eine rationale Zahl ( **Long of Long**) mit einem Zähler von 100000 gespeichert. Beispielsweise wird der Gamma Wert 2,2 als Paar (100000, 45455) gespeichert.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x0301                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagiccprofiledescriptor"></a>Propertytagiccprofiledescriptor

Mit NULL beendete Zeichenfolge, die ein ICC-Profil identifiziert.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x0302                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagsrgbrenderingintent"></a>Propertytagsrgbrenderingintent

Gibt an, wie das Bild gemäß der Definition durch das International Color Consortium (ICC) angezeigt werden soll. Wenn ein GDI+-  [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt erstellt wird, wobei der *useembeddebug* -Parameter auf **true** festgelegt ist, wird das Bild von GDI+ entsprechend der angegebenen renderingabsicht gerendert. Die Absicht kann auf "perperell", eine relative farbige Metrik, Sättigung oder absolute farbige Metrik festgelegt werden.

-   Die für Fotos geeignete perzeptive Absicht bietet eine gute Anpassung an die Anzeigegeräte Palette auf Kosten der farmetriegenauigkeit.
-   Die relative Farbe für farbige Metriken eignet sich für Bilder (z. b. Logos), für die eine Farbdarstellung in Bezug auf den weißen Punkt des Anzeige Geräts erforderlich ist.
-   Die Absicht, die sich für Diagramme und Diagramme eignet, behält die Sättigung auf Kosten von Hue und Helligkeit bei.
-   Die absolute farbige Metrik-Absicht eignet sich für Beweise (Vorschau der für ein anderes Anzeigegerät vorgesehenen Bilder), die eine Beibehaltung absoluter farmetriedaten erfordern.



Tag

0x0303

type

BYTE

Anzahl

1

0-perzeptive 1-relative farbige Metrik 2-Sättigung 3-absolute farbige Metrik



 

## <a name="propertytagimagetitle"></a>Propertytagimagetitle

Mit NULL beendete Zeichenfolge, die den Titel des Bilds angibt.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x0320                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagresolutionxunit"></a>Propertytagresolutionxunit

Einheiten, in denen die horizontale Auflösung angezeigt werden soll.



Tag

0x5001

type

Propertytagtypeshort

Anzahl

1

1-Pixel pro Zoll, 2 Pixel pro Zentimeter



 

## <a name="propertytagresolutionyunit"></a>Propertytagresolutionyunit

Einheiten, in denen die vertikale Auflösung angezeigt werden soll.



Tag

0x5002

type

Propertytagtypeshort

Anzahl

1

1-Pixel pro Zoll, 2 Pixel pro Zentimeter



 

## <a name="propertytagresolutionxlengthunit"></a>Propertytagresolutionxlängen Unit

Einheiten, in denen die Bildbreite angezeigt werden soll.



Tag

0x5003

type

Propertytagtypeshort

Anzahl

1

1-Zoll-2-Zentimeter 3-Punkte 4-Picas 5-Spalten



 

## <a name="propertytagresolutionylengthunit"></a>Propertytagresolutionyverlängert-Einheit

Einheiten, in denen die Bildhöhe angezeigt werden soll.



Tag

0x5004

type

Propertytagtypeshort

Anzahl

1

1-Zoll-2-Zentimeter 3-Punkte 4-Picas 5-Spalten



 

## <a name="propertytagprintflags"></a>Propertytagprintflags

Sequenz von booleschen 1-Byte-Werten, die Druckoptionen angeben.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5005               |
| type  | Propertytagtybäuercii |
| Anzahl | Anzahl von Flags      |



 

## <a name="propertytagprintflagsversion"></a>Propertytagprintflagsversion

Versionsflags-Version.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5006               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagprintflagscrop"></a>Propertytagprintflagscrop

Druckflags Zentrierungs Markierungen zentrieren.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5007              |
| type  | Propertytagtypebyte |
| Anzahl | 1                   |



 

## <a name="propertytagprintflagsbleedwidth"></a>Propertytagprintflagsbleedwidth

Die ausgabenflags haben die Breite



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5008              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a>Propertytagprintflagsbleedwidthscale

Die ausdruckflags haben die Breite skaliert.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5009               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytaghalftonelpi"></a>Propertytaghalftonelpi

Bildschirm Frequenz von frei Hand Eingaben in Zeilen pro Zoll.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x500a                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytaghalftonelpiunit"></a>Propertytaghalftonelpiunit

Einheiten für die Bildschirm Frequenz.



Tag

0x500.000 b

type

Propertytagtypeshort

Anzahl

1

1-Zeilen pro Zoll 2-Zeilen pro Zentimeter



 

## <a name="propertytaghalftonedegree"></a>Propertytaghalftonedegree

Der Winkel für den Bildschirm.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x500.000                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytaghalftoneshape"></a>Propertytaghalftoneshape

Die Form der halbftone-Punkte.



Tag

0x500.000 d

type

Propertytagtypeshort

Anzahl

1

0-Runde 1-Ellipse 2-Zeile 3-quadratisches 4-Kreuz 6-Diamant



 

## <a name="propertytaghalftonemisc"></a>Propertytaghalftonemisc

Sonstige Informationen.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x500e              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytaghalftonescreen"></a>Propertytaghalftonescreen

Boolescher Wert, der angibt, ob die Standard Bildschirme des Druckers verwendet werden sollen.



Tag

0x500.000 f

type

Propertytagtypebyte

Anzahl

1

1. verwenden Sie die Standard Bildschirme von Druckern 2.



 

## <a name="propertytagjpegquality"></a>Propertytagjpgquality

Privates Tag, das vom Adobe Photoshop-Format verwendet wird. Nicht für die öffentliche Verwendung.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5010               |
| type  | Propertytagtypeshort |
| Anzahl | Any                  |



 

## <a name="propertytaggridsize"></a>Propertytaggridsize

Informations Block zu Raster und Handbüchern.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0x5011                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | Any                      |



 

## <a name="propertytagthumbnailformat"></a>Propertytagthumbnailformat

Das Format des Miniatur Bilds.



Tag

0x5012

type

Propertytagtypelong

Anzahl

1

0-Rohdaten RGB 1-JPEG



 

## <a name="propertytagthumbnailwidth"></a>Propertytagthumbnailwidth

Breite des Miniatur Bilds in Pixel.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5013              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagthumbnailheight"></a>Propertytagthumbnailheight

Höhe des Miniatur Bilds in Pixel.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5014              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagthumbnailcolordepth"></a>Propertytagthumbnailcolortiefe

Bits pro Pixel (BPP) für das Miniaturbild.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5015               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailplanes"></a>Propertytagthumbnailplane

Anzahl von Farbebenen für das Miniaturbild.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5016               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailrawbytes"></a>Propertytagthumbnailrawbytes

Byte Offset zwischen Zeilen von Pixeldaten.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5017              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagthumbnailsize"></a>Propertytagthumbnailsize

Gesamtgröße (in Bytes) des Miniatur Bilds.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5018              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagthumbnailcompressedsize"></a>Propertytagthumbnailcompressedsize

Komprimierte Größe (in Bytes) des Miniatur Bilds.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5019              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagcolortransferfunction"></a>Propertytagcolortransferfunction

Tabelle mit Werten, die Farb Übertragungsfunktionen angeben.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0x501a                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | Any                      |



 

## <a name="propertytagthumbnaildata"></a>Propertytagthumbnaildata

Unformatierte Miniatur Ansichts Bits im JPEG-oder RGB-Format Hängt von propertytagthumbnailformat ab.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x501b              |
| type  | Propertytagtypebyte |
| Anzahl | Variable            |



 

## <a name="propertytagthumbnailimagewidth"></a>PropertyTagThumbnailImageWidth

Anzahl der Pixel pro Zeile in der Miniaturansicht.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x5020                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagthumbnailimageheight"></a>Propertytagthumbnailimageheight

Anzahl der Pixel Zeilen in der Miniaturansicht.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x5021                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagthumbnailbitspersample"></a>Propertytagthumbnailbitspersample

Anzahl der Bits pro Farbkomponente im Miniaturbild. Siehe auch [propertytagthumbnailsamplesperpixel](#propertytagthumbnailsamplesperpixel).



| Eigenschafts Informationen | Wert |
|-------|-----------------------------------------------------------------|
| Tag   | 0x5022                                                          |
| type  | Propertytagtypeshort                                            |
| Anzahl | Anzahl der Stichproben (Komponenten) pro Pixel im Miniaturbild |



 

## <a name="propertytagthumbnailcompression"></a>Propertytagthumbnailcompression

Komprimierungs Schema für Miniaturbild Daten.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5023               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a>Propertytagthumbnailphotomezcinterp

Wie Miniatur Ansichts Pixeldaten interpretiert werden.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5024               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailimagedescription"></a>Propertytagthumbnailimagedescription

Mit NULL beendete Zeichenfolge, die den Titel des Bilds angibt.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x5025                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagthumbnailequipmake"></a>Propertytagthumbnailequipmake

Mit NULL endende Zeichenfolge, die den Hersteller der Ausrüstung angibt, die zum Aufzeichnen des Miniatur Bilds verwendet wird.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x5026                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagthumbnailequipmodel"></a>Propertytagthumbnailequipmodel

Mit NULL endende Zeichenfolge, die den Modellnamen oder die Modellnummer der Ausrüstung angibt, die zum Aufzeichnen des Miniatur Bilds verwendet wird.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x5027                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagthumbnailstripoffsets"></a>Propertytagthumbnailstripoffsets

Der Byte Offset dieses Streifens für jeden Strip des Miniatur Bilds. Siehe auch [propertytagthumbnailrowsperstrip](#propertytagthumbnailrowsperstrip) und [propertytagthumbnailstripbytescount](#propertytagthumbnailstripbytescount).



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x5028                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | Anzahl von Bändern                            |



 

## <a name="propertytagthumbnailorientation"></a>Propertytagthumbnailorientation

Ausrichtung von Miniaturbildern in Bezug auf Zeilen und Spalten. Siehe auch [propertytagorientation](#propertytagorientation).



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5029               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a>Propertytagthumbnailsamplesperpixel

Anzahl der Farbkomponenten pro Pixel in der Miniaturansicht.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x502a               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a>Propertytagthumbnailrowsperstrip

Anzahl der Zeilen pro Strip in der Miniaturansicht. Siehe auch [propertytagthumbnailstripbytescount](#propertytagthumbnailstripbytescount) und [propertytagthumbnailstripoffsets](#propertytagthumbnailstripoffsets).



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x502b                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a>Propertytagthumbnailstripbytescount

Die Gesamtanzahl der Bytes in diesem Strip für jeden Miniaturbild Streifen.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0x502c                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | Anzahl der Bänder im Miniaturbild     |



 

## <a name="propertytagthumbnailresolutionx"></a>Propertytagthumbnailresolutionx

Auflösung von Miniaturansichten in der breiten Richtung. Die Auflösungs Einheit wird in [propertytagthumbnailresolutionunit](#propertytagthumbnailresolutionunit)angegeben.



| Eigenschafts Informationen | Wert |
|-----|--------|
| Tag | 0x502d |



 

## <a name="propertytagthumbnailresolutiony"></a>Propertytagthumbnailresolutiony

Miniatur Ansichts Auflösung in der höhenrichtung. Die Auflösungs Einheit wird in [propertytagthumbnailresolutionunit](#propertytagthumbnailresolutionunit)angegeben.



| Eigenschafts Informationen | Wert |
|-----|--------|
| Tag | 0x502e |



 

## <a name="propertytagthumbnailplanarconfig"></a>Propertytagthumbnailplanarconfig

Gibt an, ob Pixel Komponenten in der Miniaturansicht im segmentierten oder planaren Format aufgezeichnet werden. Siehe auch [propertytagplanarconfig](#propertytagplanarconfig).



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x502f               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailresolutionunit"></a>Propertytagthumbnailresolutionunit

Maßeinheit für die horizontale Auflösung und die vertikale Auflösung des Miniatur Bilds. Siehe auch [propertytagresolutionunit](#propertytagresolutionunit).



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5030               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailtransferfunction"></a>Propertytagthumbnailtransferfunction

Tabellen, die Übertragungsfunktionen für das Miniaturbild angeben. Siehe auch [propertytagtransferfunction](#propertytagtransferfunction).



| Eigenschafts Informationen | Wert |
|-------|------------------------------------------------------|
| Tag   | 0x5031                                               |
| type  | Propertytagtypeshort                                 |
| Anzahl | Die Gesamtanzahl der für die Tabellen erforderlichen 16-Bit-Wörter. |



 

## <a name="propertytagthumbnailsoftwareused"></a>Propertytagthumbnailsoftwareused

Mit NULL endende Zeichenfolge, die den Namen und die Version der Software oder Firmware des Geräts angibt, das zum Generieren des Miniatur Bilds verwendet wird.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x5032                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagthumbnaildatetime"></a>Propertytagthumbnaildatetime

Datum und Uhrzeit der Erstellung des Miniatur Bilds. Siehe auch [propertytagdatetime](#propertytagdatetime).



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5033               |
| type  | Propertytagtybäuercii |
| Anzahl | 20                   |



 

## <a name="propertytagthumbnailartist"></a>Propertytagthumbnailartist

Mit NULL beendete Zeichenfolge, die den Namen der Person angibt, die das Miniaturbild erstellt hat.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x5034                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagthumbnailwhitepoint"></a>Propertytagthumbnailwhitepoint

Die Chromatizität des weißen Punkts des Miniatur Bilds. Siehe auch [propertytagwhitepoint](#propertytagwhitepoint).



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x5035 angezeigt                  |
| type  | Propertytagtyperational |
| Anzahl | 2                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a>Propertytagthumbnailprimarychromaticities

Für jede der drei Primärfarben im Miniatur Ansichts Bild die Chromatizität dieser Farbe. Siehe auch [propertytagprimarychromaticities](#propertytagprimarychromaticities).



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x5036                  |
| type  | Propertytagtyperational |
| Anzahl | 6                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a>Propertytagthumbnailycbcrkoefficients

Koeffizienten für die Transformation von RGB zu YCbCr-Daten für das Miniaturbild. Siehe auch [propertytagycbcrkoefficients](#propertytagycbcrcoefficients).



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x5037                  |
| type  | Propertytagtyperational |
| Anzahl | 3                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a>Propertytagthumbnailycbcrsubsampling

Das Stichproben Verhältnis von Chrominanz-Komponenten in Relation zur Leuchtkraft Komponente für das Miniaturbild. Siehe auch [propertytagycbcrsubsampling](#propertytagycbcrsubsampling).



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5038               |
| type  | Propertytagtypeshort |
| Anzahl | 2                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a>Propertytagthumbnailycbcrpositionierung

Die Position von Chrominanz-Komponenten in Bezug auf die Leuchtkraft Komponente für das Miniaturbild. Siehe auch [propertytagycbcrpositionierung](#propertytagycbcrpositioning).



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5039               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a>Propertytagthumbnailref BlackWhite

Verweis-Schwarzpunkt Wert und Referenz-weiß Punkt Wert für das Miniaturbild. Siehe auch [propertytagref BlackWhite](#propertytagrefblackwhite).



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x503a                  |
| type  | Propertytagtyperational |
| Anzahl | 6                       |



 

## <a name="propertytagthumbnailcopyright"></a>Propertytagthumbnailcopyright

Mit NULL beendete Zeichenfolge, die Copyright Informationen für das Miniaturbild enthält.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x503b                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagluminancetable"></a>Propertytagluminancetable

Leuchtkraft Tabelle. Die Tabelle "Leuchtkraft" und die Tabelle Chrominanz werden verwendet, um die JPEG-Qualität zu steuern. Eine gültige Tabelle "Leuchtkraft" oder "Chrominanz" weist 64 Einträge vom Typ "propertytagtypeshort" auf. Wenn ein Bild entweder eine "Leuchtkraft"-Tabelle oder eine Chrominanz-Tabelle enthält, muss es beide Tabellen aufweisen.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5090               |
| type  | Propertytagtypeshort |
| Anzahl | 64                   |



 

## <a name="propertytagchrominancetable"></a>Propertytagchrominancetable

Chrominance-Tabelle. Die Tabelle "Leuchtkraft" und die Tabelle Chrominanz werden verwendet, um die JPEG-Qualität zu steuern. Eine gültige Tabelle "Leuchtkraft" oder "Chrominanz" weist 64 Einträge vom Typ "propertytagtypeshort" auf. Wenn ein Bild entweder eine "Leuchtkraft"-Tabelle oder eine Chrominanz-Tabelle enthält, muss es beide Tabellen aufweisen.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5091               |
| type  | Propertytagtypeshort |
| Anzahl | 64                   |



 

## <a name="propertytagframedelay"></a>Propertytagframedelay

Zeitverzögerung (in Hundertstel Sekunden) zwischen zwei Frames in einem animierten GIF-Bild.



| Eigenschafts Informationen | Wert |
|-------|-------------------------------|
| Tag   | 0x5100                        |
| type  | Propertytagtypelong           |
| Anzahl | Anzahl der Frames im Bild |



 

## <a name="propertytagloopcount"></a>Propertytagloopcount

Gibt an, wie oft die Animation in einem animierten GIF-Bild angezeigt werden soll. Der Wert 0 gibt an, dass die Animation unendlich angezeigt werden soll.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x5101               |
| type  | Propertytagtypeshort |
| Anzahl | 1                    |



 

## <a name="propertytagglobalpalette"></a>Propertytagglobalpalette

Farbpalette für eine indizierte Bitmap in einem GIF-Bild.



| Eigenschafts Informationen | Wert |
|-------|-------------------------------|
| Tag   | 0x5102                        |
| type  | Propertytagtypebyte           |
| Anzahl | 3 x Anzahl von paletteneinträgen |



 

## <a name="propertytagindexbackground"></a>Propertytagindexbackground

Der Index der Hintergrundfarbe in der Palette eines GIF-Bilds.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5103              |
| type  | Propertytagtypebyte |
| Anzahl | 1                   |



 

## <a name="propertytagindextransparent"></a>Propertytagindextransparent

Der Index der transparenten Farbe in der Palette eines GIF-Bilds.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5104              |
| type  | Propertytagtypebyte |
| Anzahl | 1                   |



 

## <a name="propertytagpixelunit"></a>Propertytagpixelunit

Einheit für propertytagpixelperunitx und propertytagpixelperunity.



Tag

0x5110

type

Propertytagtypebyte

Anzahl

1

0-unbekannt



 

## <a name="propertytagpixelperunitx"></a>Propertytagpixelperunitx

Pixel pro Einheit in der x-Richtung.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5111              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagpixelperunity"></a>Propertytagpixelperunity

Pixel pro Einheit in y-Richtung.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x5112              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagpalettehistogram"></a>Propertytagpalettehistogram

Palettenhistogramm.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x5113                  |
| type  | Propertytagtypebyte     |
| Anzahl | Länge des Histogramms |



 

## <a name="propertytagcopyright"></a>Propertytagcopyright

Mit NULL beendete Zeichenfolge, die Copyright Informationen enthält.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x8298                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagexifexposuretime"></a>Propertytagexif ExposureTime

Die Expositionszeit in Sekunden.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x829a                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexiffnumber"></a>Propertytagexiffnumber

F-Nummer.



| Eigenschafts Informationen | Wert |
|-------|----------|
| Tag   | 0x829d   |
| type  | Vernünftige |
| Anzahl | 1        |



 

## <a name="propertytagexififd"></a>Propertytagexififd

Privates Tag, das von GDI+ verwendet wird. Nicht für die öffentliche Verwendung. GDI+ verwendet dieses Tag, um EXIF-spezifische Informationen zu suchen.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x8769              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagiccprofile"></a>Propertytagiccprofile

Das in das Image eingebettete ICC-Profil.



| Eigenschafts Informationen | Wert |
|-------|-----------------------|
| Tag   | 0x8773                |
| type  | Propertytagtypebyte   |
| Anzahl | Länge des Profils |



 

## <a name="propertytagexifexposureprog"></a>Propertytagexif exposureproduktionen

Klasse des Programms, das von der Kamera verwendet wird, um die Verfügbarkeit festzulegen, wenn das Bild übernommen wird.



Tag

0x8822

type

SHORT

Anzahl

1

Standard

0

0-nicht definiert 1-manuelles 2-normales-Programm 3-Aperture-Priorität 4-Rollout Priorität 5-Creative Program (für die Tiefe des Felds voreingenommen) 6-Aktionsprogramm (für die schnelle debuggeschwindigkeit), 7-hoch-Modus (für schließende Fotos mit dem Hintergrund im Fokus), 9 bis 255-reserviert



 

## <a name="propertytagexifspectralsense"></a>Propertytagexif spectralsense

Eine auf NULL endende Zeichenfolge, die die Unterscheidung zwischen den einzelnen Kanälen der verwendeten Kamera angibt. Die Zeichenfolge ist mit dem vom ASTM Technical Committee entwickelten Standard kompatibel.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x8824                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytaggpsifd"></a>Propertytaggpsifd

Offset zu einem Block von GPS-Eigenschaften Elementen. Eigenschaften Elemente, deren Tags das Präfix propertytaggps aufweisen, werden im GPS-Block gespeichert. Die GPS-Eigenschaften Elemente werden in der EXIF-Spezifikation definiert. GDI+ verwendet dieses Tag, um GPS-Informationen zu suchen, aber GDI+ macht dieses Tag nicht für die öffentliche Verwendung verfügbar.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0x8825              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagexifisospeed"></a>Propertytagexisospeed

ISO-Geschwindigkeit und ISO-Breite der Kamera oder des Eingabe Geräts, wie in ISO 12232 angegeben.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x8827               |
| type  | Propertytagtypeshort |
| Anzahl | Any                  |



 

## <a name="propertytagexifoecf"></a>Propertytagexifoecf

Die in ISO 14524 angegebene Funktion für die optoelektronische Konvertierung (oecf). Die oecf ist die Beziehung zwischen der optischen Kameraeingabe und den bildwerten.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0x8828                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | Any                      |



 

## <a name="propertytagexifver"></a>Propertytagexifäver

Die Version des unterstützten EXIF-Standards. Wenn dieses Feld nicht vorhanden ist, bedeutet dies, dass es nicht mit dem Standard übereinstimmt. Die Übereinstimmung mit dem Standard wird durch Aufzeichnen von 0210 als 4-Byte-ASCII-Zeichenfolge angegeben. Da der Typ propertytagtypeundefiniert ist, ist kein NULL-Terminator vorhanden.



| Eigenschafts Informationen | Wert |
|---------|--------------------------|
| Tag     | 0x9000                   |
| type    | Propertytagtypeundefiniert |
| Anzahl   | 4                        |
| Standard | 0210                     |



 

## <a name="propertytagexifdtorig"></a>Propertytagexiledtorig

Datum und Uhrzeit, zu der die ursprünglichen Bilddaten generiert wurden. Bei einem DSC das Datum und die Uhrzeit der Bild Erstellung. Das Format lautet yyyy: mm: DD hh: mm: SS, wobei die Zeit im 24-Stunden-Format und das Datum und die Uhrzeit durch ein Leerzeichen (0x2000) getrennt sind. Die Länge der Zeichenfolge beträgt 20 Bytes, einschließlich des NULL-Terminator. Wenn das Feld leer ist, wird es als unbekannt behandelt.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x9003               |
| type  | Propertytagtybäuercii |
| Anzahl | 20                   |



 

## <a name="propertytagexifdtdigitized"></a>Propertytagexitdtdigit

Datum und Uhrzeit, zu denen das Image als digitale Daten gespeichert wurde. Wenn z. b. ein Image von DSC aufgezeichnet wurde und gleichzeitig die Datei aufgezeichnet wurde, haben DateTimeOriginal und datetimedigitisiert denselben Inhalt.

Das Format lautet yyyy: mm: DD hh: mm: SS, wobei die Zeit im 24-Stunden-Format und das Datum und die Uhrzeit durch ein Leerzeichen (0x2000) getrennt sind. Die Länge der Zeichenfolge beträgt 20 Bytes, einschließlich des NULL-Terminator. Wenn das Feld leer ist, wird es als unbekannt behandelt.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0x9004               |
| type  | Propertytagtybäuercii |
| Anzahl | 20                   |



 

## <a name="propertytagexifcompconfig"></a>Propertytagexif compconfig

Informationen, die für komprimierte Daten spezifisch sind. Die Kanäle der einzelnen Komponenten werden in der Reihenfolge von der ersten Komponente zum vierten angeordnet. Bei nicht komprimierten Daten wird die Daten Anordnung im Tag propertytagphoto ezcinterp angegeben.

Da propertytagphoto etricinterp jedoch nur die Reihenfolge von y, CB und CR Ausdrücken kann, wird dieses Tag für Fälle bereitgestellt, in denen komprimierte Daten andere Komponenten als Y, CB und CR verwenden und andere Sequenzen unterstützen.



Tag

0x9101

type

Propertytagtypeundefiniert

Anzahl

4

Standard

4 5 6 0 (wenn RGB nicht komprimiert ist) 1 2 3 0 (andere Fälle)

0-nicht vorhanden 1-Y 2-CB 3-CR 4-R 5-G 6-B other-reserved



 

## <a name="propertytagexifcompbpp"></a>Propertytagexibcompbpp

Informationen, die für komprimierte Daten spezifisch sind. Der für ein komprimiertes Bild verwendete Komprimierungs Modus wird in der bpp-Einheit angegeben.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x9102                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexifshutterspeed"></a>Propertytagexifshutterspeed

Die Auslösegeschwindigkeit. Bei der Einheit handelt es sich um das Additive System of Photo Exposure (APEX)-Werts.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0x9201                   |
| type  | Propertytagtypesrational |
| Anzahl | 1                        |



 

## <a name="propertytagexifaperture"></a>Propertytagexifaperture

Licht blenden. Die Einheit ist der Apex-Wert.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x9202                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexifbrightness"></a>Propertytagexif-Helligkeit

Wert für Helligkeit. Die Einheit ist der Apex-Wert. Normalerweise wird Sie im Bereich von-99,99 bis 99,99 angegeben.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0x9203                   |
| type  | Propertytagtypesrational |
| Anzahl | 1                        |



 

## <a name="propertytagexifexposurebias"></a>Propertytagexif exposurebias

Der Expositions-Bias. Die Einheit ist der Apex-Wert. Normalerweise wird Sie im Bereich von-99,99 bis 99,99 angegeben.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0x9204                   |
| type  | Propertytagtypesrational |
| Anzahl | 1                        |



 

## <a name="propertytagexifmaxaperture"></a>Propertytagexif-Aperture

Kleinste F-Zahl des Lens. Die Einheit ist der Apex-Wert. Normalerweise wird Sie im Bereich von 00,00 bis 99,99 angegeben, ist aber nicht auf diesen Bereich beschränkt.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x9205                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexifsubjectdist"></a>Propertytagexilesubjetdist

Abstand zum Betreff, gemessen in Meter.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x9206                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexifmeteringmode"></a>Propertytagexismeteringmode

Messungs Modus.



Tag

0x9207

type

Propertytagtypeshort

Anzahl

1

Standard

0

0-unbekannter 1-durchschnittlicher 2-centerweightedaverage 3-Spot 4-multiSpot 5-Pattern 6-partiell 7 bis 254-reserved 255-other



 

## <a name="propertytagexiflightsource"></a>Propertytagexiflightsource

Der Typ der Lichtquelle.



Tag

0x9208

type

Propertytagtypeshort

Anzahl

1

Standard

0

0-unbekanntes 1-Sommer 2-flourescent 3-Wolfram 17-Standard hell a 18 Standard hell B 19-Standard hell C 20-D55 21-D65 22-D75 23 bis 254-reserviert 255-other



 

## <a name="propertytagexifflash"></a>Propertytagexifflash

Flash Status. Dieses Tag wird aufgezeichnet, wenn ein Bild mithilfe eines Strobe Light (Flash) erstellt wird. Bit 0 gibt den Status des Flash auslöserstatus an, und Bits 1 und 2 geben den Status der Flash Rückgabe an.



Tag

0x9209

type

Propertytagtypeshort

Anzahl

1

Werte für Bit 0, die angeben, ob der Flash ausgelöst wurde: 0B-Flash hat nicht ausgelöst: 1B-Flash ausgelöst

Werte für Bits 1 und 2, die den Status der zurückgegebenen Beleuchtung angeben: 00B-No Strobe Return Erkennungsfunktion 01B-reserved 10B-Strobe Return Light not erkannt 11b-Strobe Return Light erkannt

Resultierende Flash-Tagwerte: 0x0000-Flash hat 0x0001 nicht ausgelöst-Flash ausgelöst 0x0005-Strobe-Rückgabe Licht nicht erkannt.



 

## <a name="propertytagexiffocallength"></a>Propertytagexiffocallength

Tatsächliche Fokuslänge des-Lens in Millimeter. Die Konvertierung wird nicht auf die Fokuslänge einer 35-Millimeter-Filmkamera durchgeführt.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0x920a                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexifmakernote"></a>Propertytagexif Makernote

Notiz Kennung. Ein Tag, das von Herstellern von EXIF-Writern verwendet wird, um Informationen aufzuzeichnen. Der Inhalt ist der Hersteller.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0x927c                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | Any                      |



 

## <a name="propertytagexifusercomment"></a>Propertytagexifusercomment

Kommentartag. Ein Tag, das von EXIF-Benutzern verwendet wird, um Schlüsselwörter oder Kommentare zu dem Bild zu schreiben, neben denen in propertytagimagedescription und ohne die Einschränkungen des Zeichen Codes des propertytagimagedescription-Tags.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0x9286                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | Any                      |



 

Der Zeichencode, der im propertytagexifusercomment-Tag verwendet wird, wird basierend auf einem ID-Code in einem fixierten 8-Byte-Bereich am Anfang des Tagdaten Bereichs identifiziert. Der nicht verwendete Teil des Bereichs wird mit NULL Zeichen (0) aufgefüllt. ID-Codes werden mithilfe der Registrierung zugewiesen. Da der Typ nicht ASCII ist, muss kein NULL-Terminator verwendet werden.

## <a name="propertytagexifdtsubsec"></a>Propertytagexif-subsec

Mit NULL beendete Zeichenfolge, die einen Bruchteil einer Sekunde für das propertytagdatetime-Tag angibt.



| Eigenschafts Informationen | Wert |
|-------|----------------------------------------------------|
| Tag   | 0x9290                                             |
| type  | Propertytagtybäuercii                               |
| Anzahl | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagexifdtorigss"></a>Propertytagexisdtorigss

Eine auf NULL endenden Zeichenfolge, die einen Bruchteil einer Sekunde für das propertytagexiatdtorig-Tag angibt.



| Eigenschafts Informationen | Wert |
|------|----------------------------------------------------|
| Tag  | 0x9291                                             |
| type | Propertytagtybäuercii                               |
| N    | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagexifdtdigss"></a>Propertytagexisdtdigss

Eine auf NULL endenden Zeichenfolge, die einen Bruchteil einer Sekunde für das propertytagexiatdtdigittag angibt.



| Eigenschafts Informationen | Wert |
|------|----------------------------------------------------|
| Tag  | 0x9292                                             |
| type | ASCII                                              |
| N    | Länge der Zeichenfolge einschließlich des NULL-Terminator |



 

## <a name="propertytagexiffpxver"></a>Propertytagexiffpxver

Die von einer fpxr-Datei unterstützte Version des Flash-Formats. Wenn die fpxr-Funktion die Version 1,0 des Flash-Formats unterstützt, wird dies ähnlich wie bei propertytagexifver durch Aufzeichnen von 0100 als 4-Byte-ASCII-Zeichenfolge angegeben. Da der Typ propertytagtypeundefiniert ist, ist kein NULL-Terminator vorhanden.



Tag

0xa000

type

Propertytagtypeundefiniert

Anzahl

4

Standard

0100

0100-Flash-Format Version 1,0 andere-reserviert



 

## <a name="propertytagexifcolorspace"></a>Propertytagexilecolorspace

Farbleerraum-Spezifizierer. Normalerweise wird sRGB (= 1) verwendet, um den Farbraum basierend auf den PC-Monitor Bedingungen und der Umgebung zu definieren. Wenn ein anderer Farbraum als sRGB verwendet wird, wird unkalibriert (= 0xFFFF) festgelegt. Bilddaten, die als nicht kalibriert aufgezeichnet werden, können bei der Konvertierung in "Flash" als sRGB behandelt werden.



Tag

0xa001

type

Propertytagtypeshort

Anzahl

1

0x1-sRGB 0xFFFF-unkalibrierte andere-reserviert



 

## <a name="propertytagexifpixxdim"></a>Propertytagexif-xdim

Informationen, die für komprimierte Daten spezifisch sind. Wenn eine komprimierte Datei aufgezeichnet wird, muss die gültige Breite des aussagekräftigen Bilds in diesem Tag aufgezeichnet werden, unabhängig davon, ob Auffüll Daten oder ein Neustart Marker vorhanden sind. Dieses Tag darf in einer nicht komprimierten Datei nicht vorhanden sein.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0xa002                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagexifpixydim"></a>Propertytagexif pixydim

Informationen, die für komprimierte Daten spezifisch sind. Wenn eine komprimierte Datei aufgezeichnet wird, muss die gültige Höhe des sinnvollen Bilds in diesem Tag aufgezeichnet werden, unabhängig davon, ob Auffüll Daten oder ein Neustart Marker vorhanden sind. Dieses Tag darf in einer nicht komprimierten Datei nicht vorhanden sein. Da das Auffüllen von Daten in vertikaler Richtung unnötig ist, ist die Anzahl von Zeilen, die in diesem gültigen Image Height-Tag aufgezeichnet werden, identisch mit der in SOF aufgezeichneten.



| Eigenschafts Informationen | Wert |
|-------|---------------------------------------------|
| Tag   | 0xa003                                      |
| type  | Propertytagtypeshort oder propertytagtypelong |
| Anzahl | 1                                           |



 

## <a name="propertytagexifrelatedwav"></a>Propertytagexifrelatedwav

Der Name einer Audiodatei, die sich auf die Bilddaten bezieht. Die einzigen als relationalen Informationen aufgezeichneten Informationen sind der Name und die Erweiterung der EXIF-Audiodatei (eine ASCII-Zeichenfolge, die aus 8 Zeichen plus einem Zeitraum (.) und 3 Zeichen besteht). Der Pfad wird nicht aufgezeichnet. Wenn Sie dieses Tag verwenden, müssen Audiodateien in Übereinstimmung mit dem EXIF-Audioformat aufgezeichnet werden. Writer können auch Audiodaten innerhalb von APP2 als Daten des Flash-Erweiterungs Datenstroms speichern.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0xa004               |
| type  | Propertytagtybäuercii |
| Anzahl | 13                   |



 

## <a name="propertytagexifinterop"></a>Propertytagexifinterop

Offset zu einem Block von Eigenschafts Elementen, die Interoperabilitäts Informationen enthalten.



| Eigenschafts Informationen | Wert |
|-------|---------------------|
| Tag   | 0xa005              |
| type  | Propertytagtypelong |
| Anzahl | 1                   |



 

## <a name="propertytagexifflashenergy"></a>Propertytagexifflashenergy

Strobe Energy, in Beam Kerzen Power seconds (BCPS), zu dem Zeitpunkt, als das Image aufgezeichnet wurde.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0xa20b                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexifspatialfr"></a>Propertytagexilespatialfr

Die Tabelle für die räumliche Häufigkeit der Kamera-oder Eingabegeräte und die Werte in der Bildbreite, Bildhöhe und Diagonal Richtung, wie in ISO 12233 angegeben.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0xa20c                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | Any                      |



 

## <a name="propertytagexiffocalxres"></a>Propertytagexiffocalxres

Die Anzahl der Pixel in der Bild breiten Richtung (x) pro Einheit auf der Kamera-Fokusebene. Die Einheit wird in propertytagexiffocalresunit angegeben.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0xa20e                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexiffocalyres"></a>Propertytagexiffocalyres

Die Anzahl der Pixel in der Bildhöhe (y)-Richtung pro Einheit auf der Kamera-Fokusebene. Die Einheit wird in propertytagexiffocalresunit angegeben.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0xa20f                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexiffocalresunit"></a>Propertytagexiffocalresunit

Maßeinheit für propertytagexiffocalxres und propertytagexiffocalyres.



Tag

0xa210

type

Propertytagtypeshort

Anzahl

1

2 Zoll, 3 Zentimeter



 

## <a name="propertytagexifsubjectloc"></a>Propertytagexilosubjetloc

Speicherort des Haupt Subjekts in der Szene. Der Wert dieses Tags stellt das Pixel in der Mitte des Haupt Subjekts relativ zum linken Rand dar. Der erste Wert gibt die Spaltennummer an, und der zweite Wert gibt die Zeilennummer an.



| Eigenschafts Informationen | Wert |
|-------|----------------------|
| Tag   | 0xa214               |
| type  | Propertytagtypeshort |
| Anzahl | 2                    |



 

## <a name="propertytagexifexposureindex"></a>Propertytagexif exposureindex

Der auf der Kamera oder dem Eingabegerät zum Zeitpunkt der Erfassung des Abbilds ausgewählte Expositions Index.



| Eigenschafts Informationen | Wert |
|-------|-------------------------|
| Tag   | 0xa215                  |
| type  | Propertytagtyperational |
| Anzahl | 1                       |



 

## <a name="propertytagexifsensingmethod"></a>Propertytagexif-singmethod

Bild Sensortyp auf der Kamera oder dem Eingabegerät.



Tag

0xa217

type

Propertytagtypeshort

Anzahl

1

1: nicht definiert 2-One-Chip-Farbbereichs Sensor 3-zwei-Chip-Farbbereichs Sensor 4-drei-Chip-Farbbereichs Sensor 5-farbige sequenzieller Bereichs Sensor 7-zweilinearer Sensor 8-farbig sequenzieller linearer Sensor-reserviert



 

## <a name="propertytagexiffilesource"></a>Propertytagexiffilesource

Die Bildquelle. Wenn ein DSC das Image aufgezeichnet hat, ist der Wert dieses Tags 3.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0xa300                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | 1                        |



 

## <a name="propertytagexifscenetype"></a>Propertytagexilescenetype

Der Typ der Szene. Wenn ein DSC das Image aufgezeichnet hat, muss der Wert dieses Tags auf 1 festgelegt werden, um anzugeben, dass das Bild direkt fotografiert wurde.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0xa301                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | 1                        |



 

## <a name="propertytagexifcfapattern"></a>Propertytagexifcfapattern

Das geometrische Muster des Farbfilter Arrays (CFA) des Bildsensors, wenn ein One-Chip-Farbbereichs Sensor verwendet wird. Es gilt nicht für alle Methoden zur Erkennung.



| Eigenschafts Informationen | Wert |
|-------|--------------------------|
| Tag   | 0xa302                   |
| type  | Propertytagtypeundefiniert |
| Anzahl | Any                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Image File Format-Spezifikationen](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Bildeigenschaften-tagkonstanten](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[**Bildeigenschaften-Tagtyp Konstanten**](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[Eigenschaften Tags in alphabetischer Reihenfolge](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[Eigenschaften Tags in numerischer Reihenfolge](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[Lesen und Schreiben von Metadaten](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



