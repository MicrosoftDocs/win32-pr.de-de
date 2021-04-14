---
title: Ivmvirtualmachine Startup2-Methode (vpccominterfaces. h)
description: Startet die virtuelle Maschine entweder über den nicht initialisierten oder gespeicherten Zustand mit erweiterten Optionen.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Startup2-Methode Virtual PC
- Startup2-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Startup2-Methode
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
ms.openlocfilehash: 51b40149b0b21abc126261d8b1ddec34b9948371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391953"
---
# <a name="ivmvirtualmachinestartup2-method"></a>Ivmvirtualmachine:: Startup2-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Startet den virtuellen Computer (VM) entweder aus dem nicht initialisierten oder gespeicherten Zustand mit erweiterten Optionen.

Diese Methode bietet einen Mechanismus zum Starten eines virtuellen Computers mit einem differenzierenden Datenträger, auch wenn der Zeitstempel des übergeordneten Datenträgers geändert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*startuption* \[ in\]
</dt> <dd>

Die erweiterte Startoption. Die möglichen Werte stammen aus der [**vmstartupoption**](vmstartupoption.md) -Enumeration.

</dd> <dt>

*startuptask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Fortschritt der Startsequenz zu verfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                     |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                               | Der *startupoption* -Parameter ist ungültig.<br/>                       |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                  | Der *startuptask* -Parameter ist **null**.<br/>                          |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt> </dl> | Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs verfügen, um diese VM zu starten<br/> |
| <dl> <dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt> </dl>                           | Der Vorgang wurde nicht rechtzeitig beendet.<br/>                |
| <dl> <dt>**VM \_ E \_ aus \_ \_ Ressource**</dt> <dt>0xa0040203</dt> </dl>                    | Es sind nicht genügend Host Ressourcen vorhanden.<br/>                              |
| <dl> <dt>**VM \_ E \_ zu \_ viele \_ VMS**</dt> <dt>0xa0040204</dt> </dl>                       | Es sind zu viele aktive VMS vorhanden.<br/>                                    |
| <dl> <dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt> </dl>                          | Der virtuelle Computer wird bereits ausgeführt.<br/>                                        |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                 |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Werte können durch die [**Error**](ivmtask-error.md) -Eigenschaft des zurückgegebenen [**ivmtask**](ivmtask.md) -Objekts zurückgegeben werden.



| [**Fehler**](ivmtask-error.md) Code/Wert                                                                                                                                                                                                                                      | BESCHREIBUNG                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xa0040950)<br/>                                                 | Die Hardware unterstützt keine Virtualisierung.<br/>              |
| <span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xa0040951)<br/> | Die Hardwarevirtualisierung ist deaktiviert.<br/>                       |
| <span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xa0040952)<br/>                             | Sowohl Virtual PC 2007 als auch Windows Virtual PC werden installiert.<br/> |
| <span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xa0040953)<br/>             | Andere Virtualisierungssoftware ist installiert.<br/>                |
| <span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)<br/>                                                                 | Es sind nicht genügend Host Ressourcen vorhanden.<br/>                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

