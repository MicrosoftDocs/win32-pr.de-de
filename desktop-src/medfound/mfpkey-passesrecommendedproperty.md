---
description: Gibt die maximale Anzahl von Durchläufen an, die vom Encoder unterstützt werden.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: MFPKEY_PASSESRECOMMENDED-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af869c6acca584547083b3de245913a35680306b47feabaf2a602a3c1c15e87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826360"
---
# <a name="mfpkey_passesrecommended-property"></a>MFPKEY \_ PASSESRECOMMENDED-Eigenschaft

Gibt die maximale Anzahl von Durchläufen an, die vom Encoder unterstützt werden. Schreibgeschützt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Eigenschaft abrufen, die [IWMCodecProps::GetCodecProp aufruft.](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) Wenn Sie **IPropertyBag** verwenden, müssen Sie zuerst den FOURCC-Wert des gewünschten komprimierten Formats mithilfe der [MFPKEY \_ FOURCC-Eigenschaft](mfpkey-fourccproperty.md) festlegen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




