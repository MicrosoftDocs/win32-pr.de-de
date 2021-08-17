---
title: IVMGuestOS IsHostTimeSyncEnabled-Eigenschaft (VPCCOMInterfaces.h)
description: Gibt an, ob die Integrationskomponenten auf diesem virtuellen Computer die Uhr des Gasts mit der Uhr des Hosts synchronisieren sollen.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- IsHostTimeSyncEnabled-Eigenschaft Virtueller PC
- IsHostTimeSyncEnabled-Eigenschaft Virtual PC , IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC , IsHostTimeSyncEnabled-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d64482db1c4d541204fa925d10e7e1d860347183f2229449937038782e22e06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136783"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a>IVMGuestOS::IsHostTimeSyncEnabled-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Gibt an, ob die Integrationskomponenten auf diesem virtuellen Computer (VM) die Uhr des Gasts mit der Uhr des Hosts synchronisieren sollen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a>Eigenschaftswert

Verwenden Sie **VARIANT \_ TRUE,** wenn die Integrationskomponenten auf diesem virtuellen Computer die Uhr des Gasts mit der Uhr des Hosts synchronisieren sollen, andernfalls **VARIANT \_ FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>               |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der *isEnabled-Parameter* ist nicht angegeben.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>               |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>           |



## <a name="remarks"></a>Hinweise

Sie können diese Einstellung nicht ändern, während der virtuelle Computer aktiv ist (d. b. ausgeführt oder im gespeicherten Zustand).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

