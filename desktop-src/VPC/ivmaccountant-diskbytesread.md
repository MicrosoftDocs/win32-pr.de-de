---
title: IVMAccountant DiskBytesRead-Eigenschaft (VPCCOMInterfaces.h)
description: Gesamtzahl der Bytes, die von allen Speichercontrollern für diesen virtuellen Computer gelesen werden.
ms.assetid: cf2c1a58-2261-496d-b8e2-a0d5285c16ab
keywords:
- DiskBytesRead-Eigenschaft Virtueller PC
- DiskBytesRead-Eigenschaft Virtueller PC, IVMAccountant-Schnittstelle
- IVMAccountant-Schnittstelle Virtueller PC , DiskBytesRead-Eigenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesRead
- IVMAccountant.get_DiskBytesRead
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e8c9513517250614da812f9c1d602a2a92b9dce1d7bc0c2b25db100016a5084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473870"
---
# <a name="ivmaccountantdiskbytesread-property"></a>IVMAccountant::D iskBytesRead-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Gesamtzahl der Bytes ab, die von allen Speichercontrollern für diesen virtuellen Computer gelesen werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DiskBytesRead(
  [out, retval] VARIANT *bytesRead
);
```



## <a name="property-value"></a>Eigenschaftswert

Die gesamte Anzahl der gelesenen Bytes Diese Daten werden als **VARIANT** vom Typ **VT \_ DECIMAL** zurückgegeben.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | Der virtuelle Computer wird nicht ausgeführt.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



## <a name="remarks"></a>Hinweise

Beachten Sie, dass Datenträger-E/A-Statistiken auf 0 (null) zurückgesetzt werden, wenn ein virtueller Computer eingeschaltet, zurückgesetzt oder aus dem gespeicherten Zustand wiederhergestellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant ist als 6376c067-7f57-4d63-b754-06e2e4f51d73 definiert.<br/>              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

