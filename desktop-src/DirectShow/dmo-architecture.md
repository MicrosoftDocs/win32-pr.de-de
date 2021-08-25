---
description: DMO Architektur
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: DMO Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2e125fda635c70e03e02af15d12e0ffb4f3ac4d5083eb91a4b99d3d3590e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906490"
---
# <a name="dmo-architecture"></a>DMO Architektur

In diesem Abschnitt wird die Gesamtarchitektur eines DMO.

**Streams**

Ein DMO ist ein Objekt, das *m Eingaben* verwendet und *n Ausgaben* erzeugt. Die Eingaben und Ausgaben werden als Streams *bezeichnet.* Jede DMO verfügt über mindestens einen Stream. Streams sind keine Objekte. Auf sie wird einfach auf der Grundlage DMO Indexnummer verwiesen. Die Anzahl der Streams wird zur Entwurfszeit festgelegt.

**Medientypen**

Alle Daten werden mithilfe eines Medientyps *typiert,* der definiert, wie der Inhalt der Daten interpretiert werden soll. Beispiel: 320 x 240 24-Bit-RGB-Video ist ein Typ. 44,1-Kilohertz (kHz) 16-Bit-Stereo-PCM-Audio ist ein anderer Typ. Medientypen werden mithilfe der [**media DMO TYP-Struktur \_ \_**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) beschrieben. Bevor der Client Daten verarbeiten kann, muss er den Medientyp für jeden Stream auf der DMO.

In der Regel kann ein Stream einen Bereich von Medientypen akzeptieren. Einige DMOs unterstützen eine größere Palette von Typen als andere. Die DMO definieren Methoden für den Client, um die unterstützten Typen zu entdecken. Beispielsweise kann eine DMO RGB-Video in jeder Bittiefe unterstützen, während eine andere möglicherweise nur 24-Bit-RGB unterstützt. Außerdem kann ein DMO auf bestimmte Kombinationen von Ein- und Ausgaben beschränkt sein. Wenn der Eingabetyp beispielsweise 16-Bit-Video ist, erfordert der Ausgabestream möglicherweise dieselbe Bittiefe. Der Client kann die bevorzugten Typen jedes Streams aufzählen und dann bestimmte Kombinationen testen.

**Puffer**

Im Standardmodell DMO der Client separate Eingabepuffer und Ausgabepuffer zu. Die Eingabepuffer werden mit Daten auffüllt und an die DMO, und der DMO schreibt neue Daten in die Ausgabepuffer.

Optional kann ein DMO "in-place"-Verarbeitung unterstützen. Bei der direkten Verarbeitung schreibt DMO Ausgabe direkt in den Eingabepuffer, über die ursprünglichen Daten. Durch die Verarbeitung vor Ort entfällt die Notwendigkeit separater Puffer. Andererseits werden die ursprünglichen Daten verändert, was für einige Anwendungen möglicherweise nicht akzeptabel ist.

Das Standardpuffermodell (nicht direkt) wird über die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) unterstützt. Diese Schnittstelle muss von allen DMOs implementiert werden. Wenn ein DMO die verarbeitung direkt unterstützt, macht er auch die [**IMediaObjectInPlace-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) verfügbar. Der Client ist für die Zuweisung aller Puffer verantwortlich, sowohl für die Eingabe als auch für die Ausgabe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DMOs](about-dmos.md)
</dt> </dl>

 

 



