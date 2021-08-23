---
description: Gibt den Anzeigenamen für ein Gerät an.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90e019b37b251ad8ec00efbd3bd0395659b96c6dd2e3a1cad247ea17ace3ece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973829"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a>ANZEIGENAME-Attribut DES MF \_ \_ \_ DEVSOURCE-ATTRIBUTS \_

Gibt den Anzeigenamen für ein Gerät an. Der *Anzeigename* ist eine für Menschen lesbare Zeichenfolge, die für die Anzeige auf einer Benutzeroberfläche geeignet ist.

## <a name="data-type"></a>Datentyp

**Wchar\***

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)auf.

Um dieses Attribut festzulegen, rufen Sie [**DIE ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)auf.

## <a name="remarks"></a>Hinweise

Dieses Attribut wird für die Aktivierungsobjekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Erfassen von Geräteattributen](capture-device-attributes.md)
</dt> </dl>

 

 




