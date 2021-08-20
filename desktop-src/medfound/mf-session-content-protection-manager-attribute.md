---
description: Stellt eine Rückrufschnittstelle bereit, über die die Anwendung ein Inhalts-Enabler-Objekt aus der PMP-Sitzung (Protected Media Path) empfangen kann.
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: MF_SESSION_CONTENT_PROTECTION_MANAGER -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 753bd3e78be4d4996477cb597170c7a3396ae819766d3f4af9ac867055dd2dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691590"
---
# <a name="mf_session_content_protection_manager-attribute"></a>MF \_ SESSION CONTENT PROTECTION \_ \_ \_ MANAGER-Attribut

Stellt eine Rückrufschnittstelle bereit, über die die Anwendung ein Inhalts-Enabler-Objekt aus der PMP-Sitzung (Protected Media Path) empfangen kann.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Zeiger auf die [**BENUTZEROBERFLÄCHECONTENTProtectionManager-Schnittstelle der**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) Anwendung.

Legen Sie dieses Attribut in der PMP-Sitzung mithilfe des *pConfiguration-Parameters* der [**MFCreatePMPMediaSession-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) fest.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEs::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Media Session Attributes](media-session-attributes.md)
</dt> <dt>

[Wiederspielen geschützter Mediendateien](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




