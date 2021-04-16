---
title: Ivmvirtualpc unregistervirtualmachine-Methode (vpccominterfaces. h)
description: Hebt die Registrierung einer VM-Konfiguration auf, ohne die Konfigurationsdatei zu löschen.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- Unregistervirtualmachine-Methode Virtual PC
- Unregistervirtualmachine-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, unregistervirtualmachine-Methode
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
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478993"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a>Ivmvirtualpc:: unregistervirtualmachine-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Hebt die Registrierung einer Konfiguration eines virtuellen Computers (VM) auf, ohne die Konfigurationsdatei zu löschen.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualmachine* \[ in\]
</dt> <dd>

Ein Zeiger auf ein [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das die VM-Konfiguration darstellt, deren Registrierung aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                | Der Parameter " *virtualmachine* " war **null**.<br/>                                         |
| <dl> <dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt> </dl>                        | Die VM wird ausgeführt.<br/>                                                                   |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl> | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

## <a name="remarks"></a>Bemerkungen

Die Registrierung von nur beendeten VMS kann aufgehoben werden. Vorhandene gespeicherte Zustands-oder rückgängig-Laufwerks Daten für diese Konfiguration bleiben erhalten, wenn die Registrierung eines virtuellen Computers aufgehoben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpc**](ivmvirtualpc.md)
</dt> </dl>

 

