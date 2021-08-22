---
description: Gibt die maximale QP an, die vom Encoder unterstützt wird.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: CODECAPI_AVEncVideoMaxQP -Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d95f605dbb647ed96ec40e89870c761400a6d414cd354cb0197bb316bd3cf27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606320"
---
# <a name="codecapi_avencvideomaxqp-property"></a>CODECAPI \_ AVEncVideoMaxQP (Eigenschaft)

Gibt die maximale QP an, die vom Encoder unterstützt wird.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoMaxQP**

## <a name="remarks"></a>Hinweise

**H.264/AVC-Encoder:**

Der Encoder muss [**GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)und [**GetParameterRange unterstützen.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Dies ist eine statische Eigenschaft, die bedeutet, dass sie nur vor beginn der Codierungssitzung festgelegt werden kann.

Der Standardwert muss der maximale QP sein, der vom entsprechenden Codierungsstandard zugelassen wird. H.264-Encoder müssen beispielsweise den Standardwert 51 haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)
</dt> </dl>

 

