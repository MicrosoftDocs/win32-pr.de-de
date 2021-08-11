---
description: Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich steuerbaren VBR-Codierung konfiguriert ist.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: MFPKEY_DYN_VBR_RAVG-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ee3d3a9b9a60b664041b9c6f84c38b8da9ceef87f73177f2ace792cf043992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242612"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>MFPKEY \_ DYN \_ VBR \_ RAVG-Eigenschaft

Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich steuerbaren VBR-Codierung konfiguriert ist.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mithilfe von [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ I4**

## <a name="remarks"></a>Hinweise

Wenn die [**Eigenschaften MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) und [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) beide auf **VARIANT \_ TRUE** festgelegt sind, verwendet der Encoder die durchschnittlich steuerbare VBR-Codierung. In diesem Fall konfiguriert sich der Encoder gemäß dem Wert dieser Eigenschaft und der [**\_ \_ VBR \_ BAVG-Eigenschaft MFPKEY DYN.**](mfpkey-dyn-vbr-bavgproperty.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
