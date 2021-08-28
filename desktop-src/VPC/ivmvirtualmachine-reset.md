---
title: IVMVirtualMachine Reset-Methode (VPCCOMInterfaces.h)
description: Setzt den virtuellen Computer zurück.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Reset method Virtual PC
- Reset method Virtual PC , IVMVirtualMachine interface
- IVMVirtualMachine-Schnittstelle Virtueller PC, Reset-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d09204afba2d5c9340350a1fad256e84f8fbf8899c544c7b52d36dfb872c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056778"
---
# <a name="ivmvirtualmachinereset-method"></a>IVMVirtualMachine::Reset-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Setzt den virtuellen Computer zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resetTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das zum Nachverfolgen des Abschlussfortschritts der Zurücksetzungssequenz des virtuellen Computers verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | Beschreibung                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                     |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                  | Der Parameter ist **NULL.**<br/>                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0X80070005</dt> </dl> | Der Aufrufer muss über Ausführungszugriffsberechtigungen verfügen, um diesen virtuellen Computer zurückzusetzen.<br/> |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ 0XA0040206**</dt> <dt></dt> </dl>                     | Der virtuelle Computer wird nicht ausgeführt.<br/>                                            |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | Die Konfiguration ist unbekannt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

