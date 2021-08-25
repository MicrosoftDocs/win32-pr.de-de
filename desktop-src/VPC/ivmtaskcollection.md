---
title: IVMTaskCollection-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die Auflistung von Taskobjekten. Um ein IVMTaskCollection-Objekt abzurufen, verwenden Sie die IVMVirtualPC Tasks-Eigenschaft.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- IVMTaskCollection-Schnittstelle Virtueller PC
- IVMTaskCollection-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150f5079258e551360f574cfd9fa0a8895d3673f5d6b38ea6a5e1c866cfbf1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958800"
---
# <a name="ivmtaskcollection-interface"></a>IVMTaskCollection-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die Auflistung von Taskobjekten. Um ein **IVMTaskCollection-Objekt** abzurufen, verwenden Sie die [**IVMVirtualPC::Tasks-Eigenschaft.**](ivmvirtualpc-tasks.md)

## <a name="members"></a>Member

Die **IVMTaskCollection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMTaskCollection** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IVMTaskCollection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp          | Beschreibung                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                        |
| [**Count**](ivmtaskcollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der Aufgaben in dieser Auflistung.<br/>                  |
| [**Element**](ivmtaskcollection-item.md)<br/>          | Schreibgeschützt<br/> | Das Aufgabenobjekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection ist als 5c4387c8-0e8b-4b97-8058-84679adf4c40 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> <dt>

[**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

