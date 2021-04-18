---
description: Gibt an, ob der Encoder eine Average-steuerbare VBR-Codierung verwendet.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345050"
---
# <a name="mfpkey_avgconstrained-property"></a>Avgeingeschränkter mfpkey- \_ Eigenschaft

Gibt an, ob der Encoder eine Average-steuerbare VBR-Codierung verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ false**

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft und die Eigenschaft [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) beide auf **Variant \_ true** festgelegt sind, verwendet der Encoder die Durchschnitt Bare VBR-Codierung. In diesem Fall konfiguriert der Encoder sich entsprechend den Werten von [**mfpkey \_ dyn \_ VBR \_ bavg**](mfpkey-dyn-vbr-bavgproperty.md) und [**mfpkey \_ dyn \_ VBR \_ Ravg**](mfpkey-dyn-vbr-ravgproperty.md).

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

 

 
