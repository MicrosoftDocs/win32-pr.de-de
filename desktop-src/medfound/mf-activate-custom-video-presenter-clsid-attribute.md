---
description: CLSID eines benutzerdefinierten Video Präsentators für die EVR-Medien Senke (Enhanced Video Renderer).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343719"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a>MF \_ \_ benutzerdefiniertes \_ \_ CLSID-Attribut für Video Presenter \_ aktivieren

CLSID eines benutzerdefinierten Video Präsentators für die EVR-Medien Senke (Enhanced Video Renderer).

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Wenn Sie den EVR mithilfe eines Aktivierungs Objekts erstellen, können Sie dieses Attribut verwenden, um eine benutzerdefinierte Videopräsentation für den EVR festzulegen. Verwenden Sie dieses Attribut wie folgt:

1.  Rufen Sie die [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion auf, um ein Aktivierungs Objekt für den EVR zu erstellen. Die-Funktion gibt einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück.

2.  Legen Sie diese Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, indem Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)aufrufen. Der Wert des-Attributs ist die CLSID des benutzerdefinierten Video Presenter der Anwendung.

Wenn dieses Attribut festgelegt ist, ruft der EVR **cokreateinstance** mit der angegebenen CLSID auf, um den benutzerdefinierten Video Presenter zu erstellen. Die Videopräsentation muss die Schnittstelle [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) verfügbar machen. Der Presenter wird als Prozess interner com-Server erstellt.

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
</dt> <dt>

[Schreiben von EVR Presenter](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




