---
description: Gibt an, wie der decodierte Videostream geschachtelt wird.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: AVDecVideoInputScanType-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b86c9499019cdc07f095bf65be5817b828c78d277b02810bc1612cc0365edce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108700"
---
# <a name="avdecvideoinputscantype-property"></a>AVDecVideoInputScanType(Eigenschaft)

Gibt an, wie der decodierte Videostream geschachtelt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoInputScanType**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVDecVideoInputScanType-Enumeration.**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)

## <a name="remarks"></a>Hinweise

Die oberen 16 Bits des Werts enthalten die Breite, und die unteren 16 Bits enthalten die Höhe.

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

 

