---
description: Gibt an, ob ein Video Beispiel ein einzelnes Feld oder zwei verschachtelte Felder enthält. Dieses Attribut gilt für Medien Beispiele.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: MFSampleExtension_SingleField-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527926"
---
# <a name="mfsampleextension_singlefield-attribute"></a>MF Sample Extension- \_ Singlefield-Attribut

Gibt an, ob ein Video Beispiel ein einzelnes Feld oder zwei verschachtelte Felder enthält. Dieses Attribut gilt für Medien Beispiele.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Wenn der Wert **true** ist, enthält das Beispiel ein Feld. Wenn der Wert **false** ist oder das-Attribut nicht festgelegt ist, enthält das Beispiel einen kompletten Frame. (Zwei Felder, wenn Zeilen Sprung oder ein progressiver Rahmen).

Wenn es sich bei dem Medientyp um progressive Frames oder verschachtelte Felder handelt, muss dieses Attribut auf " **false** " oder "unset" festgelegt sein.

Wenn der Medientyp ein einzelnes Feld ist, muss dieses Attribut " **true**" lauten. Legen Sie das Attribut " [**mfsampleextension \_ bottomfieldfirst**](mfsampleextension-bottomfieldfirst-attribute.md) " für das Beispiel fest, um anzugeben, ob es sich um das obere Feld oder das untere Feld handelt.

Zurzeit unterstützt der erweiterte Videorenderer (EVR) keine Inhalte, die zwischen Zeilen Sprung Frames und einzelnen Feldern wechseln.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> <dt>

[Video-Interlacing](video-interlacing.md)
</dt> </dl>

 

 




