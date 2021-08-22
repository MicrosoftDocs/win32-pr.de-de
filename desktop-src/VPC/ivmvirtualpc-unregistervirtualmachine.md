---
title: IVMVirtualPC UnregisterVirtualMachine-Methode (VPCCOMInterfaces.h)
description: Aufheben der Registrierung einer VM-Konfiguration, ohne die Konfigurationsdatei zu löschen.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- UnregisterVirtualMachine-Methode Virtueller PC
- UnregisterVirtualMachine-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, UnregisterVirtualMachine-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6173d6f43d51384af610b850ec654d185f0a8ce31a375b4dd90bd929c6455b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652730"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a>IVMVirtualPC::UnregisterVirtualMachine-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Die Registrierung einer VM-Konfiguration wird aufgehoben, ohne die Konfigurationsdatei zu löschen.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualMachine* \[ In\]
</dt> <dd>

Ein Zeiger auf ein [**IVMVirtualMachine-Objekt,**](ivmvirtualmachine.md) das die VM-Konfiguration darstellt, deren Registrierung aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | Beschreibung                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                | Der *virtualMachine-Parameter* war **NULL.**<br/>                                         |
| <dl> <dt>**VM \_ E \_ \_ VM, DIE**</dt> <dt>0XA0040500</dt> </dl>                        | Der virtuelle Computer wird ausgeführt.<br/>                                                                   |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0XA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

## <a name="remarks"></a>Hinweise

Nur beendete VMs können die Registrierung aufheben. Vorhandene gespeicherte Zustands- oder Rückgängig-Laufwerksdaten für diese Konfiguration werden beibehalten, wenn die Registrierung eines virtuellen Computers aufgehoben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

