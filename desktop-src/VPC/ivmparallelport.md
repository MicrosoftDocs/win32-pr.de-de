---
title: Ivmparallelport-Schnittstelle (vpccominterfaces. h)
description: Definiert einen parallelen Port innerhalb einer virtuellen Maschine.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Ivmparallelport Interface Virtual PC
- Virtueller Computer für ivmparallelport Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339596"
---
# <a name="ivmparallelport-interface"></a>Ivmparallelport-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert einen parallelen Port innerhalb einer virtuellen Maschine. Mit dieser Schnittstelle können Sie parallele Ports in einem virtuellen Computer konfigurieren. Sie können ein **ivmparallelport** -Objekt aus dem [**ivmparallelportcollection**](ivmparallelportcollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine::P arallelports**](ivmvirtualmachine-parallelports.md) -Eigenschaft zurückgegeben wird.

## <a name="members"></a>Member

Die **ivmparallelport** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmparallelport** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmparallelport** -Schnittstelle verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [**\_id**](ivmparallelport--id.md) | Ruft den internen Bezeichner des parallelen Ports ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ivmparallelport** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                        | Zugriffstyp           | BESCHREIBUNG                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [**Name**](ivmparallelport-name.md)<br/> | Lesen/Schreiben<br/> | Der Name des parallelen Anschlusses.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmparallelport ist als 097beecb-0a02-474b-abd6-298b22293fc6 definiert.<br/>            |



 

