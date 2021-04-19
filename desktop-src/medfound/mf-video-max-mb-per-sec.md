---
description: Gibt an, dass die maximale Makroblock-Verarbeitungsrate in Makroblöcke pro Sekunde von dem Hardware Encoder unterstützt wird.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: MF_VIDEO_MAX_MB_PER_SEC-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347010"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>MF- \_ Video \_ Max \_ MB \_ pro Sek \_ .-Attribut

Gibt an, dass die maximale Makroblock-Verarbeitungsrate in Makroblöcke pro [**Sekunde von dem**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)Hardware Encoder unterstützt wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist schreibgeschützt.

**H. 264/AVC-Encoder:**

Dieses Attribut wird von den folgenden Eigenschaften beeinflusst:

-   [MF \_ MT- \_ Video \_ Ebene](mf-mt-video-level.md) (die ein Alias der [MF-MT- \_ \_ \_ Ebene](mf-mt-mpeg2-level-attribute.md)ist)
-   [Codecapi \_ avenccommonqualityvsspeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [Codecapi \_ avencmpvdefaultbpicturecount](../directshow/avencmpvdefaultbpicturecount-property.md)

Wenn das [MF MT-Attribut auf \_ \_ Video \_ Ebene](mf-mt-video-level.md) vorhanden ist, sollte der Encoder die Verarbeitungsrate für die höchste Bitrate und Auflösung zurückgeben, die auf der angegebenen Ebene unterstützt wird. Wenn das MF \_ - \_ \_ Attribut auf Video Ebene nicht vorhanden ist, sollte es eine Standard Ebene von 4 verwenden.

Wenn die Eigenschaft " [codecapi \_ avenccommonqualityvsspeed](../directshow/avenccommonqualityvsspeed-property.md) icodecapi" festgelegt wurde, sollte der Encoder die Verarbeitungsrate zurückgeben, die dem für diese Eigenschaft festgelegten Wert entspricht. Wenn das Attribut codecapi \_ avenccommonqualityvsspeed nicht vorhanden ist, sollte es den Standardwert 0 (null) verwenden, der der schnellste Verarbeitungsmodus sein sollte.

Wenn die Eigenschaft " [codecapi \_ avencmpvdefaultbpicturecount](../directshow/avencmpvdefaultbpicturecount-property.md) icodecapi" auf einen gültigen und unterstützten Wert festgelegt wurde, sollte der Encoder die Verarbeitungsrate zurückgeben, die dem für diese Eigenschaft festgelegten Wert entspricht. Wenn das codecapi- \_ Attribut "avencmpvdefaultbpicturecount" nicht "presen" ist, sollte es einen Standardwert von 0 B-Frames verwenden.

Nur die unteren 28 Bits sollten von einer Anwendung verwendet werden. Die oberen 4 Bits sind für die zukünftige Verwendung reserviert. Anwendungen sollten die oberen 4 Bits ignorieren, und die oberen 4 Bits sollten von MFTs auf 0 festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
