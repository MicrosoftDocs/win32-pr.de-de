---
title: IVMDVDDrive BusNumber-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Busnummer ab, an die dieses Gerät angefügt ist.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- BusNumber-Eigenschaft Virtueller PC
- BusNumber-Eigenschaft Virtueller PC, IVMDVDDrive-Schnittstelle
- IVMDVDDrive-Schnittstelle Virtueller PC , BusNumber-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420a3ebdb2f4b4d04532e387c0466a2938e2e51c9ffafac3b975862cddb11169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136823"
---
# <a name="ivmdvddrivebusnumber-property"></a>IVMDVDDrive::BusNumber-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Busnummer ab, an die dieses Gerät angefügt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Busnummer. In einem IDE-Bus würde dieser Wert beispielsweise entweder den primären oder sekundären Standort darstellen.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                       | Bedeutung                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | Der Vorgang wurde durchgeführt.<br/>                                          |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>            | Der Parameter ist **NULL.**<br/>                                             |
| <dl> <dt>VM \_ \_E LAUFWERK \_ UNGÜLTIGE</dt> <dt>0xA0040502</dt> </dl> | Der Busspeicherort für dieses DVD-Laufwerk wurde nicht ordnungsgemäß initialisiert.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

