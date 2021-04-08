---
title: Ivmvirtualmachineevents onconfigurationchanged-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass sich ein Wert in der Konfiguration für diesen virtuellen Computer geändert hat.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Onconfigurationchanged-Methode virtueller PC
- Onconfigurationchanged-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onconfigurationchanged-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949379"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>Ivmvirtualmachineevents:: onconfigurationchanged-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass sich ein Wert in der Konfiguration für diesen virtuellen Computer geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*configKey* \[ in\]
</dt> <dd>

Der Wert in der Konfiguration, der geändert wurde.

</dd> <dt>

*ConfigData* \[ in\]
</dt> <dd>

Der neue Wert für die Konfiguration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn sich die Konfiguration für diesen virtuellen Computer ändert. Das Client Programm muss diese Schnittstellen Methode implementieren, um eine Benachrichtigung über das vmvirtualmachineevent configurationchanged-Ereignis zu erhalten, das \_ von [**ivmvirtualmachine**](ivmvirtualmachine.md)stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachineevents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

