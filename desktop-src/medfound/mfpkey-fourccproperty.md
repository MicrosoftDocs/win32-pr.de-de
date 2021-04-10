---
description: Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: MFPKEY_FOURCC-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959418"
---
# <a name="mfpkey_fourcc-property"></a>Mfpkey \_ FourCC-Eigenschaft

Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcfourcc

## <a name="data-type"></a>Datentyp

VT \_ I4 (FourCC-Wert)

## <a name="remarks"></a>Bemerkungen

Sie müssen diesen Wert festlegen, bevor Sie die Werte für die folgenden Eigenschaften mithilfe von **IPropertyBag** oder **IPropertyStore** abrufen:

-   [mfpkey \_ bufferfullnessinfirstbyte](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [mfpkey- \_ passesempfohlen](mfpkey-passesrecommendedproperty.md)

Zum Abrufen der Werte der zuvor aufgeführten FourCC-abhängigen Eigenschaften sollten Sie [**iwmcodecproperties:: getcodecprop**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) verwenden. Wenn Sie **getcodecprop** verwenden, müssen Sie **mfpkey \_ FourCC** nicht festlegen.

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

 

 




