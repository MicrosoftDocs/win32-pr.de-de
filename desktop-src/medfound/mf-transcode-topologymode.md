---
description: Gibt für eine Transcodierungstopologie an, ob das Topologielader hardwarebasierte Transformationen geladen.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e8715c135e074956af2280b8474172e94e69e1cca20cd01b020fc6dc79076c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663840"
---
# <a name="mf_transcode_topologymode-attribute"></a>MF \_ TRANSCODE \_ TOPOLOGYMODE-Attribut

Gibt für eine Transcodierungstopologie an, ob das Topologielader hardwarebasierte Transformationen geladen.

Der Topologiemodus gibt an, ob Hardwaretransformationen (z. B. Hardwarecodecs) in der Transcodierungstopologie verwendet werden können. Die Anwendung kann dieses Attribut in einem Transcodierungsprofil speichern, indem [**SIE DEN WERTTRANSCODEProfile::SetContainerAttributes aufruft.**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

## <a name="data-type"></a>Datentyp

**[**MF \_ TRANSCODE \_ \_ TOPOLOGYMODE-FLAGS, die**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** als **UINT32 gespeichert sind**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut ist optional. Sie muss einen der folgenden Werte haben.



| Wert                                              | Beschreibung                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HARDWARE FÜR \_ MF-TRANSCODIERUNGSTOPOLOGIEMODUS \_ \_ \_ ZULÄSSIG** | Das Topologielader geladen hardwarebasierte MFTs, z. B. Hardwaredecoder, falls verfügbar.<br/> Das Topologielader verwendet automatisch die Softwaredecodierung, wenn kein Hardwaredecoder gefunden wird oder ein Hardwaredecoder aus irgendeinem Grund keine Verbindung herstellen kann.<br/> |
| **NUR SOFTWARE FÜR \_ \_ MF-TRANSCODIERUNG DES \_ \_ TOPOLOGIEMODUS**    | Das Topologielader geladen nur Software-MFTs, einschließlich Softwaredecodern.                                                                                                                                                                                                    |



 

Der Standardwert ist **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**.

Wenn das Topologielader einen Hardware-MFT in die Topologie einträgt, wird das [Attribut MFT \_ ENUM HARDWARE URL Attribute (MFT-ENUM-HARDWARE-URL-Attribut) \_ \_ \_ ](mft-enum-hardware-url-attribute.md) auf dem Topologieknoten festlegen. Um zu überprüfen, ob ein Hardware-MFT vorhanden ist, aufzählen Sie die Knoten in der aufgelösten Topologie, und überprüfen Sie, ob dieses Attribut vorhanden ist.

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

[Transcodierungs-API](transcode-api.md)
</dt> <dt>

[**CODIERUNGTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**CODIERUNGTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




