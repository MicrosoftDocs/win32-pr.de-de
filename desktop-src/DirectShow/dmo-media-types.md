---
description: DMO-Medientypen
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: DMO-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1997abb1cc3c8eb10301778982ef7a46690855ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530551"
---
# <a name="dmo-media-types"></a>DMO-Medientypen

Ein Medientyp beschreibt das Format, das einem Stream von Mediendaten zugeordnet ist. In diesem Artikel wird beschrieben, wie DMOS Medientypen verarbeitet. Es richtet sich hauptsächlich an Entwickler, die eigene benutzerdefinierte DMOS schreiben.

Medientypen werden mithilfe der [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur definiert. Diese Struktur enthält die folgenden Informationen:

-   Der *Haupttyp* ist eine Globally Unique Identifier (GUID), die eine breite Kategorie definiert, wie z. b. Audiodaten oder Videos.
-   Der *Untertyp* ist eine GUID, die spezifischere Aspekte des Typs definiert. Beispielsweise enthalten die Untertypen innerhalb von Video 16-Bit-RGB-, 24-Bit-RGB-, UYVY-und DV-codierte Videos usw.
-   Der *Format Block* ist eine sekundäre Struktur, die das Format vollständig angibt. Das Layout des Format Blocks hängt von der Art der Daten ab. Beispielsweise verwendet PCM-Audiodaten die **WaveFormatEx** -Struktur. Video verwendet verschiedene andere Strukturen, einschließlich **videoinfoheader** und **VIDEOINFOHEADER2**. Das Layout des Format Blocks wird durch einen Formattyp-GUID identifiziert. Das Format \_ WaveFormatEx gibt z. b. eine **WaveFormatEx** -Struktur an.

Wenn ein DMO erstmalig erstellt wird, weisen die Streams keinen Medientyp auf. Bevor der DMO Daten verarbeiten kann, muss der Client für jeden Stream einen Medientyp festlegen. Dieser Prozess wird aus der Sicht des Clients beim [Festlegen von Medientypen in einem DMO](setting-media-types-on-a-dmo.md)beschrieben.

**Medientypen in der Registrierung**

Ein DMO kann durch Aufrufen der [**dmoregisterfunktion**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) eine Liste der von ihm unterstützten Medientypen zur Registrierung hinzufügen. Eine Anwendung kann diese Informationen verwenden, um nach DMOS zu suchen, die einem bestimmten Format entsprechen. Die Informationen in der Registrierung sind nicht als vollständig zu verstehen. Normalerweise würden Sie nur die Haupttypen einschließen, die der DMO unterstützt. Der Registrierungs Eintrag weist separate Schlüssel für Eingabe-und Ausgabetypen auf, unterscheidet jedoch nicht zwischen einzelnen Datenströmen.

Die **dmoregiester** -Funktion verwendet die [**partielle DMO- \_ \_ mediaType**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) -Struktur, um Medientypen zu beschreiben. Diese Struktur enthält eine Teilmenge der Informationen, die in der **DMO \_ - \_ Medientyp** Struktur gefunden werden – nämlich den Haupttyp und den Untertyp. Sie enthält keinen Format Block, da der Format Block in der Regel Informationen enthält, die in der Registrierung zu granulär sind, z. b. Höhe und Breite eines Video Bilds.

**Bevorzugte Medientypen**

Nachdem die Anwendung ein DMO erstellt hat, kann Sie den DMO nach den unterstützten Medientypen Abfragen. Der DMO erstellt für jeden Datenstrom eine Liste von Medientypen (möglicherweise leer), sortiert nach bevorzugten Reihenfolge. Die Methoden [**imediaobject:: getinputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) und [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) zählen die bevorzugten Typen auf. Die bevorzugten Typen eines Streams können sich dynamisch ändern, wenn die Anwendung Medientypen für andere Streams festlegt. Beispielsweise kann sich die Liste der bevorzugten Ausgabetypen ändern, nachdem der Eingabetyp festgelegt wurde, oder umgekehrt. Es ist jedoch nicht erforderlich, dass der DMO seine bevorzugten Typen dynamisch aktualisiert. Die Anwendung kann nicht davon ausgehen, dass jeder empfangene Typ gültig ist. Aus diesem Grund unterstützen die [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) -und die [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) -Methode ein Flag zum Testen eines bestimmten Typs.

Die Methoden " **getinputtype** " und " **getoutputtype** " geben eine **DMO- \_ \_ Medientyp** Struktur zurück. Der DMO kann einige der Informationen in dieser Struktur leer lassen, um einen Bereich von Typen anzugeben. Der Haupttyp oder Untertyp kann GUID \_ NULL sein, und der Format Block kann leer sein (0 Bytes). Wenn der Format Block leer ist, muss der Formattyp "GUID \_ null" lauten.

Nachdem die Anwendung alle Eingabetypen eines DMO festgelegt hat, sollte der DMO in der Regel mindestens einen vollständigen Typ für jeden Ausgabestream zurückgeben. Ein kompletter Ausgabetyp ermöglicht das Testen, und Anwendungen können ihn als angemessenen Standardwert verwenden. Die DMO-Testanwendung basiert auf diesem Verhalten. (Weitere Informationen finden [Sie unter Verwenden der dmutest-Anwendung](using-the-dmotest-application.md).)

**Festlegen der Medientypen**

Anwendungen verwenden die **setinputtype** -Methode und die **setoutputtype** -Methode, um Typen für einen angegebenen Stream zu testen, festzulegen oder zu löschen. Die Anwendung muss den Typ vollständig angeben. Der DMO überprüft, ob der vorgeschlagene Typ akzeptiert werden kann. Die Antwort hängt möglicherweise davon ab, welche Typen für andere Streams festgelegt wurden. Das Flag zum \_ Löschen der typef-Funktion von DMO \_ Löscht den \_ Typ eines Streams, sodass die Anwendung "zurück" ist und eine weitere Kombination ausprobieren kann.

**Beispielszenarien**

In den folgenden Beispielen werden einige typische Szenarien beschrieben, um die in den vorherigen Abschnitten beschriebenen Punkte zu veranschaulichen.

-   **Video-Decoders.** In einem typischen Video Decoder bestimmt der Eingabetyp teilweise den Ausgabetyp. In der Regel müssen beide Datenströme z. b. die gleichen Frameraten-und Bild Dimensionen aufweisen. Eine Möglichkeit besteht darin, keine bevorzugten Ausgabetypen zu definieren, bis der Eingabetyp festgelegt ist. Eine andere Möglichkeit besteht darin, einen Satz unvollständiger Typen aufzulisten, wobei der Format Block weggelassen wird. Verwenden Sie den Untertyp, um die unterstützten nicht komprimierten Typen anzugeben, z. b. 16-Bit-RGB, 24-Bit-RGB usw. Außerdem unterstützen Video Decoder in der Regel nicht das Festlegen des Ausgabe Typs vor dem Eingabetyp. Das übliche Szenario besteht darin, ein bekanntes Eingabeformat zu decodieren, sodass diese Einschränkung angemessen ist.
-   **Audiodecoder.** Ein Audiodecoder unterstützt möglicherweise einen begrenzten Satz von Ausgabeformaten. In diesem Fall kann es möglicherweise in der Lage sein, eine Liste der bevorzugten Ausgabeformate zu erstellen, bevor das Eingabeformat bekannt ist.
-   **Chtern.** In den meisten Fällen kann ein Video-Kompressor seine bevorzugten Ausgabeformate nicht vollständig angeben, bis die Anwendung das Eingabeformat festlegt (und umgekehrt). Stattdessen sollte der DMO einen unvollständigen Typ ohne Format Block zurückgeben. Bei der Audio-und Video Komprimierung muss die Anwendung normalerweise verschiedene Ausgabeparameter festlegen, z. b. die Bitrate. Nachdem der Eingabetyp jedoch festgelegt wurde, sollte der-Kompressor aus den zuvor erwähnten Gründen mindestens einen kompletten Ausgabetyp zurückgeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines DMO](writing-a-dmo.md)
</dt> </dl>

 

 



