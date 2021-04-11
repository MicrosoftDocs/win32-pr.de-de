---
description: Gibt an, ob Metadaten in die transcodierte Datei geschrieben werden.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: MF_TRANSCODE_SKIP_METADATA_TRANSFER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214879"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>MF- \_ transcode \_ Skip- \_ \_ metadatenübertragungs-Attribut

Gibt an, ob Metadaten in die transcodierte Datei geschrieben werden. Dieses Container Attribut wird im transcodieren-Profil gespeichert.

## <a name="data-type"></a>Datentyp

**UINT32**

Mögliche Werte für das MF \_ transcode \_ Skip \_ - \_ metadatenübertragungs-Attribut werden in der folgenden Tabelle beschrieben.



| Wert                                                                        | Bedeutung                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Überträgt automatisch Metadaten auf Dateiebene aus der Quelldatei in die transcodierte Datei.<br/> |
| <dl> <dt>1</dt> </dl> | Die Metadaten der Quelldatei werden nicht in die transcodierten Datei geschrieben.<br/>                          |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

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

[**IMF transcodeprofile:: getcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMF transcodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




