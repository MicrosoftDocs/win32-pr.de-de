---
description: Gibt an, ob das im Eingabebeispiel festgelegte ROIRectangle-Attribut "MFSampleExtension" \_ verwendet wird oder nicht.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: CODECAPI_AVEncVideoROIEnabled (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86185f6dbb9dfe16a84e7e85c3faddc8da3a7c1ead91dee2b1086e6fafa456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346980"
---
# <a name="codecapi_avencvideoroienabled-property"></a>CODECAPI \_ AVEncVideoROIEnabled (Eigenschaft)

Gibt [an, ob das im Eingabebeispiel festgelegte \_ ROIRectangle-Attribut "MFSampleExtension"](mfsampleextension-roirectangle.md) verwendet wird oder nicht.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>Hinweise

Der Standardwert ist 0.

Wenn ein Encoder MFT einen Wert von 0 (null) akzeptiert, wird erwartet, dass der Encoder das im Eingabebeispiel festgelegte [ \_ ROIRectangle-Attribut "MFSampleExtension"](mfsampleextension-roirectangle.md) akzeptiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




