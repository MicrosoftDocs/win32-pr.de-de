---
description: Gibt ein Aktivierungs Objekt an, das einen benutzerdefinierten Videomixer für die EVR-Medien Senke (Enhanced Video Renderer) erstellt.
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130728"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>MF-Attribut zum Aktivieren des \_ \_ benutzerdefinierten \_ Video \_ Mischers \_ aktivieren

Gibt ein Aktivierungs Objekt an, das einen benutzerdefinierten Videomixer für die EVR-Medien Senke (Enhanced Video Renderer) erstellt.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Wenn Sie den EVR mithilfe eines Aktivierungs Objekts erstellen, können Sie dieses Attribut verwenden, um einen benutzerdefinierten Videomixer auf dem EVR festzulegen. Verwenden Sie dieses Attribut wie folgt:

1.  Rufen Sie die [_ *mfkreatevideorendereractivation* *](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion auf, um ein Aktivierungs Objekt für den EVR zu erstellen. Die-Funktion gibt einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück.
2.  Legen Sie dieses Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, indem Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)aufrufen. Der Wert des-Attributs ist ein Zeiger auf ein vom Aufrufer implementiertes Aktivierungs Objekt. Das Aktivierungs Objekt des Aufrufers muss die **imfaktivate** -Schnittstelle verfügbar machen.

Wenn Sie dieses Attribut festlegen, ruft der EVR [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf, um den benutzerdefinierten Video Mischungs Wert zu erstellen. Der Video-Mixer muss die [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle verfügbar machen.

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

[**Imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**Imfattributes:: *-Known**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**Imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Aktivierungs Objekte](activation-objects.md)
</dt> </dl>

 

 




