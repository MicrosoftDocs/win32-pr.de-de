---
description: Gibt an, ob ein Videobeispiel ein einzelnes Feld oder zwei überlappte Felder enthält. Dieses Attribut gilt für Medienbeispiele.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: MFSampleExtension_SingleField -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747dbeebb9bcc8e773b59467f460b12645ed50ebfbddf5bbf6845119c2bba81d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462900"
---
# <a name="mfsampleextension_singlefield-attribute"></a>SingleField-Attribut "MFSampleExtension" \_

Gibt an, ob ein Videobeispiel ein einzelnes Feld oder zwei überlappte Felder enthält. Dieses Attribut gilt für Medienbeispiele.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**VERERBUNGSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Wenn der Wert **TRUE ist,** enthält das Beispiel ein Feld. Wenn der Wert **FALSE ist oder** das Attribut nicht festgelegt ist, enthält das Beispiel einen vollständigen Frame. (Zwei Felder bei Interlacing oder ein progressiver Frame.)

Wenn es sich beim Medientyp um progressive Frames oder verleerte Felder handelt, muss dieses Attribut **FALSE** sein oder nicht festgelegt bleiben.

Wenn der Medientyp ein einzelnes Feld ist, muss dieses Attribut **TRUE sein.** Legen Sie [**das \_ BottomFieldFirst-Attribut MFSampleExtension**](mfsampleextension-bottomfieldfirst-attribute.md) für das Beispiel fest, um anzugeben, ob es sich um das obere oder das untere Feld handelt.

Derzeit unterstützt der erweiterte Videorenderer (EVR) keine Inhalte, die zwischen Zwischenrahmen und einzelnen Feldern wechseln.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> <dt>

[Video Interlacing](video-interlacing.md)
</dt> </dl>

 

 




