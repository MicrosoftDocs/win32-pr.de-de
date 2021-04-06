---
title: Ivmvirtualmachine-Methode zum Speichern (vpccominterfaces. h)
description: Speichert den Zustand der virtuellen Maschine (VM).
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Virtual PC-Methode speichern
- Save Method Virtual PC, ivmvirtualmachine Interface
- Ivmvirtualmachine Interface Virtual PC, Save-Methode
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
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742881"
---
# <a name="ivmvirtualmachinesave-method"></a>Ivmvirtualmachine:: Save-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Speichert den Zustand der virtuellen Maschine (VM).

## <a name="syntax"></a>Syntax


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*savetask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Fortschritt der Zustands Speicher Sequenz der VM zu verfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                                 |
| <dl> <dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen </dl>                                     | Die VM konnte nicht gespeichert werden, da die Rückgängig-Datenträger zum Löschen markiert waren.<br/>    |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                  | Der-Parameter ist **null**.<br/>                                                    |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt> </dl> | Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs verfügen, um den Status dieser VM zu speichern.<br/> |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>                     | Der virtuelle Computer wird nicht ausgeführt.<br/>                                                        |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                                             |



 

## <a name="remarks"></a>Bemerkungen

Der virtuelle Computer wird ausgeschaltet, wenn der **Sicherungs Task den** Abschluss erreicht. Die [**ivmvirtualmachine:: State**](ivmvirtualmachine-state.md) -Eigenschaft enthält den Speicherort **vmvmstate \_** , während der Speichervorgang ausgeführt wird, gefolgt von **vmvmstate \_** , wenn der Speichervorgang abgeschlossen und der virtuelle Computer ausgeschaltet ist.

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

 

