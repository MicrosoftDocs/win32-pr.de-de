---
description: Enthält einen vom Aufrufer definierten Wert für ein METransformMarker-Ereignis.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: MF_EVENT_MFT_CONTEXT-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9518853030ec52a687f02ac0288c3fd3ffcf55b676be56c7036b349e1dec9aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104846"
---
# <a name="mf_event_mft_context-attribute"></a>MF \_ EVENT \_ MFT \_ CONTEXT-Attribut

Enthält einen vom Aufrufer definierten Wert für ein [METransformMarker-Ereignis.](metransformmarker.md)

## <a name="data-type"></a>Datentyp

**ULONG \_ PTR** als **UINT64** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT64 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)

## <a name="applies-to"></a>Gilt für:

[**WFMEDIAEVENT**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird mit dem [METransformMarker-Ereignis](metransformmarker.md) verwendet. Der Wert des Attributs wird aus dem *ulParam-Parameter* der [**PARAMETERSTransform::P rocessMessage-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) übernommen.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> </dl>

 

 




