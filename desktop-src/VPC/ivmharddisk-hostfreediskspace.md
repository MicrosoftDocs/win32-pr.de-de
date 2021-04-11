---
title: Ivmharddisk hostfrediskspace-Eigenschaft (vpccominterfaces. h)
description: Ruft den verbleibenden Speicherplatz auf dem Host für die virtuelle Festplatte ab.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Hostfrediskspace-Eigenschaft virtueller PC
- Hostfrediskspace-Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, hostfrediskspace-Eigenschaft
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
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105812"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>Ivmharddisk:: hostfrediskspace-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den verbleibenden Speicherplatz auf dem Host für die virtuelle Festplatte ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Menge des verbleibenden Speicherplatzes, der auf dem Host Computer für die aktuelle Festplatten Abbild Datei verfügbar ist. Dieser Wert ist eine **Variante** vom Typ VT \_ Decimal.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                            | Bedeutung                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                               | Der Vorgang wurde durchgeführt.<br/>                                |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                                 | Der-Parameter ist **null**.<br/>                                   |
| <dl> <dt>HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)</dt> <dt>0x800700a1</dt> </dl> | Der Pfad zur aktuellen virtuellen Festplatten Datei ist ungültig.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                         | Ein unerwarteter Fehler ist aufgetreten.<br/>                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmharddisk**](ivmharddisk.md)
</dt> </dl>

 

