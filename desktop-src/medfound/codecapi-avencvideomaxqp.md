---
description: Gibt den maximalen QP an, der vom Encoder unterstützt wird.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: CODECAPI_AVEncVideoMaxQP-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346051"
---
# <a name="codecapi_avencvideomaxqp-property"></a>Codecapi \_ avencvideomaxqp (Eigenschaft)

Gibt den maximalen QP an, der vom Encoder unterstützt wird.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideomaxqp**

## <a name="remarks"></a>Bemerkungen

**H. 264/AVC-Encoder:**

Der Encoder muss "[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)", " [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)" und " [**getparameterrange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)" unterstützen.

Dies ist eine statische Eigenschaft, die bedeutet, dass Sie nur festgelegt werden kann, bevor die Codierungs Sitzung gestartet wird.

Der Standardwert muss dem maximalen QP entsprechen, der vom entsprechenden Codierungsstandard zulässig ist. Beispielsweise müssen H. 264-Encoder den Standardwert 51 aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Codecapi \_ avencvideominqp](codecapi-avencvideominqp.md)
</dt> </dl>

 

