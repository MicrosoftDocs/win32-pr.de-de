---
description: 'MFPKEY_RESIZE_INTERLACE-Eigenschaft: Gibt an, ob der Eingabestream interlaced ist.'
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092878"
---
# <a name="mfpkey_resize_interlace-property"></a>MFPKEY \_ RESIZE \_ INTERLACE-Eigenschaft

Gibt an, ob der Eingabestream als Interlacing verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="applies-to"></a>Gilt für

-   [Video Resizer DSP](videoresizer.md)

## <a name="remarks"></a>Bemerkungen

Verwenden Sie einen der folgenden Werte:



| Wert     | BESCHREIBUNG |
|-----------|-------------|
| VT \_ FALSE | progressiv |
| VT \_ TRUE  | Interlaced  |



 

Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabemedientyp, um zu bestimmen, ob das Video interlaced ist. Sie können diese Eigenschaft festlegen, um die Medientypeinstellung zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
