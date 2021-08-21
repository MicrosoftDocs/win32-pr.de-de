---
title: IVMHardDisk HostFreeDiskSpace-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Menge des verbleibenden Speicherplatzes ab, der auf dem Host für die virtuelle Festplatte verfügbar ist.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- HostFreeDiskSpace-Eigenschaft Virtueller PC
- HostFreeDiskSpace-Eigenschaft Virtueller PC, IVMHardDisk-Schnittstelle
- IVMHardDisk-Schnittstelle Virtueller PC, HostFreeDiskSpace-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b92c8a1253fb4dbefb6db2f2ed9a9d278b907ecfb30e448edb36ec2cbe98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123700"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>IVMHardDisk::HostFreeDiskSpace-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Menge des verbleibenden Speicherplatzes ab, der auf dem Host für die virtuelle Festplatte verfügbar ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Menge des verbleibenden Speicherplatzes, der auf dem Hostcomputer für die aktuelle Festplattenimagedatei verfügbar ist. Dieser Wert ist eine **VARIANT** vom Typ VT \_ DECIMAL.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                            | Bedeutung                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                               | Der Vorgang wurde durchgeführt.<br/>                                |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                                 | Der Parameter ist **NULL.**<br/>                                   |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt> </dl> | Der Pfad zur aktuellen virtuellen Festplattendatei ist ungültig.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                         | Ein unerwarteter Fehler ist aufgetreten.<br/>                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

