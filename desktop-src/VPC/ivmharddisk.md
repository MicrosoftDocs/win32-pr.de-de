---
title: IVMHardDisk-Schnittstelle (VPCCOMInterfaces.h)
description: Ermöglicht den Zugriff auf ein Festplattenimage. Der Zugriff darauf ist über die HardDisk-Eigenschaft IVMHardDiskConnection oder die GETHardDisk-Methode IVMVirtualPC möglich.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- IVMHardDisk-Schnittstelle Virtueller PC
- IVMHardDisk-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525762f66798b95562958fb204119beda1d76a8b94a60a11a7171b0d0b2951e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768160"
---
# <a name="ivmharddisk-interface"></a>IVMHardDisk-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ermöglicht den Zugriff auf ein Festplattenimage. Der Zugriff darauf ist über die [**IVMHardDiskConnection::HardDisk-Eigenschaft**](ivmharddiskconnection-harddisk.md) oder die [**IVMVirtualPC::GetHardDisk-Methode**](ivmvirtualpc-getharddisk.md) möglich.

## <a name="members"></a>Member

Die **IVMHardDisk-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHardDisk** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMHardDisk-Schnittstelle** verfügt über diese Methoden.



| Methode                                 | Beschreibung                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kompakte**](ivmharddisk-compact.md) | Komprimiert ein dynamisch erweiterbares virtuelles Festplattenimage.<br/>                                                                                        |
| [**Convert**](ivmharddisk-convert.md) | Konvertiert jede virtuelle Festplatte entweder in eine dynamisch erweiterbare virtuelle Festplatte oder in eine virtuelle Festplatte mit fester Größe.<br/>                            |
| [**Zusammenführen**](ivmharddisk-merge.md)     | Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträgerimage zusammen.<br/>                                                                              |
| [**MergeTo**](ivmharddisk-mergeto.md) | Führt eine differenzierende virtuelle Festplatte mit allen übergeordneten Datenträgern (bis einschließlich der übergeordneten Stammfestplatte) mit einer neuen Festplattendatei zusammen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IVMHardDisk-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp           | Beschreibung                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Datei**](ivmharddisk-file.md)<br/>                           | Schreibgeschützt<br/>  | Der vollständige Pfadname der virtuellen Festplattendatei.<br/>                                   |
| [**HostFreeDiskSpace**](ivmharddisk-hostfreediskspace.md)<br/> | Schreibgeschützt<br/>  | Die Menge des verbleibenden Speicherplatzes, der auf dem Host für die virtuelle Festplatte verfügbar ist.<br/> |
| [**Parent**](ivmharddisk-parent.md)<br/>                       | Lesen/Schreiben<br/> | Das übergeordnete Element der differenzierenden virtuellen Festplatte.<br/>                                   |
| [**SizeInGuest**](ivmharddisk-sizeinguest.md)<br/>             | Schreibgeschützt<br/>  | Die Größe der virtuellen Festplatte im Gastbetriebssystem.<br/>                    |
| [**SizeOnHost**](ivmharddisk-sizeonhost.md)<br/>               | Schreibgeschützt<br/>  | Die Größe der virtuellen Festplattendatei auf dem Hostcomputer.<br/>                        |
| [**type**](ivmharddisk-type.md)<br/>                           | Schreibgeschützt<br/>  | Der Typ der virtuellen Festplatte.<br/>                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



 

