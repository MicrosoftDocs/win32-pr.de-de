---
description: Enthält einen Zeiger auf den Präsentationsdeskriptor für die Medienquelle.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: MF_TOPONODE_PRESENTATION_DESCRIPTOR-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bfa43a57bcead1312ba8138ab085771d29a008fe2558ea7c6bfb29121d631bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113706"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a>MF \_ TOPONODE \_ PRESENTATION \_ DESCRIPTOR-Attribut

Enthält einen Zeiger auf den Präsentationsdeskriptor für die Medienquelle.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Quellknoten (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**).

Der Wert des Attributs ist ein Zeiger auf die [**INTERFACESPresentationDescriptor-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) des Präsentationsdeskriptors. Dieses Attribut ist erforderlich.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 




