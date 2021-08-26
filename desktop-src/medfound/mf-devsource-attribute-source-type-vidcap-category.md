---
description: Gibt die Gerätekategorie für ein Videoaufnahmegerät an.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140a9055bdc8081d5cdea1931b199dcd00f537e73051f30790f036be4af57fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060790"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a>MF \_ \_ DEVSOURCE-ATTRIBUT \_ SOURCE TYPE \_ \_ VIDCAP \_ CATEGORY-Attribut

Gibt die Gerätekategorie für ein Videoaufnahmegerät an.

## <a name="data-type"></a>Datentyp

**GUID**

Der folgende Wert ist definiert.



| Wert                                                                                                                                                                                                                                                             | Bedeutung                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <dt>**CLSID \_ VideoInputDeviceCategory**</dt> </dl> | Videoaufnahmegerät.<br/> |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DANNATTRIBUTEs::GetGUID auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetGUID auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Attribut als Eingabe für die [**MFEnumDeviceSources-Funktion,**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) wenn Sie Videoaufnahmegeräte aufzählen.

Darüber hinaus wird dieses Attribut für die Aktivierungsobjekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Das -Attribut gilt nur für Videoaufnahmegeräte.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Erfassen von Geräteattributen](capture-device-attributes.md)
</dt> </dl>

 

 




