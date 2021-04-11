---
description: Gibt die Qualität der Ausgabe an.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: MFPKEY_WMRESAMP_FILTERQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215041"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a>Mfpkey \_ wmresamp \_ filterquality (Eigenschaft)

Gibt die Qualität der Ausgabe an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="applies-to"></a>Gilt für

-   [Audioresampler-DSP](audioresampler.md)

## <a name="remarks"></a>Bemerkungen

Der gültige Bereich dieser Eigenschaft liegt zwischen 1 und 60 (einschließlich). Höhere Werte führen zu einer Ausgabe höherer Qualität, führen jedoch zu einer höheren Latenz. Der Wert 1 ist im Wesentlichen identisch mit der linearen interpolung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
