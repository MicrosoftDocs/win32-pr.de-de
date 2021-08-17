---
description: Schreiben von Transformationsfiltern
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Schreiben von Transformationsfiltern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe8329809b6fe93ea33a9842f57733d7539a56e2ac21abfcf304d2ed780e6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816837"
---
# <a name="writing-transform-filters"></a>Schreiben von Transformationsfiltern

In diesem Abschnitt wird beschrieben, wie Sie einen Transformationsfilter schreiben, der als Filter mit genau einem Eingabepin und einem Ausgabepin definiert ist. Zur Veranschaulichung der Schritte wird in diesem Abschnitt ein hypothetischer Transformationsfilter beschrieben, der ein RLE-Video (Run-Length Encoded) ausausgabet. Der RLE-Codierungsalgorithmus selbst wird nicht beschrieben, sondern nur die Aufgaben, die für DirectShow spezifisch sind. (DirectShow bietet bereits einen RLE-Codec über den [FILTER AVI-1.)](avi-compressor-filter.md)

In diesem Abschnitt wird davon ausgegangen, dass Sie die DirectShow-Basisklassenbibliothek verwenden, um Filter zu erstellen. Obwohl Sie einen Filter ohne ihn schreiben können, wird die Basisklassenbibliothek dringend empfohlen.

> [!Note]  
> Überlegen Sie vor dem Schreiben eines Transformationsfilters, ob ein DirectX Media Object (DMO) Ihre Anforderungen erfüllt. DMOs können viele der gleichen Dinge wie Filter tun, und das Programmiermodell für DMOs ist einfacher. DMOs werden in DirectShow über den DMO [Wrapperfilter](dmo-wrapper-filter.md) gehostet, können aber auch außerhalb von DirectShow verwendet werden. DMOs sind jetzt die empfohlene Lösung für Encoder und Decoder.

 

Dieser Abschnitt schließt folgende Themen ein:

-   [Schritt 1: Auswählen einer Basisklasse](step-1--choose-a-base-class.md)
-   [Schritt 2: Deklarieren der Filter-Klasse](step-2--declare-the-filter-class.md)
-   [Schritt 3: Medientypaushandlung unterstützen](step-3--support-media-type-negotiation.md)
-   [Schritt 4. Festlegen von Zuweisungseigenschaften](step-4--set-allocator-properties.md)
-   [Schritt 5. Transformieren des Bilds](step-5--transform-the-image.md)
-   [Schritt 6. Hinzufügen von Unterstützung für COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von DirectShow-Filtern](building-directshow-filters.md)
</dt> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



