---
description: Gibt die Gerätekategorie für ein Video Erfassungsgerät an.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129785"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a>MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ Category-Attribut

Gibt die Gerätekategorie für ein Video Erfassungsgerät an.

## <a name="data-type"></a>Datentyp

**GUID**

Der folgende Wert ist definiert.



| Wert                                                                                                                                                                                                                                                             | Bedeutung                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <dt>**CLSID \_ videoinputentvicecategory**</dt> </dl> | Video Erfassungsgerät.<br/> |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.

Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Attribut als Eingabe für die [**mfenumtvicesources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) -Funktion, wenn Sie Video Erfassungsgeräte aufzählen.

Außerdem wird dieses Attribut für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MF | atedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**Mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Das-Attribut gilt nur für Video Erfassungsgeräte.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Geräte Attribute erfassen](capture-device-attributes.md)
</dt> </dl>

 

 




