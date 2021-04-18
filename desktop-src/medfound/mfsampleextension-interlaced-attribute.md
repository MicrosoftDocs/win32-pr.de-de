---
description: Gibt an, ob ein Videorahmen Zeilen Sprung oder progressiv ist.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: MFSampleExtension_Interlaced-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357432"
---
# <a name="mfsampleextension_interlaced-attribute"></a>MF Sample Extension- \_ interschnür Attribut

Gibt an, ob ein Videorahmen Zeilen Sprung oder progressiv ist. **True** gibt an, dass der Frame mit Zeilen Sprung verknüpft ist. **False** gibt an, dass der Frame progressiv ist. Wenn nicht festgelegt, beschreibt der Medientyp das Interlacing. Dieses Attribut gilt für Medien Beispiele.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Legen Sie für Videoinhalte, die gemischte und verschachtelte Rahmen enthalten, den Medientyp auf Zeilen Sprung fest, und verwenden Sie dieses Attribut für jeden Frame, um anzugeben, ob der Frame progressiv oder Zeilen Sprung ist.

Legen Sie für Videoinhalte, die vollständig mit Zeilen Sprung versehen sind, den Medientyp auf Zeilen Sprung und auslassen dieses Attributs fest, oder legen Sie es für jedes Beispiel auf **true** fest.

Legen Sie für den Medientyp, der vollständig progressiv ist, den Medientyp auf progressiv fest, und lassen Sie dieses Attribut aus, oder legen Sie es in jeder Stichprobe auf **false**

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

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> <dt>

[Video-Interlacing](video-interlacing.md)
</dt> </dl>

 

 




