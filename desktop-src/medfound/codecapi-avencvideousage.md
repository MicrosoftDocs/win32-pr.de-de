---
description: Legt die Videoverwendung für einen Videoencoder fest.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: CODECAPI_AVEncVideoUsage (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6d3ee174fbc22ca7b1ab4e309d87112463740a075b497cc35033f8c96bbe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777710"
---
# <a name="codecapi_avencvideousage-property"></a>CODECAPI \_ AVEncVideoUsage (Eigenschaft)

Legt die Videoverwendung für einen Videoencoder fest.

## <a name="data-type"></a>Datentyp

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoUsage**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird auch mit [H.264 UVC 1.5-Kameraencodern verwendet.](camera-encoder-h264-uvc-1-5.md)

[CODECAPI \_ AVEncVideoTemporalLayerCount,](codecapi-avencvideotemporallayercount.md)CODECAPI \_ AVEncVideoUsage und [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sind statische Encodereigenschaften. Nach dem Festlegen werden diese erst wirksam, nachdem ein festgelegter Medientyp auf dem Ausgabepin der Kamera aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

