---
description: Gibt auf DERTRANSFORM die maximale Verarbeitungsrate für Makroblocks in Makroblocks pro Sekunde an, die vom Hardwareencoder unterstützt wird.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: MF_VIDEO_MAX_MB_PER_SEC-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c76e6a44a6e0993f9cf6410a0092708da767f92815fc98020dd2f4d88359370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739238"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>MF \_ VIDEO MAX MB PER \_ \_ \_ \_ SEC-Attribut

Gibt bei [**DERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)die maximale Verarbeitungsrate für Makroblocks in Makroblocks pro Sekunde an, die vom Hardwareencoder unterstützt wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist schreibgeschützt.

**H.264/AVC-Encoder:**

Dieses Attribut wird von den folgenden Eigenschaften beeinflusst:

-   [MF \_ MT \_ VIDEO \_ LEVEL](mf-mt-video-level.md) (ein Alias von MF MT [ \_ \_ MPEG2 \_ LEVEL](mf-mt-mpeg2-level-attribute.md))
-   [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

Wenn das [MF \_ MT VIDEO \_ \_ LEVEL-Attribut](mf-mt-video-level.md) vorhanden ist, sollte der Encoder die Verarbeitungsrate für die höchste Bitrate und Auflösung zurückgeben, die auf der angegebenen Ebene unterstützt wird. Wenn das MF \_ MT \_ VIDEO \_ LEVEL-Attribut nicht vorhanden ist, sollte es die Standardebene 4 verwenden.

Wenn die [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI-Eigenschaft festgelegt wurde, sollte der Encoder die Verarbeitungsrate zurückgeben, die dem für diese Eigenschaft festgelegten Wert entspricht. Wenn das \_ CODECAPI AVEncCommonQualityVsSpeed-Attribut nicht vorhanden ist, sollte der Standardwert 0 verwendet werden. Dies sollte der schnellste Verarbeitungsmodus sein.

Wenn die [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI-Eigenschaft auf einen gültigen und unterstützten Wert festgelegt wurde, sollte der Encoder die Verarbeitungsrate zurückgeben, die dem für diese Eigenschaft festgelegten Wert entspricht. Wenn das ATTRIBUT CODECAPI \_ AVEncMPVDefaultBPictureCount nicht vorab angegeben ist, sollte es den Standardwert 0 B Frames verwenden.

Nur die unteren 28 Bits sollten von einer Anwendung verwendet werden. Die oberen 4 Bits sind für die zukünftige Verwendung reserviert. Anwendungen sollten die oberen 4 Bits ignorieren, und MFTs sollten die oberen 4 Bits auf 0 festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
