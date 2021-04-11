---
description: Enthält einen Zeiger auf den Präsentations Deskriptor aus dem geschützten Medien Pfad (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: MF_PD_APP_CONTEXT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217541"
---
# <a name="mf_pd_app_context-attribute"></a>MF- \_ PD- \_ App- \_ Kontext Attribut

Enthält einen Zeiger auf den Präsentations Deskriptor aus dem geschützten Medien Pfad (PMP).

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Der Medienquellen Proxy, der im PMP-Prozess erstellt wird, verwendet dieses Attribut, um den Remote Präsentations Deskriptor im Präsentations Deskriptor der Anwendung zu speichern.

Der Wert dieses Attributs ist ein Zeiger auf die [_ *imfpresentationdescriptor* *](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle.

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

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




