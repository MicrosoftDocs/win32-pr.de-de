---
description: Stellt eine Rückruf Schnittstelle bereit, damit die Anwendung ein Content Wegbereiter-Objekt von der PMP-Sitzung (Protected Media Path) empfängt.
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: MF_SESSION_CONTENT_PROTECTION_MANAGER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347493"
---
# <a name="mf_session_content_protection_manager-attribute"></a>MF- \_ Sitzungs \_ Inhalts Schutz-Manager- \_ \_ Attribut

Stellt eine Rückruf Schnittstelle bereit, damit die Anwendung ein Content Wegbereiter-Objekt von der PMP-Sitzung (Protected Media Path) empfängt.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die [_ *imfcontentschutzmanager* *](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle der Anwendung.

Legen Sie dieses Attribut für die PMP-Sitzung fest, indem Sie den *pconfiguration* -Parameter der [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) -Funktion verwenden.

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

[Medien Sitzungs Attribute](media-session-attributes.md)
</dt> <dt>

[Wiedergeben geschützter Mediendateien](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




