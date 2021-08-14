---
title: IVMVirtualMachine UndoAction-Eigenschaft (VPCCOMInterfaces.h)
description: Standardaktion, die auf allen rückgängig machenden Laufwerken ausgeführt werden soll, wenn der virtuelle Computer heruntergefahren wird.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- UndoAction-Eigenschaft Virtueller PC
- UndoAction-Eigenschaft Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtual PC , UndoAction-Eigenschaft
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
ms.openlocfilehash: ed32b0864e1a22b196001c5f75ba7e58711e7a9b6d6b2781a5f75ae0c3ced5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344545"
---
# <a name="ivmvirtualmachineundoaction-property"></a>IVMVirtualMachine::UndoAction-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Standardaktion ab, die auf allen rückgängig gemachten Laufwerken ausgeführt werden soll, wenn der virtuelle Computer (VM) mithilfe der [**TurnOff-Methode**](ivmvirtualmachine-turnoff.md) deaktiviert oder mithilfe der [**Shutdown-Methode**](ivmguestos-shutdown.md) heruntergefahren oder aus dem Gastbetriebssystem ausgeschaltet wird, und legt diese fest.

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

Gibt die Standardaktion an, die auf allen rückgängig machenden Laufwerken ausgeführt werden soll, wenn der virtuelle Computer aus dem Gastbetriebssystem heruntergefahren wird. Eine Liste der Werte finden Sie unter [**VMUndoAction**](vmundoaction.md).

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>      | Der Parameter ist ungültig.<br/>       |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



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

 

