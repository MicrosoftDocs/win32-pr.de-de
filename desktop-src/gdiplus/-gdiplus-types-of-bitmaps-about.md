---
description: Eine Bitmap ist ein Array von Bits, das die Farbe der einzelnen Pixel in einem rechteckigen Array von Pixeln angibt.
ms.assetid: fac60d01-d07e-41e9-98a3-34c592d97a92
title: Bitmaptypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4427f83e7ff0ccedbfa4fc0155ac2ef3c8968dfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557999"
---
# <a name="types-of-bitmaps"></a>Bitmaptypen

Eine Bitmap ist ein Array von Bits, das die Farbe der einzelnen Pixel in einem rechteckigen Array von Pixeln angibt. Die Anzahl von Bits, die einem einzelnen Pixel zugeordnet ist, bestimmt die Anzahl von Farben, die diesem Pixel zugewiesen werden können. Wenn beispielsweise jedes Pixel durch 4 Bits dargestellt wird, kann einem bestimmten Pixel eine von 16 verschiedenen Farben (2 ^ 4 = 16) zugewiesen werden. Die folgende Tabelle zeigt einige Beispiele für die Anzahl von Farben, die einem Pixel zugewiesen werden können, das durch eine bestimmte Anzahl von Bits dargestellt wird.



| Bits pro Pixel | Anzahl von Farben, die einem Pixel zugewiesen werden können |
|----------------|--------------------------------------------------|
| 1              | 2^1 = 2                                          |
| 2              | 2^2 = 4                                          |
| 4              | 2^4 = 16                                         |
| 8              | 2^8 = 256                                        |
| 16             | 2^16 = 65,536                                    |
| 24             | 2 ^ 24 = 16, 777, 216                              |



 

Datenträger Dateien, die Bitmaps speichern, enthalten in der Regel mindestens einen Informationsblock, in dem Informationen wie die Anzahl der Bits pro Pixel, die Anzahl der Pixel in jeder Zeile und die Anzahl der Zeilen im Array gespeichert werden. Eine solche Datei kann auch eine Farbtabelle (manchmal auch als Farbpalette bezeichnet) enthalten. In einer Farbtabelle werden Zahlen in der Bitmap bestimmten Farben zugeordnet. In der folgenden Abbildung wird ein erweitertes Bild zusammen mit dessen Bitmap und Farbtabelle dargestellt. Jedes Pixel wird durch eine 4-Bit-Zahl dargestellt, sodass in der Farbtabelle 2 ^ 4 = 16 Farben vorhanden sind. Jede Farbe in der Tabelle wird durch eine 24-Bit-Zahl dargestellt: 8 Bits für Rot, 8 Bits für Grün und 8 Bits für blau. Die Zahlen werden im Hexadezimal Format (Basis 16) angezeigt: A = 10, B = 11, C = 12, D = 13, E = 14, F = 15.

![Abbildung, die eine Matrix von Zahlen, ein Bild und eine Tabelle anzeigt, die den Matrix Zahlen mit Farben entspricht](images/aboutgdip03-art01.png)

Sehen Sie sich das Pixel in Zeile 3, Spalte 5 des Bilds an. Die entsprechende Zahl in der Bitmap ist 1. Die Color-Tabelle gibt an, dass 1 die Farbe rot darstellt, sodass das Pixel rot ist. Alle Einträge in der obersten Zeile der Bitmap sind 3. Die Color-Tabelle gibt an, dass 3 blau darstellt, sodass alle Pixel in der oberen Zeile des Bilds blau sind.

> [!Note]  
> Einige Bitmaps werden im unteren Format gespeichert. die Zahlen in der ersten Zeile der Bitmap entsprechen den Pixeln in der unteren Zeile des Bilds.

 

Eine Bitmap, die Indizes in einer Farbtabelle speichert, wird als *palettenindiziertes* Bitmap bezeichnet. Für einige Bitmaps ist eine Farbtabelle nicht erforderlich. Wenn eine Bitmap z. b. 24 Bits pro Pixel verwendet, kann diese Bitmap anstelle von Indizes in einer Farbtabelle die Farben selbst speichern. Die folgende Abbildung zeigt eine Bitmap, die Farben direkt (24 Bits pro Pixel) speichert, anstatt eine Farbtabelle zu verwenden. Die Abbildung zeigt auch eine vergrößerte Ansicht des entsprechenden Bilds. In der Bitmap steht FFFFFF für weiß, FF0000 stellt rot, 00FF00 für Grün und 0000FF für Blau dar.

![Abbildung einer Matrix von hexadezimalen Werten, gefolgt von dem Bitmap-Bild, das die Zahlen darstellen](images/aboutgdip03-art02.png)

 

## <a name="graphics-file-formats"></a>Grafikdatei Formate

Es gibt viele Standardformate für das Speichern von Bitmaps in Dateien. Windows GDI+ unterstützt die in den folgenden Abschnitten beschriebenen Grafikdatei Formate.

**Bitmap (BMP)**

BMP ist ein Standardformat, das von Windows verwendet wird, um geräteunabhängige und Anwendungs unabhängige Images zu speichern. Die Anzahl der Bits pro Pixel (1, 4, 8, 15, 24, 32 oder 64) für eine bestimmte BMP-Datei wird in einem Dateiheader angegeben. BMP-Dateien mit 24 Bits pro Pixel sind üblich.

**GIF (Graphics Interchange Format)**

GIF ist ein gängiges Format für Bilder, die auf Webseiten angezeigt werden. Die GIFs funktionieren gut für Linienzeichnungen, Bilder mit Blöcken mit voll Tonfarbe und Bilder mit Spitzen Grenzen zwischen Farben. Die GIFs werden komprimiert, während der Komprimierungs Vorgang aber keine Informationen verloren gehen. ein entkomprimiertes Bild ist exakt mit dem Original identisch. Eine Farbe in einem GIF kann als transparent festgelegt werden, sodass das Bild die Hintergrundfarbe jeder beliebigen Webseite hat, auf der es angezeigt wird. Eine Sequenz von GIF-Bildern kann in einer einzelnen Datei gespeichert werden, um eine animierte GIF zu bilden. Der Wert von "GIFs" ist höchstens 8 Bits pro Pixel, sodass Sie auf 256 Farben beschränkt sind.

**JPEG (Joint Photographic Experts Group)**

JPEG ist ein Komprimierungs Schema, das für natürliche Szenen (z. b. gescannte Fotos) gut funktioniert. Einige Informationen gehen im Komprimierungs Prozess verloren, aber häufig ist der Verlust für das menschliche Auge nicht wahrnehmbar. Color JPEG-Bilder speichern 24 Bits pro Pixel, sodass Sie mehr als 16 Millionen Farben anzeigen können. Es gibt auch ein Graustufen JPEG-Format, in dem 8 Bits pro Pixel gespeichert werden. Jpeer unterstützt keine Transparenz oder Animation.

Der Komprimierungs Grad in JPEG-Bildern ist konfigurierbar, höhere Komprimierungs Stufen (kleinere Dateien) führen jedoch zu einem größeren Informationsverlust. Ein 20:1-Komprimierungs Verhältnis erzeugt häufig ein Bild, das dem Menschen schwer zu unterscheiden ist. Die folgende Abbildung zeigt ein BMP-Bild und zwei JPEG-Bilder, die von diesem BMP-Bild komprimiert wurden. Das erste JPEG hat ein Komprimierungs Verhältnis von 4:1, und das zweite JPEG hat ein Komprimierungs Verhältnis von ungefähr 8:1.

![Abbildung mit einem Bitmap-Bild und zwei JPEG-Komprimierungen dieses Bilds die höchste Komprimierung weist eine größere Abweichung vom Original auf.](images/aboutgdip03-art03.png)

Die JPEG-Komprimierung funktioniert nicht gut für Linienzeichnungen, Blöcke mit voll Tonfarbe und Spitzen Grenzen. Die folgende Abbildung zeigt eine BMP zusammen mit zwei jpeer-und GIF-Funktionen. Die jpeer-und GIF-Datei wurden aus dem BMP komprimiert. Das Komprimierungs Verhältnis beträgt 4:1 für GIF, 4:1 für das kleinere JPEG und 8:3 für das größere JPEG. Beachten Sie, dass das GIF die Spitzen Grenzen entlang der Linien beibehält, aber die jpeer-Funktionen neigen dazu, die Grenzen zu verwischen.

![Abbildung: Vergleichen einer Bitmap einer Linie mit zwei JPEG-Entsprechungen und einem GIF Das GIF behält Farbe und Zeilen Schärfe am besten bei](images/aboutgdip03-art03a.png)

JPEG ist ein Komprimierungs Schema, kein Dateiformat. Das JPEG-Dateiaustauschformat (JFI) ist ein Datei Format, das häufig zum Speichern und übertragen von Images verwendet wird, die gemäß dem JPEG-Schema komprimiert wurden. JFI-Dateien, die von Webbrowsern angezeigt werden, verwenden die Erweiterung. jpg.

**Austauschbare Bilddatei (EXIF)**

EXIF ist ein Dateiformat für Fotos, die von Digitalkameras aufgezeichnet werden. Eine EXIF-Datei enthält ein Bild, das gemäß der JPEG-Spezifikation komprimiert wird. Eine EXIF-Datei enthält außerdem Informationen über das Foto (ergriffene Daten, die Auslösezeit usw.) und Informationen zur Kamera (Hersteller, Modell usw.).

**PNG (Portable Network Graphics)**

Das PNG-Format behält viele der Vorteile des gif-Formats bei, bietet aber auch Funktionen, die über die von GIF hinausgehen. Wie bei GIF-Dateien werden PNG-Dateien ohne Informationsverlust komprimiert. PNG-Dateien können Farben mit 8, 24 oder 48 Bits pro Pixel und graue Skalen mit 1, 2, 4, 8 oder 16 Bits pro Pixel speichern. Im Gegensatz dazu können GIF-Dateien nur 1, 2, 4 oder 8 Bits pro Pixel verwenden. Eine PNG-Datei kann auch einen Alphawert für jedes Pixel speichern, der den Grad angibt, in dem die Farbe dieses Pixels mit der Hintergrundfarbe gemischt wird.

PNG verbessert bei der GIF die Möglichkeit, ein Bild progressiv anzuzeigen. Das heißt, Sie können bessere und bessere Näherungen des Bilds anzeigen, wenn es über eine Netzwerkverbindung gelangt. PNG-Dateien können Gammakorrektur-und Farbkorrektur Informationen enthalten, damit die Bilder auf einer Vielzahl von Anzeigegeräten exakt gerendert werden können.

**Tagbild Datei Format (TIFF)**

TIFF ist ein flexibles und erweiterbares Format, das von einer Vielzahl von Plattformen und Bildverarbeitungsanwendungen unterstützt wird. TIFF-Dateien können Bilder mit einer beliebigen Anzahl von Bits pro Pixel speichern und verschiedene Komprimierungs Algorithmen verwenden. Mehrere Bilder können in einer einzelnen, mehrseitigen TIFF-Datei gespeichert werden. Informationen im Zusammenhang mit dem Image (Scanner, Host Computer, Komprimierungstyp, Ausrichtung, Beispiele pro Pixel usw.) können in der Datei gespeichert und durch die Verwendung von Tags angeordnet werden. Das TIFF-Format kann je nach Bedarf durch die Genehmigung und Addition neuer Tags erweitert werden.

 

 



