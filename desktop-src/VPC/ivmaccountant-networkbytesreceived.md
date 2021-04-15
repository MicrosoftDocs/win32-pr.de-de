---
title: Ivmaccountant-networkbytesempfangenschaft (vpccominterfaces. h)
description: Die Gesamtanzahl der Bytes, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer empfangen wurden.
ms.assetid: 6f6b32e6-d99b-405c-a788-ed646b3a7593
keywords:
- Networkbytesempfangene Eigenschaft virtueller PC
- Networkbytesempfangene Eigenschaft Virtual PC, ivmaccountant-Schnittstelle
- Ivmaccountant Interface Virtual PC, networkbytesempfangenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesReceived
- IVMAccountant.get_NetworkBytesReceived
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e14d7454516ff4e83771744c74f31ee594aa67f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479014"
---
# <a name="ivmaccountantnetworkbytesreceived-property"></a>Ivmaccountant:: networkbytesempfangenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Gesamtanzahl der Bytes ab, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer empfangen wurden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_NetworkBytesReceived(
  [out, retval] VARIANT *bytesReceived
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Gesamtanzahl der empfangenen Bytes. Diese Daten werden als **Variante** des Typs **VT \_ Decimal** zurückgegeben.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>          |
| <dl> <dt>S \_ Falsch</dt> <dt>1</dt> </dl>                    | Der virtuelle Computer wird nicht ausgeführt.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die Netzwerk-e/a-Statistiken auf Null zurückgesetzt werden, wenn ein virtueller Computer hochgefahren, zurückgesetzt oder aus dem gespeicherten Zustand wieder hergestellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmaccountant**](ivmaccountant.md)
</dt> </dl>

 

