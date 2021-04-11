---
description: Dieses Thema enthält einige Richtlinien für die Implementierung eines Decoders oder Encoders als Media Foundation Transformation (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementieren eines Codec-MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218244"
---
# <a name="implementing-a-codec-mft"></a>Implementieren eines Codec-MFT

Dieses Thema enthält einige Richtlinien für die Implementierung eines Decoders oder Encoders als Media Foundation Transformation (MFT).

-   [Encoder](#encoders)
    -   [Aushandlung des encoderformats](#encoder-format-negotiation)
-   [Decoder](#decoders)
    -   [Nur-transcode-decoderer](#transcode-only-decoders)
    -   [Telecine-Attribute](#telecine-attributes)
-   [Zugehörige Themen](#related-topics)

## <a name="encoders"></a>Encoder

### <a name="encoder-format-negotiation"></a>Aushandlung des encoderformats

Das folgende Verfahren wird verwendet, um einen Encoder zu initialisieren:

1.  Fragen Sie die MFT für die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle ab.
2.  Aufrufen von [**icodecapi:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) , um Codierungs Eigenschaften festzulegen.
3.  Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , um das Codierungsformat festzulegen.
4.  Wenn Sie [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) aufrufen, erhalten Sie eine Liste der kompatiblen Eingabetypen. (Dieser Schritt kann übersprungen werden.)
5.  Um das unkomprimierte Eingabeformat festzulegen, wird [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) aufgerufen.

Nachdem der Ausgabetyp in Schritt 3 festgelegt wurde, muss die [**getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) -Methode eine Liste von Eingabetypen zurückgeben, die mit dem aktuellen Ausgabetyp kompatibel sind. Dies bedeutet, dass alle von **getinputavailabletype** an dieser Stelle zurückgegebenen Typen für " [**tartinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)" gültig sein müssen.

Für Decoders wird die Reihenfolge, in der die Typen festgelegt werden, umgekehrt: der Eingabetyp wird zuerst festgelegt, gefolgt vom Ausgabetyp. Nachdem der Eingabetyp festgelegt wurde, muss die [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode eine Liste von Typen zurückgeben, die an die [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) -Methode weitergegeben werden können.

Encoder und Decoder sollten NV12 als häufiges nicht komprimiertes Format unterstützen. Dadurch wird sichergestellt, dass Pipeline Komponenten mit minimalen colorspace-Konvertierungen interagieren können. Natürlich können auch andere Formate unterstützt werden.

## <a name="decoders"></a>Decoder

### <a name="transcode-only-decoders"></a>Transcode-Only Decoders

Einige Decoder sind für das transcodieren optimiert (decodieren und erneutes Codieren eines Streams) und sind nicht für die Verwendung während der Wiedergabe geeignet.

Wenn ein Decoder-MFT nur für die Transcodierung vorgesehen ist, legen Sie das Flag für die **MFT- \_ Enum- \_ Flag \_ \_ nur transcode** fest, wenn Sie die MFT registrieren. (Weitere Informationen finden Sie unter [**MF tregiester**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)

Standardmäßig werden transcodieren-Decoder nicht von der [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben. Zum Auflisten von transcodieren-Decodern müssen Sie **mftenumex** aufrufen und das Flag für die MFT-Enumeration für **\_ \_ \_ transcodieren \_ only** im *Flags* -Parameter festlegen. Bei Verwendung in der **msumex** -Funktion zählt dieses Flag sowohl transcodieren-Decoder als auch andere Decoder auf.



| Mftregiester-MFT-Aufzählungs **\_ \_ Flag \_ \_ nur transcode** | Mftenumex-MFT-Aufzählungs **\_ \_ Flag \_ \_ nur transcode** | Ist MFT aufgezählt? |
|--------------------------------------------------|------------------------------------------------|--------------------|
| 1                                                | 1                                              | Ja                |
| 1                                                | 0                                              | Nein                 |
| 0                                                | 1                                              | Ja                |
| 0                                                | 0                                              | Ja                |



 

### <a name="telecine-attributes"></a>Telecine-Attribute

Die Medienquelle kann die folgenden telecine-Attribute an die übermittelt Medien Beispiele anfügen.



| Attribut                                                                                   | BESCHREIBUNG                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [**MF Sample Extension \_ repeatfirstfield**](mfsampleextension-repeatfirstfield-attribute.md) | Entspricht dem Flag "Repeat First Field" (RFF). |
| [**MF Sample Extension \_ bottomfieldfirst**](mfsampleextension-bottomfieldfirst-attribute.md) | Umgekehrter Wert für das Flag "Top Field First" (tff).       |



 

Diese Flags stellen einen Hinweis für den erweiterten Videorenderer (EVR) dar, wenn Sie Deinterlacing ausführt. Ein Decoder sollte diese Flags nach unten weitergeben, indem Sie Sie in die Ausgabe Beispiele kopieren, damit Sie den EVR erreichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 
