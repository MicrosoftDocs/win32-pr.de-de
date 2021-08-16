---
description: CLSID einer benutzerdefinierten Videomoderator für die Mediensenke des erweiterten Videorenderers (Enhanced Video Renderer, EVR).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd39cf31cd0efaff4dc4d32756e1e27433d87fac643e4058897babd0f4f50f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877253"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a>MF \_ ACTIVATE CUSTOM VIDEO \_ \_ \_ PRESENTER \_ CLSID-Attribut

CLSID einer benutzerdefinierten Videomoderator für die Mediensenke des erweiterten Videorenderers (Enhanced Video Renderer, EVR).

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Wenn Sie die EVR über ein Aktivierungsobjekt erstellen, können Sie dieses Attribut verwenden, um eine benutzerdefinierte Videowiedergabe auf der EVR festzulegen. Verwenden Sie dieses Attribut wie folgt:

1.  Rufen Sie die [**MFCreateVideoRendererActivate-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) auf, um ein Aktivierungsobjekt für die EVR zu erstellen. Die Funktion gibt einen Zeiger auf die [**INTERFACESActivate-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) zurück.

2.  Legen Sie diese Verteilung auf den [**POINTERACTIVate-Zeiger fest,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) indem Sie [**DIE ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)aufrufen. Der Wert des Attributs ist die CLSID der benutzerdefinierten Videowiedergabe der Anwendung.

Wenn dieses Attribut festgelegt ist, ruft der EVR **CoCreateInstance** mit der angegebenen CLSID auf, um die benutzerdefinierte Videowiedergabe zu erstellen. Die Videopräsentation muss die [**SCHNITTSTELLE "WFVideoPresenter"**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) verfügbar machen. Der Presenter wird als prozessübergreifender COM-Server erstellt.

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
</dt> <dt>

[Schreiben eines EVR-Presenters](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




