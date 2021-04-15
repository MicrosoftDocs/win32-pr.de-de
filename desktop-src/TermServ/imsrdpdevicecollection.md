---
title: Imsrdpdebug-Schnittstelle
description: Stellt eine Auflistung von Geräte Objekten dar.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Imsrdpentvicecollection-Schnittstelle Remotedesktopdienste
- Imsrdpdebug-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391524"
---
# <a name="imsrdpdevicecollection-interface"></a>Imsrdpdebug-Schnittstelle

Stellt eine Auflistung von Geräte Objekten dar.

## <a name="members"></a>Member

Die **imsrdpdebug** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imsrdptovicecollection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **imsrdpdevicecollection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**Redevices**](imsrdpdevicecollection-rescandevices.md) | Aktualisiert die Liste der-Objekte in der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **imsrdpentvicecollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp          | BESCHREIBUNG                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [**Devicebyid**](imsrdpdevicecollection-devicebyid.md)<br/>       | Schreibgeschützt<br/> | Ruft das Gerät mit dem angegebenen Bezeichner ab.<br/> |
| [**Devicebyindex**](imsrdpdevicecollection-devicebyindex.md)<br/> | Schreibgeschützt<br/> | Ruft das Gerät am angegebenen Index ab.<br/>        |
| [**DeviceCount**](imsrdpdevicecollection-devicecount.md)<br/>     | Schreibgeschützt<br/> | Ruft die Anzahl der-Objekte in der-Auflistung ab.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ imsrdpendvicecollection ist als 56540617-d281-488c-8738-6a8sdf64a118 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**Imsrdpdevice**](imsrdpdevice.md)
</dt> </dl>

 

