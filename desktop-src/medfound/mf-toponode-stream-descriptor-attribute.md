---
description: Enthält einen Zeiger auf den Datenstrom Deskriptor für die Medienquelle.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: MF_TOPONODE_STREAM_DESCRIPTOR-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368148"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a>Das MF- \_ toponode- \_ \_ streamdeskriptorattribut

Enthält einen Zeiger auf den Datenstrom Deskriptor für die Medienquelle.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Quellknoten (_ * MF- \_ Topologie \_ sourcestream- \_ Knoten * *).

Der Wert des-Attributs ist ein Zeiger auf die [**imfstreamdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) -Schnittstelle des Stream-Deskriptors. Dieses Attribut ist erforderlich.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**Imfattributes:: *-Known**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




