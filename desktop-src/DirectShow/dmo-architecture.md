---
description: DMO-Architektur
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: DMO-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343122"
---
# <a name="dmo-architecture"></a>DMO-Architektur

In diesem Abschnitt wird die allgemeine Architektur eines DMO beschrieben.

**Streams**

Ein DMO ist ein Objekt, das *m* Eingaben annimmt und *n* Ausgaben erzeugt. Die Eingaben und Ausgaben werden als *Streams* bezeichnet. Jeder DMO verfügt über mindestens einen Stream. Streams sind keine Objekte. auf Sie wird einfach durch die Indexnummer in der DMO verwiesen. Die Anzahl der Streams ist zur Entwurfszeit korrigiert.

**Medientypen**

Alle Daten werden mit einem *Medientyp* typisiert, der definiert, wie der Inhalt der Daten interpretiert werden soll. Beispielsweise ist 320 x 240 24 Bit RGB Video ein Typ. 44,1-Kilohertz (kHz) 16-Bit-Stereo PCM-Audiodatei ist ein anderer Typ. Medientypen werden mithilfe der [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur beschrieben. Bevor der Client Daten verarbeiten kann, muss er den Medientyp für jeden Stream in der DMO festlegen.

In der Regel kann ein Stream einen Bereich von Medientypen akzeptieren. Einige DMOS unterstützen eine größere Anzahl von Typen als andere. Die DMO-Schnittstellen definieren Methoden für den Client, um die unterstützten Typen zu ermitteln. Beispielsweise kann ein DMO RGB-Video in beliebiger bidirektiontiefe unterstützen, während ein anderes nur 24-Bit-RGB unterstützt. Außerdem kann ein DMO auf bestimmte Kombinationen von Eingaben und Ausgaben beschränkt sein. Wenn der Eingabetyp beispielsweise ein 16-Bit-Video ist, kann der Ausgabestream die gleiche Bittiefe erfordern. Der Client kann die bevorzugten Typen jedes Streams auflisten und dann bestimmte Kombinationen testen.

**Puffer**

Im DMO-Standardmodell ordnet der Client separate Eingabepuffer und Ausgabepuffer zu. Sie füllt die Eingabepuffer mit Daten und übergibt sie an den DMO, und der DMO schreibt neue Daten in die Ausgabepuffer.

Optional kann ein DMO die direkte Verarbeitung unterstützen. Bei der direkten Verarbeitung schreibt der DMO die Ausgabe direkt in den Eingabepuffer, und zwar über die ursprünglichen Daten. Durch die direkte Verarbeitung entfällt die Notwendigkeit separater Puffer. Auf der anderen Seite ändert Sie die ursprünglichen Daten, die für einige Anwendungen möglicherweise nicht zulässig sind.

Das standardmäßige (nicht direkte) Puffer Modell wird durch die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle unterstützt. Alle DMOS müssen diese Schnittstelle implementieren. Wenn ein DMO die direkte Verarbeitung unterstützt, wird auch die [**imediaobjectinplace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) -Schnittstelle verfügbar gemacht. Der Client ist für die Zuordnung aller Puffer (Eingabe und Ausgabe) verantwortlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DMOS](about-dmos.md)
</dt> </dl>

 

 



