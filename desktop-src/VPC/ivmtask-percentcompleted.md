---
title: IVMTask PercentCompleted-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft den Abschlussprozentsatz der Aufgabe ab.
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- PercentCompleted-Eigenschaft Virtueller PC
- PercentCompleted-Eigenschaft Virtueller PC, IVMTask-Schnittstelle
- IVMTask-Schnittstelle Virtueller PC, PercentCompleted-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb15d187b4e9246c0c7a5b0af03e0ab8a9eec2bb6b8b9242120f9faf4c6fc96f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958860"
---
# <a name="ivmtaskpercentcompleted-property"></a>IVMTask::P ercentCompleted-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Abschlussprozentsatz der Aufgabe ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a>Eigenschaftswert

Der aktuelle Abschlussprozentsatz. Der Wert ist eine Zahl zwischen 0 und 100.

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
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask ist als ab72b222-6e9c-48ae-aa54-85e3e635767c definiert.<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

