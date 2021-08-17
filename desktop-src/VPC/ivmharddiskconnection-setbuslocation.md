---
title: IVMHardDiskConnection SetBusLocation-Methode (VPCCOMInterfaces.h)
description: Legt den Busstandort fest, an den diese Festplatte angefügt ist.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- SetBusLocation-Methode Virtueller PC
- SetBusLocation-Methode Virtueller PC, IVMHardDiskConnection-Schnittstelle
- IVMHardDiskConnection-Schnittstelle Virtueller PC, SetBusLocation-Methode
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f2ff59b0318c321d1fb5ce75bac8c5604c5e96474c52565732ec3794b4aab0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974350"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a>IVMHardDiskConnection::SetBusLocation-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Legt den Busstandort fest, an den diese Festplatte angefügt ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vmBusNumber* \[ In\]
</dt> <dd>

Die zu verwendende Busnummer.

</dd> <dt>

*vmDeviceNumber* \[ In\]
</dt> <dd>

Die zu verwendende Gerätenummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                               | Beschreibung                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | Der Vorgang wurde durchgeführt.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                    | Der angegebene Busstandort ist ungültig.<br/>                                                         |
| <dl> <dt>**VM \_ E \_ \_ VM, DIE \_ AUSGEFÜHRT WIRD ODER \_ 0XA004020B**</dt> <dt></dt> </dl>    | Der Busstandort konnte nicht festgelegt werden, da sich der virtuelle Computer in einem ausgeführten oder gespeicherten Zustand befindet.<br/>    |
| <dl> <dt>**VM \_ E \_ DRIVE \_ BUS \_ LOC IN USE \_ \_ 0XA00400503**</dt> <dt></dt> </dl> | Der Busstandort konnte nicht festgelegt werden, da derzeit ein anderes Gerät an diesen Standort angefügt ist.<br/> |
| <dl> <dt>**VM \_ E \_ DRIVE \_ INVALID**</dt> <dt>0xA0040502</dt> </dl>            | Das aktuelle Laufwerk ist ungültig.<br/>                                                                  |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>               | Der aktuelle virtuelle Computer ist ungültig.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>               | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection ist als aefa36a5-463a-46ae-9e6c-a1fb4e12e671 definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

