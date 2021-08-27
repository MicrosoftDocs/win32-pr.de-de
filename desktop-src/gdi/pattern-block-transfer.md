---
description: Der Name der PatBlt-Funktion (eine Abkürzung für die Musterblockübertragung) impliziert, dass diese Funktion einfach den Pinsel (oder das Muster) repliziert, bis sie ein angegebenes Rechteck füllt.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Musterblockübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecb51cbe12da80ca643e2d520e8ebe25c4c9fe03d56a8a16e0c55caf5f1ce10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092930"
---
# <a name="pattern-block-transfer"></a>Musterblockübertragung

Der Name der [**PatBlt-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (eine Abkürzung für die Musterblockübertragung) impliziert, dass diese Funktion einfach den Pinsel (oder das Muster) repliziert, bis sie ein angegebenes Rechteck füllt. Die Funktion ist jedoch wesentlich leistungsfähiger. Vor dem Replizieren des Pinsels werden die Farbdaten für das Muster mit den Farbdaten für die vorhandenen Pixel auf der Videoanzeige kombiniert, indem ein Rastervorgang (ROP) verwendet wird. Ein ROP ist ein bitweiser Vorgang, der auf die Bits von Farbdaten für den replizierten Pinsel und die Bits von Farbdaten für das Zielrechteck auf dem Anzeigegerät angewendet wird. Es gibt 256 ROPs. Die **PatBlt-Funktion** erkennt jedoch nur diejenigen, die ein Muster und ein Ziel erfordern (nicht diejenigen, die eine Quelle erfordern). In der folgenden Tabelle sind die gängigsten ROPs aufgeführt.



| Rop       | BESCHREIBUNG                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| PATCOPY   | Kopiert das Muster in die Zielbitmap.                                       |
| PATINVERT | Kombiniert die Zielbitmap mit dem Muster unter Verwendung des booleschen XOR-Operators. |
| DSTINVERT | Invertiert die Zielbitmap.                                                     |
| Schwärze | Wandelt die gesamte Ausgabe in binäre Nullen um.                                                   |
| Weiße | Wandelt alle Ausgaben in binäre Ausgaben um.                                                    |



 

Weitere Informationen finden Sie unter [Rasteroperationscodes.](raster-operation-codes.md)

 

 



