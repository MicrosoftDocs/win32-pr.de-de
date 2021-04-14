---
title: Ivmvirtualmachine UndoAction-Eigenschaft (vpccominterfaces. h)
description: Standardaktion, die auf allen rückgängig-Laufwerken ausgeführt werden soll, wenn der virtuelle Computer heruntergefahren wird.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- UndoAction-Eigenschaft virtueller PC
- UndoAction-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, UndoAction-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478321"
---
# <a name="ivmvirtualmachineundoaction-property"></a>Ivmvirtualmachine:: UndoAction (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Hiermit wird die Standardaktion abgerufen und festgelegt, die auf allen rückgängig-Laufwerken ausgeführt werden soll, wenn der virtuelle Computer mithilfe der [**Turnoff**](ivmvirtualmachine-turnoff.md) -Methode ausgeschaltet oder mithilfe der [**Shutdown**](ivmguestos-shutdown.md) -Methode heruntergefahren oder innerhalb des Gast Betriebssystems ausgeschaltet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die Standardaktion an, die auf allen rückgängig-Laufwerken ausgeführt werden soll, wenn der virtuelle Computer innerhalb des Gast Betriebssystems heruntergefahren wird. Eine Liste der Werte finden Sie unter [**vmundoaction**](vmundoaction.md).

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>      | Der Parameter ist ungültig.<br/>       |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



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

 

