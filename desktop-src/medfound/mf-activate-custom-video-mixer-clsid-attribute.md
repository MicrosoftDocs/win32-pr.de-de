---
description: CLSID eines benutzerdefinierten Video Mischers für die EVR-Medien Senke (Enhanced Video Renderer).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343948"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a>\_ \_ Benutzerdefiniertes \_ \_ \_ CLSID-Attribut für benutzerdefiniertes Video

CLSID eines benutzerdefinierten Video Mischers für die EVR-Medien Senke (Enhanced Video Renderer).

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Wenn Sie den EVR mithilfe eines Aktivierungs Objekts erstellen, können Sie dieses Attribut verwenden, um einen benutzerdefinierten Videomixer auf dem EVR festzulegen. Verwenden Sie dieses Attribut wie folgt:

1.  Rufen Sie die [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion auf, um ein Aktivierungs Objekt für den EVR zu erstellen. Die-Funktion gibt einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück.

2.  Legen Sie diese Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, indem Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)aufrufen. Der Wert des-Attributs ist die CLSID des benutzerdefinierten Video Mischers der Anwendung.

Wenn dieses Attribut festgelegt ist, ruft der EVR **cokreateinstance** mit der angegebenen CLSID auf, um den benutzerdefinierten Video Mischungs Wert zu erstellen. Der Video-Mixer muss die [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle verfügbar machen. Der Mixer wird als Prozess interner com-Server erstellt.

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

[**Imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**Imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Aktivierungs Objekte](activation-objects.md)
</dt> </dl>

 

 




