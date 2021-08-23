---
description: Gibt die Standardeinstellung für das ursprüngliche Bit im MPEG-1-Audiostream an. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: AVEncMPAOriginalBitstream-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d39b34339e25d08b138fd1c55a64e8a84d6cf4b4db302cbab1e5f50b8ccebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689740"
---
# <a name="avencmpaoriginalbitstream-property"></a>AVEncMPAOriginalBitstream-Eigenschaft

Gibt die Standardeinstellung für das ursprüngliche Bit im MPEG-1-Audiostream an. Diese Eigenschaft gilt für MPEG-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPAOriginalBitstream**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | Beschreibung          |
|----------------|----------------------|
| VARIANT \_ FALSE | Das ursprüngliche Bit ist deaktiviert. |
| VARIANT \_ TRUE  | Das ursprüngliche Bit ist eingeschaltet.  |



 

## <a name="remarks"></a>Hinweise

Der Encoder überschreibt diese Einstellung möglicherweise basierend auf dem Inhalt des Eingabestreams.

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

 

 




