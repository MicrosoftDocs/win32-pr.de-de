---
description: Gibt die maximale Anzahl von durch den Encoder unterstützten Durchläufen an.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: MFPKEY_PASSESRECOMMENDED-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215505"
---
# <a name="mfpkey_passesrecommended-property"></a>Mfpkey \_ passesrecommended-Eigenschaft

Gibt die maximale Anzahl von durch den Encoder unterstützten Durchläufen an. Schreibgeschützt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcpassesrecommended, g \_ wszwmcpmaxpass

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Eigenschaft abrufen, indem Sie [iwmcodec-Eigenschaften:: getcodecprop](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)aufrufen. Wenn Sie **IPropertyBag** verwenden, müssen Sie zuerst den FourCC-Wert des gewünschten komprimierten Formats mithilfe der Eigenschaft [mfpkey \_ FourCC](mfpkey-fourccproperty.md) festlegen.

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

 

 




