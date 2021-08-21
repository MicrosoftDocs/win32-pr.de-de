---
title: IMsRdpDrive-Schnittstelle
description: Enthält Informationen zu einem Laufwerkobjekt.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- IMsRdpDrive-Remotedesktopdienste
- IMsRdpDrive-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efccf0459375e23375b3ac40067bcbd3965ed7f6c0b51ddb60f6362fb419688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000730"
---
# <a name="imsrdpdrive-interface"></a>IMsRdpDrive-Schnittstelle

Enthält Informationen zu einem Laufwerkobjekt.

## <a name="members"></a>Member

Die **IMsRdpDrive-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDrive** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpDrive-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Name**](imsrdpdrive-name.md)<br/>                         | Schreibgeschützt<br/>  | Ruft den Namen des Laufwerks ab.<br/>              |
| [**RedirectionState**](imsrdpdrive-redirectionstate.md)<br/> | Lesen/Schreiben<br/> | Gibt den Umleitungsstatus des Laufwerks an.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive ist als d28b5458-f694-47a8-8e61-40356a767e46 definiert.<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

