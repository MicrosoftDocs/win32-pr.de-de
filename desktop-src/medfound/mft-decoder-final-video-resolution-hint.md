---
description: Gibt die endgültige Ausgabeauflösung des decodierten Bilds nach der Videoverarbeitung an.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847a2925f2249c741e9a45a1dcc4826a1cbe3d6bb12cda4d8017ee0fb5de0069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973139"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>\_MFT DECODER \_ FINAL VIDEO \_ RESOLUTION \_ \_ HINT-Attribut

Gibt die endgültige Ausgabeauflösung des decodierten Bilds nach der Videoverarbeitung an.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Dieses Attribut wird von einigen Videodecodern unterstützt. Eine Anwendung kann dieses Attribut festlegen, um die Breite und Höhe des Bilds nach der Videoverarbeitung anzugeben. Der Decoder kann diese Informationen verwenden, um den Decodierungsprozess zu optimieren, insbesondere, wenn die endgültige Bildgröße viel kleiner als die Größe des nativen Images ist. Beispielsweise kann der Decoder einen Out-of-Loop-Filter überspringen.

Die oberen 32 Bits enthalten die Breite und die unteren 32 Bits die Höhe.

So legen Sie dieses Attribut fest:

1.  Rufen Sie [**ÜBERTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder auf, um einen [**POINTERAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abzurufen.
2.  Rufen Sie [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) auf, um das Attribut hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




