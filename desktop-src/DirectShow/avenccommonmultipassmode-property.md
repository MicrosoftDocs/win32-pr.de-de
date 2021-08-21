---
description: Gibt die Anzahl der vom Encoder unterstützten Codierungsüberläufe an.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: AVEncCommonMultipassMode-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6fb909e58dbdfd5d1431d0101365db78efa83fd68e9299b8578f19770787fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159808"
---
# <a name="avenccommonmultipassmode-property"></a>AVEncCommonMultipassMode (Eigenschaft)

Gibt die Anzahl der vom Encoder unterstützten Codierungsüberläufe an.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird als Wertebereich zurückgegeben. Um den unterstützten Bereich zu erhalten, rufen [**Sie ICodecAPI::GetParameterRange auf.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)

## <a name="remarks"></a>Hinweise

Die Decodierungslatenz wird als die Datenmenge definiert, die der Decoder puffern muss. Wenn Sie diese Eigenschaft beispielsweise auf **VARIANT \_ TRUE für** einen MPEG-Videoencoder festlegen, werden die Typen von GOP-Strukturen, die der Encoder verwenden kann, beschränkt.

Legen Sie zum Festlegen des aktuellen Codierungspasses die [**EIGENSCHAFT AVEncCommonPassStart**](avenccommonpassstart-property.md) fest.

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

 

 




