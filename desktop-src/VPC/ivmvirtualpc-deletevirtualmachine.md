---
title: Ivmvirtualpc deletevirtualmachine-Methode (vpccominterfaces. h)
description: Löscht die Konfiguration einer virtuellen Maschine.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Deletevirtualmachine-Methode Virtual PC
- Deletevirtualmachine-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, deletevirtualmachine-Methode
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
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343460"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>Ivmvirtualpc::D eletevirtualmachine-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Löscht die Konfiguration einer virtuellen Maschine.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualmachine* \[ in\]
</dt> <dd>

Ein Zeiger auf ein [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das die zu löschende Konfiguration der virtuellen Maschine darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**S \_ Falsch**</dt> <dt>1</dt> </dl>                                           | Die angegebene Konfiguration wurde nicht gefunden.<br/>                                      |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                | Der Parameter " *virtualmachine* " war **null**.<br/>                                         |
| <dl> <dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt> </dl>                        | Der virtuelle Computer wird ausgeführt.<br/>                                                      |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl> | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

## <a name="remarks"></a>Bemerkungen

Es können nur beendete virtuelle Computer gelöscht werden. Beachten Sie, dass alle vorhandenen gespeicherten Zustands-oder rückgängig-Laufwerks Daten für diese Konfiguration zusätzlich zur Konfigurationsdatei gelöscht werden.

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

 

