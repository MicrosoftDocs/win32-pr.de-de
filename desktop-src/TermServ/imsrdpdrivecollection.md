---
title: IMsRdpDriveCollection-Schnittstelle
description: Stellt eine Auflistung von Laufwerksobjekten dar.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- IMsRdpDriveCollection-Schnittstelle Remotedesktopdienste
- IMsRdpDriveCollection-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9f85a491da97fe0093d9b02e8ceda59c3562f237d8678323078e2613250f28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125630"
---
# <a name="imsrdpdrivecollection-interface"></a>IMsRdpDriveCollection-Schnittstelle

Stellt eine Auflistung von Laufwerksobjekten dar.

## <a name="members"></a>Member

Die **IMsRdpDriveCollection-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDriveCollection** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpDriveCollection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                     | Beschreibung                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDrives**](imsrdpdrivecollection-rescandrives.md) | Aktualisiert die Liste der Objekte in der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IMsRdpDriveCollection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp          | Beschreibung                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [**DriveByIndex**](imsrdpdrivecollection-drivebyindex.md)<br/> | Schreibgeschützt<br/> | Ruft das Laufwerk am angegebenen Index ab.<br/>       |
| [**DriveCount**](imsrdpdrivecollection-drivecount.md)<br/>     | Schreibgeschützt<br/> | Ruft die Anzahl der Objekte in der Auflistung ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

