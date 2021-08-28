---
title: IVMVirtualMachine RemoveHardDiskConnection-Methode (VPCCOMInterfaces.h)
description: Entfernt die angegebene Festplattenverbindung vom virtuellen Computer.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- RemoveHardDiskConnection-Methode Virtueller PC
- RemoveHardDiskConnection-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, RemoveHardDiskConnection-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdcf09118e8fd9911937a7ab8323266ed33c7e974e0b98579fb30a75dae7f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998660"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a>IVMVirtualMachine::RemoveHardDiskConnection-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Entfernt die angegebene Festplattenverbindung vom virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hardDiskConnection* \[ In\]
</dt> <dd>

Ein [**IVMHardDiskConnection-Objekt,**](ivmharddiskconnection.md) das die zu entfernende Festplattenverbindung darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                            | Beschreibung                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                              |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                    | Der Parameter ist **NULL.**<br/>                                 |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                              |
| <dl> <dt>**VM \_ E \_ \_ VM, DIE \_ AUSGEFÜHRT WIRD ODER \_ 0XA004020B**</dt> <dt></dt> </dl> | Der virtuelle Computer befindet sich in einem ausgeführten oder gespeicherten Zustand.<br/>        |
| <dl> <dt>**VM \_ E \_ DRIVE \_ INVALID**</dt> <dt>0xA0040502</dt> </dl>         | Das angegebene Laufwerk ist nicht mit diesem Busstandort verbunden.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                          |



 

## <a name="remarks"></a>Hinweise

Sie können nur eine vorhandene Festplattenverbindung von einem beendeten virtuellen Computer entfernen. Eine Liste der Verbindungen, die derzeit an den virtuellen Computer angefügt sind, wird durch Auflisten der [**HardDiskConnections-Eigenschaft**](ivmvirtualmachine-harddiskconnections.md) ermittelt.

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

 

