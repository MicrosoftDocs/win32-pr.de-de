---
title: IVMVirtualMachine Save-Methode (VPCCOMInterfaces.h)
description: Speichert den Status des virtuellen Computers.
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Save method Virtual PC
- Save method Virtual PC , IVMVirtualMachine interface
- IVMVirtualMachine-Schnittstelle Virtueller PC, Save-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609125ed9ae8deab897163d6a841e9cb665659c2c5af76baff3a1d96fb235e92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124790"
---
# <a name="ivmvirtualmachinesave-method"></a>IVMVirtualMachine::Save-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Speichert den Status des virtuellen Computers.

## <a name="syntax"></a>Syntax


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*saveTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das verwendet wird, um den Abschlussstatus der Zustandsspeichersequenz des virtuellen Computers nachzuverfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | Beschreibung                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                                 |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0x80004005</dt> </dl>                                     | Der virtuelle Computer konnte nicht gespeichert werden, da die Rückgängigdatenträger zum Löschen markiert wurden.<br/>    |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                  | Der Parameter ist **NULL.**<br/>                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Der Aufrufer muss über Ausführungszugriffsberechtigungen verfügen, um den Status dieses virtuellen Computers zu speichern.<br/> |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,**</dt> <dt>0xA0040206</dt> </dl>                     | Der virtuelle Computer wird nicht ausgeführt.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                             |



 

## <a name="remarks"></a>Hinweise

Der virtuelle Computer wird deaktiviert, wenn der Task **Speichern** abgeschlossen ist. Die [**IVMVirtualMachine::State-Eigenschaft**](ivmvirtualmachine-state.md) enthält **vmVMState \_ Saving,** während der Speicher ausgeführt wird, gefolgt von **vmVMState \_ Saved,** wenn der Speicher abgeschlossen und der virtuelle Computer deaktiviert ist.

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

 

