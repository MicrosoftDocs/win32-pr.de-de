---
description: Bitmap-Klassifizierungen
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Bitmap-Klassifizierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215220"
---
# <a name="bitmap-classifications"></a>Bitmap-Klassifizierungen

Es gibt zwei Klassen von Bitmaps:

-   [Geräteunabhängige Bitmaps](device-independent-bitmaps.md) (DIB). Das DIB-Dateiformat wurde entworfen, um sicherzustellen, dass mit einer Anwendung erstellte bitzugeordnete Grafiken geladen und in einer anderen Anwendung angezeigt werden können. dabei bleibt die Darstellung des Originals unverändert.

-   [Geräte abhängige Bitmaps](device-dependent-bitmaps.md) (DDB), die auch als GDI-Bitmaps bezeichnet werden, waren die einzigen Bitmaps, die in früheren Versionen von 16-Bit-Versionen von Microsoft Windows (vor Version 3,0) verfügbar waren. Wenn jedoch die Anzeige Technologie verbessert wurde und die Anzahl der verfügbaren Anzeigegeräte zunimmt, sind bestimmte inhärente Probleme aufgetreten, die nur mit Disb gelöst werden konnten. Es gab z. b. keine Methode zum Speichern (oder abrufen) der Auflösung des Anzeige Typs, für den eine Bitmap erstellt wurde, sodass eine Zeichnungsanwendung nicht schnell feststellen konnte, ob eine Bitmap für den Typ des Videoanzeige Geräts geeignet war, auf dem die Anwendung ausgeführt wurde.

    Trotz dieser Probleme sind DDSB (auch als kompatible Bitmaps bezeichnet) weiterhin für eine bessere GDI-Leistung und in anderen Situationen nützlich.

 

 



