---
description: Unterobjekte
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Unterobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf828d0049816c0cbf932b96344b0270c4c9dbfb835a0750736551ff67b319b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633480"
---
# <a name="subobjects"></a>Unterobjekte

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Quellen, Effekte und Übergänge verfügen über interne Zeiger auf andere COM-Objekte, die als *Unterobjekte bezeichnet werden.* Das Unterobjekt führt die eigentliche Arbeit des Objekts aus. Das Unterobjekt einer Quelle ist die Komponente, die die Video- oder Audiodaten erstellt. Das Unterobjekt eines Effekts oder Übergangs ist die Komponente, die die Daten transformiert. Beispielsweise wird in einem Videoeffekt der visuelle Effekt im Videostream erstellt.

Der Typ des Unterobjekts hängt vom Typ des Objekts ab:

-   Quelle: Jeder DirectShow-Quellfilter oder Parserfilter, der such- und erzeugt ein Format erzeugt, das DES unterstützt. Es kann ein komprimiertes Format sein, wenn DirectShow-Filter vorhanden sind, um es zu decodieren.
-   Auswirkung: Für Videos werden alle 2D-1-Eingaben von Microsoft® DirectX® Transform-Objekt verwendet. Für Audio, einen beliebigen DirectShow-Audioeffektfilter.
-   Übergang: Für Videos jedes 2D-DirectX Transform-Objekt mit zwei Eingaben. Audio unterstützt keine Übergänge.

Gruppen, Kompositionen und Spuren verfügen nicht über Unterobjekte.

Die Anwendung setzt den Unterobjektzeiger nicht direkt. Für Effekte und Übergänge ruft die Anwendung die [**IAMTimelineObj::SetSubObjectGUID-Methode**](iamtimelineobj-setsubobjectguid.md) auf, um die GUID des Unterobjekts anzugeben. Bei Quellobjekten ruft eine Anwendung in der Regel [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) auf, um den Namen einer Quelldatei anzugeben. Die **SetSubObjectGUID-Methode** kann jedoch auch für Quellobjekte verwendet werden, um den Klassenbezeichner (CLSID) eines Filters anzugeben.

Weitere Informationen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md) und Arbeiten mit [Effekten und Übergängen.](working-with-effects-and-transitions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Zeitachsenkomponenten](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



