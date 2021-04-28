---
description: 'MFPKEY_COLORCONV_MODE-Eigenschaft: Gibt an, ob der Eingabestream übersprungen wird.'
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087578"
---
# <a name="mfpkey_colorconv_mode-property"></a>MFPKEY \_ COLORCONV \_ MODE-Eigenschaft

Gibt an, ob der Eingabestream übersprungen wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mithilfe von [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Wird vom DSP aus dem Quellvideo berechnet.

## <a name="applies-to"></a>Gilt für

-   [Farbkonverter-DSP](colorconverter.md)

## <a name="remarks"></a>Bemerkungen

Verwenden Sie einen der folgenden Werte.



| Wert | BESCHREIBUNG |
|-------|-------------|
| 0     | progressiv |
| 2     | Interlaced  |



 

Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabemedientyp, um zu bestimmen, ob das Video übersprungen wird. Sie können diese Eigenschaft festlegen, um die Medientypeinstellung zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
