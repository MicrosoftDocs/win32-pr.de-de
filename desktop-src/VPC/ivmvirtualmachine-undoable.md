---
title: IVMVirtualMachine Undoable-Eigenschaft (VPCCOMInterfaces.h)
description: Bestimmt, ob rückgängig machende Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer verbunden sind.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Rückgängigbare Eigenschaft Virtueller PC
- Rückgängigbare Eigenschaft Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, Rückgängigbare Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7663cefb8f94809f0fd016e002102c9956066b64ca21fb79766598b592ec3dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752073"
---
# <a name="ivmvirtualmachineundoable-property"></a>IVMVirtualMachine::Undoable-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Bestimmt, ob Rückgängig-Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer (VM) verbunden sind.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt **VARIANT \_ TRUE** an, wenn rückgängig gemachte Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer verbunden sind, andernfalls **VARIANT \_ FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                         | Bedeutung                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/> |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>              | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>VM \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | Der virtuelle Computer wird ausgeführt oder gespeichert.<br/>       |



## <a name="remarks"></a>Hinweise

Wenn rückgängige Laufwerke deaktiviert sind, werden alle vorhandenen Rückgängig-Laufwerksdateien gelöscht.

Sie können diese Eigenschaft nicht festlegen, wenn der virtuelle Computer ausgeführt oder gespeichert wird.

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

 

