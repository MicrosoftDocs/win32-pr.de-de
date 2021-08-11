---
description: 'MFPKEY_COLORCONV_MODE-Eigenschaft: Gibt an, ob der Eingabestream übersprungen wird.'
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86ed10873c1587aefba342392afa7f84f8c635788339d64deca18b76629255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242889"
---
# <a name="mfpkey_colorconv_mode-property"></a>MFPKEY \_ COLORCONV \_ MODE-Eigenschaft

Gibt an, ob der Eingabestream übersprungen wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Wird vom DSP aus dem Quellvideo berechnet.

## <a name="applies-to"></a>Gilt für

-   [Farbkonverter-DSP](colorconverter.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie einen der folgenden Werte.



| Wert | BESCHREIBUNG |
|-------|-------------|
| 0     | progressiv |
| 2     | Interlaced  |



 

Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabemedientyp, um zu bestimmen, ob das Video übersprungen wird. Sie können diese Eigenschaft festlegen, um die Medientypeinstellung zu überschreiben.

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

 

 
