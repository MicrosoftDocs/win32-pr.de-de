---
title: IVMVirtualMachine Pause-Methode (VPCCOMInterfaces.h)
description: Hält den virtuellen Computer an.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Pause-Methode Virtueller PC
- Pause-Methode Virtual PC , IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, Pause-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbab3da710a66c1e737e02693cb2002452ec11154b1be3da0e3568fea38e59f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471480"
---
# <a name="ivmvirtualmachinepause-method"></a>IVMVirtualMachine::P ause-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Hält den virtuellen Computer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                     |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0x80004005</dt> </dl>                                     | Der virtuelle Computer ist bereits angehalten.<br/>                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Der Aufrufer muss über Ausführungszugriffsberechtigungen verfügen, um diesen virtuellen Computer anzuhalten.<br/> |
| <dl> <dt>**VM \_ E \_ \_ TIMED OUT**</dt> <dt>0xA0040202</dt> </dl>                           | Der Vorgang wurde nicht rechtzeitig abgeschlossen.<br/>                |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT**</dt> <dt>0xA0040206</dt> </dl>                     | Der virtuelle Computer wird nicht ausgeführt.<br/>                               |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | Die Konfiguration ist unbekannt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                 |



 

## <a name="remarks"></a>Hinweise

**Pause** speichert den aktuellen Status des virtuellen Computers nicht.

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

 

