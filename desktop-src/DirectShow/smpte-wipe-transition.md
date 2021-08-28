---
description: SMPTE-Löschübergang
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: SMPTE-Löschübergang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40db8097b61d1b750f8e17067bda08f94a54504c8e990656b7416d84a9a1c089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050435"
---
# <a name="smpte-wipe-transition"></a>SMPTE-Löschübergang

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Der SMPTE-Zurücksetzungsübergang erzeugt alle Standardlöschungen, die von der Society of Motion Picture and Tv Engineers (SMPTE) im SMPTE-Dokument 258M-1993 definiert wurden, mit Ausnahme der Quad-Aufteilung.

![Der Übergang zum Löschen wird in Bearbeitung](images/trans-wipe.png)

Klassen-ID (CLSID): {DE75D012-7A65-11D2-8CEA-00A0C9441E20}

CLSID-Variablenname: CLSID \_ DxtJpeg

Name der Beschriftung: "DxtJpeg"

Eigenschaften



| Eigenschaft       | type   | Standard  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BorderColor    | long   | 0x000000 | Farbe des Rahmens um die Ränder des Zurücksetzungsmusters. Der Wert dieses Attributs ist eine Hexadezimalzahl im Format 0x *RRGGBB,* wobei *RR* der rote Wert, *GG* der grüne Wert und *BB* der blaue Wert ist. (Daher sind reines Rot, Grün und Blau 0xFF000, 0x00FF00 und 0x0000FF bzw.) |
| BorderSoftness | long   | 0        | Breite des unscharfen Bereich um die Ränder des Zurücksetzungsmusters. Geben Sie 0 (null) für keinen unscharfen Bereich an.                                                                                                                                                                                                              |
| Rahmenbreite    | long   | 0        | Breite des Vollbildrands entlang der Ränder des Zurücksetzungsmusters. Geben Sie 0 (null) für keinen Rahmen an.                                                                                                                                                                                                                       |
| MaskName       | BSTR   | **NULL** | Wenn nicht **NULL,** gibt den Namen einer JPEG-Datei an, die anstelle einer standardmäßigen, integrierten Zurücksetzung als Zurücksetzungsmaske verwendet werden soll. Die Datei muss einen monotonen Farbverlauf von 8 Bits pro Pixel enthalten. Der Farbverlauf wird als Maske verwendet, um den Fortschritt der Zurücksetzung zu definieren.                                                                 |
| MaskNum        | long   | 1        | Standard-SMPTE-Zurücksetzungscode, der den Stil der zu verwendenden Zurücksetzung an gibt. Eine Liste der Zurücksetzungscodes und der zugehörigen Schemata finden Sie im SMPTE-Dokument 258M-1993.                                                                                                                                                            |
| OffsetX        | long   | 0        | Horizontaler Offset des Zurücksetzungsabdrucks von der Mitte des Bilds. Nur für Werte von **MaskNum** von 101 bis 131 gültig.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Verical offset of the wipe origin from the center of the image. Nur für Werte von **MaskNum** von 101 bis 131 gültig.                                                                                                                                                                                            |
| ReplicateX     | long   | 0        | Gibt an, wie oft das Zurücksetzungsmuster horizontal repliziert werden soll. Nur für Werte von **MaskNum** von 101 bis 131 gültig.                                                                                                                                                                                                |
| Replizieren     | long   | 0        | Gibt an, wie oft das Zurücksetzungsmuster vertikal repliziert werden soll. Nur für Werte von **MaskNum** von 101 bis 131 gültig.                                                                                                                                                                                                  |
| Scalex         | double | 1.0      | Der Betrag, um den die Zurücksetzung horizontal gestreckt werden soll, als Prozentsatz der ursprünglichen Zurücksetzungsdefinition. Nur für Werte von **MaskNum** von 101 bis 131 gültig.                                                                                                                                                         |
| Scaley         | double | 1.0      | Der Betrag, um den die Zurücksetzung vertikal gestreckt werden soll, als Prozentsatz der ursprünglichen Zurücksetzungsdefinition. Nur für Werte von **MaskNum** von 101 bis 131 gültig.                                                                                                                                                           |



 

## <a name="remarks"></a>Hinweise

Dieser Übergang unterstützt die folgenden Standard-SMPTE-Zurücksetzungen:



| Number | BESCHREIBUNG                   | Number | BESCHREIBUNG                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Horizontal                    | 211    | Radial, links-rechts, oben                     |
| 2      | Vertical                      | 212    | Radial, nach oben, rechts                      |
| 3      | Obere linke Seite                    | 213    | Radial, links-rechts, oben unten              |
| 4      | Oben rechts                   | 214    | Radial, nach oben, links rechts                 |
| 5      | Unten rechts                   | 221    | Radial, oben                                 |
| 6      | Unten links                    | 222    | Radial, rechts                               |
| 7      | Vier Ecken                  | 223    | Radial, unten                              |
| 8      | Vier Quadrate                  | 224    | Radial, links                                |
| 21     | Balkentüren, vertikal          | 225    | Radial, oben im Uhrzeigersinn, unterer Uhrzeigersinn     |
| 22     | Barn-Türen, horizontal        | 226    | Radial, links im Uhrzeigersinn, rechts im Uhrzeigersinn     |
| 23     | Obere Mitte                    | 227    | Radial, oben im Uhrzeigersinn, unterer Anticlockwise |
| 24     | Rechte Mitte                  | 228    | Radial, links im Uhrzeigersinn, rechts anticlockwise |
| 25     | Untere Mitte                 | 231    | Radial, obere Teilung                           |
| 26     | Linke Mitte                   | 232    | Radiale, rechte Teilung                         |
| 41     | Diagonal, NW zu SE            | 233    | Radial, untere Teilung                        |
| 42     | Diagonal, NE zu SW            | 234    | Radial, linke Teilung                          |
| 43     | Dreiecke, oben/unten         | 235    | Radiale, obere untere Teilung                    |
| 44     | Dreiecke, links/rechts         | 236    | Radiale, links-rechts-Teilung                    |
| 45     | Diagonaler Stripe, SW zu NE     | 241    | Radiale, linke obere Ecke                     |
| 46     | Diagonaler Stripe, NW zu SE     | 242    | Radiale, linke untere Ecke                  |
| 47     | Cross                         | 243    | Radiale, rechte untere Ecke                 |
| 48     | Diamond Box                   | 244    | Radial, obere rechte Ecke                    |
| 61     | Wedge, top                    | 245    | Radial, oben links, unten rechts              |
| 62     | Wedge, right                  | 246    | Radial, unten links, oben rechts              |
| 63     | Wedge, unten                 | 251    | Zentriert radial, oben                          |
| 64     | Wedge, left                   | 252    | Radiale Mitte, links                         |
| 65     | V                             | 253    | Zentriert radial, unten                       |
| 66     | V, rechts                      | 254    | Radiale Mitte, rechts                        |
| 67     | V, invertiert                   | 261    | Box radial, right                           |
| 68     | V, links                       | 262    | Box radial, top                             |
| 71     | Sawtooth, links                | 263    | Zentriert radial, oben, unten                  |
| 72     | Sawtooth, oben                 | 264    | Radiale Mitte, links, rechts                  |
| 73     | Sawtooth, vertikal            | 301    | Matrix, horizontal                          |
| 74     | Sawtooth, horizontal          | 302    | Matrix, vertikal                            |
| 101    | Feld                           | 303    | Matrix, diagonal, oben links                  |
| 102    | Diamond                       | 304    | Matrix, diagonal, oben rechts                 |
| 103    | Dreieck, nach oben                  | 305    | Matrix, diagonal, unten rechts              |
| 104    | Dreieck, rechts               | 306    | Matrix, diagonal, unten links               |
| 105    | Dreieck, unten              | 310    | Matrix, im Uhrzeigersinn oben links                  |
| 106    | Dreieck, links                | 311    | Matrix, im Uhrzeigersinn oben rechts                 |
| 107    | Pfeil nach oben                | 312    | Matrix, im Uhrzeigersinn unten rechts              |
| 108    | Pfeilkopf, rechts             | 313    | Matrix, im Uhrzeigersinn unten links               |
| 109    | Pfeil nach unten              | 314    | Matrix, anticlockwise top-left              |
| 110    | Pfeilspitze, links              | 315    | Matrix, anticlockwise top-right             |
| 111    | Über- und nach oben                  | 316    | Matrix, anticlockwise bottom-right          |
| 112    | Über- und Nach-Unten-1                | 317    | Matrix, anticlockwise bottom-left           |
| 113    | Sechskant                       | 320    | Matrix, vertikal links oben, oben rechts        |
| 114    | Sechseck, gedreht              | 321    | Matrix, vertikal links unten, unten rechts  |
| 119    | Circle                        | 322    | Matrix, vertikal links oben, unten rechts     |
| 120    | Oval, horizontal              | 323    | Matrix, vertikal unten links, oben rechts     |
| 121    | Oval, vertikal                | 324    | Matrix, horizontal links oben, unten links    |
| 122    | Augen, horizontal               | 325    | Matrix, horizontal oben rechts, unten rechts  |
| 123    | Augen, vertikal                 | 326    | Matrix, horizontal links oben, unten rechts   |
| 124    | Abgerundetes Rechteck, horizontal | 327    | Matrix, horizontal oben rechts, unten links   |
| 125    | Abgerundetes Rechteck, vertikal   | 328    | Matrix, diagonal unten links, oben rechts     |
| 127    | 4-Punkt-Stern                  | 329    | Matrix, diagonal oben links, unten rechts     |
| 128    | 4-Punkt-Stern                  | 340    | Matrix, Top Double-2016                   |
| 129    | 6-Punkt-Stern                  | 341    | Matrix, unteres doppeltes Doppelte                |
| 130    | Heart                         | 342    | Matrix, linker doppelseitiger Kasten                  |
| 131    | Schlüsselloch                       | 343    | Matrix, rechter doppeler Kasten                 |
| 201    | Radial, 12 Uhr            | 344    | Matrix, Quader, top-bottom             |
| 202    | Radial, 3 Uhr             | 345    | Matrix, Quad-Quader, links-rechts             |
| 203    | Radial, 6 Uhr             | 350    | Wasserfall, links                             |
| 204    | Radial, 9 Uhr             | 351    | Wasserfall, rechts                            |
| 205    | Radial, 12 + 6 Uhr        | 352    | Wasserfall, horizontal, links                 |
| 206    | Radial, 3 + 9 Uhr         | 353    | Wasserfall, horizontal, rechts                |
| 207    | Radial, 4-wege                 | 409    | Zufällige Maske                                 |



 

 

 



