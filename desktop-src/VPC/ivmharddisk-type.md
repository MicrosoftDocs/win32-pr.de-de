---
title: IVMHardDisk Type-Eigenschaft (VPCCOMInterfaces.h)
description: Typ der virtuellen Festplatte.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Type-Eigenschaft Virtueller PC
- Type-Eigenschaft Virtual PC , IVMHardDisk-Schnittstelle
- IVMHardDisk-Schnittstelle Virtueller PC, Type-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c2ba462496f6791d129918b93401c971b755ef40c40ef9a1177059dc7bcce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998930"
---
# <a name="ivmharddisktype-property"></a>IVMHardDisk::Type-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Typ der virtuellen Festplatte ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Typ des aktuellen Festplattenimages.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                  |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                                    | Der Parameter ist **NULL.**<br/>                                                     |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0x80070002</dt> </dl> | Die aktuelle Festplattenimagedatei wurde nicht gefunden.<br/>                           |
| <dl> <dt>VM \_ E \_ LAUFWERK \_ UNGÜLTIGE</dt> <dt>0xA0040502</dt> </dl>                         | Der Typ des aktuellen Festplattenimages ist ungültig.<br/>                            |
| <dl> <dt>VM \_ E \_ HD IMAGE OPEN \_ \_ \_ FAIL</dt> <dt>0xA004067C</dt> </dl>                  | Fehler beim Öffnen der aktuellen Festplattenimagedatei.<br/>   |
| <dl> <dt>VM \_ E \_ HD \_ IMAGE \_ ACCESS</dt> <dt>0xA0040681</dt> </dl>                      | Fehler beim Zugreifen auf die aktuelle Festplattenimagedatei.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

