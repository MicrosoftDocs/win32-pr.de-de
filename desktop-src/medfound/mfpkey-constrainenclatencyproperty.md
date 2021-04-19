---
description: Gibt an, ob der Encoder durch eine maximale Latenz Anforderung eingeschränkt wird.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349782"
---
# <a name="mfpkey_constrainenclatency-property"></a>Mfpkey- \_ einschrängericlatency (Eigenschaft)

Gibt an, ob der Encoder durch eine maximale Latenz Anforderung eingeschränkt wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ false**

## <a name="remarks"></a>Bemerkungen

Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ false** belassen, listet der Encoder einen Standardsatz von Modi auf, die ungefähr 2000 Millisekunden der Encoder-Latenzzeit haben. Wenn Sie diese Eigenschaft auf **Variant \_ true** festlegen, müssen Sie auch eine maximale encoderwartezeit angeben, indem Sie die Eigenschaft " [**mfpkey \_ maxenclatencyms**](mfpkey-maxenclatencymsproperty.md) " festlegen. In diesem Fall erstellt der Encoder Modi, die die Latenz Anforderung erfüllen, und listet nur diese Modi auf. Der Encoder garantiert ein Ausgabe Beispiel, sobald der Encoder Eingaben für einen Zeitraum empfangen hat, der **mfpkey \_ maxenclatencyms** entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
