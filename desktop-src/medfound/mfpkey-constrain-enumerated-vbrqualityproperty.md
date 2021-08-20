---
description: Gibt an, ob vom Encoder aufzählte Modi auf diejenigen gesetzt werden, die eine von MFPKEY \_ DESIRED \_ VBRQUALITY gegebene Qualitätsanforderung erfüllen.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d138bbf7e9e77673821b6deed574b7395a3d4e51269e71b18b67cda711ed4bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690442"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY-Eigenschaft

Gibt an, ob vom Encoder aufzählte Modi auf diejenigen gesetzt werden, die eine Qualitätsanforderung von [**MFPKEY \_ DESIRED \_ VBRQUALITY erfüllen.**](mfpkey-desired-vbrqualityproperty.md)

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ BOOL**

## <a name="default-value"></a>Standardwert

**VARIANT \_ FALSE**

## <a name="remarks"></a>Hinweise

Legen Sie die folgenden Encodereigenschaften fest, um VBR-Modi aufzählen zu können, die eine bestimmte Qualitätsanforderung erfüllen.

-   Legen [**Sie MFPKEY \_ VBRENABLED auf**](mfpkey-vbrenabledproperty.md) VARIANT TRUE **\_ fest.**
-   Legen **Sie MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY** auf **VARIANT TRUE \_ fest.**
-   Legen [**Sie MFPKEY \_ DESIRED \_ VBRQUALITY auf**](mfpkey-desired-vbrqualityproperty.md) die gewünschte Qualität fest. Legen Sie für verlustfreie Modi die gewünschte Qualität auf 100 fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
