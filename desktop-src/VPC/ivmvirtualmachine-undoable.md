---
title: Nicht doable-Eigenschaft für ivmvirtualmachine (vpccominterfaces. h)
description: Bestimmt, ob rückgängig-Laufwerke für Festplatten aktiviert sind, die mit der VM verbunden sind.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Nicht doable Property Virtual PC
- Nicht doable Property Virtual PC, ivmvirtualmachine Interface
- Ivmvirtualmachine Interface Virtual PC, undoable-Eigenschaft
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
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517855"
---
# <a name="ivmvirtualmachineundoable-property"></a>Ivmvirtualmachine:: undoable-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Bestimmt, ob rückgängig-Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer (VM) verbunden sind.

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

Gibt **Variant \_ true** an, wenn rückgängig-Laufwerke für Festplatten aktiviert sind, die mit dem virtuellen Computer verbunden sind, und andernfalls **\_ false** .

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                         | Bedeutung                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>      | Ein unerwarteter Fehler ist aufgetreten.<br/> |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>              | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>      | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>VM \_ E \_ Pref- \_ VM \_ aktiv</dt> <dt>0xa0040302</dt> </dl> | Die VM wird ausgeführt oder gespeichert.<br/>       |



## <a name="remarks"></a>Bemerkungen

Wenn rückgängig-Laufwerke deaktiviert sind, werden alle vorhandenen rückgängig-Laufwerks Dateien gelöscht.

Diese Eigenschaft kann nicht festgelegt werden, wenn die VM ausgeführt wird oder gespeichert wird.

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

 

