---
description: CLSID eines benutzerdefinierten Videomixers für die MEDIENSenke des erweiterten Videorenderers (Enhanced Video Renderer, EVR).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a110d6ef5b6cc65fcf3d81fc252737bbcc70575c2d1600751281f9222b032a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464580"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a>MF \_ ACTIVATE CUSTOM VIDEO MIXER \_ \_ \_ \_ CLSID-Attribut

CLSID eines benutzerdefinierten Videomixers für die MEDIENSenke des erweiterten Videorenderers (Enhanced Video Renderer, EVR).

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Wenn Sie die EVR über ein Aktivierungsobjekt erstellen, können Sie dieses Attribut verwenden, um einen benutzerdefinierten Videomixer auf der EVR festzulegen. Verwenden Sie dieses Attribut wie folgt:

1.  Rufen Sie die [**MFCreateVideoRendererActivate-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) auf, um ein Aktivierungsobjekt für die EVR zu erstellen. Die Funktion gibt einen Zeiger auf die [**INTERFACESActivate-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) zurück.

2.  Legen Sie diese Verteilung auf den [**POINTERACTIVate-Zeiger fest,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) indem Sie [**DIE ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)aufrufen. Der Wert des Attributs ist die CLSID des benutzerdefinierten Videomixers der Anwendung.

Wenn dieses Attribut festgelegt ist, ruft die EVR **CoCreateInstance** mit der angegebenen CLSID auf, um den benutzerdefinierten Videomixer zu erstellen. Der Videomixer muss die [**INTERFACESTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verfügbar machen. Der Mixer wird als prozessübergreifender COM-Server erstellt.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Erweiterte Videorendererattribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**SPRECHATTRIBUTE::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**ÜBER DIE AKTIONAKTIVIEREN**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Aktivierungsobjekte](activation-objects.md)
</dt> </dl>

 

 




