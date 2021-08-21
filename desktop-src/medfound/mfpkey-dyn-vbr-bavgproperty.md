---
description: Gibt das Pufferfenster für einen Encoder in Millisekunden an, der für die Verwendung der durchschnittlich steuerbaren VBR-Codierung konfiguriert ist.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: MFPKEY_DYN_VBR_BAVG-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77ba4d3f3d7a5587a7c8aa90771f58accd8a80864dd5a875c6c580eb9e29e01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738160"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>MFPKEY \_ DYN \_ VBR \_ BAVG-Eigenschaft

Gibt das Pufferfenster für einen Encoder in Millisekunden an, der für die Verwendung der durchschnittlich steuerbaren VBR-Codierung konfiguriert ist.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mithilfe von [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ I4**

## <a name="remarks"></a>Hinweise

Wenn die [**Eigenschaften MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) und [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) beide auf **VARIANT \_ TRUE** festgelegt sind, verwendet der Encoder die durchschnittlich steuerbare VBR-Codierung. In diesem Fall konfiguriert sich der Encoder gemäß dem Wert dieser Eigenschaft und der [**\_ \_ VBR \_ RAVG-Eigenschaft MFPKEY DYN.**](mfpkey-dyn-vbr-ravgproperty.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
