---
title: IVMHardDiskConnection-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die Verbindung für eine Festplatte innerhalb des virtuellen Computers.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- IVMHardDiskConnection-Schnittstelle Virtueller PC
- IVMHardDiskConnection-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8522a6f8c24f2f80728a878435b42ac4179432e1cca4234feb29261fe2c11f8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510790"
---
# <a name="ivmharddiskconnection-interface"></a>IVMHardDiskConnection-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die Verbindung für eine Festplatte innerhalb des virtuellen Computers. Ein **IVMHardDiskConnection-Objekt** wird von der [**IVMVirtualMachine::AddHardDiskConnection-Methode**](ivmvirtualmachine-addharddiskconnection.md) zurückgegeben. Sie können auch ein **IVMHardDiskConnection-Objekt** aus dem [**IVMHardDiskConnectionCollection-Objekt**](ivmharddiskconnectioncollection.md) abrufen, das von der [**IVMVirtualMachine::HardDiskConnections-Eigenschaft zurückgegeben**](ivmvirtualmachine-harddiskconnections.md) wird.

## <a name="members"></a>Member

Die **IVMHardDiskConnection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHardDiskConnection** verfügt auch über diese Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMHardDiskConnection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                         | Beschreibung                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [**SetBusLocation**](ivmharddiskconnection-setbuslocation.md) | Legt den Busstandort fest, an den diese Festplatte angefügt ist.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IVMHardDiskConnection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp          | Beschreibung                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [**BusNumber**](ivmharddiskconnection-busnumber.md)<br/>       | Schreibgeschützt<br/> | Die Busnummer, an die das Laufwerkimage angefügt ist.<br/>                   |
| [**DeviceNumber**](ivmharddiskconnection-devicenumber.md)<br/> | Schreibgeschützt<br/> | Die Gerätenummer, an die das Laufwerkimage angefügt ist.<br/>                |
| [**Festplatte**](ivmharddiskconnection-harddisk.md)<br/>         | Schreibgeschützt<br/> | Ein Festplattenobjekt, das dieser Verbindung entspricht.<br/>                   |
| [**UndoHardDisk**](ivmharddiskconnection-undoharddisk.md)<br/> | Schreibgeschützt<br/> | Ein Festplattenobjekt, das dem Rückgängig-Datenträgerimage dieser Verbindung entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection ist als aefa36a5-463a-46ae-9e6c-a1fb4e12e671 definiert.<br/>      |



 

