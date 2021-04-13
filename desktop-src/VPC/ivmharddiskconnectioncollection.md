---
title: Ivmharddiskconnectioncollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung von Festplatten Verbindungen innerhalb des virtuellen Computers. Verwenden Sie zum Abrufen eines ivmharddiskconnectioncollection-Objekts die ivmvirtualmachine harddiskconnections-Eigenschaft.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Ivmharddiskconnectioncollection-Schnittstelle virtueller PC
- Ivmharddiskconnectioncollection-Schnittstelle virtueller PC, beschrieben
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475033"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>Ivmharddiskconnectioncollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Sammlung von Festplatten Verbindungen innerhalb des virtuellen Computers. Verwenden Sie zum Abrufen eines **ivmharddiskconnectioncollection** -Objekts die [**ivmvirtualmachine:: harddiskconnections**](ivmvirtualmachine-harddiskconnections.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmharddiskconnectioncollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmharddiskconnectioncollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmharddiskconnectioncollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp          | BESCHREIBUNG                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmharddiskconnectioncollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                        |
| [**Countdown**](ivmharddiskconnectioncollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der Festplatten Verbindungen in dieser Sammlung.<br/>                  |
| [**Element**](ivmharddiskconnectioncollection-item.md)<br/>          | Schreibgeschützt<br/> | Das Festplatten Verbindungs Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                          |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                               |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                      |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ ivmharddiskconnectioncollection ist definiert als b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmharddiskconnection**](ivmharddiskconnection.md)
</dt> <dt>

[**Ivmvirtualmachine:: harddiskconnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

