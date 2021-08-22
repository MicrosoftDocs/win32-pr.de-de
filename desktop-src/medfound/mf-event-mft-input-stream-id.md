---
description: Gibt einen Eingabestream für eine Media Foundation Transform (MFT) an.
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: MF_EVENT_MFT_INPUT_STREAM_ID -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d211eb30280e6b7390df8509795d49567c7f8a8c9016b2825786858fe888b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973809"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a>MF \_ EVENT \_ MFT INPUT STREAM \_ \_ \_ ID-Attribut

Gibt einen Eingabestream für eine Media Foundation Transform (MFT) an.

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert ist ein Eingabestreambezeichner.

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**BESENKMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird mit den folgenden Ereignissen verwendet:

-   [METransformDgreifComplete](metransformdraincomplete.md)
-   [METransformNeedInput](metransformneedinput.md)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> </dl>

 

 




