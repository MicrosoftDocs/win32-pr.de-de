---
description: Die folgenden Funktionen werden mit Regionen verwendet.
ms.assetid: 3a42fc7a-4c07-4540-99a7-520f99532f33
title: Regions Funktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0f55549f978dd2868f231b9ff042f6f825459d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978345"
---
# <a name="region-functions-windows-gdi"></a>Regions Funktionen (Windows GDI)

Die folgenden Funktionen werden mit Regionen verwendet.



| Funktion                                                       | BESCHREIBUNG                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Combinergn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)                               | Kombiniert zwei Bereiche und speichert das Ergebnis in einer dritten Region.                                |
| [**"Kreateellipticrgn"**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)                 | Erstellt einen elliptischen Bereich.                                                                |
| [**"Kreateellipticrgnindirekte"**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) | Erstellt einen elliptischen Bereich.                                                                |
| [**"Kreatepolygonrgn"**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)                   | Erstellt einen polygonalen Bereich.                                                                  |
| [**"Kreatepolypolygonrgn"**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)           | Erstellt einen Bereich, der aus einer Reihe von Polygonen besteht.                                         |
| [**"Kreaterectrgn"**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)                         | Erstellt einen rechteckigen Bereich.                                                                |
| [**"Kreaterectrgnindirekte"**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)         | Erstellt einen rechteckigen Bereich.                                                                |
| [**"Kreateroundrectrgn"**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)               | Erstellt einen rechteckigen Bereich mit abgerundeten Ecken.                                           |
| [**Equalrgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn)                                   | Überprüft die beiden angegebenen Regionen, um zu bestimmen, ob Sie identisch sind.                    |
| [**Extkreateregion**](/windows/desktop/api/Wingdi/nf-wingdi-extcreateregion)                     | Erstellt einen Bereich aus dem angegebenen Bereich und den Transformations Daten.                          |
| [**Fillrgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn)                                     | Füllt einen Bereich mit dem angegebenen Pinsel.                                                 |
| [**Framergn**](/windows/desktop/api/Wingdi/nf-wingdi-framergn)                                   | Zeichnet mit dem angegebenen Pinsel einen Rahmen um den angegebenen Bereich.                     |
| [**Getpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)                     | Ruft den aktuellen Polygon Füll Modus ab.                                                     |
| [**GetRegionData**](/windows/desktop/api/Wingdi/nf-wingdi-getregiondata)                         | Füllt den angegebenen Puffer mit Daten, die einen Bereich beschreiben.                                    |
| [**Getrgnbox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox)                                 | Ruft das umgebende Rechteck des angegebenen Bereichs ab.                                    |
| [**Umkehren**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn)                                 | Kehrt die Farben im angegebenen Bereich um.                                                  |
| [**Offort**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)                                 | Verschiebt einen Bereich um die angegebenen Offsets.                                                     |
| [**Paintrgn**](/windows/desktop/api/Wingdi/nf-wingdi-paintrgn)                                   | Zeichnet den angegebenen Bereich mithilfe des derzeit im Gerätekontext ausgewählten Pinsels.   |
| [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion)                               | Bestimmt, ob sich der angegebene Punkt innerhalb des angegebenen Bereichs befindet.                       |
| [**Rectinregion**](/windows/desktop/api/Wingdi/nf-wingdi-rectinregion)                           | Bestimmt, ob ein Teil des angegebenen Rechtecks innerhalb der Grenzen eines Bereichs liegt. |
| [**Setpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)                     | Legt den Polygon Füll Modus für Funktionen fest, die Polygone ausfüllen.                                 |
| [**Setrectrgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)                               | Konvertiert einen Bereich in einen rechteckigen Bereich mit den angegebenen Koordinaten.                  |



 

 

 



