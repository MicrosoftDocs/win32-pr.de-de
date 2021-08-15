---
title: IVMFloppyDriveCollection-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert eine Auflistung von Diskettenlaufwerken innerhalb des virtuellen Computers.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- IVMFloppyDriveCollection-Schnittstelle Virtueller PC
- IVMFloppyDriveCollection-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6637c0c4a8c8b87f4458081b0893b0939c8eaf04c97738c02d39da5e0fd8eebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653590"
---
# <a name="ivmfloppydrivecollection-interface"></a>IVMFloppyDriveCollection-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert eine Auflistung von Diskettenlaufwerken innerhalb des virtuellen Computers. Um ein **IVMFloppyDriveCollection-Objekt** abzurufen, verwenden Sie die [**IVMVirtualMachine::FloppyDrives-Eigenschaft.**](ivmvirtualmachine-floppydrives.md)

## <a name="members"></a>Member

Die **IVMFloppyDriveCollection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFloppyDriveCollection** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IVMFloppyDriveCollection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                          | Zugriffstyp          | BESCHREIBUNG                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                |
| [**Anzahl**](ivmfloppydrivecollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der Diskettenlaufwerke in dieser Auflistung.<br/>                  |
| [**Element**](ivmfloppydrivecollection-item.md)<br/>          | Schreibgeschützt<br/> | Das Diskettenlaufwerkobjekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection ist als 8ba70a25-f698-4ee5-85ce-3cc93a925516 definiert.<br/>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> <dt>

[**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

