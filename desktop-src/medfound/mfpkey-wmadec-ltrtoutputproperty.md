---
description: Gibt an, ob der Decoder einen Lt-Rt ausführen soll.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76d086fd0f57262d249784fcabc5a98e8a18668cf0697618f3fbbe5528a2cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713810"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>MFPKEY \_ WKYC \_ LTRTOUTPUT-Eigenschaft

Gibt an, ob der Decoder einen Lt-Rt ausführen soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ BOOL**

## <a name="default-value"></a>Standardwert

**VARIANT \_ FALSE**

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft über den Wert VARIANT FALSE verfügt und die Ausgabe Stereo ist, verwendet der Audiodecoder ein \_ einfaches Kanalfalten. Wenn diese Eigenschaft über den Wert VARIANT TRUE verfügt, führt der Audiodecoder Lt-Rt (matrixed) fold down to stereo aus, und dann kann jeder Dolby Surround-Decoder verwendet werden, um die matrixierte Umschließung zu \_ decodieren. Beispielsweise kann der Audiodecoder eine Lt-Rt 5.1- oder 7.1-Inhalt ausführen.

Diese Eigenschaft wird nur unterstützt, wenn der Decoder als DirectX Media Object (DMO. Es wird kein Fold-Down unterstützt, wenn der Decoder als MFT (Media Foundation Transform) agiert.

Wenn Windows Vista eine **IPropertyStore-Schnittstelle** für einen Audiodecoder abrufen, fungiert der Decoder als MFT. Daher kann diese Eigenschaft nicht auf Windows Vista verwendet werden. Informationen dazu, wann ein Decoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codec-Referenzseiten unter [Codec-Objekte.](codecobjects.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
