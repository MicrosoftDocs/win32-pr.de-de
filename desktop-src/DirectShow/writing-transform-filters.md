---
description: Schreiben von Transformations Filtern
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Schreiben von Transformations Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959937"
---
# <a name="writing-transform-filters"></a>Schreiben von Transformations Filtern

In diesem Abschnitt wird beschrieben, wie ein Transformations Filter geschrieben wird, der als Filter mit genau einer Eingabe-PIN und einer Ausgabe-PIN definiert ist. Um die Schritte zu veranschaulichen, wird in diesem Abschnitt ein hypothetischer Transformations Filter beschrieben, der ein RLE-Video (Run-Length-codiert) ausgibt. Der RLE-Codierungs Algorithmus selbst wird nicht beschrieben, sondern nur die Aufgaben, die für DirectShow spezifisch sind. (DirectShow stellt bereits einen RLE-Codec über den [AVI-Kompressor](avi-compressor-filter.md) -Filter bereit.)

In diesem Abschnitt wird davon ausgegangen, dass Sie die DirectShow-Basisklassen Bibliothek verwenden, um Filter zu erstellen. Obwohl Sie einen Filter ohne diesen schreiben können, wird dringend empfohlen, die Basisklassen Bibliothek zu erstellen.

> [!Note]  
> Vor dem Schreiben eines Transformations Filters sollten Sie überprüfen, ob ein DirectX-Medienobjekt (DMO) Ihre Anforderungen erfüllt. DMOS kann viele der gleichen Aufgaben wie Filter ausführen, und das Programmiermodell für DMOS ist einfacher. DMOS werden in DirectShow über den [DMO-Wrapper](dmo-wrapper-filter.md) Filter gehostet, können aber auch außerhalb von DirectShow verwendet werden. DMOS sind nun die empfohlene Lösung für Encoder und Decoders.

 

Dieser Abschnitt schließt folgende Themen ein:

-   [Schritt 1: Basisklasse auswählen](step-1--choose-a-base-class.md)
-   [Schritt 2: Deklarieren der Filter Klasse](step-2--declare-the-filter-class.md)
-   [Schritt 3. Unterstützung der Medientyp Aushandlung](step-3--support-media-type-negotiation.md)
-   [Schritt 4: Festlegen von zuordnereigenschaften](step-4--set-allocator-properties.md)
-   [Schritt 5: Transformieren des Bilds](step-5--transform-the-image.md)
-   [Schritt 6: Unterstützung für com hinzufügen](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufbauen von DirectShow-Filtern](building-directshow-filters.md)
</dt> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



