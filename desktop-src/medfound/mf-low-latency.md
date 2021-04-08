---
description: Ermöglicht die Verarbeitung mit niedriger Latenz in der Microsoft Media Foundation Pipeline.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757866"
---
# <a name="mf_low_latency-attribute"></a>\_Attribut mit geringer Latenz bei MF \_

Ermöglicht die Verarbeitung mit niedriger Latenz in der Microsoft Media Foundation Pipeline.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Geringe Latenzzeit wird als kleinste mögliche Verzögerung beim Generieren (oder empfangen) der Mediendaten beim Rendern definiert. Geringe Latenzzeit ist für echt Zeit Kommunikationsszenarien wünschenswert. In anderen Szenarien, wie z. b. der lokalen Wiedergabe oder der Transcodierung, sollten Sie in der Regel den Modus mit niedriger Latenz nicht aktivieren, da dies die Qualität beeinflussen kann.

> [!Note]  
> Der GUID-Wert dieses Attributs ist mit der Eigenschaft " [codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md) " identisch, die für die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle definiert ist.

 

Legen Sie dieses Attribut für Pipeline Komponenten wie folgt fest:

-   Medienquelle: Verwenden Sie die [**imfmediasourceex:: getsourceattributormethode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .
-   Media Foundation Transformation (MFT): Verwenden Sie die [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode. Bei Encodern unterstützt der Encoder möglicherweise eine geringe Latenzzeit über die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle.
-   Medien Senke: Abfragen der Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle.

Anwendungen legen dieses Attribut in der Regel nicht direkt auf den Pipeline Komponenten fest, sondern legen stattdessen das-Attribut für eines der folgenden Objekte fest:

-   [Medien Sitzung](media-session.md): Verwenden Sie den *pkonfigurations* -Parameter der [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) -oder [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) -Funktion, oder legen Sie das-Attribut in der Topologie fest.
-   [Quell Leser](source-reader.md): Legen Sie das-Attribut mit den Konfigurations Eigenschaften beim Erstellen des Quell Readers fest. Weitere Informationen finden Sie unter [Attribute des Quell Readers](source-reader-attributes.md).
-   [Sink Writer](sink-writer.md): Legen Sie das-Attribut mit den Konfigurations Eigenschaften fest, wenn Sie den Senke-Writer erstellen. Weitere Informationen finden Sie unter [senkenwriter-Attribute](sink-writer-attributes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Senkenwriter-Attribute](sink-writer-attributes.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 
