---
description: Profilflags, die die streameinstellungen für die transcodieren-Topologie definieren. Die Flags werden in der MF- \_ Enumeration für das transcodeanpassungsecodeumeration definiert \_ \_ \_ .
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: MF_TRANSCODE_ADJUST_PROFILE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348829"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>MF- \_ transcode- \_ Anpassungs \_ Profil Attribut

Profilflags, die die streameinstellungen für die transcodieren-Topologie definieren. Die Flags werden in der MF-Enumeration für das [**\_ \_ \_ \_ transcodeanpassungsecodeumeration**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) definiert.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann dieses Attribut auf Container Ebene für das transcodieren-Profil festlegen. Wenn dieses Attribut festgelegt ist, ändert die MF-Funktion die Stream-Attribute bei der [**topologiebildung**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) abhängig vom angegebenen Flag. Wenn die Anwendung z. b. das kennflag für das **MF- \_ transcode- \_ Anpassungs \_ Profil \_** angibt, werden die von der Anwendung angegebenen streameinstellungen verwendet, um das Profil zu erstellen.

Für den Videostream wird die Framerate basierend auf der Medienquelle aktualisiert. Wenn die Anwendung den Zeilen Sprung Modus nicht angibt, wird das Profil so aktualisiert, dass standardmäßig progressive Frames verwendet werden.

Wenn in der Anwendung das Flag für die **\_ Verwendung der \_ \_ \_ \_ Quell \_ Attribute für das MF-transcodieren-Profil** angegeben ist, werden fehlende Datenstrom Attribute aus der Eingabemedien Quelle in die streameinstellungen im transcodieren-Profil kopiert.

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

[**IMF transcodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




