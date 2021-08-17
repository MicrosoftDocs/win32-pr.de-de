---
description: 'MFPKEY_RESIZE_INTERLACE-Eigenschaft: Gibt an, ob der Eingabestream interlaced ist.'
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c614865d0c8a49238b9c8d6f7714787bb22aaadaa317a8a3a0405a7f51c87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873034"
---
# <a name="mfpkey_resize_interlace-property"></a>MFPKEY \_ RESIZE \_ INTERLACE-Eigenschaft

Gibt an, ob der Eingabestream als Interlacing verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="applies-to"></a>Gilt für

-   [Video Resizer DSP](videoresizer.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie einen der folgenden Werte:



| Wert     | Beschreibung |
|-----------|-------------|
| VT \_ FALSE | progressiv |
| VT \_ TRUE  | Interlaced  |



 

Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabemedientyp, um zu bestimmen, ob das Video interlaced ist. Sie können diese Eigenschaft festlegen, um die Medientypeinstellung zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
