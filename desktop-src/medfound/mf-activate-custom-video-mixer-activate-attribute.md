---
description: Gibt ein Aktivierungsobjekt an, das einen benutzerdefinierten Videomixer für die EVR-Mediensenke (Enhanced Video Renderer) erstellt.
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1966efe66efaba56c0206a9f6fac59aba30a1aea9d47100c4ce19a30af96a863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877297"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>MF \_ ACTIVATE CUSTOM VIDEO MIXER \_ \_ \_ \_ ACTIVATE-Attribut

Gibt ein Aktivierungsobjekt an, das einen benutzerdefinierten Videomixer für die EVR-Mediensenke (Enhanced Video Renderer) erstellt.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Hinweise

Wenn Sie die EVR über ein Aktivierungsobjekt erstellen, können Sie mit diesem Attribut einen benutzerdefinierten Videomixer für die EVR festlegen. Verwenden Sie dieses Attribut wie folgt:

1.  Rufen Sie die [**Funktion MFCreateVideoRendererActivate auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) um ein Aktivierungsobjekt für die EVR zu erstellen. Die -Funktion gibt einen Zeiger auf die [**BERACTIVate-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) zurück.
2.  Legen Sie dieses Attribut auf dem [**ZEIGER FÜR DIE AKTION**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) fest, indem Sie DURCH AUFRUFEN VON [**ATTRIBUTEs::SetUnknown aufrufen.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) Der Wert des Attributs ist ein Zeiger auf ein Aktivierungsobjekt, das vom Aufrufer implementiert wird. Das Aktivierungsobjekt des Aufrufers muss die **BERACTIVate-Schnittstelle verfügbar** machen.

Wenn Sie dieses Attribut festlegen, ruft der EVR [**DEN BENUTZERDEFINIERTEN Aktivieren::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf, um den benutzerdefinierten Videomixer zu erstellen. Der Videomixer muss die [**BENUTZEROBERFLÄCHETransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verfügbar machen.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Erweiterte Videorendererattribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEs::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**ACTIVate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Aktivierungsobjekte](activation-objects.md)
</dt> </dl>

 

 




