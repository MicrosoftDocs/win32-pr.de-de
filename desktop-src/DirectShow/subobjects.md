---
description: Unter Objekte
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Unter Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867083"
---
# <a name="subobjects"></a>Unter Objekte

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Quellen, Effekte und Übergänge verfügen über interne Zeiger auf andere COM-Objekte, die als unter *geordnete* Objekte bezeichnet werden. Das untergeordnete Objekt führt die eigentliche Arbeit des-Objekts aus. Das untergeordnete Objekt einer Quelle ist die Komponente, mit der die Video-oder Audiodaten erstellt werden. Das untergeordnete Objekt eines Effekts oder Übergangs ist die Komponente, die die Daten transformiert. Beispielsweise werden in einem Videoeffekt die visuellen Effekte im Videostream erstellt.

Der Typ des untergeordneten Objekts hängt vom Objekttyp ab:

-   Quelle: jeder DirectShow-Quell Filter oder Parserfilter, der Suchvorgänge unterstützt und ein von der unterstützte Format unterstützt. Es kann ein komprimiertes Format sein, wenn DirectShow-Filter vorhanden sind, um es zu decodieren.
-   Auswirkung: bei einem Video werden alle 2D-Eingaben von Microsoft® DirectX® Transform-Objekt. Für Audiodaten wird ein beliebiger DirectShow-audiowirkungs Filter verwendet.
-   Übergang: bei einem Video handelt es sich um ein beliebiges 2D-DirectX-Transformations Objekt mit zwei Eingaben. Das Audioformat unterstützt keine Übergänge.

Gruppen, Kompositionen und Spuren verfügen über keine unter Objekte.

Der untergeordnete Zeiger wird von der Anwendung nicht direkt festgelegt. Bei Effekten und Übergängen Ruft die Anwendung die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode auf, um die GUID des unter Objekts anzugeben. Bei Quell Objekten Ruft eine Anwendung in der Regel [**iamtimelinesrc:: setmedianame**](iamtimelinesrc-setmedianame.md) auf, um den Namen einer Quelldatei anzugeben. Die **setsubobjectguid** -Methode kann jedoch auch für Quell Objekte verwendet werden, um den Klassen Bezeichner (CLSID) eines Filters anzugeben.

Weitere Informationen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md) und [Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Zeitachsen Komponenten](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



