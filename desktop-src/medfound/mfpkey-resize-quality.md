---
description: Gibt an, ob ein Algorithmus verwendet werden soll, der ein Video mit höherer Qualität oder einen schnelleren Algorithmus erzeugt.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360194"
---
# <a name="mfpkey_resize_quality-property"></a>Eigenschaft "mfpkey \_ Resize \_ Quality"

Gibt an, ob ein Algorithmus verwendet werden soll, der ein Video mit höherer Qualität oder einen schnelleren Algorithmus erzeugt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="applies-to"></a>Gilt für

-   [Video Resizer DSP](videoresizer.md)

## <a name="remarks"></a>Bemerkungen

Verwenden Sie einen der folgenden Werte:



| Wert     | BESCHREIBUNG          |
|-----------|----------------------|
| VT \_ false | Schnellerer Algorithmus     |
| VT \_ true  | Video mit höherer Qualität |



 

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

 

 
