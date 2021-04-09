---
description: Passt die Helligkeit an.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: MFPKEY_COLOR_BRIGHTNESS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864775"
---
# <a name="mfpkey_color_brightness-property"></a>Eigenschaft "mfpkey \_ Color \_ Helligkeit"

Passt die Helligkeit an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="applies-to"></a>Gilt für

-   [Farb Steuerungs Transformation (DSP)](colorcontroltransform.md)

## <a name="remarks"></a>Bemerkungen

Die Helligkeitsanpassung wird durch Hinzufügen eines Werts zum Luma-Kanal durchgeführt.

Diese Eigenschaft hat einen Bereich von-127 bis 127. NULL gibt an, dass die Helligkeit nicht geändert werden soll.

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

 

 
