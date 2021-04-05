---
description: Enthält einen vom Aufrufer definierten Wert für ein metransformmarker-Ereignis.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: MF_EVENT_MFT_CONTEXT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041958"
---
# <a name="mf_event_mft_context-attribute"></a>\_ \_ MFT- \_ Kontext Attribut für das MF-Ereignis

Enthält einen vom Aufrufer definierten Wert für ein [metransformmarker](metransformmarker.md) -Ereignis.

## <a name="data-type"></a>Datentyp

**Ulong \_** Als **UINT64** gespeicherter PTR

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Gilt für:

[**IMF Media Event**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit dem [metransformmarker](metransformmarker.md) -Ereignis verwendet. Der Wert des-Attributs wird aus dem *ulparam* -Parameter der [**IMF Transform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) -Methode entnommen.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> </dl>

 

 




