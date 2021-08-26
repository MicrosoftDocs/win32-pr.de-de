---
description: Passt den Farbton an.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: MFPKEY_COLOR_HUE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646d9e3ae0e72e11ae8952d28df9e4e3afc4147eaa7983bd1f0e9c82266ca5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954440"
---
# <a name="mfpkey_color_hue-property"></a>MFPKEY \_ COLOR \_ HUE-Eigenschaft

Passt den Farbton an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="applies-to"></a>Gilt für

-   [Farbsteuerelementtransformations-DSP](colorcontroltransform.md)

## <a name="remarks"></a>Hinweise

Die Farbtonanpassung erfolgt durch Mischen der Cb- und Cr-Werte. (Wenn Cb und Cr in einem zweidimensionalen Raum gezeichnet werden, wird die Farbtonanpassung durchgeführt, indem um den Ursprung gedreht wird.)

Diese Eigenschaft hat einen Bereich von -127 bis 127. Null gibt an, dass sich der Farbton nicht ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
