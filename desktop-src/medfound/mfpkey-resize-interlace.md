---
description: Gibt an, ob der Eingabedaten Strom mit Zeilen Sprung verknüpft ist.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356903"
---
# <a name="mfpkey_resize_interlace-property"></a>Mfpkey \_ Resize \_ Interlace-Eigenschaft

Gibt an, ob der Eingabedaten Strom mit Zeilen Sprung verknüpft ist.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="applies-to"></a>Gilt für

-   [Video Resizer DSP](videoresizer.md)

## <a name="remarks"></a>Bemerkungen

Verwenden Sie einen der folgenden Werte:



| Wert     | BESCHREIBUNG |
|-----------|-------------|
| VT \_ false | progressiv |
| VT \_ true  | Interlaced  |



 

Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabe Medientyp, um zu bestimmen, ob das Video mit Zeilen Sprung verknüpft ist. Sie können diese Eigenschaft festlegen, um die Medientyp Einstellung außer Kraft zu setzen.

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

 

 
