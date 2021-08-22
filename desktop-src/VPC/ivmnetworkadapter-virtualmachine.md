---
title: IVMNetworkAdapter VirtualMachine-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft den virtuellen Computer ab, der dieser Netzwerkschnittstelle zugeordnet ist.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- VirtualMachine-Eigenschaft Virtueller PC
- VirtualMachine-Eigenschaft Virtual PC , IVMNetworkAdapter-Schnittstelle
- IVMNetworkAdapter-Schnittstelle Virtueller PC, VirtualMachine-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a407b3c8158dca27e76d24fd1b104362225ba65a4d66586d82f8461d3293b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510480"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a>IVMNetworkAdapter::VirtualMachine-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den virtuellen Computer ab, der dieser Netzwerkschnittstelle zugeordnet ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**IVMVirtualMachine-Schnittstelle,**](ivmvirtualmachine.md) die den virtuellen Computer darstellt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>        |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>           |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Der virtuelle Computer wurde nicht gefunden.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter ist als e32e4165-22b8-4dc0-8d57-850171ae207a definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

