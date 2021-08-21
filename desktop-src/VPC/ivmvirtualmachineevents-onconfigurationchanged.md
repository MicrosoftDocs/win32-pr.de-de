---
title: IVMVirtualMachineEvents OnConfigurationChanged-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass sich ein Wert in der Konfiguration für diesen virtuellen Computer geändert hat.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- OnConfigurationChanged-Methode Virtueller PC
- OnConfigurationChanged-Methode Virtueller PC, IVMVirtualMachineEvents-Schnittstelle
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC , OnConfigurationChanged-Methode
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
ms.openlocfilehash: 36ca4d3b72d9cd2b06db2ca7b7b65e0c63795a4db0e52ccd9b76a62ff8b192e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056638"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>IVMVirtualMachineEvents::OnConfigurationChanged-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*configKey* \[ In\]
</dt> <dd>

Der Wert innerhalb der geänderten Konfiguration.

</dd> <dt>

*configData* \[ In\]
</dt> <dd>

Der neue Wert für die Konfiguration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn sich die Konfiguration für diesen virtuellen Computer ändert. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das Ereignis vmVirtualMachineEvent ConfigurationChanged zu erhalten, das \_ von [**IVMVirtualMachine**](ivmvirtualmachine.md)stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents ist als 9d84f560-bb67-4961-bd12-a4da780c67e4 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

