---
description: Legt die Anzahl der temporalen Videoebenen für einen Videoencoder fest.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81ceaf82d9d202e97927e0e141aa03a4e8e27c49a28880509aa9bb3c24f9319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743843"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>CODECAPI \_ AVEncVideoTemporalLayerCount (Eigenschaft)

Legt die Anzahl der temporalen Videoebenen für einen Videoencoder fest.

## <a name="data-type"></a>Datentyp

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoTemporalLayerCount**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird auch mit [H.264 UVC 1.5-Kameraencodern verwendet.](camera-encoder-h264-uvc-1-5.md)

CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)und [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sind statische Encodereigenschaften. Nach dem Festlegen werden diese erst wirksam, nachdem ein festgelegter Medientyp auf dem Ausgabepin der Kamera aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

