---
title: CMY- und CMYK-Farbraum
description: Die CMY- und CMYK-Farbräume werden häufig beim Farbdruck verwendet. Ein CMY-Farbraum verwendet Cyan, Magenta und Gelb (CMY) als Primärfarben. Rot, Grün und Blau sind die sekundären Farben.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Color System (WCS), CMY-Farbräume
- WCS (Windows Color System), CMY-Farbräume
- Bildfarbverwaltung, CMY-Farbräume
- Farbverwaltung, CMY-Farbräume
- Farben, CMY-Farbräume
- Farbräume, CMY
- CMY-Farbräume
- Windows Color System (WCS), CMYK-Farbräume
- WCS (Windows Color System), CMYK-Farbräume
- Bildfarbverwaltung, CMYK-Farbräume
- Farbverwaltung, CMYKcolor-Leerzeichen
- Farben, CMYK-Farbräume
- Farbräume, CMYK
- CMYK-Farbräume
- cyan
- magenta
- yellow
- cyan magenta yellow (CMY)
- CMY (cyan magenta yellow)
- cyan magenta yellow black (CMYK)
- CMYK (cyan magenta yellow black)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcb1ea33bd32346dd541894342ec4af02274e4381eaf0c1925e2a4bc20e10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452099"
---
# <a name="cmy-and-cmyk-color-spaces"></a>CMY- und CMYK-Farbraum

Die [CMY-](c.md) und CMYK-Farbräume werden häufig beim Farbdruck verwendet. Ein CMY-Farbraum verwendet Cyan, Magenta und Gelb (CMY) als [Primärfarben.](p.md) Rot, Grün und Blau sind die sekundären Farben.

Die folgenden Abbildungen sind Farbdarstellungen des CMY-Farbraums. Der CMY-Farbraum wird normalisiert.

![Cmy-Farbraumcube mit Maximalwerten](images/cmyclrs1.png)

![Cmy-Farbraumcube mit Mindestwerten](images/cmyclrs2.png)

Der CMY-Farbraum ist subtrahtiv. Daher ist Weiß bei (0,0, 0,0, 0,0) und schwarz bei (1,0, 1,0, 1,0). Wenn Sie mit Weiß beginnen und keine Farben subtrahieren, erhalten Sie Weiß. Wenn Sie mit Weiß beginnen und alle Farben gleichmäßig subtrahieren, erhalten Sie Schwarz.

Der CMYK-Farbraum ist eine Variation des CMY-Modells. Es wird schwarz (Cyan, Magenta, Yellow und blacK) hinzugefügt. Der CMYK-Farbraum schließt die Lücke zwischen Theorie und Praxis. Theoretisch ist die zusätzliche schwarze Komponente nicht erforderlich. Die Erfahrung mit verschiedenen Arten von Farben und Dokumenten hat jedoch gezeigt, dass das Ergebnis in der Regel dunkelblau und nicht schwarz ist, wenn gleiche Komponenten von Cyan-, Magenta- und gelben Farben gemischt sind. Das Hinzufügen von Schwarzer Ink zur Mischung löst dieses Problem.

Die CMY- und CMYK-Farbräume können geräteunabhängig sein, aber meistens werden sie als Verweis auf ein bestimmtes Gerät verwendet.

 

 




