---
description: Gibt an, ob der Encoder eine bevorzugte Framegröße verwenden soll, die in der Anzahl von Stichproben pro Frame angegeben ist.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: MFPKEY_REQUESTING_A_FRAMESIZE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c39d1d9ecdba27e46a1e49949f1607fc60d53501d321e49c4899f9b8928ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555430"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY \_ FORDERT EINE \_ \_ FRAMESIZE-Eigenschaft an

Gibt an, ob der Encoder eine bevorzugte Framegröße verwenden soll, die in der Anzahl von Stichproben pro Frame angegeben ist.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ BOOL**

## <a name="remarks"></a>Hinweise

Legen Sie zum Festlegen einer bevorzugten Framegröße die folgenden Eigenschaften fest.

-   Legen **Sie MFPKEY \_ REQUESTING A \_ \_ FRAMESIZE auf** VARIANT TRUE \_ fest.
-   Legen [**Sie MFPKEY \_ PREFERRED \_ FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) auf die Anzahl von Stichproben fest, die Sie in jedem Frame verwenden möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
