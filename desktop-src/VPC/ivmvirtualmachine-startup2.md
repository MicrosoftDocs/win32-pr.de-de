---
title: IVMVirtualMachine Startup2-Methode (VPCCOMInterfaces.h)
description: Startet den virtuellen Computer entweder aus dem nicht initialisierten oder gespeicherten Zustand mit erweiterten Optionen.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- 'Startup2-Methode : Virtueller PC'
- Startup2-Methode Virtual PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, Startup2-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b76364f80d9faaaeeb0f9760ce434d91658afc6699a7acdeee98f0a2e65548d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652890"
---
# <a name="ivmvirtualmachinestartup2-method"></a>IVMVirtualMachine::Startup2-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Startet den virtuellen Computer (VM) mit erweiterten Optionen entweder aus dem nicht initialisierten oder gespeicherten Zustand.

Diese Methode bietet einen Mechanismus zum Starten eines virtuellen Computers mit einem sich unterscheidenden Datenträger, auch wenn der Zeitstempel des übergeordneten Datenträgers geändert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*startupOption* \[ In\]
</dt> <dd>

Die erweiterte Startoption. Die möglichen Werte sind aus der [**VMStartupOption-Enumeration.**](vmstartupoption.md)

</dd> <dt>

*startupTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das zum Nachverfolgen des Abschlussfortschritts der Startsequenz verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | Beschreibung                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                               | Der *startupOption-Parameter* ist ungültig.<br/>                       |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                  | Der *startupTask-Parameter* ist **NULL.**<br/>                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0X80070005</dt> </dl> | Der Aufrufer muss über Ausführungszugriffsberechtigungen verfügen, um diesen virtuellen Computer zu starten.<br/> |
| <dl> <dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt> </dl>                           | Der Vorgang wurde nicht rechtzeitig abgeschlossen.<br/>                |
| <dl> <dt>**VM \_ E \_ OUT \_ OF \_ RESOURCE**</dt> <dt>0XA0040203</dt> </dl>                    | Es sind nicht genügend Hostressourcen vorhanden.<br/>                              |
| <dl> <dt>**VM \_ E \_ TOO \_ MANY \_ VMS**</dt> <dt>0xA0040204</dt> </dl>                       | Es gibt zu viele aktive VMs.<br/>                                    |
| <dl> <dt>**VM \_ E \_ \_ VM, DIE**</dt> <dt>0XA0040500</dt> </dl>                          | Der virtuelle Computer wird bereits ausgeführt.<br/>                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                 |



 

## <a name="remarks"></a>Hinweise

Die folgenden Werte können über die [**Error-Eigenschaft**](ivmtask-error.md) des zurückgegebenen [**IVMTask-Objekts zurückgegeben**](ivmtask.md) werden.



| [](ivmtask-error.md) Fehlercode/-wert                                                                                                                                                                                                                                      | Beschreibung                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)<br/>                                                 | Die Hardware unterstützt keine Virtualisierung.<br/>              |
| <span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)<br/> | Die Hardwarevirtualisierung ist deaktiviert.<br/>                       |
| <span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)<br/>                             | Sowohl Virtual PC 2007 als auch Windows Virtual PC sind installiert.<br/> |
| <span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)<br/>             | Andere Virtualisierungssoftware ist installiert.<br/>                |
| <span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)<br/>                                                                 | Es sind nicht genügend Hostressourcen vorhanden.<br/>                       |



 

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

 

