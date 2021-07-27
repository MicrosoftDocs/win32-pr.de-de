---
title: REFERENZ ZUM BC7-Formatmodus
description: Diese Dokumentation enthält eine Liste der 8 Blockmodi und Bitzuordnungen für BC7-Texturkomprimierungsformatblöcke.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9756582d7d5ac52d4c16b2f4734decebbd66ae8
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436105"
---
# <a name="bc7-format-mode-reference"></a>REFERENZ ZUM BC7-Formatmodus

Diese Dokumentation enthält eine Liste der 8 Blockmodi und Bitzuordnungen für BC7-Texturkomprimierungsformatblöcke.

Die Farben für jede Teilmenge innerhalb eines Blocks werden durch zwei explizite Endpunktfarben und einen Satz interpolierter Farben zwischen ihnen dargestellt. Je nach Indexgenauigkeit des Blocks kann jede Teilmenge 4, 8 oder 16 mögliche Farben haben.

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

BC7 Mode 0 hat die folgenden Merkmale:

-   Nur Farbkomponenten (kein Alpha)
-   3 Teilmengen pro Block
-   RGBP 4.4.4.1-Endpunkte mit einem eindeutigen P-Bit pro Endpunkt
-   3-Bit-Indizes
-   16 Partitionen

![0-Bit-Moduslayout](images/bc7-mode0.png)

## <a name="mode-1"></a>Modus 1

BC7-Modus 1 hat die folgenden Merkmale:

-   Nur Farbkomponenten (kein Alpha)
-   2 Teilmengen pro Block
-   RGBP 6.6.6.1-Endpunkte mit einem freigegebenen P-Bit pro Teilmenge)
-   3-Bit-Indizes
-   64 Partitionen

![1-Bit-Moduslayout](images/bc7-mode1.png)

## <a name="mode-2"></a>Modus 2

BC7 Mode 2 hat die folgenden Merkmale:

-   Nur Farbkomponenten (kein Alpha)
-   3 Teilmengen pro Block
-   RGB 5.5.5-Endpunkte
-   2-Bit-Indizes
-   64 Partitionen

![2-Bit-Moduslayout](images/bc7-mode2.png)

## <a name="mode-3"></a>Modus 3

BC7-Modus 3 hat die folgenden Merkmale:

-   Nur Farbkomponenten (kein Alpha)
-   2 Teilmengen pro Block
-   RGBP 7.7.7.1-Endpunkte mit einem eindeutigen P-Bit pro Teilmenge)
-   2-Bit-Indizes
-   64 Partitionen

![3-Bit-Moduslayout](images/bc7-mode3.png)

## <a name="mode-4"></a>Modus 4

BC7 Mode 4 hat die folgenden Merkmale:

-   Farbkomponenten mit separater Alphakomponente
-   1 Teilmenge pro Block
-   RGB 5.5.5-Farbendpunkte
-   6-Bit-Alphaendpunkte
-   16 x 2-Bit-Indizes
-   16 x 3-Bit-Indizes
-   2-Bit-Komponentenrotation
-   1-Bit-Indexauswahl (unabhängig davon, ob die 2- oder 3-Bit-Indizes verwendet werden)

![4-Bit-Moduslayout](images/bc7-mode4.png)

## <a name="mode-5"></a>Modus 5

BC7 Mode 5 hat die folgenden Merkmale:

-   Farbkomponenten mit separater Alphakomponente
-   1 Teilmenge pro Block
-   RGB 7.7.7-Farbendpunkte
-   8-Bit-Alphaendpunkte
-   16 x 2-Bit-Farbindizes
-   16 x 2-Bit-Alphaindizes
-   2-Bit-Komponentenrotation

![5-Bit-Moduslayout](images/bc7-mode5.png)

## <a name="mode-6"></a>Modus 6

BC7 Mode 6 hat die folgenden Merkmale:

-   Kombinierte Farb- und Alphakomponenten
-   Eine Teilmenge pro Block
-   RGBAP 7.7.7.7.1-Farbendpunkte (und Alphaendpunkte) (eindeutigeS P-Bit pro Endpunkt)
-   16 x 4-Bit-Indizes

![6-Bit-Moduslayout](images/bc7-mode6.png)

## <a name="mode-7"></a>Modus 7

BC7 Mode 7 hat die folgenden Merkmale:

-   Kombinierte Farb- und Alphakomponenten
-   2 Teilmengen pro Block
-   RGBAP 5.5.5.5.1-Farbendpunkte (und Alphaendpunkte) (eindeutigeS P-Bit pro Endpunkt)
-   2-Bit-Indizes
-   64 Partitionen

![7-Bit-Moduslayout](images/bc7-mode7.png)

## <a name="remarks"></a>Hinweise

Modus 8 (das am wenigsten signifikante Byte ist auf 0x00) ist reserviert. Verwenden Sie sie nicht in Ihrem Encoder. Wenn Sie diesen Modus an die Hardware übergeben, wird ein mit allen Nullen initialisierter Block zurückgegeben.

In BC7 können Sie die Alphakomponente auf eine der folgenden Arten codieren:

-   Blocktypen ohne explizite Alphakomponentencodierung. In diesen Blöcken verfügen die Farbendpunkte über eine nur RGB-Codierung, bei der die Alphakomponente für alle Texel auf 1,0 decodiert wird.
-   Blocktypen mit kombinierten Farb- und Alphakomponenten. In diesen Blöcken werden die Endpunktfarbwerte im RGBA-Format angegeben, und die Alphakomponentenwerte werden zusammen mit den Farbwerten interpoliert.
-   Blocktypen mit getrennten Farb- und Alphakomponenten. In diesen Blöcken werden die Farb- und Alphawerte separat angegeben, jeweils mit einem eigenen Satz von Indizes. Daher verfügen sie über einen effektiven Vektor und einen separat codierten Skalarkanal, wobei der Vektor häufig die Farbkanäle R, G, B und der Skalar den Alphakanal \[ A \] \[ \] angibt. Zur Unterstützung dieses Ansatzes wird ein separates 2-Bit-Feld in der Codierung bereitgestellt, das die Angabe der separaten Kanalcodierung als Skalarwert ermöglicht. Daher kann der -Block eine der folgenden vier verschiedenen Darstellungen dieser Alphacodierung haben (wie durch das 2-Bit-Feld angegeben):
    -   RGB \| A: Alphakanal getrennt
    -   COLOR \| R: "roter" Farbkanal getrennt
    -   TIPP \| G: "grüner" Farbkanal getrennt
    -   RGA \| B: "blauer" Farbkanal getrennt

    Der Decoder ordnet die Kanal reihenfolge nach der Decodierung wieder zu RGBA zurück, sodass das interne Blockformat für den Entwickler nicht sichtbar ist. Blöcke mit separaten Farb- und Alphakomponenten verfügen auch über zwei Sätze von Indexdaten: einen für den vektorierten Satz von Kanälen und einen für den Skalarkanal. (Im Fall von Modus 4 haben diese Indizes eine unterschiedliche Breite \[ von 2 oder 3 \] Bits. Modus 4 enthält auch einen 1-Bit-Selektor, der angibt, ob der Vektor oder der Skalarkanal die 3-Bit-Indizes verwendet.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[BC7-Format](bc7-format.md)
</dt> </dl>

 

 




