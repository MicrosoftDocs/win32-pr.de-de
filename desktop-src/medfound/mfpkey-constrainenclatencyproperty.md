---
description: Gibt an, ob der Encoder durch eine maximale Latenzanforderung eingeschränkt ist.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172b92b0b4d39602f0535b8bf1ef4456a896972e56c6da10f6585e5221fa7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113420"
---
# <a name="mfpkey_constrainenclatency-property"></a>MFPKEY \_ CONSTRAINENCLATENCY-Eigenschaft

Gibt an, ob der Encoder durch eine maximale Latenzanforderung eingeschränkt ist.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ BOOL**

## <a name="default-value"></a>Standardwert

**VARIANT \_ FALSE**

## <a name="remarks"></a>Hinweise

Wenn Sie diese Eigenschaft bei ihrem Standardwert **VARIANT \_ FALSE** belassen, zählt der Encoder einen Standardsatz von Modi auf, die eine Encoderlatenz von ca. 2.000 Millisekunden aufweisen. Wenn Sie diese Eigenschaft auf **VARIANT \_ TRUE** festlegen, müssen Sie auch eine maximale Encoderlatenz angeben, indem Sie die [**MFPKEY \_ MAXENCLATENCYMS-Eigenschaft**](mfpkey-maxenclatencymsproperty.md) festlegen. In diesem Fall erstellt der Encoder Modi, die die Latenzanforderung erfüllen, und listet nur diese Modi auf. Der Encoder garantiert ein Ausgabebeispiel, sobald der Encoder eine Eingabe für einen Zeitraum erhalten hat, der **MFPKEY \_ MAXENCLATENCYMS entspricht.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
