---
title: Bzw bc7-formatmodusverweis
description: Diese Dokumentation enthält eine Liste der 8 Block Modi und bitbelegungen für bzw bc7 Textur Komprimierungs-Format Blöcke.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2020
ms.locfileid: "104389727"
---
# <a name="bc7-format-mode-reference"></a>Bzw bc7-formatmodusverweis

Diese Dokumentation enthält eine Liste der 8 Block Modi und bitbelegungen für bzw bc7 Textur Komprimierungs-Format Blöcke.

Die Farben für jede Teilmenge innerhalb eines Blocks werden von zwei expliziten Endpunkt Farben und einem Satz interversierter Farben zwischen Ihnen dargestellt. Abhängig von der Index Genauigkeit des Blocks kann jede Teilmenge über 4, 8 oder 16 mögliche Farben verfügen.

-   [Modus 0](#mode-0)
-   [Modus 1](#mode-1)
-   [Modus 2](#mode-2)
-   [Modus 3](#mode-3)
-   [Modus 4](#mode-4)
-   [Modus 5](#mode-5)
-   [Modus 6](#mode-6)
-   [Modus 7](#mode-7)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="mode-0"></a>Modus 0

Bzw bc7 Mode 0 weist die folgenden Eigenschaften auf:

-   Nur Farbkomponenten (kein Alpha)
-   3 Teilmengen pro Block
-   Rgbp 4.4.4.1 Endpunkte mit einem eindeutigen P-Bit pro Endpunkt
-   3-Bit-Indizes
-   16 Partitionen

![Mode 0-bitlayout](images/bc7-mode0.png)

## <a name="mode-1"></a>Modus 1

Bzw bc7 Mode 1 weist die folgenden Eigenschaften auf:

-   Nur Farbkomponenten (kein Alpha)
-   2 Teilmengen pro Block
-   Rgbp 6.6.6.1-Endpunkte mit einem freigegebenen P-Bit pro Teilmenge)
-   3-Bit-Indizes
-   64 Partitionen

![Mode-1-Bit-Layout](images/bc7-mode1.png)

## <a name="mode-2"></a>Modus 2

Bzw bc7 Mode 2 weist die folgenden Eigenschaften auf:

-   Nur Farbkomponenten (kein Alpha)
-   3 Teilmengen pro Block
-   RGB 5.5.5 Endpunkte
-   2-Bit-Indizes
-   64 Partitionen

![Modus 2 Bit Layout](images/bc7-mode2.png)

## <a name="mode-3"></a>Modus 3

Bzw bc7 Mode 3 weist die folgenden Eigenschaften auf:

-   Nur Farbkomponenten (kein Alpha)
-   2 Teilmengen pro Block
-   Rgbp 7.7.7.1-Endpunkte mit einem eindeutigen P-Bit pro Teilmenge)
-   2-Bit-Indizes
-   64 Partitionen

![Modus 3 Bit Layout](images/bc7-mode3.png)

## <a name="mode-4"></a>Modus 4

Bzw bc7 Mode 4 weist die folgenden Eigenschaften auf:

-   Farbkomponenten mit separater Alpha Komponente
-   1 Teilmenge pro Block
-   RGB 5.5.5 Farb Endpunkte
-   6-Bit-Alpha-Endpunkte
-   16 x 2-Bit-Indizes
-   16 x 3-Bit-Indizes
-   2-Bit-Komponenten Drehung
-   1-Bit-indexselektor (unabhängig davon, ob die Indizes mit 2 oder 3 Bit verwendet werden)

![Modus 4 Bit Layout](images/bc7-mode4.png)

## <a name="mode-5"></a>Modus 5

Bzw bc7 Mode 5 weist die folgenden Eigenschaften auf:

-   Farbkomponenten mit separater Alpha Komponente
-   1 Teilmenge pro Block
-   RGB 7.7.7 Farb Endpunkte
-   8-Bit-Alpha-Endpunkte
-   16 x 2-Bit-Farbindizes
-   16 x 2-Bit-Alpha Indizes
-   2-Bit-Komponenten Drehung

![Layout des 5-Bit-Modus](images/bc7-mode5.png)

## <a name="mode-6"></a>Modus 6

Bzw bc7 Mode 6 weist die folgenden Eigenschaften auf:

-   Kombinierte Farbe und Alpha Komponenten
-   Eine Teilmenge pro Block
-   Rgbap 7.7.7.7.1 Farbe (und Alpha) Endpunkte (eindeutiges P-Bit pro Endpunkt)
-   16 x 4-Bit-Indizes

![Modus 6 Bit Layout](images/bc7-mode6.png)

## <a name="mode-7"></a>Modus 7

Bzw bc7 Mode 7 weist die folgenden Eigenschaften auf:

-   Kombinierte Farbe und Alpha Komponenten
-   2 Teilmengen pro Block
-   Rgbap 5.5.5.5.1 Farbe (und Alpha) Endpunkte (eindeutiges P-Bit pro Endpunkt)
-   2-Bit-Indizes
-   64 Partitionen

![Modus 7 Bit Layout](images/bc7-mode7.png)

## <a name="remarks"></a>Bemerkungen

Modus 8 (das am wenigsten signifikante Byte ist auf 0x00 festgelegt) ist reserviert. Verwenden Sie Sie nicht in Ihrem Encoder. Wenn Sie diesen Modus an die Hardware übergeben, wird ein Block zurückgegeben, der mit allen Nullen initialisiert wird.

In bzw bc7 können Sie die Alpha Komponente auf eine der folgenden Arten codieren:

-   Block Typen ohne explizite Alpha Komponenten Codierung. In diesen Blöcken haben die Farb Endpunkte eine nur-RGB-Codierung, wobei die Alpha Komponente für alle Texels in 1,0 decodiert wird.
-   Block Typen mit kombinierten Farben und Alpha Komponenten. In diesen Blöcken werden die endpunktfarbwerte im RGBA-Format angegeben, und die Alpha Komponenten Werte werden zusammen mit den Farbwerten interpoliert.
-   Block Typen mit getrennten Farben und Alpha Komponenten. In diesen Blöcken werden die Werte für Farbe und Alpha separat angegeben, jeweils mit einem eigenen Satz von Indizes. Demzufolge verfügen Sie über einen effektiven Vektor und einen skalarchannel, der separat codiert ist, wobei der Vektor häufig die Farbkanäle \[ R, G \] und B angibt und der Skalar den Alphakanal \[ a angibt \] . Zur Unterstützung dieses Ansatzes wird in der Codierung ein separates 2-Bit-Feld bereitgestellt, das die Angabe der separaten Kanalcodierung als Skalarwert ermöglicht. Folglich kann der-Block eine der folgenden vier unterschiedlichen Darstellungen dieser Alpha Codierung aufweisen (wie durch das 2-Bit-Feld angegeben):
    -   RGB \| A: separater Alphakanal
    -   AGB \| R: "Roter" Farbkanal getrennt
    -   Rab \| G: "grüner" Farbkanal getrennt
    -   RGA \| B: "blauer" Farbkanal getrennt

    Der Decoder ordnet die Kanal Reihenfolge nach der Decodierung an RGBA zurück, sodass das interne Block Format für den Entwickler unsichtbar ist. Schwarze mit separaten Farb-und Alpha Komponenten verfügen auch über zwei Sätze von Indexdaten: einen für den Vektor Satz von Kanälen und einen für den skalaren Kanal. (Im Fall von Modus 4 haben diese Indizes eine abweichende Breite von \[ 2 oder 3 Bits \] . In Modus 4 ist auch ein 1-Bit-Selektor enthalten, der angibt, ob der Vektor oder der skalare Kanal die 3-Bit-Indizes verwendet.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bzw bc7-Format](bc7-format.md)
</dt> </dl>

 

 




