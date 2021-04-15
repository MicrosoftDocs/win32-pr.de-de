---
title: Imsrdpdrivecollection-Schnittstelle
description: Stellt eine Auflistung von Laufwerk Objekten dar.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Imsrdpdrivecollection-Schnittstelle Remotedesktopdienste
- Imsrdpdrivecollection-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477736"
---
# <a name="imsrdpdrivecollection-interface"></a>Imsrdpdrivecollection-Schnittstelle

Stellt eine Auflistung von Laufwerk Objekten dar.

## <a name="members"></a>Member

Die **imsrdpdrivecollection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imsrdpdrivecollection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **imsrdpdrivecollection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [**Neu eingängig**](imsrdpdrivecollection-rescandrives.md) | Aktualisiert die Liste der-Objekte in der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **imsrdpdrivecollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp          | BESCHREIBUNG                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [**Drivebyindex**](imsrdpdrivecollection-drivebyindex.md)<br/> | Schreibgeschützt<br/> | Ruft das Laufwerk am angegebenen Index ab.<br/>       |
| [**Drivecount**](imsrdpdrivecollection-drivecount.md)<br/>     | Schreibgeschützt<br/> | Ruft die Anzahl der-Objekte in der-Auflistung ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ imsrdpdrivecollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**Imsrdpdrive**](imsrdpdrive.md)
</dt> </dl>

 

