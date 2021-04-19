---
description: Gibt einen Gerätetyp an, z. b. Audioerfassung oder Video Erfassung.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359882"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a>\_ \_ \_ Quelltyp Attribut des MF-devsource-Attributs \_

Gibt den Typ eines Geräts an, z. b. Audioerfassung oder Video Erfassung.

## <a name="data-type"></a>Datentyp

**GUID**

Die folgenden Werte sind für dieses Attribut definiert:



| Wert                                                                                                                                                                                                                                                                 | Bedeutung                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <dt>**MF \_ devsource \_ - \_ Attribut \_ Quelltyp ( \_ audcap- \_ GUID)**</dt> </dl> | Audioerfassungs Gerät.<br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <dt>**MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ GUID**</dt> </dl> | Video Erfassungsgerät.<br/> |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.

Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Attribut als Eingabe für die folgenden Funktionen:

-   [**MF | atedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MF | atedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**Mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Außerdem wird dieses Attribut für die Aktivierungs Objekte festgelegt, die von der [**mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) -Funktion zurückgegeben werden.

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

 

 




