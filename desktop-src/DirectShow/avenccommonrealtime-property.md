---
description: Gibt an, ob die Anwendung die Codierungsleistung in Echtzeit erfordert.
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: AVEncCommonRealTime-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b718f4f58d230448689700fc2e681c109e645d48cb33eb1788e45ac607350951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403890"
---
# <a name="avenccommonrealtime-property"></a>AVEncCommonRealTime-Eigenschaft

Gibt an, ob die Anwendung die Codierungsleistung in Echtzeit erfordert.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonRealTime**

## <a name="remarks"></a>Hinweise

Um anzugeben, dass die Codierung in Echtzeit ausgeführt werden muss, legen Sie diese Eigenschaft auf **VARIANT \_ TRUE fest.** Codecs können diese Eigenschaft auch als Funktion zurückgeben.

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

 

 




