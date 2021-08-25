---
title: IVMVirtualMachine TurnOff-Methode (VPCCOMInterfaces.h)
description: Der virtuelle Computer wird heruntergefahren.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- TurnOff-Methode Virtueller PC
- TurnOff-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, TurnOff-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5351aacc3e21cd620aa31798314fd7f6728cf98653cb83cbaa2f19439d530c44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864160"
---
# <a name="ivmvirtualmachineturnoff-method"></a>IVMVirtualMachine::TurnOff-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Der virtuelle Computer wird heruntergefahren.

## <a name="syntax"></a>Syntax


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*turnOffTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das verwendet wird, um den Abschlussfortschritt der Turnoffsequenz des virtuellen Computers nachzuverfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                                     |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                  | Der Parameter ist **NULL.**<br/>                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Der Aufrufer muss über Ausführungszugriffsberechtigungen verfügen, um diesen virtuellen Computer zu deaktivieren.<br/> |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,**</dt> <dt>0xA0040206</dt> </dl>                     | Der virtuelle Computer wird nicht ausgeführt.<br/>                                               |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | Die Konfiguration ist unbekannt.<br/>                                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                 |



 

## <a name="remarks"></a>Hinweise

Diese Methode schaltet den virtuellen Computer auf die gleiche Weise wie das Ausschalten eines physischen Computers aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

