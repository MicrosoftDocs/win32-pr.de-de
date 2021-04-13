---
description: Konfigurieren von Codec-DMOS
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Konfigurieren von Codec-DMOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564c0e6c566d9f583a495238f3ea6f0716d7adde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484083"
---
# <a name="configuring-codec-dmos"></a>Konfigurieren von Codec-DMOS

In diesem Thema wird der Prozess der Konfiguration der Codec-DMOS beschrieben. Jeder Codec verfügt über bestimmte Prozeduren, aber die gemeinsamen Informationen werden hier beschrieben.

## <a name="configuring-dmo-inputs-and-outputs"></a>Konfigurieren von DMO-Eingaben und-Ausgaben

Jeder DMO unterstützt bestimmte Eingabe-und Ausgabetypen. Sie können unterstützte Typen für Eingaben und Ausgaben abrufen, indem Sie [**imediaobject:: getinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) für Eingaben und [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) für Ausgaben aufrufen. Sie können die unterstützten Formate auflisten, indem Sie wiederholte Aufrufe an beide Methoden vornehmen und den Typindex bei jedem Aufruf erhöhen. Wenn der Index die des endgültigen unterstützten Typs überschreitet, gibt der-Rückruf DMO \_ E \_ nicht \_ mehr \_ Elemente zurück.

Für die Video Codecs wird nur ein Ausgabetyp oder Eingabetyp für einen angegebenen Medien Untertyp aufgelistet. Bei den Audiocodecs wird jeder einzelne unterstützte Typ aufgezählt. Weitere Informationen zu unterstützten Typen für einzelne Codecs finden Sie unter [Arbeiten mit Audiodaten](workingwithaudio.md) und [Arbeiten mit Videos](workingwithvideo.md).

Nachdem Sie die Medientypen für die Eingabe-und Ausgabedaten Ströme konfiguriert haben, legen Sie Sie durch Aufrufen von [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) bzw. [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) fest. Beide Methoden geben den **DMO \_ E- \_ Typ \_ nicht \_ akzeptiert** zurück, wenn der angegebene Typ ungültig ist.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Konfigurieren der Codec-DMOS für die Codierung

Alle Windows Media Audio-und Video Codecs unterstützen eine Vielzahl von Codierungs Features. Diese Features werden in der Regel durch Festlegen der Eigenschaften für den DMO konfiguriert, indem die Methoden der **IPropertyBag** -Schnittstelle verwendet werden. Einige Eigenschaften werden mithilfe spezieller Codec-Schnittstellen konfiguriert. Diese Schnittstellen werden für jeden Codec im Abschnitt [Codec-Objekte](codecobjects.md)aufgelistet.

Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren eines Codierungs-DMO lautet wie folgt:

1.  Konfigurieren Sie die Codec-Features wie gewünscht mithilfe der Methoden von **IPropertyBag**.
2.  Verwenden Sie die Codec-DMO-Schnittstellen, um zusätzliche Features zu konfigurieren, falls erforderlich.
3.  Konfigurieren Sie die Eingabe-und Ausgabetypen. Die Reihenfolge, in der die Typen konfiguriert werden sollten, variiert für einzelne Codecs. Weitere Informationen finden Sie unter [Arbeiten mit Audiodaten](workingwithaudio.md) und [Arbeiten mit Videos](workingwithvideo.md).

## <a name="configuring-the-codec-dmos-for-decoding"></a>Konfigurieren der Codec-DMOS für das Decodieren

Decodierung ist einfacher als die Codierung, da weniger Decoder-Features unterstützt werden.

Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren einer DMO-Decodierung lautet wie folgt:

1.  Konfigurieren Sie die decoderfeatures wie gewünscht mithilfe der Methoden von **IPropertyBag**.
2.  Legen Sie den Eingabetyp auf den für die encoderausgabe verwendeten Typ fest.
3.  Konfigurieren Sie den Ausgabetyp. Die unterstützten Ausgabetypen unterscheiden sich für unterschiedliche Eingaben.

> [!Note]  
> Es ist wichtig, den gleichen Medientyp für die decodereingabe zu verwenden, die für die encoderausgabe verwendet wurde. Dies liegt daran, dass die Windows Media Audio-und Video Codecs Medienformate mit zusätzlichen Daten verwenden. Diese Daten werden an die Struktur angehängt, auf die der **pbformat** -Member der [**DMO \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur zeigt (in der Regel [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) oder [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85))). Für einige Typen sind die zusätzlichen Daten Teil des Enumerationstyps des enumerierten Encoders. Für andere Typen müssen Sie diese Daten manuell anfügen. Ohne die erweiterten Formatierungsdaten können Sie den komprimierten Inhalt nicht decodieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
</dt> </dl>

 

 
