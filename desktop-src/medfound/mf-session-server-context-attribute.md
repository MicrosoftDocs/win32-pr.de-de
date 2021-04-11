---
description: Ermöglicht zwei Instanzen der Medien Sitzung, den gleichen PMP-Prozess (Protected Media Path) gemeinsam zu nutzen.
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: MF_SESSION_SERVER_CONTEXT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131957"
---
# <a name="mf_session_server_context-attribute"></a>Kontext Attribut des MF- \_ Sitzungs \_ Servers \_

Ermöglicht zwei Instanzen der Medien Sitzung, den gleichen PMP-Prozess (Protected Media Path) gemeinsam zu nutzen.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Attribut, wenn Sie die PMP-Medien Sitzung in einem vorhandenen PMP-Prozess erstellen möchten. Der Wert des-Attributs ist ein Zeiger auf die [_ *imfpmpserver* *](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) -Schnittstelle.

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
</dt> </dl>

 

 




