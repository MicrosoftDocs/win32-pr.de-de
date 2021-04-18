---
title: CMY- und CMYK-Farbraum
description: Die CMY-und CMYK-Farbbereiche werden häufig beim Drucken von Farben verwendet. Ein CMY-Farbraum verwendet Cyan, Magenta und gelb (CMY) als primäre Farben. Rot, grün und blau sind die sekundären Farben.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Color System (WCS), CMY Color Spaces
- WCS (Windows Color System), CMY Color Spaces
- Bild Farbverwaltung, CMY-Farbraum
- Farbverwaltung, CMY-Farbbereiche
- Farben, CMY-Farbbereiche
- Farbbereiche, CMY
- CMY-Farbbereiche
- Windows Color System (WCS), CMYK-Farbraum
- WCS (Windows Color System), CMYK-Farbraum
- Bild Farbverwaltung, CMYK-Farbraum
- Farbverwaltung, cmykcolor-Leerzeichen
- Farben, CMYK-Farbraum
- Farbbereiche, CMYK
- CMYK-Farbraum
- cyan
- magenta
- yellow
- Zyan Magenta Gelb (CMY)
- CMY (Cyan Magenta Gelb)
- Zyan Magenta Gelb Schwarz (CMYK)
- CMYK (Cyan Magenta gelb schwarz)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106354883"
---
# <a name="cmy-and-cmyk-color-spaces"></a>CMY- und CMYK-Farbraum

Die CMY-und CMYK- [Farbbereiche](c.md) werden häufig beim Drucken von Farben verwendet. Ein CMY-Farbraum verwendet Cyan, Magenta und gelb (CMY) als [primäre Farben](p.md). Rot, grün und blau sind die sekundären Farben.

Die folgenden Abbildungen sind Farbdarstellungen des CMY-Farbraum. Der CMY-Farbraum wird normalisiert.

![CMY-Farb Raum Cube mit maximalen Werten](images/cmyclrs1.png)

![CMY-Farb Raum Cube mit minimalen Werten](images/cmyclrs2.png)

Der CMY-Farbraum ist Subtraktiv. Daher befindet sich weiß an (0,0, 0,0, 0,0) und schwarz auf (1,0, 1,0, 1,0). Wenn Sie mit weiß beginnen und keine Farben subtrahieren, erhalten Sie weiß. Wenn Sie mit weiß beginnen und alle Farben gleichmäßig subtrahieren, werden Sie schwarz.

Der CMYK-Farbraum ist eine Variation des CMY-Modells. Er fügt schwarz (Cyan, Magenta, gelb und schwarz) hinzu. Der CMYK-Farbraum schließt die Lücke zwischen Theorie und Praxis. Theoretisch ist die extra schwarze Komponente nicht erforderlich. Allerdings hat die Darstellung mit verschiedenen Arten von Farben und Dokumenten gezeigt, dass das Ergebnis in der Regel eine dunkelbraune, nicht schwarz ist, wenn die gleichen Komponenten von Cyan, Magenta und gelben Farben gemischt werden. Durch das Hinzufügen von blackink zur Mischung wird dieses Problem gelöst.

Die "CMY"-und "CMYK"-Farben können Geräte unabhängig sein, aber Sie werden in den meisten Fällen als Verweis auf ein bestimmtes Gerät verwendet.

 

 




