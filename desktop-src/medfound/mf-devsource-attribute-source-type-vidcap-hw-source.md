---
description: Gibt an, ob es sich bei einer Videoaufnahmequelle um ein Hardwaregerät oder ein Softwaregerät handelt.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399a486c5637cb617aec0570daa673db5b07874747f8ee9caae359f94087b5a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060724"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a>MF \_ \_ DEVSOURCE-ATTRIBUT \_ \_ QUELLTYP \_ VIDCAP \_ HW \_ SOURCE-Attribut

Gibt an, ob es sich bei einer Videoaufnahmequelle um ein Hardwaregerät oder ein Softwaregerät handelt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Wenn der Wert **TRUE ist,** ist die Erfassungsquelle ein Hardwaregerät. Wenn der Wert **FALSE ist,** handelt es sich um ein Softwaregerät. Der Standardwert ist **FALSE**.

Dieses Attribut wird für die Aktivierungsobjekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Das Attribut gilt nur für Videoaufnahmegeräte.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Erfassen von Geräteattributen](capture-device-attributes.md)
</dt> </dl>

 

 




