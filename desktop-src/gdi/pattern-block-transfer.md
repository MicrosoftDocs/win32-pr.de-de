---
description: Der Name der patblt-Funktion (eine Abkürzung für die Musterblock Übertragung) impliziert, dass diese Funktion einfach den Pinsel (oder das Muster) repliziert, bis Sie ein angegebenes Rechteck füllt.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Muster Block Übertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993934"
---
# <a name="pattern-block-transfer"></a>Muster Block Übertragung

Der Name der [**patblt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) -Funktion (eine Abkürzung für die Musterblock Übertragung) impliziert, dass diese Funktion einfach den Pinsel (oder das Muster) repliziert, bis Sie ein angegebenes Rechteck füllt. Allerdings ist die-Funktion tatsächlich viel leistungsfähiger. Vor dem Replizieren des Pinsels werden die Farbdaten für das Muster mit den Farbdaten für die vorhandenen Pixel in der Videoanzeige mithilfe eines Raster Vorgangs (ROP) kombiniert. Ein ROP ist eine bitweise Operation, die auf die Bits der Farbdaten für den replizierten Pinsel und die Bits der Farbdaten für das Ziel Rechteck auf dem Anzeigegerät angewendet wird. Es sind 256 ROPS vorhanden. die **patblt** -Funktion erkennt jedoch nur diejenigen, die ein Muster und ein Ziel erfordern (nicht diejenigen, die eine Quelle erfordern). In der folgenden Tabelle sind die gängigsten ROPS aufgeführt.



| PS       | BESCHREIBUNG                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| Patcopy   | Kopiert das Muster in die Ziel Bitmap.                                       |
| Patinvert | Kombiniert die Ziel Bitmap mit dem Muster mithilfe des booleschen XOR-Operators. |
| Dstinvert | Kehrt die Ziel Bitmap um.                                                     |
| Blackness | Wandelt die gesamte Ausgabe in binäre Nullen um.                                                   |
| Whitheit | Wandelt die gesamte Ausgabe in binäre Dateien um.                                                    |



 

Weitere Informationen finden Sie unter [Raster Vorgangs Codes](raster-operation-codes.md).

 

 



