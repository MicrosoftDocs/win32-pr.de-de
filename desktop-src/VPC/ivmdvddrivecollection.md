---
title: Ivmdvddrivecollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung von CD-und DVD-Laufwerken innerhalb des virtuellen Computers. Verwenden Sie zum Abrufen eines ivmdvddrivecollection-Objekts die ivmvirtualmachine-dvdromdrives-Eigenschaft.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Ivmdvddrivecollection Interface Virtual PC
- Virtueller Computer ivmdvddrivecollection Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346724"
---
# <a name="ivmdvddrivecollection-interface"></a>Ivmdvddrivecollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Sammlung von CD-und DVD-Laufwerken innerhalb des virtuellen Computers. Verwenden Sie zum Abrufen eines **ivmdvddrivecollection** -Objekts die [**ivmvirtualmachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmdvddrivecollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmdvddrivecollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmdvddrivecollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                       | Zugriffstyp          | BESCHREIBUNG                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmdvddrivecollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                   |
| [**Countdown**](ivmdvddrivecollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der CD-und DVD-Laufwerke in dieser Sammlung.<br/>                 |
| [**Element**](ivmdvddrivecollection-item.md)<br/>          | Schreibgeschützt<br/> | Das CD-oder DVD-Laufwerks Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdvddrivecollection ist als bc86e297-e55f-4742-9614-ad11d3131f68 definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdvddrive**](ivmdvddrive.md)
</dt> <dt>

[**Ivmvirtualmachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

