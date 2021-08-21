---
title: IVMVirtualMachine BIOSSerialNumber-Eigenschaft (VPCCOMInterfaces.h)
description: BIOS-Seriennummer.
ms.assetid: a105009d-1c44-4079-a7d4-103cb02bad71
keywords:
- BIOSSerialNumber-Eigenschaft Virtueller PC
- BIOSSerialNumber-Eigenschaft Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, BIOSSerialNumber-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSSerialNumber
- IVMVirtualMachine.get_BIOSSerialNumber
- IVMVirtualMachine.put_BIOSSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f5cbf848f35cda387b1f596e68a7316e99cc7392c2c8c93c806186b961b37e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123180"
---
# <a name="ivmvirtualmachinebiosserialnumber-property"></a>IVMVirtualMachine::BIOSSerialNumber-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die BIOS-Seriennummer ab und legt sie fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BIOSSerialNumber(
  [in]          BSTR biosSerialNumber
);

HRESULT get_BIOSSerialNumber(
  [out, retval] BSTR *biosSerialNumber
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die BIOS-Seriennummer an.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                               | Bedeutung                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                                               |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                    | Der Parameter ist **NULL.**<br/>                                                  |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>                 | Der Parameter ist größer als 32 Zeichen, eine leere Zeichenfolge oder ungültig.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                                               |
| <dl> <dt>VM \_ \_E-VM, \_ AUF DER 0XA004020B AUSGEFÜHRT ODER GESPEICHERT \_ \_ WIRD</dt> <dt></dt> </dl> | Der virtuelle Computer befindet sich in einem ausgeführten oder gespeicherten Zustand.<br/>                         |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                           |



## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält erst dann gültige Informationen, nachdem der virtuelle Computer zum ersten Mal gestartet wurde. Eine leere Zeichenfolge wird zurückgegeben, wenn sie vor dem ersten Start gelesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

