---
description: DMO Medientypen
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: DMO Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d67be6775163695189c2dc2c2742f65bcd0181032d9935b2a2a3ce2df2e900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016128"
---
# <a name="dmo-media-types"></a>DMO Medientypen

Ein Medientyp beschreibt das Format, das einem Datenstrom von Mediendaten zugeordnet ist. In diesem Artikel wird beschrieben, wie DMOs Medientypen behandeln. Es ist in erster Linie für Entwickler gedacht, die ihre eigenen benutzerdefinierten DMOs schreiben.

Medientypen werden mithilfe der [**media DMO \_ \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) definiert. Diese Struktur enthält die folgenden Informationen:

-   Der *Haupttyp ist* ein global eindeutiger Bezeichner (Globally Unique Identifier, GUID), der eine breite Kategorie definiert, z. B. Audio oder Video.
-   Der *Untertyp* ist eine GUID, die spezifischere Aspekte des Typs definiert. Die Untertypen im Video umfassen beispielsweise 16-Bit RGB, 24-Bit RGB, UY ASCII, DV-codiertes Video usw.
-   Der *Formatblock ist* eine sekundäre Struktur, die das Format vollständig angibt. Das Layout des Formatblocks hängt vom Datentyp ab. PCM-Audio verwendet beispielsweise die **WAVEFORMATEX-Struktur.** Video verwendet verschiedene andere Strukturen, einschließlich **VIDEOINFOHEADER** und **VIDEOINFOHEADER2**. Das Layout des Formatblocks wird durch eine Formattyp-GUID identifiziert. Format \_ WaveFormatEx gibt beispielsweise eine **WAVEFORMATEX-Struktur** an.

Wenn ein DMO erstellt wird, haben die Streams keinen Medientyp. Bevor die DMO Daten verarbeiten kann, muss der Client einen Medientyp für jeden Stream festlegen. Dieser Prozess wird aus Clientsicht unter [Setting Media Types on a DMO](setting-media-types-on-a-dmo.md).

**Medientypen in der Registrierung**

Ein DMO kann der Registrierung eine Liste von Medientypen hinzufügen, die er unterstützt, indem die [**DMORegister-Funktion aufruft.**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) Eine Anwendung kann diese Informationen verwenden, um nach DMOs zu suchen, die mit einem bestimmten Format übereinstimmen. Die Informationen in der Registrierung sollen nicht umfassend sein. In der Regel würden Sie nur die Haupttypen enthalten, die DMO unterstützt. Der Registrierungseintrag verfügt über separate Schlüssel für Eingabe- und Ausgabetypen, unterscheidet jedoch nicht zwischen einzelnen Streams.

Die **DMORegister-Funktion** verwendet die DMO [**PARTIAL \_ \_ MEDIATYPE-Struktur,**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) um Medientypen zu beschreiben. Diese Struktur enthält eine Teilmenge der Informationen, die in der MEDIA **\_ \_ TYPE DMO struktur** gefunden werden, nämlich den Haupttyp und den Untertyp. Es enthält keinen Formatblock, da der Formatblock in der Regel Informationen enthält, die zu präzise sind, um sie in die Registrierung einfingen zu können, z. B. die Höhe und Breite eines Videobilds.

**Bevorzugte Medientypen**

Nachdem die Anwendung eine DMO erstellt hat, kann sie die DMO medientypen abfragen, die sie unterstützt. Für jeden Stream erstellt der DMO eine Liste von Medientypen (möglicherweise leer), die in der Reihenfolge ihrer Präferenz geordnet sind. Die [**Methoden IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) und [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) aufzählen die bevorzugten Typen. Die bevorzugten Typen eines Streams können sich dynamisch ändern, wenn die Anwendung Medientypen für andere Streams fest legt. Beispielsweise kann sich die Liste der bevorzugten Ausgabetypen ändern, nachdem der Eingabetyp festgelegt wurde oder umgekehrt. Die -DMO ist jedoch nicht erforderlich, um ihre bevorzugten Typen dynamisch zu aktualisieren. Die Anwendung kann nicht davon ausgehen, dass jeder empfangene Typ gültig ist. Aus diesem Grund unterstützen die [**Methoden IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) und [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) ein Flag zum Testen eines bestimmten Typs.

Die **Methoden GetInputType** **und GetOutputType** geben beide eine DMO **MEDIA \_ \_ TYPE-Struktur** zurück. Der DMO kann einige der Informationen in dieser Struktur leer lassen, um einen Bereich von Typen anzugeben. Der Haupttyp oder Untertyp kann GUID \_ NULL sein, und der Formatblock kann leer sein (null Bytes). Wenn der Formatblock leer ist, muss der Formattyp GUID \_ NULL sein.

Nachdem die Anwendung alle Eingabetypen eines DMO legt, sollte die DMO in der Regel mindestens einen vollständigen Typ für jeden Ausgabestream zurückgeben. Ein vollständiger Ausgabetyp erleichtert das Testen, und Anwendungen können ihn als angemessene Standardeinstellung verwenden. Die DMO Testanwendung basiert auf diesem Verhalten. (Siehe [Verwenden der DMOTest-Anwendung](using-the-dmotest-application.md).)

**Festlegen der Medientypen**

Anwendungen verwenden die **Methoden SetInputType** und **SetOutputType,** um Typen in einem angegebenen Stream zu testen, festzulegen oder zu löschen. Die Anwendung muss den Typ vollständig angeben. Der DMO überprüft, ob er den vorgeschlagenen Typ akzeptieren kann. Die Antwort hängt möglicherweise davon ab, welche Typen für andere Streams festgelegt wurden. Das DMO SET TYPEF CLEAR-Flag löschen den Typ eines Streams, sodass die Anwendung "back out" (Zurücksuchen) und eine \_ \_ andere Kombination ausprobieren \_ kann.

**Beispielszenarien**

In den folgenden Beispielen werden einige typische Szenarien beschrieben, um die Punkte in den vorherigen Abschnitten zu veranschaulichen.

-   **Videodecoder.** In einem typischen Videodecoder bestimmt der Eingabetyp teilweise den Ausgabetyp. Beispielsweise müssen in der Regel beide Streams die gleiche Bildfrequenz und die gleiche Bildabmessungen haben. Eine Möglichkeit besteht in der Definition bevorzugter Ausgabetypen, bis der Eingabetyp festgelegt ist. Eine weitere Möglichkeit besteht im Aufzählen eines Sets unvollständiger Typen, ohne den Formatblock zu verwenden. Verwenden Sie den Untertyp , um die unterstützten nicht komprimierten Typen anzugeben, z. B. 16-Bit RGB, 24-Bit RGB usw. Darüber hinaus unterstützen Videodecoder in der Regel nicht das Festlegen des Ausgabetyps vor dem Eingabetyp. Das übliche Szenario ist die Decodierung aus einem bekannten Eingabeformat, daher ist diese Einschränkung sinnvoll.
-   **Audiodecoder.** Ein Audiodecoder unterstützt möglicherweise einen begrenzten, festen Satz von Ausgabeformaten. In diesem Fall kann er möglicherweise eine Liste der bevorzugten Ausgabeformate erstellen, bevor das Eingabeformat bekannt ist.
-   **Kompressoren.** In den meisten Fällen kann ein Videoreproduktionsvideo seine bevorzugten Ausgabeformate erst vollständig angeben, wenn die Anwendung das Eingabeformat festgelegt hat und umgekehrt. Stattdessen sollte die DMO einen unvollständigen Typ ohne Formatblock zurückgeben. Für die Audio- und Videokomprimierung muss die Anwendung in der Regel verschiedene Ausgabeparameter festlegen, z. B. die Bitrate. Nachdem jedoch der Eingabetyp festgelegt wurde, sollte die Ehrung aus den oben genannten Gründen mindestens einen vollständigen Ausgabetyp zurückgeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines DMO](writing-a-dmo.md)
</dt> </dl>

 

 



