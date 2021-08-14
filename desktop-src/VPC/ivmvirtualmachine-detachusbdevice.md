---
title: IVMVirtualMachine DetachUSBDevice-Methode (VPCCOMInterfaces.h)
description: Gibt ein USB-Gerät von einem virtuellen Computer frei.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- DetachUSBDevice-Methode Virtueller PC
- DetachUSBDevice-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC , DetachUSBDevice-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5b45821f56a9533ed851f6c73342fbd15801223832cf9bad9a380b3f97f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344674"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a>IVMVirtualMachine::D etachUSBDevice-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Gibt ein USB-Gerät von einem virtuellen Computer frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inUSBDevice* \[ In\]
</dt> <dd>

Ein [**IVMUSBDevice-Zeiger,**](ivmusbdevice.md) der das USB-Gerät darstellt, das vom virtuellen Computer getrennt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                          | BESCHREIBUNG                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                  | Der Parameter ist **NULL.**<br/>          |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT**</dt> <dt>0xA0040206</dt> </dl>     | Der virtuelle Computer wird nicht ausgeführt.<br/> |
| <dl> <dt>**VM \_ E \_ USB \_ DETACH \_ FAILED**</dt> <dt>0xA00400927</dt> </dl> | Fehler beim Trennen.<br/>        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>          | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

