---
title: Ivmparallelportcollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung paralleler Ports innerhalb des virtuellen Computers. Zum Abrufen eines ivmparallelportcollection-Objekts verwenden Sie die ivmvirtualmachine Parallelports-Eigenschaft.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Ivmparallelportcollection-Schnittstelle virtueller PC
- Ivmparallelportcollection-Schnittstelle virtueller PC, beschrieben
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106052"
---
# <a name="ivmparallelportcollection-interface"></a>Ivmparallelportcollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Sammlung paralleler Ports innerhalb des virtuellen Computers. Verwenden Sie zum Abrufen eines **ivmparallelportcollection** -Objekts die [**ivmvirtualmachine::P arallelports**](ivmvirtualmachine-parallelports.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmparallelportcollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmparallelportcollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmparallelportcollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                           | Zugriffstyp          | BESCHREIBUNG                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmparallelportcollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                 |
| [**Countdown**](ivmparallelportcollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl paralleler Ports in dieser Auflistung.<br/>                  |
| [**Element**](ivmparallelportcollection-item.md)<br/>          | Schreibgeschützt<br/> | Das parallele Port Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmparallelportcollection ist als 27c3e036-198l-430c-8735-6e652f 7203fd definiert.<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmparallelport**](ivmparallelport.md)
</dt> <dt>

[**Ivmvirtualmachine::P arallelports**](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

