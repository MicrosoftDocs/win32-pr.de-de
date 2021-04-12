---
description: Gibt ein Aktivierungs Objekt an, das eine benutzerdefinierte Videopräsentation für die EVR-Medien Senke (Enhanced Video Renderer) erstellt.
ms.assetid: 65d88832-0969-4d85-bee2-fd0aa68e9f3b
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75855c18faba8568547f9efcfb19e04574c4885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344608"
---
# <a name="mf_activate_custom_video_presenter_activate-attribute"></a>MF Aktivieren des \_ \_ benutzerdefinierten \_ Video \_ Presenter- \_ Aktivierungs Attributs

Gibt ein Aktivierungs Objekt an, das eine benutzerdefinierte Videopräsentation für die EVR-Medien Senke (Enhanced Video Renderer) erstellt.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Wenn Sie den EVR mithilfe eines Aktivierungs Objekts erstellen, können Sie dieses Attribut verwenden, um eine benutzerdefinierte Videopräsentation für den EVR festzulegen. Verwenden Sie dieses Attribut wie folgt:

1.  Rufen Sie die [_ *mfkreatevideorendereractivation* *](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion auf, um ein Aktivierungs Objekt für den EVR zu erstellen. Die-Funktion gibt einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück.
2.  Legen Sie dieses Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, indem Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)aufrufen. Der Wert des-Attributs ist ein Zeiger auf ein vom Aufrufer implementiertes Aktivierungs Objekt. Das Aktivierungs Objekt des Aufrufers muss die **imfaktivate** -Schnittstelle verfügbar machen.

Wenn Sie dieses Attribut festlegen, ruft der EVR [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf, um den benutzerdefinierten Video Presenter zu erstellen. Die Videopräsentation muss die Schnittstelle [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) verfügbar machen.

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
</dt> <dt>

[Schreiben von EVR Presenter](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




