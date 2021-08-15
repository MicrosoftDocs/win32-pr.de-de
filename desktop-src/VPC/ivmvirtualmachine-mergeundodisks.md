---
title: IVMVirtualMachine MergeUndoDisks-Methode (VPCCOMInterfaces.h)
description: Führt die virtuellen Rückgängig-Datenträger zusammen.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- MergeUndoDisks-Methode – Virtueller PC
- MergeUndoDisks-Methode Virtual PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, MergeUndoDisks-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d30558ddb8acdd75d72955048beb34f0141206b53f3f5873e42627fb155f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998680"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>IVMVirtualMachine::MergeUndoDisks-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Führt die virtuellen Rückgängig-Datenträger zusammen.

## <a name="syntax"></a>Syntax


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*undoMergeTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das zum Nachverfolgen der Erstellung des Images verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                    | Der Parameter ist **NULL.**<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0x80070003</dt> </dl> | Das System kann den durch den *convertedDiskImagePath-Parameter* angegebenen Pfad nicht finden, oder einer der übergeordneten Datenträger ist ungültig.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                               | Der aktuelle Benutzer hat nicht genügend Zugriff auf die übergeordnete Datei.<br/>                                                                 |
| <dl> <dt>**E \_ HANDLE**</dt> <dt>0x80070006</dt> </dl>                                     | Einer der übergeordneten Datenträger wird verwendet.<br/>                                                                                           |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | Die Konfiguration ist unbekannt.<br/>                                                                                                |
| <dl> <dt>**VM \_ E \_ VM \_ RUNNING**</dt> <dt>0xA0040500</dt> </dl>                            | Der virtuelle Computer wird ausgeführt.<br/>                                                                                              |
| <dl> <dt>**VM \_ E \_ FILE READ ONLY \_ \_ 0xA004067A**</dt> <dt></dt> </dl>                       | Das übergeordnete Element virtueller Rückgängig-Datenträger ist als schreibgeschützt gekennzeichnet.<br/>                                                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                            |



 

## <a name="remarks"></a>Hinweise

**MergeUndoDisks kann** nicht aufgerufen werden, während der virtuelle Computer noch ausgeführt wird. Verwenden Sie [**IVMVirtualMachine::Save,**](ivmvirtualmachine-save.md) um den Zustand des virtuellen Computers vor dem Aufruf von **MergeUndoDisks** zu speichern, oder [**IVMVirtualMachine::TurnOff,**](ivmvirtualmachine-turnoff.md) um den virtuellen Computer zu deaktivieren, ohne zuvor seinen aktuellen Zustand zu speichern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

