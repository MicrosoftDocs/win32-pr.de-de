---
description: Gibt die VBR-Qualitätsstufe des zuletzt aufgezählten Ausgabe Typs an.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352122"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>\_ \_ Aktuell \_ aufgelistete \_ vbrquality-Eigenschaft für mfpkey

Gibt die VBR-Qualitätsstufe des zuletzt aufgezählten Ausgabe Typs an. Schreibgeschützt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="remarks"></a>Bemerkungen

Wenn der Encoder als Media Foundation Transformation (MFT) fungiert und einen Ausgabetyp für einen [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)-Befehl auflistet, können Sie die MFT für die zuletzt **\_ \_ \_ aufgezählte \_ vbrquality-Eigenschaft von mfpkey** Abfragen. Der zurückgegebene Wert gibt die VBR-Qualität des zuletzt zurückgegebenen Ausgabemedien Typs an. Anschließend können Sie diesen Wert verwenden, um die [**\_ gewünschte \_ Eigenschaft "mfpkey**](mfpkey-desired-vbrqualityproperty.md) " des Encoders festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**mfpkey \_ schränkt die \_ Enumeration von \_ vbrquality ein**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
