---
description: Konfigurieren von Codec-DMOs
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Konfigurieren von Codec-DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4040c0a16c0311d14b0553336e1d9b70a7a6c1fd28a0f01277c955eea55ec7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958330"
---
# <a name="configuring-codec-dmos"></a>Konfigurieren von Codec-DMOs

In diesem Thema wird der Prozess der Konfiguration der Codec-DMOs beschrieben. Jeder Codec verfügt über bestimmte Verfahren, aber die informationen, die allen gemeinsam sind, werden hier beschrieben.

## <a name="configuring-dmo-inputs-and-outputs"></a>Konfigurieren DMO Eingaben und Ausgaben

Jede DMO unterstützt bestimmte Eingabe- und Ausgabetypen. Sie können unterstützte Typen für Eingaben und Ausgaben abrufen, indem [**Sie IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) für Eingaben und [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) für Ausgaben aufrufen. Sie können die unterstützten Formate aufzählen, indem Sie wiederholte Aufrufe an beide Methoden vornehmen und den Typindex mit jedem Aufruf erhöhen. Wenn der Index den des letzten unterstützten Typs überschreitet, gibt der Aufruf DMO \_ E NO MORE ITEMS \_ \_ \_ zurück.

Für die Videocodecs wird nur ein Ausgabetyp oder Eingabetyp für einen bestimmten Medienuntertyp aufzählt. Für die Audiocodecs wird jeder einzelne unterstützte Typ aufzählt. Weitere Informationen zu unterstützten Typen für einzelne Codecs finden Sie unter [Working with Audio (Arbeiten mit Audio)](workingwithaudio.md) und [Working with Video (Arbeiten mit Video).](workingwithvideo.md)

Nachdem Sie die Medientypen für die Eingabe- und Ausgabestreams konfiguriert haben, legen Sie sie fest, indem [**Sie IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) bzw. [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) aufrufen. Beide Methoden geben **DMO \_ E TYPE NOT \_ ACCEPTED \_ \_ zurück,** wenn der angegebene Typ ungültig ist.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Konfigurieren der Codec-DMOs für die Codierung

Alle Windows Medienaudio- und Videocodecs unterstützen eine Vielzahl von Codierungsfunktionen. Diese Features werden im Allgemeinen konfiguriert, indem Eigenschaften auf dem DMO mithilfe der Methoden der **IPropertyBag-Schnittstelle** festgelegt werden. Einige Eigenschaften werden mit speziellen Codecschnittstellen konfiguriert. Diese Schnittstellen sind für jeden Codec im Abschnitt [CodecObjekte](codecobjects.md)aufgeführt.

Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren einer Codierungs-DMO lautet wie folgt:

1.  Konfigurieren Sie Codecfunktionen wie gewünscht mithilfe der Methoden von **IPropertyBag**.
2.  Verwenden Sie den Codec DMO Schnittstellen, um bei Bedarf zusätzliche Features zu konfigurieren.
3.  Konfigurieren Sie die Eingabe- und Ausgabetypen. Die Reihenfolge, in der die Typen konfiguriert werden sollen, variiert für einzelne Codecs. Weitere Informationen finden Sie unter [Working with Audio (Arbeiten mit Audio)](workingwithaudio.md) und [Working with Video (Arbeiten mit Video).](workingwithvideo.md)

## <a name="configuring-the-codec-dmos-for-decoding"></a>Konfigurieren der Codec-DMOs für die Decodierung

Die Decodierung ist einfacher als die Codierung, da weniger Decoderfeatures unterstützt werden.

Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren eines Decodierungs-DMO lautet wie folgt:

1.  Konfigurieren Sie Decoderfeatures wie gewünscht mithilfe der Methoden von **IPropertyBag**.
2.  Legen Sie den Eingabetyp auf den Typ fest, der für die Encoderausgabe verwendet wird.
3.  Konfigurieren Sie den Ausgabetyp. Die unterstützten Ausgabetypen unterscheiden sich für verschiedene Eingaben.

> [!Note]  
> Es ist wichtig, für die Decodereingabe denselben Medientyp wie für die Encoderausgabe zu verwenden. Dies liegt daran, dass die Windows Medienaudio- und Videocodecs Medienformate mit zusätzlichen Daten verwenden. Diese Daten werden an die Struktur angefügt, auf die der **pbFormat-Member** der [**DMO MEDIA \_ \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) zeigt (normalerweise [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) oder [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))). Bei einigen Typen sind die zusätzlichen Daten Teil des Enumerationsausgabetyps des Encoders. Bei anderen Typen müssen Sie diese Daten manuell anfügen. Ohne die erweiterten Formatdaten können Sie den komprimierten Inhalt nicht decodieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
