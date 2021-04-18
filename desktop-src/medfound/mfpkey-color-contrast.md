---
description: Passt den Kontrast an.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: MFPKEY_COLOR_CONTRAST-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368254"
---
# <a name="mfpkey_color_contrast-property"></a>Eigenschaft für den mfpkey- \_ Farb \_ Kontrast

Passt den Kontrast an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="applies-to"></a>Gilt für

-   [Farb Steuerungs Transformation (DSP)](colorcontroltransform.md)

## <a name="remarks"></a>Bemerkungen

Die Kontrast Anpassung erfolgt durch Multiplikation der YCbCr-Werte mit einem Skalierungsfaktor.

Diese Eigenschaft hat einen Bereich von-127 bis 127. NULL gibt an, dass keine Änderung im Gegensatz dazu besteht.

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

 

 
