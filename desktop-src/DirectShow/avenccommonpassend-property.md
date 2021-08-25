---
description: Beendet den aktuellen Codierungsdurchlauf oder fragt ab, ob der aktuelle Codierungsdurchlauf der letzte ist.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: AVEncCommonPassEnd-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02faeb9d78f10b962b7134fd316bda348b0f03e1a82ace210956c2243231df19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873370"
---
# <a name="avenccommonpassend-property"></a>AVEncCommonPassEnd-Eigenschaft

Beendet den aktuellen Codierungsdurchlauf oder fragt ab, ob der aktuelle Codierungsdurchlauf der letzte ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Hinweise

Wenn Sie diese Eigenschaft auf **VARIANT \_ TRUE** festlegen, wird der aktuelle Codierungsdurchlauf beendet. Wenn Sie diese Eigenschaft auf **VARIANT \_ FALSE** festlegen, wird die Multipasscodierung beendet.

Beim Lesen dieser Eigenschaft wird abgefragt, ob der aktuelle Codierungsdurchlauf der letzte ist.

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

 

 




