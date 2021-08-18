---
description: Enthält Konfigurationseigenschaften für einen Encoder.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: MFT_PREFERRED_ENCODER_PROFILE -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85acf742e518d91c6512b2b887cca910c3b19d21180500bd1180e6972255e54f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722505"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>MFT \_ PREFERRED \_ ENCODER \_ PROFILE-Attribut

Enthält Konfigurationseigenschaften für einen Encoder.

## <a name="data-type"></a>Datentyp

**[**DURCHATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \* *_ gespeichert als _* Iunknown\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DANNATTRIBUTEs::GetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)

## <a name="applies-to"></a>Gilt für:

[**ACTIVate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Hinweise

Dieses Attribut kann für das Aktivierungsobjekt festgelegt werden, das von der [**MFCreateTransformActivate-Funktion zurückgegeben**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) wird. Das -Attribut gilt nur, wenn das Aktivierungsobjekt zum Erstellen eines Encoders konfiguriert ist. Der Wert des Attributs ist ein Zeiger auf einen Attributspeicher, der selbst Eigenschaften enthält, die für den Encoder festgelegt werden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




