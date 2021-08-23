---
title: IVMAccountant DiskBytesWritten-Eigenschaft (VPCCOMInterfaces.h)
description: Gesamtanzahl von Bytes, die von allen Speichercontrollern für diesen virtuellen Computer geschrieben wurden.
ms.assetid: a2a5730b-a411-48b8-aca8-d09cf09432a9
keywords:
- DiskBytesWritten-Eigenschaft Virtueller PC
- DiskBytesWritten-Eigenschaft Virtueller PC, IVMAccountant-Schnittstelle
- IVMAccountant-Schnittstelle Virtueller PC, DiskBytesWritten-Eigenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesWritten
- IVMAccountant.get_DiskBytesWritten
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5268f2cad452cad907f12031996e1d3092d9a91c0f52f8c045e1bfeaebc53f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654410"
---
# <a name="ivmaccountantdiskbyteswritten-property"></a>IVMAccountant::D iskBytesWritten-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Gesamtzahl der Bytes ab, die von allen Speichercontrollern für diesen virtuellen Computer geschrieben wurden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DiskBytesWritten(
  [out, retval] VARIANT *bytesWritten
);
```



## <a name="property-value"></a>Eigenschaftswert

Die gesamte Anzahl der gelesenen Bytes Diese Daten werden als **VARIANT** vom Typ **VT \_ DECIMAL zurückgegeben.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | Der virtuelle Computer wird nicht ausgeführt.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



## <a name="remarks"></a>Hinweise

Beachten Sie, dass Datenträger-E/A-Statistiken auf 0 (null) zurückgesetzt werden, wenn ein virtueller Computer aus dem gespeicherten Zustand ausgeschaltet, zurückgesetzt oder wiederhergestellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant ist als 6376c067-7f57-4d63-b754-06e2e4f51d73 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

