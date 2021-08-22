---
title: IVMAccountant NetworkBytesReceived-Eigenschaft (VPCCOMInterfaces.h)
description: Gesamtanzahl von Bytes, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer empfangen wurden.
ms.assetid: 6f6b32e6-d99b-405c-a788-ed646b3a7593
keywords:
- NetworkBytesReceived-Eigenschaft Virtueller PC
- NetworkBytesReceived-Eigenschaft Virtueller PC, IVMAccountant-Schnittstelle
- IVMAccountant-Schnittstelle Virtueller PC, NetworkBytesReceived -Eigenschaft
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
ms.openlocfilehash: 483bc038622278e23bd46688fa55695c6b11e91d7b602377ae8eb9ddaeab86c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473750"
---
# <a name="ivmaccountantnetworkbytesreceived-property"></a>IVMAccountant::NetworkBytesReceived (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Gesamtzahl der Bytes ab, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer empfangen werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_NetworkBytesReceived(
  [out, retval] VARIANT *bytesReceived
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Gesamtzahl der empfangenen Bytes. Diese Daten werden als **VARIANT** vom Typ **VT \_ DECIMAL zurückgegeben.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | Der virtuelle Computer wird nicht ausgeführt.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



## <a name="remarks"></a>Hinweise

Beachten Sie, dass die Netzwerk-E/A-Statistiken auf 0 (null) zurückgesetzt werden, wenn ein virtueller Computer aus dem gespeicherten Zustand ausgeschaltet, zurückgesetzt oder wiederhergestellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant ist als 6376c067-7f57-4d63-b754-06e2e4f51d73 definiert.<br/>              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

