---
description: Gibt die Standardeinstellung für das Copyrightbit im MPEG-1-Audiostream an. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: AVEncMPACopyright-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd747de4f4351e5d540fcf8235194308457e0dcc985500f2743209061cedbdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824270"
---
# <a name="avencmpacopyright-property"></a>AVEncMPACopyright-Eigenschaft

Gibt die Standardeinstellung für das Copyrightbit im MPEG-1-Audiostream an. Diese Eigenschaft gilt für MPEG-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPACopyright**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann die folgenden Werte haben.



| Wert          | BESCHREIBUNG           |
|----------------|-----------------------|
| VARIANT \_ FALSE | Copyright-Bit ist deaktiviert. |
| VARIANT \_ TRUE  | Copyright-Bit ist ein on.  |



 

## <a name="remarks"></a>Hinweise

Der Encoder kann diese Einstellung basierend auf dem Inhalt des Eingabestreams überschreiben.

## <a name="requirements"></a>Requirements (Anforderungen)



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

 

 




