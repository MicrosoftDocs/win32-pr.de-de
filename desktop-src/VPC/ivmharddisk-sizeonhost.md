---
title: IVMHardDisk SizeOnHost-Eigenschaft (VPCCOMInterfaces.h)
description: Größe der virtuellen Festplattendatei auf dem Hostcomputer.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- SizeOnHost-Eigenschaft Virtueller PC
- SizeOnHost-Eigenschaft Virtueller PC, IVMHardDisk-Schnittstelle
- IVMHardDisk-Schnittstelle Virtueller PC, SizeOnHost-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8952428665ef651d5d420bc457f1eed52f6c6ded78a7b448c8325ab09f352a9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867120"
---
# <a name="ivmharddisksizeonhost-property"></a>IVMHardDisk::SizeOnHost-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Größe der virtuellen Festplattendatei auf dem Hostcomputer ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Größe der Festplattenimagedatei in Bytes. Dieser Wert ist eine **VARIANT** vom Typ **VT \_ DECIMAL**.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>           |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                                    | Der Parameter ist **NULL.**<br/>              |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>       |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0x80070002</dt> </dl> | Die Festplattenimagedatei wurde nicht gefunden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

