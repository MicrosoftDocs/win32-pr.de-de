---
description: Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: MFPKEY_DYN_VBR_RAVG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959420"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>Eigenschaft "mfpkey \_ dyn \_ VBR \_ Ravg"

Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ I4**

## <a name="remarks"></a>Bemerkungen

Wenn die Eigenschaften [**mfpkey, \_ avgeingeschränkter**](mfpkey-avgconstrainedproperty.md) und [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) beide auf **Variant \_ true** festgelegt sind, verwendet der Encoder die durchschnittliche steuerbare VBR-Codierung. In diesem Fall wird der Encoder gemäß dem Wert dieser Eigenschaft und der Eigenschaft [**mfpkey \_ dyn \_ VBR \_ bavg**](mfpkey-dyn-vbr-bavgproperty.md) konfiguriert.

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

 

 
