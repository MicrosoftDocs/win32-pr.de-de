---
title: IVMHardDisk SizeInGuest-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Größe der virtuellen Festplatte im Gastbetriebssystem ab.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- SizeInGuest-Eigenschaft Virtueller PC
- SizeInGuest-Eigenschaft Virtueller PC, IVMHardDisk-Schnittstelle
- IVMHardDisk-Schnittstelle Virtueller PC, SizeInGuest-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efbdcf9f5aa60a8dfdce9c71de745e0567995b90df13ffd39b5969689de099c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653290"
---
# <a name="ivmharddisksizeinguest-property"></a>IVMHardDisk::SizeInGuest (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Größe der virtuellen Festplatte im Gastbetriebssystem ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Größe des Festplattenimages in Bytes. Dieser Wert ist eine **VARIANT** vom Typ VT \_ DECIMAL.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                  |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                                    | Der Parameter ist **NULL.**<br/>                                                     |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0X80070002</dt> </dl> | Die aktuelle virtuelle Festplattendatei wurde nicht gefunden.<br/>                         |
| <dl> <dt>VM \_ FEHLER BEIM ÖFFNEN DES E \_ \_ \_ \_ HD-IMAGES</dt> <dt>0xA004067C</dt> </dl>                  | Fehler beim Öffnen der aktuellen Festplattenimagedatei.<br/>   |
| <dl> <dt>VM \_ E \_ HD IMAGE ACCESS \_ \_ 0xA0040681</dt> <dt></dt> </dl>                      | Fehler beim Zugreifen auf die aktuelle Festplattenimagedatei.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

