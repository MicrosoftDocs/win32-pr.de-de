---
description: Gibt an, ob ein deinter verschachtelter Videoframe vom oberen oder unteren Feld abgeleitet wurde.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: MFSampleExtension_DerivedFromTopField -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 376cc499dd76702abb4c7054014a7c720118f33a732856202c4e654992c30985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241190"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>MFSampleExtension \_ DerivedFromTopField-Attribut

Gibt an, ob ein deinter verschachtelter Videoframe vom oberen oder unteren Feld abgeleitet wurde. Dieses Attribut gilt für Medienbeispiele.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**VERERBUNGSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Dieses Attribut ist nur für Deinterlaced-Beispiele gültig. Legen Sie dieses Attribut fest, wenn der Frame durch Interpolieren eines der Felder deinterlaced wurde.

Wenn der Wert **TRUE ist,** wurde das untere Feld aus dem oberen Feld interpoliert. Wenn der Wert **FALSE ist,** wurde das obere Feld aus dem unteren Feld interpoliert.

Wenn das Attribut nicht festgelegt ist, wurde der Frame nicht deinterlaced. Der Frame ist entweder ein echter progressiver Rahmen oder ein Interlaced-Frame.

Dieses Attribut ist informationell. Ein Softwaredeinterlacer kann dieses Attribut festlegen. Wenn dieses Attribut festgelegt ist, gibt es einen Hinweis darauf, dass Sie das ursprüngliche Feld wiederherstellen können, indem Sie die interpolierten Scanzeilen löschen. Wenn das Attribut beispielsweise **TRUE** ist, können Sie das ursprüngliche obere Feld wiederherstellen, indem Sie das interpolierte untere Feld löschen.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> <dt>

[Video Interlacing](video-interlacing.md)
</dt> </dl>

 

 




