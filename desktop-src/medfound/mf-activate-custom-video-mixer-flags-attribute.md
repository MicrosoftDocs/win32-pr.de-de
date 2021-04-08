---
description: Gibt an, wie ein benutzerdefinierter Mixer für den erweiterten Videorenderer (EVR) erstellt wird.
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757867"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>MF \_ - \_ Attribut für benutzerdefinierte \_ Video- \_ \_ mischflags aktivieren

Gibt an, wie ein benutzerdefinierter Mixer für den erweiterten Videorenderer (EVR) erstellt wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festlegen, der von der MF-Funktion der [**MF**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion abgerufen wird. Der Wert dieses Attributs ist ein bitweises **or** der folgenden Werte.



| Wert                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ Aktivieren von \_ benutzerdefiniertem \_ Mixer \_ allowfail** | Wenn die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode den benutzerdefinierten Mixer der Anwendung nicht erstellen kann, wird stattdessen der standardmäßige EVR-Mixer verwendet. Wenn das [**imfactivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Objekt bei der Erstellung des benutzerdefinierten Mischers fehlschlägt, schlägt die **activateobject** -Methode standardmäßig fehl. |



 

Anwendungen können das CLSID-Attribut " [**\_ \_ benutzerdefiniertes \_ Video- \_ Mixer \_ aktivieren**](mf-activate-custom-video-mixer-clsid-attribute.md) " verwenden, um einen benutzerdefinierten Mixer für den EVR anzugeben.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Erweiterte Videorenderer-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Aktivierungs Objekte](activation-objects.md)
</dt> </dl>

 

 




