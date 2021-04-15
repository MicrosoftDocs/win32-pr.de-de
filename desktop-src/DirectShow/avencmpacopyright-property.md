---
description: Gibt die Standardeinstellung für das Copyright-Bit im MPEG-1-Audiodatenstrom an. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Avencmpacopyright-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392758"
---
# <a name="avencmpacopyright-property"></a>Avencmpacopyright (Eigenschaft)

Gibt die Standardeinstellung für das Copyright-Bit im MPEG-1-Audiodatenstrom an. Diese Eigenschaft gilt für MPEG-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencmpacopyright**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG           |
|----------------|-----------------------|
| Variant \_ false | Copyright-Bit ist deaktiviert. |
| Variant \_ true  | Copyright-Bit ist on.  |



 

## <a name="remarks"></a>Bemerkungen

Der Encoder kann diese Einstellung basierend auf dem Inhalt des Eingabestreams überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




