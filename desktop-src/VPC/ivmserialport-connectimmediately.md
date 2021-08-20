---
title: IVMSerialPort ConnectImmediately-Eigenschaft (VPCCOMInterfaces.h)
description: Bestimmt, ob der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modembefehl empfangen wird.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- ConnectImmediately-Eigenschaft Virtueller PC
- ConnectImmediately-Eigenschaft Virtueller PC, IVMSerialPort-Schnittstelle
- IVMSerialPort-Schnittstelle Virtueller PC, ConnectImmediately-Eigenschaft
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a2a052f946039e8ae7a5e1c2905e90596da7d537cbc06d0789adb0f01760bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753005"
---
# <a name="ivmserialportconnectimmediately-property"></a>IVMSerialPort::ConnectImmediately-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Bestimmt, ob der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modembefehl empfangen wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a>Eigenschaftswert

**VARIANT \_ TRUE,** wenn der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modembefehl empfangen wird. **VARIANT \_ Andernfalls FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                            |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>                               |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                        |



## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur gültig, wenn die [**Type-Eigenschaft**](ivmserialport-type.md) des Ports **vmSerialPort \_ HostPort ist.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

