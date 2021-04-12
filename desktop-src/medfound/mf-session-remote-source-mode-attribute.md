---
description: Gibt an, dass die Medienquelle in einem Remote Prozess erstellt wird.
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: MF_SESSION_REMOTE_SOURCE_MODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217025"
---
# <a name="mf_session_remote_source_mode-attribute"></a>\_ \_ Remote \_ Quell Modus- \_ Attribut der MF-Sitzung

Gibt an, dass die Medienquelle in einem Remote Prozess erstellt wird.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut für die PMP-Sitzung (Protected Media Path) mithilfe des Parameters *pconfiguration* der Funktion [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) festlegen.

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

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Medien Sitzungs Attribute](media-session-attributes.md)
</dt> <dt>

[PMP-Medien Sitzung](pmp-media-session.md)
</dt> </dl>

 

 




