---
description: Gibt die endgültige Ausgabeauflösung des decodierten Bilds nach der Videoverarbeitung an.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215036"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>\_ \_ Letztes \_ Video \_ Auflösungs \_ Hinweis Attribut des MFT-Decoders

Gibt die endgültige Ausgabeauflösung des decodierten Bilds nach der Videoverarbeitung an.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird von einigen Video-Decodern unterstützt. Eine Anwendung kann dieses Attribut festlegen, um die Breite und Höhe des Bilds nach der Videoverarbeitung anzugeben. Der Decoder kann diese Informationen verwenden, um den Decodierungs Prozess zu optimieren, insbesondere dann, wenn die endgültige Bildgröße wesentlich kleiner ist als die Größe des systemeigenen Bilds. Der Decoder könnte z. b. einen Out-of-Loop-Filter überspringen.

Die oberen 32 Bits enthalten die Breite, und die unteren 32 Bits enthalten die Höhe.

So legen Sie dieses Attribut fest:

1.  Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder zum Abrufen eines [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeigers.
2.  Zum Hinzufügen des Attributs muss [**mftstributesize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




