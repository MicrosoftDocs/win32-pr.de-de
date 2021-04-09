---
description: Gibt an, ob der Decoder Lt-Rt-Fold ausführen soll.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130541"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>Mfpkey \_ wmadec \_ ltrtoutput (Eigenschaft)

Gibt an, ob der Decoder Lt-Rt-Fold ausführen soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ false**

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft den Wert Variant false aufweist \_ und die Ausgabe Stereo ist, verwendet der Audiodecoder die einfache kanaldown-Eigenschaft. Wenn für diese Eigenschaft der Wert Variant \_ true festgelegt ist, führt der Audiodecoder Lt-Rt (matrixt) Fold (matrixt) in Stereo aus, und anschließend kann ein beliebiger Dolby Surround-Decoder zum Decodieren der matriten umschließenden verwendet werden. Der Audiodecoder könnte z. b. Lt-Rt für den Inhalt von 5,1 oder 7,1 ausführen.

Diese Eigenschaft wird nur unterstützt, wenn der Decoder als DirectX-Medienobjekt (DMO) fungiert. Wenn der Decoder als Media Foundation Transformation (MFT) fungiert, wird kein Fold unterstützt.

Wenn Sie unter Windows Vista eine **IPropertyStore** -Schnittstelle für einen Audiodecoder erhalten, fungiert der Decoder als MFT. Folglich kann diese Eigenschaft nicht unter Windows Vista verwendet werden. Informationen darüber, wann ein Decoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codec-Referenzseiten unter [Codec-Objekte](codecobjects.md).

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

 

 
