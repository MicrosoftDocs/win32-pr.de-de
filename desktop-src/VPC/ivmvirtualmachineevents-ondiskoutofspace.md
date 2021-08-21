---
title: IVMVirtualMachineEvents OnDiskOutOfSpace-Methode (VPCCOMInterfaces.h)
description: Empfängt die Benachrichtigung, dass für einen für einen virtuellen Computer erforderlichen Datenträger wenig freier Speicherplatz verfügbar ist.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- OnDiskOutOfSpace-Methode Virtueller PC
- OnDiskOutOfSpace-Methode Virtual PC , IVMVirtualMachineEvents-Schnittstelle
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC , OnDiskOutOfSpace-Methode
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
ms.openlocfilehash: c482f0a713fda7e13436dc28d295469237273a7c607e522ce457ec908f210223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056628"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>IVMVirtualMachineEvents::OnDiskOutOfSpace-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt die Benachrichtigung, dass für einen für einen virtuellen Computer (VM) erforderlichen Datenträger wenig freier Speicherplatz verfügbar ist. Wenn der freie Speicherplatz unter 100 MB fällt, wird dieses Ereignis als Warnung empfangen, und wenn der freie Speicherplatz unter 20 MB fällt, wird dieses Ereignis erneut als Fehler empfangen, und die VM wird angehalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*criticallyLow* \[ In\]
</dt> <dd>

Legen Sie auf **VARIANT \_ TRUE** fest, wenn der Datenträger weniger als 20 MB frei hat, und auf **VARIANT \_ FALSE,** wenn der freie Speicherplatz mehr als 20 MB, aber weniger als 100 MB beträgt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

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

 

