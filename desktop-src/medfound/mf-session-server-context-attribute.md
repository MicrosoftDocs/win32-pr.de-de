---
description: Ermöglicht zwei Instanzen der Mediensitzung, denselben PMP-Prozess (Protected Media Path) gemeinsam zu verwenden.
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: MF_SESSION_SERVER_CONTEXT-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc9674a2e25a7cdfd0a88ebcc43c18d6fd636bf22116f76a24255b55f857a677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102336"
---
# <a name="mf_session_server_context-attribute"></a>MF \_ SESSION \_ SERVER \_ CONTEXT-Attribut

Ermöglicht zwei Instanzen der Mediensitzung, denselben PMP-Prozess (Protected Media Path) gemeinsam zu verwenden.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Attribut, wenn Sie die PMP-Mediensitzung in einem vorhandenen PMP-Prozess erstellen möchten. Der Wert des Attributs ist ein Zeiger auf die [**IMFPMPServer-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)

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

[Mediensitzungsattribute](media-session-attributes.md)
</dt> </dl>

 

 




