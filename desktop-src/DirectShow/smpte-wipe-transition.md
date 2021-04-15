---
description: Übergang von SMPTE-Löschung
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: Übergang von SMPTE-Löschung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47de62c450ff0d75f72e5fac466801991b987834
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521712"
---
# <a name="smpte-wipe-transition"></a>Übergang von SMPTE-Löschung

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Der Übergang des SMPTE-Zurücksetzens erzeugt alle Standard-setzt, die von der Motion Picture-und TV Engineers (SMPTE) im SMPTE-Dokument 258m-1993 definiert werden, mit Ausnahme der Quad-Teilung.

![der Übergang wurde fortgesetzt.](images/trans-wipe.png)

Klassen-ID (CLSID): {DE75D012-7A65-11d2-8CEA-00A0C9441E20}

CLSID-Variablen Name: CLSID \_ DXTJPEG

Anzeige Name: "DXTJPEG"

Eigenschaften



| Eigenschaft       | type   | Standard  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BorderColor    | long   | 0x000000 | Farbe des Rahmens um die Ränder des Abbild-Musters. Der Wert dieses Attributs ist eine hexadezimale Zahl mit dem Format 0x *RRGGBB*, wobei *RR* der rote Wert, *GG* der grüne Wert und *BB* der blaue Wert ist. (Die reinen roten, grünen und blauen sind also 0xFF000, 0x00FF00 und 0x0000FF.) |
| Borderweichheit | long   | 0        | Breite des unscharf-Bereichs um die Ränder des-tokenmusters. Geben Sie 0 (null) für keine verschwommene Region an                                                                                                                                                                                                              |
| Rahmenbreite    | long   | 0        | Breite des vollständigen Rahmens entlang der Kanten des Abbild-Musters. Geben Sie NULL für keinen Rahmen an.                                                                                                                                                                                                                       |
| Maskname       | BSTR   | **NULL** | Wenn Not **null** ist, wird der Name einer JPEG-Datei angegeben, die anstelle eines standardmäßigen, integrierten neueinsetzens als-ablösmaske verwendet werden soll. Die Datei muss einen Farbverlauf von 8 Bits pro Pixel enthalten. Der Farbverlauf wird als Maske zum Definieren des Fortschritts der Löschung verwendet.                                                                 |
| Masknum        | long   | 1        | Standard mäßiger SMPTE-Code, der die Art der zu verwendenden Löschung angibt. Eine Liste der Codes für das Löschen und die zugehörigen Schemas finden Sie unter SMPTE Document 258m-1993.                                                                                                                                                            |
| OffsetX        | long   | 0        | Horizontaler Offset des Ursprungs, der aus der Mitte des Bilds entfernt wurde. Gilt nur für die Werte von **masknum** zwischen 101 und 131.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Ververtierte Abweichung des Ursprungs der Löschung von der Mitte des Bilds. Gilt nur für die Werte von **masknum** zwischen 101 und 131.                                                                                                                                                                                            |
| Replialisiex     | long   | 0        | Gibt an, wie oft das Abbild der Löschung horizontal repliziert wird. Gilt nur für die Werte von **masknum** zwischen 101 und 131.                                                                                                                                                                                                |
| Replialisier     | long   | 0        | Häufigkeit, mit der das Abbild für das Löschen vertikal repliziert wird. Gilt nur für die Werte von **masknum** zwischen 101 und 131.                                                                                                                                                                                                  |
| ScaleX         | double | 1.0      | Der Betrag, um den die Löschung horizontal gestreckt werden soll, als Prozentsatz der ursprünglichen Definition für das Löschen. Gilt nur für die Werte von **masknum** zwischen 101 und 131.                                                                                                                                                         |
| ScaleY         | double | 1.0      | Der Betrag, um den die Löschung vertikal gestreckt werden soll, als Prozentsatz der ursprünglichen Definition für das Löschen. Gilt nur für die Werte von **masknum** zwischen 101 und 131.                                                                                                                                                           |



 

## <a name="remarks"></a>Bemerkungen

Dieser Übergang unterstützt die folgenden standardmäßigen SMPTE-Wipes:



| Number | BESCHREIBUNG                   | Number | BESCHREIBUNG                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Horizontal                    | 211    | Radiales, linksbündig, oben                     |
| 2      | Vertical                      | 212    | Radial, nach unten, rechts                      |
| 3      | Oben links                    | 213    | Radiales, linksbündig, oben nach unten              |
| 4      | Oben rechts                   | 214    | Radial, nach unten, linksbündig                 |
| 5      | Unten rechts                   | 221    | Radiale, obere                                 |
| 6      | Unten links                    | 222    | Radiales, rechts                               |
| 7      | Vier Ecken                  | 223    | Radiales, unten                              |
| 8      | Vier Quadrate                  | 224    | Radiales, Links                                |
| 21     | Stalltüren, vertikal          | 225    | Radiale, obere im Uhrzeigersinn, unten im Uhrzeigersinn     |
| 22     | Stalltüren, horizontal        | 226    | Radiale, Links im Uhrzeigersinn, rechts im Uhrzeigersinn     |
| 23     | Top-Mitte                    | 227    | Radiale, obere im Uhrzeigersinn, unterer Uhrzeigersinn |
| 24     | Rechts zentriert                  | 228    | Radiale, nach links im Uhrzeigersinn, rechtsbündig |
| 25     | Unten zentriert                 | 231    | Radiale, obere Teilung                           |
| 26     | Links zentriert                   | 232    | Radiale, Rechte Teilung                         |
| 41     | Diagonal, von NW zu SE            | 233    | Radiale, untere Teilung                        |
| 42     | Diagonal, ne bis SW            | 234    | Radiale, linke Teilung                          |
| 43     | Dreiecke, oben/unten         | 235    | Radiale, obere untere Teilung                    |
| 44     | Dreiecke, links/rechts         | 236    | Radiale, linksbündig Aufteilungen                    |
| 45     | Diagonaler Stripe, SW zu ne     | 241    | Radiale, linke obere Ecke                     |
| 46     | Diagonaler Streifen, von NW zu SE     | 242    | Radiale linke Ecke                  |
| 47     | Cross                         | 243    | Radiale, untere rechte Ecke                 |
| 48     | Diamant Feld                   | 244    | Radiale, obere rechte Ecke                    |
| 61     | Keil, oben                    | 245    | Radiale, oben links, unten rechts              |
| 62     | Keil, rechts                  | 246    | Radiales, unten links, oben rechts              |
| 63     | Keil, unten                 | 251    | Zentrieren, oben                          |
| 64     | Keil, Links                   | 252    | Mittel fördig, Links                         |
| 65     | V                             | 253    | Mittel förmigem Mittel, unten                       |
| 66     | V, Right                      | 254    | Zentrieren, rechts                        |
| 67     | V, invertiert                   | 261    | Feld Radiat, Right                           |
| 68     | V, Links                       | 262    | Feld Radiat, Top                             |
| 71     | Sägezahn, Links                | 263    | Zentrieren, von oben nach unten                  |
| 72     | Sägezahn, oben                 | 264    | Mittel fördig, Links, rechts                  |
| 73     | Sägezahn, vertikal            | 301    | Matrix, horizontal                          |
| 74     | Sägezahn, horizontal          | 302    | Matrix, vertikal                            |
| 101    | Feld                           | 303    | Matrix, Diagonal, oben links                  |
| 102    | Diamond                       | 304    | Matrix, Diagonal, oben rechts                 |
| 103    | Dreieck, nach oben                  | 305    | Matrix, Diagonal, unten rechts              |
| 104    | Dreieck, rechts               | 306    | Matrix, Diagonal, unten links               |
| 105    | Dreieck, unten              | 310    | Matrix, oben links im Uhrzeigersinn                  |
| 106    | Dreieck, Links                | 311    | Matrix, oben rechts im Uhrzeigersinn                 |
| 107    | Pfeilspitze, nach oben                | 312    | Matrix im Uhrzeigersinn unten rechts              |
| 108    | Pfeilspitze, rechts             | 313    | Matrix im Uhrzeigersinn unten links               |
| 109    | Pfeilspitze, nach unten              | 314    | Matrix, gegen den Uhrzeigersinn oben links              |
| 110    | Pfeilspitze, Links              | 315    | Matrix, gegen den Uhrzeigersinn oben rechts             |
| 111    | Pentagon, nach oben                  | 316    | Matrix, gegen den Uhrzeigersinn unten rechts          |
| 112    | Pentagon, nach unten                | 317    | Matrix, rechtsbündig unten links           |
| 113    | Sechseck                       | 320    | Matrix, vertikal oben links, oben rechts        |
| 114    | Hexseck, gedreht              | 321    | Matrix, vertikal unten links, unten rechts  |
| 119    | Circle                        | 322    | Matrix, vertikal oben links, unten rechts     |
| 120    | Oval, horizontal              | 323    | Matrix, vertikal unten links, oben rechts     |
| 121    | Oval, vertikal                | 324    | Matrix, horizontal Links oben links, unten links    |
| 122    | Eye, horizontal               | 325    | Matrix, horizontal oben rechts, unten rechts  |
| 123    | Eye, vertikal                 | 326    | Matrix, horizontal oben links, unten rechts   |
| 124    | Abgerundetes Rechteck, horizontal | 327    | Matrix, horizontal oben rechts, unten links   |
| 125    | Abgerundetes Rechteck, vertikal   | 328    | Matrix, diagonal unten links, oben rechts     |
| 127    | 4-Punkt-Stern                  | 329    | Matrix, diagonal oben links, unten rechts     |
| 128    | 4-Punkt-Stern                  | 340    | Matrix, obere doppelte Spirale                   |
| 129    | 6-punktstern                  | 341    | Matrix, untere doppelte Spirale                |
| 130    | Heart                         | 342    | Matrix, linke doppelte Spirale                  |
| 131    | Keyhole                       | 343    | Matrix, rechts doppelte Spirale                 |
| 201    | Radiale, 12 Uhr            | 344    | Matrix, Quad-Spirale, oben nach unten             |
| 202    | Radiales, 3 Uhr             | 345    | Matrix, Quad-Spirale, linksbündig             |
| 203    | Radiale, 6 Uhr             | 350    | Wasserfall, Links                             |
| 204    | Radiale, 9 Uhr             | 351    | Wasserfall, rechts                            |
| 205    | Radiale, 12 + 6 Uhr        | 352    | Wasserfall, Horizontal, Links                 |
| 206    | Radiale, 3 + 9 Uhr         | 353    | Wasserfall, Horizontal, rechts                |
| 207    | Radiales, 4-Wege-                 | 409    | Zufällige Maske                                 |



 

 

 



