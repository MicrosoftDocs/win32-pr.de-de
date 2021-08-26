---
description: Gibt eine numerische Darstellung des Kompromisses zwischen Bewegungsglättung und Bildqualität der Codecausgabe an.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 177ae5e9d1c8a9aba359000e04483c8e45c44f823c9db924155dd5ef3d5989a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954260"
---
# <a name="mfpkey_crisp-property"></a>\_MFPKEY-EIGENSCHAFT "KEYKEY"

Gibt eine numerische Darstellung des Kompromisses zwischen Bewegungsglättung und Bildqualität der Codecausgabe an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCCrisp

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

75

## <a name="remarks"></a>Hinweise

Dieser ganzzahlige Wert kann zwischen 0 und 100 liegen. Je höher der Wert ist, desto stärker optimiert der Codec die Codierung für die Bildqualität einzelner Frames, was in der Regel die Bewegungsglättung reduziert.

Diese Eigenschaft sollte nur für die CBR-Codierung (Constant Bit Rate) festgelegt werden. Die Optimierungen für die VBR-Codierung (Variable Bit Rate) funktionieren anders.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




