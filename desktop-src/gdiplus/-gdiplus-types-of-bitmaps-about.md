---
description: Eine Bitmap ist ein Array von Bits, das die Farbe jedes Pixels in einem rechteckigen Array von Pixeln angibt.
ms.assetid: fac60d01-d07e-41e9-98a3-34c592d97a92
title: Bitmaptypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0503bec0f8b029e373ff414b51a60c3b1201a37b9151b722cdfc94d4cdea46cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977300"
---
# <a name="types-of-bitmaps"></a>Bitmaptypen

Eine Bitmap ist ein Array von Bits, das die Farbe jedes Pixels in einem rechteckigen Array von Pixeln angibt. Die Anzahl der Bits, die einem einzelnen Pixel zugeordnet sind, bestimmt die Anzahl der Farben, die diesem Pixel zugewiesen werden können. Wenn jedes Pixel beispielsweise durch 4 Bits dargestellt wird, kann einem bestimmten Pixel eine von 16 verschiedenen Farben (2^4 = 16) zugewiesen werden. Die folgende Tabelle zeigt einige Beispiele für die Anzahl von Farben, die einem Pixel zugewiesen werden können, das durch eine bestimmte Anzahl von Bits dargestellt wird.



| Bits pro Pixel | Anzahl von Farben, die einem Pixel zugewiesen werden können |
|----------------|--------------------------------------------------|
| 1              | 2^1 = 2                                          |
| 2              | 2^2 = 4                                          |
| 4              | 2^4 = 16                                         |
| 8              | 2^8 = 256                                        |
| 16             | 2^16 = 65,536                                    |
| 24             | 2^24 = 16, 777, 216                              |



 

Datenträgerdateien, die Bitmaps speichern, enthalten in der Regel einen oder mehrere Informationsblöcke, in denen Informationen wie die Anzahl der Bits pro Pixel, die Anzahl der Pixel in jeder Zeile und die Anzahl der Zeilen im Array gespeichert werden. Eine solche Datei kann auch eine Farbtabelle enthalten (manchmal auch als Farbpalette bezeichnet). Eine Farbtabelle ordnet Zahlen in der Bitmap bestimmten Farben zu. Die folgende Abbildung zeigt ein vergrößertes Bild zusammen mit seiner Bitmap- und Farbtabelle. Jedes Pixel wird durch eine 4-Bit-Zahl dargestellt, sodass die Farbtabelle 2^4 = 16 Farben enthält. Jede Farbe in der Tabelle wird durch eine 24-Bit-Zahl dargestellt: 8 Bits für Rot, 8 Bits für Grün und 8 Bits für Blau. Die Zahlen werden in hexadezimaler Form (Basis 16) angezeigt: A = 10, B = 11, C = 12, D = 13, E = 14, F = 15.

![Abbildung, die eine Matrix von Zahlen, ein Bild und eine Tabelle zeigt, die die Matrixzahlen mit Farben ab stimmt](images/aboutgdip03-art01.png)

Sehen Sie sich das Pixel in Zeile 3, Spalte 5 des Bilds an. Die entsprechende Zahl in der Bitmap ist 1. Die Farbtabelle gibt an, dass 1 die Farbe Rot darstellt, sodass das Pixel rot ist. Alle Einträge in der obersten Zeile der Bitmap sind 3. Die Farbtabelle gibt an, dass 3 blau darstellt, sodass alle Pixel in der oberen Zeile des Bilds blau sind.

> [!Note]  
> Einige Bitmaps werden im Bottom-Up-Format gespeichert. Die Zahlen in der ersten Zeile der Bitmap entsprechen den Pixeln in der unteren Zeile des Bilds.

 

Eine Bitmap, die Indizes in einer Farbtabelle speichert, wird als *palettenindizierte Bitmap* bezeichnet. Einige Bitmaps benötigen keine Farbtabelle. Wenn eine Bitmap beispielsweise 24 Bits pro Pixel verwendet, kann diese Bitmap die Farben selbst statt in Indizes in einer Farbtabelle speichern. Die folgende Abbildung zeigt eine Bitmap, die Farben direkt speichert (24 Bits pro Pixel), anstatt eine Farbtabelle zu verwenden. Die Abbildung zeigt auch eine vergrößerte Ansicht des entsprechenden Bilds. In der Bitmap stellt FFFFFF weiß dar, FF0000 steht für Rot, 00FF00 für Grün und 0000FF für Blau.

![Abbildung einer Matrix von Hexadezimalwerten gefolgt von dem Bitmapbild, das die Zahlen darstellen](images/aboutgdip03-art02.png)

 

## <a name="graphics-file-formats"></a>Grafikdateiformate

Es gibt viele Standardformate zum Speichern von Bitmaps in Dateien. Windows GDI+ unterstützt die in den folgenden Abschnitten beschriebenen Grafikdateiformate.

**Bitmap (BMP)**

BMP ist ein Standardformat, das von Windows zum Speichern geräteunabhängiger und anwendungsunabhängiger Images verwendet wird. Die Anzahl der Bits pro Pixel (1, 4, 8, 15, 24, 32 oder 64) für eine angegebene BMP-Datei wird in einem Dateiheader angegeben. BMP-Dateien mit 24 Bits pro Pixel sind üblich.

**GIF (Graphics Interchange Format)**

GIF ist ein gängiges Format für Bilder, die auf Webseiten angezeigt werden. GIFs funktionieren gut für Linienzeichnungen, Bilder mit Volltonblöcken und Bilder mit starken Begrenzungen zwischen Farben. GIFs werden komprimiert, aber beim Komprimierungsprozess gehen keine Informationen verloren. ein dekomprimiertes Bild ist genau dasselbe wie das Original. Eine Farbe in einem GIF kann als transparent festgelegt werden, sodass das Bild die Hintergrundfarbe jeder Webseite hat, auf der es angezeigt wird. Eine Sequenz von GIF-Bildern kann in einer einzelnen Datei gespeichert werden, um ein animiertes GIF zu bilden. GIFs speichern maximal 8 Bits pro Pixel, sodass sie auf 256 Farben beschränkt sind.

**JPEG (Joint Photographic Experts Group)**

JPEG ist ein Komprimierungsschema, das gut für natürliche Szenen wie gescannte Fotos funktioniert. Einige Informationen gehen beim Komprimierungsprozess verloren, aber häufig ist der Verlust für das menschliche Auge nicht wahrnehmbar. JPEG-Farbbilder speichern 24 Bits pro Pixel, sodass sie mehr als 16 Millionen Farben anzeigen können. Es gibt auch ein JPEG-Graustufenformat, in dem 8 Bits pro Pixel gespeichert werden. JPEGs unterstützen keine Transparenz oder Animation.

Der Grad der Komprimierung in JPEG-Bildern ist konfigurierbar, aber höhere Komprimierungsstufen (kleinere Dateien) führen zu einem größeren Informationsverlust. Ein Komprimierungsverhältnis von 20:1 erzeugt häufig ein Bild, das das menschliche Auge schwer vom Original unterscheiden kann. Die folgende Abbildung zeigt ein BMP-Bild und zwei JPEG-Bilder, die aus diesem BMP-Bild komprimiert wurden. Das erste JPEG hat ein Komprimierungsverhältnis von 4:1, das zweite JPEG ein Komprimierungsverhältnis von etwa 8:1.

![Abbildung, die ein Bitmapbild und zwei JPEG-Komprimierungen dieses Bilds zeigt; die höchste Komprimierung hat mehr Abweichungen vom Original](images/aboutgdip03-art03.png)

Die JPEG-Komprimierung funktioniert nicht gut für Linienzeichnungen, Volltonblöcke und spitze Begrenzungen. Die folgende Abbildung zeigt einen BMP zusammen mit zwei JPEGs und einem GIF. Die JPEGs und das GIF wurden aus dem BMP komprimiert. Das Komprimierungsverhältnis beträgt 4:1 für das GIF, 4:1 für das kleinere JPEG und 8:3 für das größere JPEG. Beachten Sie, dass das GIF die spitzen Grenzen entlang der Linien bei sich hält, aber die JPEGs tendieren dazu, die Grenzen zu verwischen.

![Abbildung, die eine Bitmap einer Linienzeichnung mit zwei JPEG-Entsprechungen und einem GIF vergleicht; Die GIF-Datei behält die Farb- und Linienschärfe am besten bei.](images/aboutgdip03-art03a.png)

JPEG ist ein Komprimierungsschema, kein Dateiformat. DAS JPEG File Interchange Format (JFIF) ist ein Dateiformat, das häufig zum Speichern und Übertragen von Bildern verwendet wird, die gemäß dem JPEG-Schema komprimiert wurden. JFIF-Dateien, die von Webbrowsern angezeigt werden, verwenden die .jpg Erweiterung.

**Austauschbare Bilddatei (Exif)**

Exif ist ein Dateiformat, das für Fotos verwendet wird, die von Digitalkameras erfasst werden. Eine Exif-Datei enthält ein Bild, das gemäß der JPEG-Spezifikation komprimiert wird. Eine Exif-Datei enthält auch Informationen über das Foto (Aufgenommenes Datum, Geschwindigkeit, Belichtungszeit und so weiter) und Informationen zur Kamera (Hersteller, Modell und so weiter).

**PNG (Portable Network Graphics)**

Das PNG-Format behält viele Vorteile des GIF-Formats bei, bietet aber auch Funktionen, die über die von GIF hinausgehen. Wie GIF-Dateien werden PNG-Dateien ohne Verlust von Informationen komprimiert. PNG-Dateien können Farben mit 8, 24 oder 48 Bits pro Pixel und grauen Skalen mit 1, 2, 4, 8 oder 16 Bits pro Pixel speichern. Im Gegensatz dazu können GIF-Dateien nur 1, 2, 4 oder 8 Bits pro Pixel verwenden. Eine PNG-Datei kann auch einen Alphawert für jedes Pixel speichern, der den Grad angibt, in dem die Farbe dieses Pixels mit der Hintergrundfarbe kombiniert wird.

PNG verbessert gif in seiner Fähigkeit, ein Bild progressiv anzuzeigen. das heißt, um bessere und bessere Näherungen des Bilds anzuzeigen, wenn es über eine Netzwerkverbindung eintrifft. PNG-Dateien können Gammakorrektur- und Farbkorrekturinformationen enthalten, damit die Bilder auf einer Vielzahl von Anzeigegeräten genau gerendert werden können.

**Tag Image File Format (TIFF) (Tagbilddateiformat (TIFF))**

TIFF ist ein flexibles und erweiterbares Format, das von einer Vielzahl von Plattformen und Bildverarbeitungsanwendungen unterstützt wird. TIFF-Dateien können Bilder mit einer beliebigen Anzahl von Bits pro Pixel speichern und eine Vielzahl von Komprimierungsalgorithmen verwenden. Mehrere Bilder können in einer TIFF-Datei mit mehreren Seiten gespeichert werden. Informationen im Zusammenhang mit dem Bild (Scannermarken, Hostcomputer, Komprimierungstyp, Ausrichtung, Stichproben pro Pixel) können in der Datei gespeichert und mithilfe von Tags angeordnet werden. Das TIFF-Format kann bei Bedarf durch die Genehmigung und das Hinzufügen neuer Tags erweitert werden.

 

 



