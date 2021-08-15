---
description: Gibt an, ob der Encoder eine durchschnittlich steuerbare VBR-Codierung verwendet.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e7231cb3807be8f4467592ac0138a75ea277bdf8a13dfb3564d3572036e7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874092"
---
# <a name="mfpkey_avgconstrained-property"></a>MFPKEY \_ AVGCONSTRAINED-Eigenschaft

Gibt an, ob der Encoder eine durchschnittlich steuerbare VBR-Codierung verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ BOOL**

## <a name="default-value"></a>Standardwert

**VARIANT \_ FALSE**

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft und die [**MFPKEY \_ VBRENABLED-Eigenschaft**](mfpkey-vbrenabledproperty.md) beide auf **VARIANT \_ TRUE** festgelegt sind, verwendet der Encoder durchschnittlich steuerbare VBR-Codierung. In diesem Fall konfiguriert sich der Encoder gemäß den Werten von [**MFPKEY \_ DYN \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) und [**MFPKEY \_ DYN \_ VBR \_ VBR VBG**](mfpkey-dyn-vbr-ravgproperty.md).

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

 

 
