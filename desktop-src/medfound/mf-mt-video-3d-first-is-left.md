---
description: Gibt für ein 3D-Videoformat an, welche Ansicht die linke Ansicht ist.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: MF_MT_VIDEO_3D_FIRST_IS_LEFT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393789"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>MF \_ MT \_ \_ -Video 3D \_ erste \_ ist Left- \_ Attribut

Gibt für ein 3D-Videoformat an, welche Ansicht die linke Ansicht ist.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Bei 3D-Videos enthält jedes Video Beispiel zwei Ansichten, die als *erste Ansicht* und *zweite Ansicht* bezeichnet werden. Das genaue Layout der Ansichten im Arbeitsspeicher wird durch das Format Attribut des " [MF \_ MT \_ \_ -Video 3D \_ ](mf-mt-video-3d-format.md) " angegeben.



| Format               | Erste Ansicht              | Zweite Ansicht               |
|----------------------|-------------------------|---------------------------|
| Seite-an-Seite gepackt  | Linke Hälfte des Puffers | Rechte Hälfte des Puffers  |
| Von oben nach unten gepackt | Obere Hälfte des Puffers  | Untere Hälfte des Puffers |
| MultiView            | Puffer Index 0          | Puffer Index 1            |
| Basis Ansicht            | Ganzer Frame            | Nicht vorhanden               |



 

Standardmäßig ist die erste Ansicht die linke Ansicht, die zweite Ansicht ist die Rechte Ansicht. Wenn die linke und die Rechte Ansicht ausgetauscht werden, legen Sie für das MF \_ MT \_ \_ -Video 3D- \_ \_ Attribut erste ist Left- \_ Attribut im Medientyp auf **false** fest.

> [!Note]  
> Im Format der *Basis Ansicht* (**MFVideo3DSampleFormat \_ baseview**) wird nur die Basis Ansicht beibehalten, sodass dieses Attribut nicht angewendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




