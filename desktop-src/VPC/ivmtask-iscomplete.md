---
title: IVMTask IsComplete-Eigenschaft (VPCCOMInterfaces.h)
description: Bestimmt, ob die Aufgabe abgeschlossen wurde.
ms.assetid: 181fa220-4de2-4ab3-950b-fffc4fe4de64
keywords:
- IsComplete-Eigenschaft Virtueller PC
- IsComplete-Eigenschaft Virtueller PC, IVMTask-Schnittstelle
- IVMTask-Schnittstelle Virtueller PC, IsComplete-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.IsComplete
- IVMTask.get_IsComplete
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c4c347abf9f1cee52990fe779593083b5cbcaadede8c663175e677c8c1f793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998730"
---
# <a name="ivmtaskiscomplete-property"></a>IVMTask::IsComplete-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Bestimmt, ob die Aufgabe abgeschlossen wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsComplete(
  [out, retval] VARIANT_BOOL *isComplete
);
```



## <a name="property-value"></a>Eigenschaftswert

**TRUE,** wenn die Aufgabe abgeschlossen wurde, **andernfalls FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameterwert ist **NULL.**<br/>  |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask ist als ab72b222-6e9c-48ae-aa54-85e3e635767c definiert.<br/>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

