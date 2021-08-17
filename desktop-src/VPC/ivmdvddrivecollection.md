---
title: IVMDVDDriveCollection-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die Sammlung von CD- und DVD-Laufwerken auf dem virtuellen Computer. Verwenden Sie zum Abrufen eines IVMDVDDriveCollection-Objekts die IVMVirtualMachine DVDROMDrives-Eigenschaft.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- IVMDVDDriveCollection-Schnittstelle Virtueller PC
- IVMDVDDriveCollection-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77225134a88ff2c66be3f53f5d3d44c9f8353d8f44077fb0862f0c943c5aec3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056858"
---
# <a name="ivmdvddrivecollection-interface"></a>IVMDVDDriveCollection-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die Sammlung von CD- und DVD-Laufwerken auf dem virtuellen Computer. Um ein **IVMDVDDriveCollection-Objekt** zu erhalten, verwenden Sie die [**IVMVirtualMachine::D VUMADrives-Eigenschaft.**](ivmvirtualmachine-dvdromdrives.md)

## <a name="members"></a>Member

Die **IVMDVDDriveCollection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDVDDriveCollection** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IVMDVDDriveCollection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                       | Zugriffstyp          | Beschreibung                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmdvddrivecollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                   |
| [**Anzahl**](ivmdvddrivecollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der CD- und DVD-Laufwerke in dieser Sammlung.<br/>                 |
| [**Element**](ivmdvddrivecollection-item.md)<br/>          | Schreibgeschützt<br/> | Das CD- oder DVD-Laufwerksobjekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection ist als bc86e297-e55f-4742-9614-ad11d3131f68 definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMVirtualMachine::D VUMADrives**](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

