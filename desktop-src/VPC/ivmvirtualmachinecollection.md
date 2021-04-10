---
title: Ivmvirtualmachinecollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung virtueller Computer innerhalb von Windows Virtual PC. Verwenden Sie zum Abrufen eines ivmvirtualmachinecollection-Objekts die ivmvirtualpc-Eigenschaft VirtualMachines.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Ivmvirtualmachinecollection Interface Virtual PC
- Ivmvirtualmachinecollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105645"
---
# <a name="ivmvirtualmachinecollection-interface"></a>Ivmvirtualmachinecollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Sammlung virtueller Computer innerhalb von Windows Virtual PC. Verwenden Sie zum Abrufen eines **ivmvirtualmachinecollection** -Objekts die [**ivmvirtualpc:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmvirtualmachinecollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmvirtualmachinecollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmvirtualmachinecollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp          | BESCHREIBUNG                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmvirtualmachinecollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                   |
| [**Countdown**](ivmvirtualmachinecollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der virtuellen Computer in dieser Sammlung.<br/>                  |
| [**Element**](ivmvirtualmachinecollection-item.md)<br/>          | Schreibgeschützt<br/> | Das virtuelle Maschinen Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ ivmvirtualmachinecollection ist als 59F 31786-2a3d-4sbf-9896-d85338ca0da1 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> <dt>

[**Ivmvirtualpc:: VirtualMachines**](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

