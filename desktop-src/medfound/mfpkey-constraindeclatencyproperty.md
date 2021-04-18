---
description: Gibt an, ob der Encoder durch eine maximale Anzahl von decoderlatenzanforderungen eingeschränkt wird.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: MFPKEY_CONSTRAINDECLATENCY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345285"
---
# <a name="mfpkey_constraindeclatency-property"></a>Mfpkey- \_ einschränkeyclatency (Eigenschaft)

Gibt an, ob der Encoder durch eine maximale Anzahl von decoderlatenzanforderungen eingeschränkt wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ false**

## <a name="remarks"></a>Bemerkungen

Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ false** belassen, listet der Encoder einen Standardsatz von Modi auf, die ungefähr 1500 Millisekunden von Decoder-Latenzzeit haben. Wenn Sie diese Eigenschaft auf **Variant \_ true** festlegen, müssen Sie auch eine maximale decoderwartezeit angeben, indem Sie die Eigenschaft " [**mfpkey \_ maxdeclatencyms**](mfpkey-maxdeclatencymsproperty.md) " festlegen. In diesem Fall erstellt der Encoder Modi, die die Latenz Anforderung erfüllen, und listet nur diese Modi auf. Der Encoder stellt sicher, dass die vorab Anforderungen (Decoder-Puffergröße) kleiner oder gleich **mfpkey \_ maxdeclatencyms** sind.

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

 

 
