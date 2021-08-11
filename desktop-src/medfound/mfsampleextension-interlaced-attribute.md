---
description: Gibt an, ob ein Videoframe übersprungen oder progressiv ist.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: MFSampleExtension_Interlaced Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d928d42fc2399536d5beee4f4af87cbacaa82171048ad191a4e9fc7ef3e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240647"
---
# <a name="mfsampleextension_interlaced-attribute"></a>\_MFSampleExtension-Interlaced-Attribut

Gibt an, ob ein Videoframe übersprungen oder progressiv ist. True gibt an, dass der Frame übersprungen wird. False gibt an, dass der Frame progressiv ist. Wenn diese Einstellung nicht festgelegt ist, beschreibt der Medientyp das Interlacing. Dieses Attribut gilt für Medienbeispiele.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**DIESSAMPLE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Legen Sie für Videoinhalte, die gemischte progressive und interlaced-Frames enthalten, den Medientyp auf interlaced fest, und verwenden Sie dieses Attribut für jeden Frame, um anzugeben, ob der Frame progressiv oder interlaced ist.

Legen Sie für Videoinhalte, die vollständig per Interlacing verknüpft sind, den Medientyp auf interlaced fest, und lassen Sie dieses Attribut aus, oder legen Sie es für jedes Beispiel auf **TRUE** fest.

Legen Sie für Videoinhalte, die vollständig progressiv sind, den Medientyp auf progressiv fest, und lassen Sie dieses Attribut aus, oder legen Sie es für jedes Beispiel auf **FALSE** fest.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ZUSAMMENHÄNGENDEAttribute::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**DIESSAMPLE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> <dt>

[Videointerlacing](video-interlacing.md)
</dt> </dl>

 

 




