---
description: Handle für das Video Clipping-Fenster.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: MF_ACTIVATE_VIDEO_WINDOW-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351784"
---
# <a name="mf_activate_video_window-attribute"></a>MF \_ - \_ Video \_ Fenster Attribut aktivieren

Handle für das Video Clipping-Fenster.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **DWORD \_ ptr** (**HWND**) behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für das Aktivierungs Objekt für den erweiterten Videorenderer (EVR). Der Wert wird automatisch festgelegt, wenn Sie [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) aufrufen, um das EVR-Aktivierungs Objekt zu erstellen.

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

[**Imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[Aktivierungs Objekte](activation-objects.md)
</dt> </dl>

 

 




