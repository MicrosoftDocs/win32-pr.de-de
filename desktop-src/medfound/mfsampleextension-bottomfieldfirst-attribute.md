---
description: Gibt die Felddominanz für einen Geschachtelten Videoframe an.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: MFSampleExtension_BottomFieldFirst -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ab0a9847977ea25d93190911bbf2280629f0219eba3d4c4ddfb492e9fdcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113070"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>MFSampleExtension \_ BottomFieldFirst-Attribut

Gibt die Felddominanz für einen Geschachtelten Videoframe an. Dieses Attribut gilt für Medienbeispiele.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**DURCHSCHN.Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Wenn der Videoframe geschachtelt ist und das Beispiel zwei verschachtelte Felder enthält, gibt dieses Attribut an, welches Feld zuerst angezeigt wird. True **gibt an,** dass das untere Feld zum ersten Mal angezeigt wird. False **gibt an,** dass das oberste Feld zuerst angezeigt wird.

Wenn der Frame ein Interlacing ist und das Beispiel ein einzelnes Feld enthält, gibt dieses Attribut an, welches Feld das Beispiel enthält. True **gibt an,** dass das Beispiel das untere Feld enthält. False **gibt an,** dass das Beispiel das oberste Feld enthält.

Wenn der Frame progressiv ist, beschreibt dieses Attribut, wie die Felder beim Verschachteln der Ausgabe geordnet werden sollen. True **gibt an,** dass das untere Feld zuerst ausgegeben werden sollte. False **gibt** an, dass das oberste Feld zuerst ausgegeben werden sollte.

Wenn dieses Attribut nicht festgelegt ist, beschreibt der Medientyp die Felddominanz.

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

 

 




