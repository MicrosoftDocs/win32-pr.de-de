---
description: Bei einem 3D-Videoformat gibt an, welche Ansicht die linke Ansicht ist.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: MF_MT_VIDEO_3D_FIRST_IS_LEFT-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b7deed122f3de419455abf54bfcc18ad50ef199d87afa8bcaad8d34000a011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876801"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>MF \_ MT \_ VIDEO \_ 3D \_ FIRST IS \_ \_ LEFT-Attribut

Bei einem 3D-Videoformat gibt an, welche Ansicht die linke Ansicht ist.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Für 3D-Videos enthält jedes Videobeispiel zwei Ansichten, die als *erste Ansicht* und *zweite Ansicht* festgelegt sind. Das genaue Layout der Ansichten im Arbeitsspeicher wird durch das [MF \_ MT VIDEO \_ \_ 3D \_ FORMAT-Attribut](mf-mt-video-3d-format.md) angegeben.



| Format               | Erste Ansicht              | Zweite Ansicht               |
|----------------------|-------------------------|---------------------------|
| Nebeneinander gepackt  | Linke Hälfte des Puffers | Rechte Hälfte des Puffers  |
| Von oben nach unten gepackt | Obere Hälfte des Puffers  | Untere Hälfte des Puffers |
| Multiview            | Pufferindex 0          | Pufferindex 1            |
| Basisansicht            | Gesamter Frame            | Nicht vorhanden               |



 

Standardmäßig ist die erste Ansicht die linke Ansicht, und die zweite Ansicht ist die rechte Ansicht. Wenn die linke und die rechte Ansicht ausgetauscht werden, legen Sie das \_ MF MT \_ VIDEO \_ 3D \_ FIRST IS \_ \_ LEFT-Attribut im Medientyp auf **FALSE** fest.

> [!Note]  
> Im *Basisansichtsformat* **(MFVideo3DSampleFormat \_ BaseView)** wird nur die Basisansicht beibehalten, sodass dieses Attribut nicht angewendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




