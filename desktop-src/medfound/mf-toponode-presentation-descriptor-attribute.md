---
description: Enthält einen Zeiger auf den Präsentations Deskriptor für die Medienquelle.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: MF_TOPONODE_PRESENTATION_DESCRIPTOR-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753160"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a>MF- \_ toponode- \_ Präsentations \_ deskriptorattribut

Enthält einen Zeiger auf den Präsentations Deskriptor für die Medienquelle.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Quellknoten (_ * MF- \_ Topologie \_ sourcestream- \_ Knoten * *).

Der Wert des-Attributs ist ein Zeiger auf die [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle des Präsentations Deskriptors. Dieses Attribut ist erforderlich.

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

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 




