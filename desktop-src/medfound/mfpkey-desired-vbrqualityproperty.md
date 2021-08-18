---
description: Gibt den gewünschten Qualitätsgrad für die qualitätsbasierte (1-Durch-) VBR-Codierung (Variable Bit Rate) von Audiostreams an.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f52ab8cc791a5309b5df6537d133bce68e49d66a15ab79c12beeb7411cece8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939943"
---
# <a name="mfpkey_desired_vbrquality-property"></a>GEWÜNSCHTE \_ \_ VBRQUALITY-Eigenschaft für MFPKEY

Gibt den gewünschten Qualitätsgrad für die qualitätsbasierte (1-Durch-) VBR-Codierung (Variable Bit Rate) von Audiostreams an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Dieser Wert kann zwischen 0 und 100 sein, wobei 100 die maximale Qualität ist. Der Wert 0 gibt an, dass die qualitätsbasierte VBR-Codierungsmethode nicht verwendet werden soll.

Legen Sie die folgenden Encodereigenschaften fest, um VBR-Modi aufzählen zu können, die eine bestimmte Qualitätsanforderung erfüllen.

-   Legen [**Sie MFPKEY \_ VBRENABLED auf**](mfpkey-vbrenabledproperty.md) VARIANT TRUE **\_ fest.**
-   Legen [**Sie MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) auf **VARIANT TRUE \_ fest.**
-   Legen **Sie MFPKEY \_ DESIRED \_ VBRQUALITY auf** die gewünschte Qualität fest. Legen Sie für verlustfreie Modi die gewünschte Qualität auf 100 fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
