---
description: Gibt für eine transcodetopologie an, ob das topologielader hardwarebasierte Transformationen lädt.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863171"
---
# <a name="mf_transcode_topologymode-attribute"></a>MF- \_ transcode- \_ topologymode-Attribut

Gibt für eine transcodetopologie an, ob das topologielader hardwarebasierte Transformationen lädt.

Der topologiemodus gibt an, ob Hardware Transformationen (z. b. Hardware Codecs) in der transcodieren-Topologie verwendet werden können. Die Anwendung kann dieses Attribut in einem transcodieren-Profil speichern, indem [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)aufgerufen wird.

## <a name="data-type"></a>Datentyp

**[**MF \_ Transcode- \_ topologymode- \_ Flags**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** , die als **UInt32** gespeichert sind

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional. Er muss einen der folgenden Werte aufweisen.



| Wert                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF- \_ transcode- \_ topologymode- \_ Hardware \_ zulässig** | Das topologielader lädt hardwarebasierte MFTs (z. b. Hardware Decoder), wenn diese verfügbar sind.<br/> Das topologielader greift automatisch auf Software Decodierung zurück, wenn kein Hardware Decoder gefunden wird oder wenn ein Hardware Decoder aus irgendeinem Grund keine Verbindung herstellen kann.<br/> |
| **nur für die MF- \_ transcode- \_ topologymode- \_ Software \_**    | Das topologielader lädt nur Software-MFTs, einschließlich Software Decoder.                                                                                                                                                                                                    |



 

Der Standardwert ist **nur für die MF- \_ transcode- \_ topologymode- \_ Software \_**.

Wenn das topologielader eine Hardware-MFT in die Topologie einfügt, wird das Attribut Attribut der [MFT- \_ Enum- \_ Hardware- \_ \_ URL](mft-enum-hardware-url-attribute.md) für den topologieknoten festgelegt. Um zu überprüfen, ob eine Hardware-MFT vorhanden ist, müssen Sie die Knoten in der aufgelösten Topologie auflisten und überprüfen, ob dieses Attribut vorhanden ist.

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

[Transcode-API](transcode-api.md)
</dt> <dt>

[**IMF transcodeprofile:: getcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMF transcodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




