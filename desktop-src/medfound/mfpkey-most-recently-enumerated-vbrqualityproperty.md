---
description: Gibt die VBR-Qualitätsstufe des zuletzt aufzählten Ausgabetyps an.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68e609f8dc7b95eb9cfd4bf537af47d1a11cb4ba625f0bbc65897b008ff03a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689794"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>VBRQUALITY-Eigenschaft für MFPKEY \_ \_ ZULETZT \_ \_ AUFZÄHLEN

Gibt die VBR-Qualitätsstufe des zuletzt aufzählten Ausgabetyps an. Schreibgeschützt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="remarks"></a>Hinweise

Wenn der Encoder als Media Foundation Transform (MFT) agiert und einen Ausgabetyp bei einem Aufruf von VBRQUALITY vom Typ **\_ \_ \_ \_ "VBRQUALITY" (ZULETZT ENUMERATED)** aufzählt, können Sie den MFT abfragen. [](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) Der zurückgegebene Wert gibt die VBR-Qualität des zuletzt zurückgegebenen Ausgabemedientyps an. Anschließend können Sie mit diesem Wert die [**MFPKEY \_ DESIRED \_ VBRQUALITY-Eigenschaft**](mfpkey-desired-vbrqualityproperty.md) des Encoders festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
