---
title: IVMTaskCollection Item-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft das Taskobjekt ab, das dem angegebenen Index entspricht.
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- Item-Eigenschaft Virtueller PC
- Item-Eigenschaft Virtual PC, IVMTaskCollection-Schnittstelle
- IVMTaskCollection-Schnittstelle Virtueller PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d721bcd990ab84e763003f3fff457fec41ec9dd3764797c373e2d094fa288526
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958830"
---
# <a name="ivmtaskcollectionitem-property"></a>IVMTaskCollection::Item-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft das Taskobjekt ab, das dem angegebenen Index entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a>Eigenschaftswert

Das [**IVMTask-Objekt.**](ivmtask.md)

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt. <br/>                                                      |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der *Taskparameter* ist **NULL.** <br/>                                                  |
| <dl> <dt>DISP \_ E \_ BADINDEX-0x8002000B</dt> <dt></dt> </dl>  | Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung. <br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection ist als 5c4387c8-0e8b-4b97-8058-84679adf4c40 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> <dt>

[**IVMTaskCollection**](ivmtaskcollection.md)
</dt> </dl>

 

