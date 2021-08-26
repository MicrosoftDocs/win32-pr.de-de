---
description: Startet den ersten Codierungsdurchlauf.
ms.assetid: a062be3f-7806-4f1c-b98e-2c9ed31f010c
title: AVEncCommonPassStart-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7830537e6345d43927c7009e0e3ec9148505217818e981d7354a100a4ff2d68e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000140"
---
# <a name="avenccommonpassstart-property"></a>AVEncCommonPassStart-Eigenschaft

Startet den ersten Codierungsdurchlauf.

Diese Eigenschaft ist lesegeschützt.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonPassStart**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist der zu startde Codierungsdurchlauf. Um den Bereich der unterstützten Werte abzurufen, fragen Sie die [**AVEncCommonMultipassMode-Eigenschaft**](avenccommonmultipassmode-property.md) des Encoders ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




