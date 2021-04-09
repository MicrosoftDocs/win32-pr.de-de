---
title: Ivmvirtualmachineevents ondiskouesfspace-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass der freie Speicherplatz auf einem für einen virtuellen Computer erforderlichen Datenträger gering ist.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Ondiskoudef Space-Methode virtueller PC
- Ondiskoudef Space-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, ondiskouesf Space-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858625"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>Ivmvirtualmachineevents:: ondiskoudef Space-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass der freie Speicherplatz für einen virtuellen Computer (VM) nicht ausreichend ist. Fällt der freie Speicherplatz unter 100 MB, wird dieses Ereignis als Warnung empfangen, und wenn der freie Speicherplatz unter 20 MB sinkt, wird dieses Ereignis erneut als Fehler empfangen, und der virtuelle Computer wird angehalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*criticallylow* \[ in\]
</dt> <dd>

Legen Sie diese Einstellung auf **Variant \_ true** fest, wenn der Datenträger weniger als 20 MB frei ist, und auf **\_ false** , wenn der freie Speicherplatz größer als 20 MB, aber kleiner als 100 MB ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

 

