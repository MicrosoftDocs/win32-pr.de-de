---
description: Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124106"
---
# <a name="providing-a-custom-video-resizer"></a>Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

> [!Note]  
> Für dieses Feature ist DirectX 9,0 oder höher erforderlich.

 

Wenn [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) (von) die Größe eines Video Quell Clips ändern, ist das Standardverhalten eine *StretchBlt*, die schnell, aber nicht mit Antialiasing versehen ist. Sie können das Größen Änderungs Verhalten ändern, indem Sie eine benutzerdefinierte resialisierung als DirectShow-Transformations Filter implementieren. Der Filter muss die Schnittstelle [**iresize**](iresize.md) verfügbar machen, die es ermöglicht, die Videogröße für die Eingabe und die Ausgabe anzugeben. Weitere Informationen zum Schreiben eines Transformations Filters finden Sie unter [Schreiben von Transformations Filtern](writing-transform-filters.md). Die **ctransformfilter** -Basisklasse wird als Ausgangspunkt empfohlen. Beachten Sie beim Implementieren des Filters Folgendes:

-   Unterstützung der **iresize** -Schnittstelle für den Filter (nicht die Pins).
-   Der Filter sollte nur [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Formate ( \_ Video Info Format) akzeptieren. Ablehnen anderer Format Typen.
-   Das Videoformat von des kann ein beliebiger nicht komprimierter RGB-Typ sein, einschließlich 32-Bit-RGB mit Alpha (mediasubtype \_ ARGB32). Der Filter kann Formate mit **biheight** < 0 (null) auf sichere Weise ablehnen.
-   Bevor die Renderingengine die Ausgabepin des Filters verbindet, wird [**iresize::p UT \_ mediaType**](iresize-put-mediatype.md) aufgerufen, um den Ausgabetyp festzulegen. Es kann auch " [**iresize::p UT \_ size**](iresize-put-size.md) " aufgerufen werden, um die Ausgabegröße anzupassen. Diese beiden Methoden können beliebig oft in beliebiger Reihenfolge aufgerufen werden, bevor die Ausgabe-PIN verbunden wird.
-   Nachdem die Renderingengine eine Verbindung mit der Ausgabe-PIN hergestellt hat, kann Sie die **Put- \_ Größe** erneut Der Filter für die Größenänderung sollte die Ausgabe-PIN erneut mit der neuen Größe verbinden.
-   Strecken Sie in der [**ctransformfilter:: Transform**](ctransformfilter-transform.md) -Methode des Filters das Eingabe Video auf die Ausgabegröße.
-   Der Filter sollte niemals das Diskontinuität-Flag für das Ausgabe Beispiel festlegen oder einen Medientyp an das Ausgabe Beispiel anfügen.
-   Implementieren Sie die **IPersistStream** -Schnittstelle, um den Status des Filters in einer GraphEdit-Datei (grf-Datei) zu speichern. (Dies ist optional, aber zum Testen hilfreich.)

Um den Filter zum Ändern der Größe zu verwenden, muss der Filter als COM-Objekt im System des Benutzers registriert werden. Bevor die Anwendung das Videoprojekt rendert, Fragen Sie die Rendering-Engine nach der [**IRenderEngine2**](irenderengine2.md) -Schnittstelle ab, und nennen Sie [**IRenderEngine2:: setresizerguid**](irenderengine2-setresizerguid.md) mit der CLSID des resizerfilterfilters.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Projekts](rendering-a-project.md)
</dt> </dl>

 

 



