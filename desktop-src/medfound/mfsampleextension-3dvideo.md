---
description: Gibt an, ob ein Medien Beispiel einen 3D-Videoframe enthält.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: MFSampleExtension_3DVideo-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355570"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>MF Sample Extension \_ 3dvideo-Attribut

Gibt an, ob ein Medien Beispiel einen 3D-Videoframe enthält.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut " **true**" ist, enthält das Beispiel "Media" einen Videorahmen mit mindestens zwei stereoskopischen Ansichten. Der Standardwert ist **FALSE**.

Eine Komponente, die 3D-Video Frames generiert, sollte dieses Attribut für jedes Medien Beispiel, das einen 3D-Frame enthält, auf " **true** " festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MF Sample Extension \_ 3dvideo \_ Sample Format](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




