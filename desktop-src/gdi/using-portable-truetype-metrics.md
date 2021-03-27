---
description: Anwendungen, die die TrueType-textmetriken verwenden, können einen hohen Grad an Drucker-und dokumentportabilität erzielen. Sie können TrueType-Metriken auch dann verwenden, wenn Sie mit den frühen 16-Bit-Versionen von Windows kompatibel sein müssen.
ms.assetid: 29b54315-7c4e-4b8c-ad79-0b85c7386860
title: Verwenden portabler TrueType-Metriken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83360b620bde11e20726b0ee4124d35bf6cf00b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994566"
---
# <a name="using-portable-truetype-metrics"></a>Verwenden portabler TrueType-Metriken

Anwendungen, die die TrueType-textmetriken verwenden, können einen hohen Grad an Drucker-und dokumentportabilität erzielen. Sie können TrueType-Metriken auch dann verwenden, wenn Sie mit den frühen 16-Bit-Versionen von Windows kompatibel sein müssen.

Mithilfe von Entwurfs breiten werden die meisten Probleme mit Geräte abhängigem Text, der von physischen Geräten eingeführt wurde, gelöst. Entwurfs breiten sind eine Art logischer Breite. Unabhängig von den rasterisierungsproblemen oder der Skalierung von Transformationen weist jedes Symbol eine logische Breite und Höhe auf. Jedes Zeichen in einer Zeichenfolge besteht aus einer logischen Seite, die unabhängig von der physischen Gerätebreite ist. Obwohl eine logische Breite impliziert, dass breiten bei allen Punktgrößen linear skaliert werden können, gilt dies nicht unbedingt für nicht Portable oder die meisten TrueType-Schriftarten. Bei kleineren Punktgrößen werden einige Symbole relativ zu ihrer Höhe erhöht, um die Lesbarkeit zu verbessern.

Die Zeichen in TrueType-Kern Schriftarten sind auf das Raster 2048 nach 2048 ausgelegt. Die Entwurfs Breite ist die Breite eines Zeichens in diesen Raster Einheiten. (TrueType unterstützt alle ganzzahligen Raster Größen von bis zu 16.384 bis 16.384. Raster Größen, bei denen es sich um ganzzahlige Potenzen von 2 handelt

Die Schriftart Gliederung ist in imaginärer-Einheiten konzipiert. Das EM-Quadrat ist das Knoten Raster, für das die Schriftart Kontur angepasst ist. (Sie können das **otmemsquare** -Element von [outlinetextmetric](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) und den **ntmsizeem** -Member von [newtextmetric](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) verwenden, um die Größe des EM-Quadrats in imaginärer-Einheiten abzurufen.) Wenn eine Schriftart erstellt wird, deren Punktgröße (in Geräte Einheiten) gleich der Größe des zugehörigen EM-Quadrats ist, sind die ABC-breiten für diese Schriftart die gewünschte Entwurfs Breite. Angenommen, die Größe eines EM-Quadrats ist 1000, und die ABC-Breite eines Zeichens in der Schriftart beträgt 150, 400 und 150. Ein Zeichen in dieser Schriftart, das 10 Geräte Einheiten hoch ist, verfügt über die ABC-Breite 1,5, 4 bzw. 1,5. Da der mm \_ -Text-Mapping-Modus am häufigsten mit Schriftarten verwendet wird (und mm- \_ Text entspricht Geräte Einheiten), handelt es sich hierbei um eine einfache Berechnung.

Aufgrund der hohen Auflösung der TrueType-Entwurfs Breite müssen Anwendungen, die diese verwenden, die großen numerischen Werte berücksichtigen, die erstellt werden können. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Geräte im Vergleich zu Entwurfs Einheiten](device-vs--design-units.md)
-   [Metriken für Portable Dokumente](metrics-for-portable-documents.md)

 

 



