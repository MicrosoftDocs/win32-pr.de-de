---
title: IVMHardDiskConnectionCollection-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die Auflistung von Festplattenverbindungen innerhalb des virtuellen Computers. Um ein IVMHardDiskConnectionCollection-Objekt abzurufen, verwenden Sie die IVMVirtualMachine HardDiskConnections-Eigenschaft.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- IVMHardDiskConnectionCollection-Schnittstelle Virtueller PC
- IVMHardDiskConnectionCollection-Schnittstelle Virtueller PC , beschrieben
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
ms.openlocfilehash: 997cbe915e7e4addac60c639a7ee6c260f07271ff5981939b25dbefd49fcba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345704"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>IVMHardDiskConnectionCollection-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die Auflistung von Festplattenverbindungen innerhalb des virtuellen Computers. Um ein **IVMHardDiskConnectionCollection-Objekt** abzurufen, verwenden Sie die [**IVMVirtualMachine::HardDiskConnections-Eigenschaft.**](ivmvirtualmachine-harddiskconnections.md)

## <a name="members"></a>Member

Die **IVMHardDiskConnectionCollection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHardDiskConnectionCollection** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IVMHardDiskConnectionCollection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp          | BESCHREIBUNG                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                        |
| [**Anzahl**](ivmharddiskconnectioncollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der Festplattenverbindungen in dieser Sammlung.<br/>                  |
| [**Element**](ivmharddiskconnectioncollection-item.md)<br/>          | Schreibgeschützt<br/> | Das Festplattenverbindungsobjekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                          |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                               |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                      |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection ist als b9f2caf4-0aeb-4085-b105-ceddb90dbf62 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

