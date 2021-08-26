---
description: Gibt die durchschnittliche codierte Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für die Codierungsmodi Constant Bit Rate (CBR) und Variable Bit Rate (VBR).
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: AVEncCommonMeanBitRate-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c1db672b09e257959a409182288cdfbfd271d0679335c9d9e14048c1e31781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983780"
---
# <a name="avenccommonmeanbitrate-property"></a>AVEncCommonMeanBitRate (Eigenschaft)

Gibt die durchschnittliche codierte Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für die Codierungsmodi Constant Bit Rate (CBR) und Variable Bit Rate (VBR).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonMeanBitRate**

## <a name="property-value"></a>Eigenschaftswert

Encoder können diese Eigenschaft als enumerierte Menge oder als linearen Bereich implementieren.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird auch mit [H.264 UVC 1.5-Kameraencodern verwendet.](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

