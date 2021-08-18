---
title: IVMVirtualMachine ChassisSerialNumber-Eigenschaft (VPCCOMInterfaces.h)
description: Seriennummer des Gehäuses.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- ChassisSerialNumber-Eigenschaft Virtueller PC
- ChassisSerialNumber-Eigenschaft Virtual PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, ChassisSerialNumber-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40b9922f862e52cc6b1cce3d6f508254f37ca41ec314f4312ffa159cb9cde15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752438"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a>IVMVirtualMachine::ChassisSerialNumber-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Seriennummer des Gehäuses ab und legt sie fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die Seriennummer des Gehäuses an.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                               | Bedeutung                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                                               |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                    | Der Parameter ist **NULL.**<br/>                                                  |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>                 | Der -Parameter ist größer als 32 Zeichen, eine leere Zeichenfolge oder ungültig.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                                               |
| <dl> <dt>VM \_ E \_ \_ VM, DIE \_ AUSGEFÜHRT WIRD ODER \_ 0XA004020B</dt> <dt></dt> </dl> | Der virtuelle Computer befindet sich in einem ausgeführten oder gespeicherten Zustand.<br/>                         |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                           |



## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält erst gültige Informationen, nachdem der virtuelle Computer zum ersten Mal gestartet wurde. Eine leere Zeichenfolge wird zurückgegeben, wenn sie vor dem ersten Start gelesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

