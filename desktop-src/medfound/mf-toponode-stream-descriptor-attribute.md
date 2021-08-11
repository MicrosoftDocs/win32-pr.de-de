---
description: Enthält einen Zeiger auf den Streamdeskriptor für die Medienquelle.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: MF_TOPONODE_STREAM_DESCRIPTOR-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92517560f0a1f60681afc1209d6d14d3e3c5d663958d365d18b20558c0003199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244324"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a>MF \_ TOPONODE \_ STREAM \_ DESCRIPTOR-Attribut

Enthält einen Zeiger auf den Streamdeskriptor für die Medienquelle.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Quellknoten (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**).

Der Wert des Attributs ist ein Zeiger auf die [**POINTERStreamDescriptor-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) des Streamdeskriptors. Dieses Attribut ist erforderlich.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




