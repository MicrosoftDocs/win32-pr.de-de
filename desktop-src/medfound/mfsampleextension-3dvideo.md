---
description: Gibt an, ob ein Medienbeispiel einen 3D-Videoframe enthält.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: MFSampleExtension_3DVideo -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb959accfb3326e90068a26247eeab25e9aeaddacb720a0dfd64aa6e5b237a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722800"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>MFSampleExtension \_ 3DVideo-Attribut

Gibt an, ob ein Medienbeispiel einen 3D-Videoframe enthält.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut **TRUE ist,** enthält das Medienbeispiel einen Videoframe, der über zwei oder mehr stereoleere Ansichten verfügt. Der Standardwert ist **FALSE**.

Eine Komponente, die 3D-Videoframes generiert, sollte dieses Attribut für jedes Medienbeispiel, das einen 3D-Frame enthält, auf **TRUE** festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




