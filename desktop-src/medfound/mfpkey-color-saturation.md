---
description: Passt die Sättigung an.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: MFPKEY_COLOR_SATURATION-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528685"
---
# <a name="mfpkey_color_saturation-property"></a>Eigenschaft für mfpkey- \_ Farb \_ Sättigung

Passt die Sättigung an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="applies-to"></a>Gilt für

-   [Farb Steuerungs Transformation (DSP)](colorcontroltransform.md)

## <a name="remarks"></a>Bemerkungen

Die Sättigungs Anpassung wird durch die Multiplikation der Werte CB und CR durch eine Konstante durchgeführt.

Diese Eigenschaft hat einen Bereich von-127 bis 127. NULL gibt an, dass die Sättigung nicht geändert werden soll.

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

 

 
