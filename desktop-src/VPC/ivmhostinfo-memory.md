---
title: IVMHostInfo-Speichereigenschaft (VPCCOMInterfaces.h)
description: Ruft die Gesamtmenge des physischen Arbeitsspeichers auf dem Hostcomputer in Megabyte ab.
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Memory-Eigenschaft Virtueller PC
- Memory-Eigenschaft Virtueller PC, IVMHostInfo-Schnittstelle
- IVMHostInfo-Schnittstelle Virtueller PC, Memory-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22eeae9bcd7be7436d02f9aa116882acc4d8e0e8ee5d2703790b5e20cd4d744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753329"
---
# <a name="ivmhostinfomemory-property"></a>IVMHostInfo::Memory-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Gesamtmenge des physischen Arbeitsspeichers auf dem Hostcomputer in Megabyte ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Gesamtmenge des physischen Arbeitsspeichers in Megabyte. Dieser Wert ist eine **VARIANT** vom Typ VT \_ DECIMAL.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

