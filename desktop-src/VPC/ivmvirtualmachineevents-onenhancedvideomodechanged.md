---
title: IVMVirtualMachineEvents OnEnhancedVideoModeChanged-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass sich die Unterstützung eines virtuellen Computers für den erweiterten Videomodus geändert hat.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- OnEnhancedVideoModeChanged-Methode Virtueller PC
- OnEnhancedVideoModeChanged-Methode Virtual PC, IVMVirtualMachineEvents-Schnittstelle
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC, OnEnhancedVideoModeChanged-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bcdee9db2cf4b37b40d0cc77d6592c5ca1552b0a59642a01c2fe84bf4f69f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056618"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a>IVMVirtualMachineEvents::OnEnhancedVideoModeChanged-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass sich die Unterstützung eines virtuellen Computers für den erweiterten Videomodus geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*enhancedVideoMode* \[ In\]
</dt> <dd>

Gibt an, ob der erweiterte Videomodus verfügbar ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents ist als 9d84f560-bb67-4961-bd12-a4da780c67e4 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

