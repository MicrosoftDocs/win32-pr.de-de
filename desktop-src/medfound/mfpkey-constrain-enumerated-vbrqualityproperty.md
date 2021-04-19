---
description: Gibt an, ob vom Encoder aufgelistete Modi mit den von mfpkey \_ gewünschten \_ vbrquality übereinstimmen.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370934"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>Mfpkey- \_ Einschränkung für \_ aufgelistete \_ vbrquality-Eigenschaft

Gibt an, ob vom Encoder aufgelistete Modi mit den von [**mfpkey \_ gewünschten \_ vbrquality**](mfpkey-desired-vbrqualityproperty.md)übereinstimmen.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ false**

## <a name="remarks"></a>Bemerkungen

Legen Sie die folgenden Codierungs Eigenschaften fest, um VBR-Modi aufzulisten, die eine bestimmte Qualitätsanforderung erfüllen.

-   Legen Sie [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) auf **Variant \_ true** fest.
-   Legen Sie **mfpkey- \_ \_ Enumeration \_ vbrquality** auf **Variant \_ true** fest.
-   Legen Sie für [**mfpkey die \_ gewünschte \_ vbrquality**](mfpkey-desired-vbrqualityproperty.md) auf die gewünschte Qualität fest. Legen Sie für den Modus ohne Verlust die gewünschte Qualität auf 100 fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
