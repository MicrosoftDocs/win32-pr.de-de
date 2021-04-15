---
title: Ivmtaskcollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Auflistung von Task-Objekten. Zum Abrufen eines ivmtaskcollection-Objekts verwenden Sie die ivmvirtualpc Tasks-Eigenschaft.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Ivmtaskcollection-Schnittstelle virtueller PC
- Virtueller Computer der ivmtaskcollection-Schnittstelle, beschrieben
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
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392104"
---
# <a name="ivmtaskcollection-interface"></a>Ivmtaskcollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Auflistung von Task-Objekten. Verwenden Sie zum Abrufen eines **ivmtaskcollection** -Objekts die [**ivmvirtualpc:: Tasks**](ivmvirtualpc-tasks.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmtaskcollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmtaskcollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmtaskcollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp          | BESCHREIBUNG                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmtaskcollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                        |
| [**Countdown**](ivmtaskcollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der Tasks in dieser Auflistung.<br/>                  |
| [**Element**](ivmtaskcollection-item.md)<br/>          | Schreibgeschützt<br/> | Das Task-Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmtaskcollection ist definiert als 5c4387c8-0e8b-4b97-8058-84679adf 4c40<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmtask**](ivmtask.md)
</dt> <dt>

[**Ivmvirtualpc:: Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

