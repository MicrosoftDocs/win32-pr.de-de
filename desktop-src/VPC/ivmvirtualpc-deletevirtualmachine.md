---
title: IVMVirtualPC DeleteVirtualMachine-Methode (VPCCOMInterfaces.h)
description: Löscht die Konfiguration eines virtuellen Computers.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- DeleteVirtualMachine-Methode Virtueller PC
- DeleteVirtualMachine-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, DeleteVirtualMachine-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3471106beeffdfe756ad0793004b68d0a55fd14dda28a9796f4540d2503a88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471330"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>IVMVirtualPC::D eleteVirtualMachine-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Löscht die Konfiguration eines virtuellen Computers.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualMachine* \[ In\]
</dt> <dd>

Ein Zeiger auf ein [**IVMVirtualMachine-Objekt,**](ivmvirtualmachine.md) das die zu löschende Konfiguration des virtuellen Computers darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                           | Die angegebene Konfiguration wurde nicht gefunden.<br/>                                      |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                | Der *virtualMachine-Parameter* war **NULL.**<br/>                                         |
| <dl> <dt>**VM \_ E \_ VM \_ RUNNING**</dt> <dt>0xA0040500</dt> </dl>                        | Der virtuelle Computer wird ausgeführt.<br/>                                                      |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0XA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

## <a name="remarks"></a>Hinweise

Nur beendete virtuelle Computer können gelöscht werden. Beachten Sie, dass alle vorhandenen gespeicherten Zustands- oder Rückgängig-Laufwerksdaten für diese Konfiguration zusätzlich zur Konfigurationsdatei gelöscht werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

